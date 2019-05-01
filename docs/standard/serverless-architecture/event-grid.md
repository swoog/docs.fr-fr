---
title: Azure Event Grid - applications sans serveur
description: Azure Event Grid est une solution sans serveur pour livraison fiable d’événement et le routage à grande échelle sur un modèle de paiement par événement.
author: JEREMYLIKNESS
ms.author: jeliknes
ms.date: 06/26/2018
ms.openlocfilehash: 4970130ede0c96c645129ee6c8c7d54cb1114042
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61959390"
---
# <a name="event-grid"></a>Event Grid

[Azure Event Grid](/azure/event-grid/overview) fournit une infrastructure sans serveur pour les applications basées sur des événements. Vous pouvez publier sur Event Grid à partir de n’importe quelle source et consommer des messages à partir de n’importe quelle plateforme. Event Grid dispose également d’une prise en charge intégrée pour les événements à partir des ressources Azure pour simplifier l’intégration avec vos applications. Par exemple, vous pouvez vous abonner aux événements de stockage blob pour avertir votre application lors du chargement d’un fichier. Votre application peut ensuite publier un message de grille d’événement personnalisé qui est consommé par d’autres cloud ou applications locales. Event Grid est conçu pour gérer de manière fiable à grande échelle. Vous bénéficiez des avantages de la publication et l’abonnement aux messages sans la surcharge liée à la configuration de l’infrastructure nécessaire.

![Logo de grille d’événement](./media/event-grid-logo.png)

Les principales fonctionnalités de grille d’événement sont les suivantes :

* Routage d’événement entièrement géré.
* Près de diffusion d’événements en temps réel à grande échelle.
* Une large couverture à l’intérieur et en dehors d’Azure.

## <a name="scenarios"></a>Scénarios

Event Grid résout les différents scénarios. Cette section couvre trois des plus courants.

### <a name="ops-automation"></a>Automatisation des opérations

![Automatisation des opérations](./media/ops-automation.png)

Event Grid peut aider à automation de vitesse et simplifier l’application des stratégies en notifiant [Azure Automation](https://docs.microsoft.com/azure/automation) lorsque l’infrastructure est configurée.

### <a name="application-integration"></a>Intégration d’applications

![Intégration d’applications](./media/app-integration.png)

Vous pouvez utiliser Event Grid pour connecter votre application à d’autres services. À l’aide des protocoles HTTP standard, les applications héritées même peuvent être facilement modifiées pour publier des messages d’Event Grid. Raccordements Web sont disponibles pour d’autres services et les plateformes pour consommer les messages d’Event Grid.

### <a name="serverless-apps"></a>Applications sans serveur

![Applications sans serveur](./media/serverless-apps.png)

Event Grid peut déclencher Azure Functions, Logic Apps ou votre propre code personnalisé. Le principal avantage de l’utilisation d’Event Grid est qu’il utilise un *push* mécanisme pour envoyer des messages lorsque des événements se produisent. L’architecture de push consomme moins de ressources et évolue mieux que *d’interrogation* mécanismes. L’interrogation doit vérifier les mises à jour selon un intervalle régulier.

## <a name="event-grid-vs-other-azure-messaging-services"></a>Event Grid et autres services de messagerie Azure

Azure fournit plusieurs services de messagerie, y compris [Event Hubs](https://docs.microsoft.com/azure/event-hubs) et [Service Bus](https://docs.microsoft.com/azure/service-bus-messaging). Chacun est conçu pour traiter un ensemble spécifique de cas d’usage. Le diagramme suivant fournit une vue d’ensemble des différences entre les services.

![Comparaison de la messagerie de Azure](./media/azure-messaging-services.png)

Pour une comparaison plus détaillée, consultez [comparer les services de messagerie](https://docs.microsoft.com/azure/event-grid/compare-messaging-services).

## <a name="performance-targets"></a>Objectifs de performance

À l’aide d’Event Grid, vous pouvez tirer parti des performances suivant garantit :

* Subsecond latence de bout en bout dans le 99e centile.
* disponibilité de 99,99 %.
* 10 millions d’événements par seconde par région.
* abonnements de 100 millions par région.
* latence du serveur de publication de 50 millisecondes.
* nouvelle tentative de 24 heures avec interruption exponentielle pour la remise garantie dans la fenêtre de 1 jour.
* Basculement régional transparent.

## <a name="event-grid-schema"></a>Schéma Event Grid

Event Grid utilise un schéma standard pour encapsuler des événements personnalisés. Le schéma ressemble à une enveloppe qui encapsule votre élément de données personnalisées. Voici un exemple de message Event Grid :

```json
[{
    "id": "03e24f21-a955-43cc-8921-1f61a6081ce0",
    "eventType": "myCustomEvent",
    "subject": "foo/bar/12",
    "eventTime": "2018-09-22T10:36:01+00:00",
    "data": {
        "favoriteColor": "blue",
        "favoriteAnimal": "panther",
        "favoritePlanet": "Jupiter"
    },
    "dataVersion": "1.0"
}]
```

Tout savoir sur le message est standard, sauf le `data` propriété. Vous pouvez inspecter le message et utiliser le `eventType` et `dataVersion` désérialiser la partie personnalisée de la charge utile.

## <a name="azure-resources"></a>Ressources Azure

Le principal avantage de l’utilisation d’Event Grid est les messages automatique générés par Azure. Dans Azure, ressources publient automatiquement sur un *rubrique* qui vous permet de vous abonner à différents événements. Le tableau suivant répertorie les types de ressources, les types de messages et les événements qui sont disponibles automatiquement.

| Ressources Azure | Type d'événement | Description |
| -------------- | ---------- | ----------- |
| Abonnement Azure | Microsoft.Resources.ResourceWriteSuccess | Déclenché quand une ressource créer ou mettre à jour d’opération réussit. |
| | Microsoft.Resources.ResourceWriteFailure | Déclenché lors de la création d’une ressource ou opération de mise à jour échoue. |
| | Microsoft.Resources.ResourceWriteCancel | Déclenché quand une ressource créer ou mettre à jour d’opération est annulée. |
|  | Microsoft.Resources.ResourceDeleteSuccess | Déclenché lorsqu’une opération de suppression de ressource réussit. |
|  | Microsoft.Resources.ResourceDeleteFailure | Déclenché lorsqu’une opération de suppression de ressource échoue. |
| | Microsoft.Resources.ResourceDeleteCancel | Déclenché lorsqu’une opération de suppression de ressource est annulée. Cet événement se produit lorsque le déploiement d’un modèle est annulé. |
| Stockage d’objets BLOB | Microsoft.Storage.BlobCreated | Déclenché lorsqu’un objet blob est créé. |
| | Microsoft.Storage.BlobDeleted | Déclenché lorsqu’un objet blob est supprimé. |
| Concentrateurs d’événements | Microsoft.EventHub.CaptureFileCreated | Déclenché lorsqu’un fichier de capture est créé.
| IoT Hub | Microsoft.Devices.DeviceCreated | Publié quand un appareil est inscrit à un IoT hub. |
| | Microsoft.Devices.DeviceDeleted | Publié quand un appareil est supprimé d’un hub IoT. |
| Groupes de ressources | Microsoft.Resources.ResourceWriteSuccess | Déclenché quand une ressource créer ou mettre à jour d’opération réussit. |
| | Microsoft.Resources.ResourceWriteFailure | Déclenché lors de la création d’une ressource ou opération de mise à jour échoue. |
| | Microsoft.Resources.ResourceWriteCancel | Déclenché quand une ressource créer ou mettre à jour d’opération est annulée. |
| | Microsoft.Resources.ResourceDeleteSuccess | Déclenché lorsqu’une opération de suppression de ressource réussit. |
| | Microsoft.Resources.ResourceDeleteFailure | Déclenché lorsqu’une opération de suppression de ressource échoue. |
| | Microsoft.Resources.ResourceDeleteCancel | Déclenché lorsqu’une opération de suppression de ressource est annulée. Cet événement se produit lorsque le déploiement d’un modèle est annulé. |

Pour plus d’informations, consultez [schéma d’Azure Event Grid](https://docs.microsoft.com/azure/event-grid/event-schema).

Vous pouvez accéder à Event Grid à partir de n’importe quel type d’application, même s’il s’exécute en local.

## <a name="conclusion"></a>Conclusion

Ce chapitre vous a présenté la plateforme serverless Azure qui se compose d’Azure Functions, Logic Apps et Event Grid. Vous pouvez utiliser ces ressources pour créer une architecture d’application entièrement sans serveur, ou créer une solution hybride qui interagit avec d’autres ressources de cloud et serveurs locaux. Combiné avec une plateforme de données sans serveur telles que [SQL Azure](https://docs.microsoft.com/azure/sql-database) ou [CosmosDB](https://docs.microsoft.com/azure/cosmos-db/introduction), vous pouvez créer entièrement géré cloud des applications natives.

## <a name="recommended-resources"></a>Ressources recommandées

* [Plans app service](https://docs.microsoft.com/azure/app-service/azure-web-sites-web-hosting-plans-in-depth-overview)
* [Application Insights](https://docs.microsoft.com/azure/application-insights)
* [Application Insights Analytique](https://docs.microsoft.com/azure/application-insights/app-insights-analytics)
* [Azure : Importez votre application dans le cloud avec Azure Functions sans serveur](https://channel9.msdn.com/events/Connect/2017/E102)
* [Azure Event Grid](https://docs.microsoft.com/azure/event-grid/overview)
* [Schéma d’événement Azure Event Grid](https://docs.microsoft.com/azure/event-grid/event-schema)
* [Azure Event Hubs](https://docs.microsoft.com/azure/event-hubs)
* [Documentation Azure Functions](https://docs.microsoft.com/azure/azure-functions)
* [Azure Functions concepts des déclencheurs et liaisons](https://docs.microsoft.com/azure/azure-functions/functions-triggers-bindings)
* [Azure Logic Apps](https://docs.microsoft.com/azure/logic-apps)
* [Azure Service Bus](https://docs.microsoft.com/azure/service-bus-messaging)
* [Stockage Table Azure](https://docs.microsoft.com/azure/cosmos-db/table-storage-overview)
* [Comparer functions 1.x et 2.x](https://docs.microsoft.com/azure/azure-functions/functions-versions)
* [Connexion aux sources de données sur site avec la passerelle de données Azure en local](https://docs.microsoft.com/azure/analysis-services/analysis-services-gateway)
* [Créer votre première fonction dans le portail Azure](https://docs.microsoft.com/azure/azure-functions/functions-create-first-azure-function)
* [Créer votre première fonction à l’aide de l’interface CLI Azure](https://docs.microsoft.com/azure/azure-functions/functions-create-first-azure-function-azure-cli)
* [Créer votre première fonction à l’aide de Visual Studio](https://docs.microsoft.com/azure/azure-functions/functions-create-your-first-function-visual-studio)
* [Fonctions prises en charge des langues](https://docs.microsoft.com/azure/azure-functions/supported-languages)
* [Surveiller les fonctions Azure](https://docs.microsoft.com/azure/azure-functions/functions-monitoring)
* [Travailler avec Azure Functions Proxies](https://docs.microsoft.com/azure/azure-functions/functions-proxies)

>[!div class="step-by-step"]
>[Précédent](logic-apps.md)
>[Suivant](durable-azure-functions.md)
