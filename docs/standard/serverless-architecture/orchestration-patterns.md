---
title: Modèles d’orchestration - applications sans serveur
description: Demande de tirage de fonctions durables Azure
author: cecilphillip
ms.author: cephilli
ms.date: 06/26/2018
ms.openlocfilehash: c3b9dbe473ba9272a8c8c07cec86e11fcd9fc12d
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53129309"
---
# <a name="orchestration-patterns"></a>Modèles d’orchestration

Fonctions durables rend plus facile de créer des flux de travail avec état qui est composés d’activités discrètes, à long terme dans un environnement sans serveur. Dans la mesure où les fonctions durables peut suivre la progression de votre flux de travail et régulièrement des points de contrôle de l’historique d’exécution, il se prête à l’implémentation de certains modèles intéressants.

## <a name="function-chaining"></a>Chaînage de fonctions

Dans un procédé séquentiel typique, les activités doivent exécuter l’une après l’autre dans un ordre particulier. Si vous le souhaitez, l’activité à venir peut nécessiter une sortie à partir de la fonction précédente. Cette dépendance sur l’ordre des activités crée une chaîne de la fonction de l’exécution.

L’avantage d’utiliser des fonctions durables pour implémenter ce modèle de flux de travail provient de sa capacité à faire des points de contrôle. Si le serveur tombe en panne, le réseau arrive à expiration ou un autre problème se produit, fonctions durables peuvent reprendre à partir du dernier état connu et continuer à exécuter votre flux de travail, même si elle est sur un autre serveur.

```csharp
[FunctionName("PlaceOrder")]
public static async Task<string> PlaceOrder([OrchestrationTrigger] DurableOrchestrationContext context)
{
    OrderRequestData orderData = context.GetInput<OrderRequestData>();

    await context.CallActivityAsync<bool>("CheckAndReserveInventory", orderData);
    await context.CallActivityAsync<bool>("ProcessPayment", orderData);

    string trackingNumber = await context.CallActivityAsync<string>("ScheduleShipping", orderData);
    await context.CallActivityAsync<string>("EmailCustomer", trackingNumber);

    return trackingNumber;
}
```

Dans l’exemple de code précédent, le `CallActivityAsync` (fonction) est chargée d’exécuter une activité donnée sur une machine virtuelle dans le centre de données. Lorsque l’expression await retourne et la tâche sous-jacente est terminée, l’exécution est enregistrée dans la table d’historique. Le code dans la fonction d’orchestrateur peut faire utiliser chacune des constructions familiers de la bibliothèque parallèle de tâches et les mots clés async/await.

Le code suivant est un exemple simplifié de ce à quoi le `ProcessPayment` méthode peut ressembler à :

```csharp
[FunctionName("ProcessPayment")]
public static bool ProcessPayment([ActivityTrigger] DurableActivityContext context)
{
    OrderRequestData orderData = context.GetInput<OrderRequestData>();

    ApplyCoupons(orderData);
    if(IssuePaymentRequest(orderData)) {
        return true;
    }

    return false;
}
```

## <a name="asynchronous-http-apis"></a>API HTTP asynchrones

Dans certains cas, les flux de travail peut-être contenir des activités qui prennent une relativement longue période de temps. Imaginez un processus qui lance la sauvegarde du support de fichiers dans le stockage blob. Selon la taille et la quantité des fichiers multimédias, ce processus de sauvegarde peut prendre des heures de travail.

Dans ce scénario, le `DurableOrchestrationClient`de possibilité de vérifier l’état d’un workflow en cours d’exécution devient utile. Lorsque vous utilisez un `HttpTrigger` pour démarrer un flux de travail, le `CreateCheckStatusResponse` méthode peut être utilisée pour retourner une instance de `HttpResponseMessage`. Cette réponse fournit au client avec un URI dans la charge utile qui peut être utilisé pour vérifier l’état du processus en cours d’exécution.

```csharp
[FunctionName("OrderWorkflow")]
public static async Task<HttpResponseMessage> Run(
    [HttpTrigger(AuthorizationLevel.Function, "POST")]HttpRequestMessage req,
    [OrchestrationClient ] DurableOrchestrationClient orchestrationClient)
{
    OrderRequestData data = await req.Content.ReadAsAsync<OrderRequestData>();

    string instanceId = await orchestrationClient.StartNewAsync("PlaceOrder", data);

    return orchestrationClient.CreateCheckStatusResponse(req, instanceId);
}
```

Le résultat de l’exemple ci-dessous illustre la structure de la charge utile de réponse.

```json
{
    "id": "instanceId",
    "statusQueryGetUri": "http://host/statusUri",
    "sendEventPostUri": "http://host/eventUri",
    "terminatePostUri": "http://host/terminateUri"
}
```

À l’aide de votre client HTTP par défaut, les requêtes GET est possible à l’URI dans statusQueryGetUri pour inspecter l’état du flux de travail en cours d’exécution. La réponse de l’état renvoyé doit ressembler au code suivant.

```json
{
    "runtimeStatus": "Running",
    "input": {
        "$type": "DurableFunctionsDemos.OrderRequestData, DurableFunctionsDemos"
    },
    "output": null,
    "createdTime": "2018-01-01T00:22:05Z",
    "lastUpdatedTime": "2018-01-01T00:22:09Z"
}
```

À mesure que le processus, la réponse d’état sera alors soit **échec** ou **terminé**. Opération réussie, le **sortie** propriété dans la charge utile contient les données retournées.

## <a name="monitoring"></a>Analyse

Pour des tâches récurrentes simples, Azure Functions fournit le `TimerTrigger` qui peuvent être planifiés selon une expression CRON. Le minuteur fonctionne bien pour les tâches de courte durées, simples, mais il peut y avoir des scénarios où une planification plus flexible est nécessaire. Ce scénario est lorsque le modèle de surveillance et les fonctions durables peuvent aider.

Fonctions durables permet des intervalles de planifications flexibles, la gestion de la durée de vie et la création de plusieurs processus d’analyse à partir d’une fonction d’orchestration unique. Un cas d’usage pour cette fonctionnalité peut consister à créer des observateurs pour les modifications de prix de l’action une fois remplies d’un certain seuil.

```csharp
[FunctionName("CheckStockPrice")]
public static async Task CheckStockPrice([OrchestrationTrigger] DurableOrchestrationContext context)
{
    StockWatcherInfo stockInfo = context.GetInput<StockWatcherInfo>();
    const int checkIntervalSeconds = 120;
    StockPrice initialStockPrice = null;

    DateTime fireAt;
    DateTime exitTime = context.CurrentUtcDateTime.Add(stockInfo.TimeLimit);

    while (context.CurrentUtcDateTime < exitTime)
    {
        StockPrice currentStockPrice = await context.CallActivityAsync<StockPrice>("GetStockPrice", stockInfo);

        if (initialStockPrice == null)
        {
            initialStockPrice = currentStockPrice;
            fireAt = context.CurrentUtcDateTime.AddSeconds(checkIntervalSeconds);
            await context.CreateTimer(fireAt, CancellationToken.None);
            continue;
        }

        decimal percentageChange = (initialStockPrice.Price - currentStockPrice.Price) /
                               ((initialStockPrice.Price + currentStockPrice.Price) / 2);

        if (Math.Abs(percentageChange) >= stockInfo.PercentageChange)
        {
            // Change threshold detected
            await context.CallActivityAsync("NotifyStockPercentageChange", currentStockPrice);
            break;
        }

        // Sleep til next polling interval
        fireAt = context.CurrentUtcDateTime.AddSeconds(checkIntervalSeconds);
        await context.CreateTimer(fireAt, CancellationToken.None);
    }
}
```

`DurableOrchestrationContext`de `CreateTimer` méthode configure la planification pour l’appel suivant de la boucle de vérifier les modifications de prix de l’action. `DurableOrchestrationContext` possède également un `CurrentUtcDateTime` propriété à obtenir la valeur de date/heure actuelle au format UTC. Il est préférable d’utiliser cette propriété au lieu de `DateTime.UtcNow` , car il est facilement simulée pour le test.

## <a name="recommended-resources"></a>Ressources recommandées

* [Azure Functions Durable](https://docs.microsoft.com/azure/azure-functions/durable-functions-overview)
* [Tests unitaires dans .NET Core et .NET Standard](https://docs.microsoft.com/dotnet/core/testing/)

>[!div class="step-by-step"]
>[Précédent](durable-azure-functions.md)
>[Suivant](serverless-business-scenarios.md)