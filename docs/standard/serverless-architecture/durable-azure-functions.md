---
title: Azure functions durables - applications sans serveur
description: Azure functions durables étendent le runtime Azure Functions pour activer le flux de travail avec état dans le code.
author: cecilphillip
ms.author: cephilli
ms.date: 06/26/2018
ms.openlocfilehash: 8ad354e1708eb88f016130f8235f534b967eb122
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61776010"
---
# <a name="durable-azure-functions"></a>Fonctions Azure durables

Lorsque vous créez des applications sans serveur avec Azure Functions, vos opérations seront généralement conçues pour s’exécuter sans état. La raison de ce choix de conception est, car comme les échelles de plateforme, il devient difficile de savoir quels serveurs le code est en cours d’exécution. Il devient également difficile de savoir combien d’instances est actifs à un moment donné. Toutefois, il existe des classes d’applications qui nécessitent l’état actuel d’un processus connu. Considérons le processus de soumission d’une commande à un magasin en ligne. L’opération d’extraction peut être un flux de travail qui se compose de plusieurs opérations qui doivent connaître l’état du processus. Ces informations peuvent inclure l’inventaire de produits, si le client dispose d’aucun crédit sur leur compte et également les résultats du traitement de la carte de crédit. Ces opérations peuvent être facilement leurs propres flux de travail interne ou un voire des services à partir des systèmes tiers.

Différents modèles existent aujourd'hui cet assist la coordination de l’état de l’application entre les systèmes internes et externes. Il est courant de rencontrer des solutions qui s’appuient sur les systèmes centralisés de file d’attente, les magasins de clés-valeurs distribuées ou des bases de données partagées pour gérer cet état. Toutefois, il s’agit de toutes les autres ressources qui doivent désormais être configurés et gérés. Dans un environnement sans serveur, votre code peut devenir fastidieux d’essayer de coordonner avec ces ressources manuellement. Azure Functions offre une alternative pour la création des fonctions avec état appelées fonctions durables.

Fonctions durables est une extension pour le runtime Azure Functions qui permet la définition de flux de travail avec état dans le code. En décomposant en activités de flux de travail, l’extension fonctions durables peut gérer l’état de créer des points de contrôle de progression et gérer la distribution des appels de fonction entre les serveurs. En arrière-plan, elle rend utiliser d’un compte de stockage Azure pour conserver l’historique d’exécution, de planifier les fonctions d’activité et de récupérer des réponses. Votre code sans serveur ne doit jamais interagir avec les informations persistantes dans ce compte de stockage et est généralement pas quelque chose que les développeurs ont besoin d’interagir.

## <a name="triggering-a-stateful-workflow"></a>Déclencher un flux de travail avec état

Flux de travail avec état dans fonctions durables peut être divisé en deux composants intrinsèques. déclencheurs d’orchestration et l’activité. Déclencheurs et liaisons sont les principaux composants utilisés par Azure Functions pour permettre à vos fonctions sans serveur être averti pour démarrer, la réception d’entrée et retourner des résultats.

### <a name="working-with-the-orchestration-client"></a>Utilisation du client d’Orchestration

Orchestrations sont uniques par rapport aux autres styles d’opérations déclenchées dans Azure Functions. Fonctions durables permet l’exécution de fonctions qui peut prendre plusieurs heures voire plusieurs jours pour terminer. Ce type de comportement est fourni avec la nécessité de vérifier l’état d’une orchestration en cours d’exécution, titre préventif terminer, ou envoyer des notifications d’événements externes.

Dans ces cas, l’extension fonctions durables fournit la `DurableOrchestrationClient` classe qui vous permet d’interagir avec orchestré fonctions. Vous obtenez l’accès au client d’orchestration à l’aide de la `OrchestrationClientAttribute` liaison. En règle générale, vous devez inclure cet attribut avec un autre type de déclencheur, comme un `HttpTrigger` ou `ServiceBusTrigger`. Une fois que la fonction de la source a été déclenchée, le client de l’orchestration peut être utilisé pour démarrer une fonction d’orchestrateur.

```csharp
[FunctionName("KickOff")]
public static async Task<HttpResponseMessage> Run(
    [HttpTrigger(AuthorizationLevel.Function, "POST")]HttpRequestMessage req,
    [OrchestrationClient ] DurableOrchestrationClient<orchestrationClient>)
{
    OrderRequestData data = await req.Content.ReadAsAsync<OrderRequestData>();

    string instanceId = await orchestrationClient.StartNewAsync("PlaceOrder", data);

    return orchestrationClient.CreateCheckStatusResponse(req, instanceId);
}
```

### <a name="the-orchestrator-function"></a>La fonction d’orchestrateur

Annoter une fonction avec la OrchestrationTriggerAttribute dans Azure Functions marques cette fonction comme une fonction d’orchestrateur. Il est chargé de gérer les différentes activités qui composent votre flux de travail avec état.

Les fonctions d’orchestrateur ne parvenons pas à utiliser des liaisons autres que le OrchestrationTriggerAttribute. Cet attribut peut uniquement être utilisé avec un type de paramètre de DurableOrchestrationContext. Aucune entrée n’est utilisable dans la mesure où la désérialisation des entrées dans la signature de fonction n’est pas pris en charge. Pour obtenir des entrées fournies par le client d’orchestration, le GetInput\<T\> méthode doit être utilisée.

En outre, les types de retour des fonctions d’orchestration doivent être void, tâche ou une valeur sérialisable JSON.

> *Gestion du code d’erreur a été omis par souci de concision*

```csharp
[FunctionName("PlaceOrder")]
public static async Task<string> PlaceOrder([OrchestrationTrigger] DurableOrchestrationContext context)
{
    OrderRequestData orderData = context.GetInput<OrderRequestData>();

    await context.CallActivityAsync<bool>("CheckAndReserveInventory", orderData);
    await context.CallActivityAsync<string>("ProcessPayment", orderData);

    string trackingNumber = await context.CallActivityAsync<string>("ScheduleShipping", orderData);
    await context.CallActivityAsync<string>("EmailCustomer", trackingNumber);

    return trackingNumber;
}
```

Plusieurs instances d’une orchestration peuvent être démarré et s’exécute en même temps. Appel de la `StartNewAsync` méthode sur le `DurableOrchestrationClient` lance une nouvelle instance de l’orchestration. La méthode retourne un `Task<string>` qui se termine lorsque l’orchestration a démarré. Une exception de type `TimeoutException` obtient levée si l’orchestration n’a pas démarré dans les 30 secondes.

Fin du `Task<string>` de `StartNewAsync` doit contenir l’ID unique de l’instance d’orchestration. Cet ID d’instance peut être utilisé pour appeler des opérations sur cette orchestration. L’orchestration peut être interrogée pour connaître l’état ou envoyée des notifications d’événements.

### <a name="the-activity-functions"></a>Les fonctions d’activité

Fonctions d’activité sont les opérations discrètes obtient décomposées au sein d’une fonction d’orchestration pour créer le workflow. Voici où a lieu la plupart du travail réel. Ils représentent la logique métier, longs processus en cours d’exécution et les pièces du puzzle à une solution plus vaste.

Le `ActivityTriggerAttribute` est utilisé pour annoter un paramètre de fonction de type `DurableActivityContext`. À l’aide de l’annotation informe le runtime de que la fonction est destinée à être utilisée comme une fonction d’activité. Les valeurs d’entrée pour les fonctions d’activité sont récupérés à l’aide de la `GetInput<T>` méthode de le `DurableActivityContext` paramètre.

Comme pour les fonctions d’orchestration, les types de retour des fonctions d’activité doivent être void, tâche ou une valeur sérialisable JSON.

Les exceptions non gérées levées dans les fonctions d’activité obtient envoyées à la fonction d’orchestrateur appelant et présentées sous la forme un `TaskFailedException`. À ce stade, l’erreur peut être interceptée et connecté l’orchestrateur, et l’activité peut être retentée.

```csharp
[FunctionName("CheckAndReserveInventory")]
public static bool CheckAndReserveInventory([ActivityTrigger] DurableActivityContext context)
{
    OrderRequestData orderData = context.GetInput<OrderRequestData>();

    // Connect to inventory system and try to reserve items
    return true;
}
```

## <a name="recommended-resources"></a>Ressources recommandées

* [Fonctions durables](https://docs.microsoft.com/azure/azure-functions/durable-functions-overview)
* [Liaisons pour fonctions durables](https://docs.microsoft.com/azure/azure-functions/durable-functions-bindings)
* [Gérer des instances dans fonctions durables](https://docs.microsoft.com/azure/azure-functions/durable-functions-instance-management)

>[!div class="step-by-step"]
>[Précédent](event-grid.md)
>[Suivant](orchestration-patterns.md)