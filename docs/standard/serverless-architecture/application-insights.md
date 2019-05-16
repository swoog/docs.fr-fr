---
title: Application Insights - applications sans serveur
description: Application Insights est une plateforme de diagnostics sans serveur qui permet aux développeurs de détecter, trier et diagnostiquer les problèmes dans les applications web, les applications mobiles, les applications de bureau et les microservices.
author: JEREMYLIKNESS
ms.author: jeliknes
ms.date: 06/26/2018
ms.openlocfilehash: 1f5b99fba448c2c1c12139524ffdcd3708b3c956
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65643354"
---
# <a name="telemetry-with-application-insights"></a><span data-ttu-id="2940f-103">Données de télémétrie avec Application Insights</span><span class="sxs-lookup"><span data-stu-id="2940f-103">Telemetry with Application Insights</span></span>

<span data-ttu-id="2940f-104">[Application Insights](https://docs.microsoft.com/azure/application-insights) est une plateforme de diagnostics sans serveur qui permet aux développeurs de détecter, trier et diagnostiquer les problèmes dans les applications web, les applications mobiles, les applications de bureau et les microservices.</span><span class="sxs-lookup"><span data-stu-id="2940f-104">[Application Insights](https://docs.microsoft.com/azure/application-insights) is a serverless diagnostics platform that enables developers to detect, triage, and diagnose issues in web apps, mobile apps, desktop apps, and microservices.</span></span> <span data-ttu-id="2940f-105">Vous pouvez activer Application Insights pour les applications de fonction simplement en mettant en marche d’un commutateur dans le portail.</span><span class="sxs-lookup"><span data-stu-id="2940f-105">You can turn on Application Insights for function apps simply by flipping a switch in the portal.</span></span> <span data-ttu-id="2940f-106">Application Insights fournit toutes ces fonctionnalités sans avoir à configurer un serveur ou configurer votre propre base de données.</span><span class="sxs-lookup"><span data-stu-id="2940f-106">Application Insights provides all of these capabilities without you having to configure a server or set up your own database.</span></span> <span data-ttu-id="2940f-107">Toutes les fonctionnalités d’Application Insights sont fournis en tant que service qui intègre automatiquement avec vos applications.</span><span class="sxs-lookup"><span data-stu-id="2940f-107">All of Application Insights' capabilities are provided as a service that automatically integrates with your apps.</span></span>

![Logo d’application Insights](./media/application-insights-logo.png)

<span data-ttu-id="2940f-109">Ajout d’Application Insights aux applications existantes, il suffit que l’ajout d’une clé d’instrumentation aux paramètres de votre application.</span><span class="sxs-lookup"><span data-stu-id="2940f-109">Adding Application Insights to existing apps is as easy as adding an instrumentation key to your application's settings.</span></span> <span data-ttu-id="2940f-110">Avec Application Insights, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="2940f-110">With Application Insights you can:</span></span>

* <span data-ttu-id="2940f-111">Créer des graphiques personnalisés et des alertes en fonction des mesures telles que le nombre d’appels de fonction, le temps que nécessaire pour exécuter une fonction et les exceptions</span><span class="sxs-lookup"><span data-stu-id="2940f-111">Create custom charts and alerts based on metrics such as number of function invocations, the time it takes to run a function, and exceptions</span></span>
* <span data-ttu-id="2940f-112">Analyser les défaillances et les exceptions du serveur</span><span class="sxs-lookup"><span data-stu-id="2940f-112">Analyze failures and server exceptions</span></span>
* <span data-ttu-id="2940f-113">Explorez les performances par opération et de mesurer le temps que nécessaire pour appeler des dépendances tierces</span><span class="sxs-lookup"><span data-stu-id="2940f-113">Drill into performance by operation and measure the time it takes to call third-party dependencies</span></span>
* <span data-ttu-id="2940f-114">Surveiller l’utilisation processeur, mémoire et les tarifs sur tous les serveurs qui hébergent vos applications de fonction</span><span class="sxs-lookup"><span data-stu-id="2940f-114">Monitor CPU usage, memory, and rates across all servers that host your function apps</span></span>
* <span data-ttu-id="2940f-115">Afficher un flux live de métriques, notamment le nombre de demandes et la latence pour vos applications de fonction</span><span class="sxs-lookup"><span data-stu-id="2940f-115">View a live stream of metrics including request count and latency for your function apps</span></span>
* <span data-ttu-id="2940f-116">Utilisez [Analytique](https://docs.microsoft.com/azure/application-insights/app-insights-analytics) pour rechercher, interroger et créer des graphiques personnalisés sur vos données (fonction)</span><span class="sxs-lookup"><span data-stu-id="2940f-116">Use [Analytics](https://docs.microsoft.com/azure/application-insights/app-insights-analytics) to search, query, and create custom charts over your function data</span></span>

![Explorateur de mesures](./media/metrics-explorer.png)

<span data-ttu-id="2940f-118">En plus des données de télémétrie intégrée, il est également possible de générer des données de télémétrie personnalisées.</span><span class="sxs-lookup"><span data-stu-id="2940f-118">In addition to built-in telemetry, it's also possible to generate custom telemetry.</span></span> <span data-ttu-id="2940f-119">L’extrait de code suivant crée un client de télémétrie personnalisée à l’aide de la clé d’instrumentation définie pour l’application de fonction :</span><span class="sxs-lookup"><span data-stu-id="2940f-119">The following code snippet creates a custom telemetry client using the instrumentation key set for the function app:</span></span>

```csharp
public static TelemetryClient telemetry = new TelemetryClient()
{
    InstrumentationKey = Environment.GetEnvironmentVariable("APPINSIGHTS_INSTRUMENTATIONKEY")
};
```

<span data-ttu-id="2940f-120">Le code suivant mesure le temps nécessaire pour insérer une nouvelle ligne dans un [stockage Table Azure](https://docs.microsoft.com/azure/cosmos-db/table-storage-overview) instance :</span><span class="sxs-lookup"><span data-stu-id="2940f-120">The following code measures how long it takes to insert a new row into an [Azure Table Storage](https://docs.microsoft.com/azure/cosmos-db/table-storage-overview) instance:</span></span>

```csharp
var operation = TableOperation.Insert(entry);
var startTime = DateTime.UtcNow;
var timer = System.Diagnostics.Stopwatch.StartNew();
await table.ExecuteAsync(operation);
telemetry.TrackDependency("AzureTableStorageInsert", "Insert", startTime, timer.Elapsed, true);
```

<span data-ttu-id="2940f-121">Le graphique de performances résultant s’affiche :</span><span class="sxs-lookup"><span data-stu-id="2940f-121">The resulting performance graph is shown:</span></span>

![Télémétrie personnalisée](./media/custom-telemetry.png)

<span data-ttu-id="2940f-123">Les données de télémétrie personnalisées révèle le temps moyen pour insérer une nouvelle ligne est 32.6 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="2940f-123">The custom telemetry reveals the average time to insert a new row is 32.6 milliseconds.</span></span>

<span data-ttu-id="2940f-124">Application Insights fournit un moyen puissant et pratique pour se connecter à des données de télémétrie détaillées relatives à vos applications sans serveur.</span><span class="sxs-lookup"><span data-stu-id="2940f-124">Application Insights provides a powerful, convenient way to log detailed telemetry about your serverless applications.</span></span> <span data-ttu-id="2940f-125">Vous contrôlez totalement le niveau de suivi et de journalisation qui est fournie.</span><span class="sxs-lookup"><span data-stu-id="2940f-125">You have full control over the level of tracing and logging that is provided.</span></span> <span data-ttu-id="2940f-126">Vous pouvez suivre les statistiques personnalisées telles que les événements, les dépendances et affichage de page.</span><span class="sxs-lookup"><span data-stu-id="2940f-126">You can track custom statistics such as events, dependencies, and page view.</span></span> <span data-ttu-id="2940f-127">Enfin, l’analytique puissantes permettre d’écrire des requêtes qui poser des questions importantes et génèrent des graphiques et des informations avancées.</span><span class="sxs-lookup"><span data-stu-id="2940f-127">Finally, the powerful analytics enable you to write queries that ask important questions and generate charts and advanced insights.</span></span>

<span data-ttu-id="2940f-128">Pour plus d’informations, consultez [moniteur Azure Functions](https://docs.microsoft.com/azure/azure-functions/functions-monitoring).</span><span class="sxs-lookup"><span data-stu-id="2940f-128">For more information, see [Monitor Azure Functions](https://docs.microsoft.com/azure/azure-functions/functions-monitoring).</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="2940f-129">[Précédent](azure-functions.md)
>[Suivant](logic-apps.md)</span><span class="sxs-lookup"><span data-stu-id="2940f-129">[Previous](azure-functions.md)
[Next](logic-apps.md)</span></span>
