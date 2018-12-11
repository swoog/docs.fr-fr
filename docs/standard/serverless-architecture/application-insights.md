---
title: Application Insights - applications sans serveur
description: Application Insights est une plateforme de diagnostics sans serveur qui permet aux développeurs de détecter, trier et diagnostiquer les problèmes dans les applications web, les applications mobiles, les applications de bureau et les microservices.
author: JEREMYLIKNESS
ms.author: jeliknes
ms.date: 06/26/2018
ms.openlocfilehash: b4884d483de07c1c2077f7280b6b77c6059572c0
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53154254"
---
# <a name="telemetry-with-application-insights"></a>Données de télémétrie avec Application Insights

[Application Insights](https://docs.microsoft.com/azure/application-insights) est une plateforme de diagnostics sans serveur qui permet aux développeurs de détecter, trier et diagnostiquer les problèmes dans les applications web, les applications mobiles, les applications de bureau et les microservices. Vous pouvez activer Application Insights pour les applications de fonction simplement en mettant en marche d’un commutateur dans le portail. Application Insights fournit toutes ces fonctionnalités sans avoir à configurer un serveur ou configurer votre propre base de données. Toutes les fonctionnalités d’Application Insights sont fournis en tant que service qui intègre automatiquement avec vos applications.

![Logo d’application Insights](./media/application-insights-logo.png)

Ajout d’Application Insights aux applications existantes, il suffit que l’ajout d’une clé d’instrumentation aux paramètres de votre application. Avec Application Insights, vous pouvez :

* Créer des graphiques personnalisés et des alertes en fonction des mesures telles que le nombre d’appels de fonction, le temps que nécessaire pour exécuter une fonction et les exceptions
* Analyser les défaillances et les exceptions du serveur
* Explorez les performances par opération et de mesurer le temps que nécessaire pour appeler des dépendances tierces
* Surveiller l’utilisation processeur, mémoire et les tarifs sur tous les serveurs qui hébergent vos applications de fonction
* Afficher un flux live de métriques, notamment le nombre de demandes et la latence pour vos applications de fonction
* Utilisez [Analytique](https://docs.microsoft.com/azure/application-insights/app-insights-analytics) pour rechercher, interroger et créer des graphiques personnalisés sur vos données (fonction)

![Explorateur de mesures](./media/metrics-explorer.png)

En plus des données de télémétrie intégrée, il est également possible de générer des données de télémétrie personnalisées. L’extrait de code suivant crée un client de télémétrie personnalisée à l’aide de la clé d’instrumentation définie pour l’application de fonction :

```csharp
public static TelemetryClient telemetry = new TelemetryClient()
{
    InstrumentationKey = Environment.GetEnvironmentVariable("APPINSIGHTS_INSTRUMENTATIONKEY")
};
```

Le code suivant mesure le temps nécessaire pour insérer une nouvelle ligne dans un [stockage Table Azure](https://docs.microsoft.com/azure/cosmos-db/table-storage-overview) instance :

```csharp
var operation = TableOperation.Insert(entry);
var startTime = DateTime.UtcNow;
var timer = System.Diagnostics.Stopwatch.StartNew();
await table.ExecuteAsync(operation);
telemetry.TrackDependency("AzureTableStorageInsert", "Insert", startTime, timer.Elapsed, true);
```

Le graphique de performances résultant s’affiche :

![Télémétrie personnalisée](./media/custom-telemetry.png)

Les données de télémétrie personnalisées révèle le temps moyen pour insérer une nouvelle ligne est 32.6 millisecondes.

Application Insights fournit un moyen puissant et pratique pour se connecter à des données de télémétrie détaillées relatives à vos applications sans serveur. Vous contrôlez totalement le niveau de suivi et de journalisation qui est fournie. Vous pouvez suivre les statistiques personnalisées telles que les événements, les dépendances et affichage de page. Enfin, l’analytique puissantes permettre d’écrire des requêtes qui poser des questions importantes et génèrent des graphiques et des informations avancées.

Pour plus d’informations, consultez [moniteur Azure Functions](https://docs.microsoft.com/azure/azure-functions/functions-monitoring).

>[!div class="step-by-step"]
>[Précédent](azure-functions.md)
>[Suivant](logic-apps.md)