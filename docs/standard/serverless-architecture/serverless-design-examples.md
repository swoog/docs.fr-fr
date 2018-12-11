---
title: Exemples de conception sans serveur - applications sans serveur
description: Comprendre l’éventail de scénarios pris en charge par les architectures sans serveur, à partir de la planification et le traitement basé sur les événements déclencheurs de fichier et du processus de flux de données.
author: JEREMYLIKNESS
ms.author: jeliknes
ms.date: 06/26/2018
ms.openlocfilehash: cf46c601ac6aa401c7c37bd64c1f8981589ebd2e
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53146705"
---
# <a name="serverless-design-examples"></a>Exemples de conception sans serveur

Il existe de nombreux modèles de conception qui existent pour sans serveur. Cette section comporte quelques scénarios courants qui utilisent sans serveur. Ce que tous les exemples ont en commun est la combinaison fondamentale d’une événement déclencheur et la logique métier.

## <a name="scheduling"></a>Planification

Planification des tâches est une fonction commune. Le diagramme suivant montre une base de données héritée n’ayant pas de vérifications d’intégrité approprié. La base de données doive être nettoyé régulièrement. La fonction sans serveur trouve des données non valides et il nettoie. Le déclencheur est un minuteur qui exécute le code selon une planification.

![Planification sans serveur](./media/serverless-scheduling.png)

## <a name="command-and-query-responsibility-segregation-cqrs"></a>Commande et répartition de responsabilité de requête (CQRS)

Commande et répartition de requête (CQRS) est un modèle qui fournit les données de différentes interfaces pour lecture (ou l’interrogation) et les opérations qui modifient les données. Elle résout plusieurs problèmes courants. Dans les systèmes traditionnels de créer en lecture mise à jour et supprimer (CRUD) en fonction, conflits peuvent se produire à partir d’un volume élevé de lectures et écritures dans le même magasin de données. Le verrouillage peut se produisent fréquemment et ralentir considérablement les lectures. Souvent, les données sont présentées comme un composite de plusieurs objets de domaine et les opérations de lecture doit combiner des données à partir de différentes entités.

À l’aide de la CQRS, une lecture peut impliquer une entité « aplatie » spéciale qui modélise la manière de consommer les données. La lecture est gérée différemment de la façon dont elle est stockée. Par exemple, bien que la base de données peut stocker un contact en tant qu’en-tête enregistrement avec un enregistrement d’adresse enfant, la lecture peut impliquer une entité avec en-tête et de propriétés de l’adresse. Il existe une multitude d’approches pour créer le modèle de lecture. Il peut être matérialisé à partir de vues. Les opérations de mise à jour peuvent être encapsulées en tant qu’événements isolés qui déclenchent puis les mises à jour des deux modèles différents. Il existe des modèles distincts pour lire et écrire.

![Exemple CQRS](./media/cqrs-example.png)

Sans serveur peut prendre en charge le modèle CQRS en fournissant les points de terminaison séparées. Une fonction sans serveur prend en charge les requêtes ou les lectures et une autre fonction sans serveur ou un ensemble de fonctions gère les opérations de mise à jour. Une fonction sans serveur peut également être responsable de la mise à jour du modèle de lecture et peut être déclenchée par la base de données [le flux de modification](https://docs.microsoft.com/azure/cosmos-db/change-feed). Développement frontal est simplifiée à la connexion aux points de terminaison nécessaires. Traitement d’événements est géré sur le serveur principal. Ce modèle s’adapte également bien pour les grands projets, car les différentes équipes peuvent travailler sur les différentes opérations.

## <a name="event-based-processing"></a>Traitement basé sur des événements

Dans les systèmes basés sur le message, les événements sont souvent collectés dans les files d’attente ou rubriques éditeur/abonné faisant l’objet de fonction. Ces événements peuvent déclencher des fonctions sans serveur pour exécuter une partie de la logique métier. Un exemple de traitement basé sur des événements est un système de source d’événement. Un « événement » est déclenché pour marquer une tâche comme terminée. Une fonction sans serveur déclenchée par l’événement met à jour le document de base de données appropriée. Une deuxième fonction sans serveur peut utiliser l’événement pour mettre à jour le modèle de lecture pour le système. [Azure Event Grid](https://docs.microsoft.com/azure/event-grid/overview) offre un moyen d’intégrer des événements avec des fonctions en tant qu’abonnés.

> Les événements sont des messages d’information. Pour plus d’informations, consultez [modèle d’approvisionnement en événements](https://docs.microsoft.com/azure/architecture/patterns/event-sourcing).

## <a name="file-triggers-and-transformations"></a>Les déclencheurs de fichier et transformations

Extraire, transformer et chargement (ETL) est une fonction d’entreprise courants. Sans serveur est une excellente solution pour ETL, car il permet au code d’être déclenchée dans le cadre d’un pipeline. Composants de code individuels peuvent adresser des différents aspects. Une fonction sans serveur peut télécharger le fichier, un autre applique la transformation, et une autre charge les données. Le code peut être testé et déployé indépendamment, rendant ainsi plus facile à maintenir et mettre à l’échelle lorsque cela est nécessaire.

![Transformations et les déclencheurs de fichier sans serveur](./media/serverless-file-triggers.png)

Dans le diagramme, « froid de stockage » fournit des données qui sont analysées dans [Azure Stream Analytique](https://docs.microsoft.com/azure/stream-analytics). Les problèmes rencontrés dans le flux de données déclenchent une fonction Azure pour résoudre l’anomalie.

## <a name="asynchronous-background-processing-and-messaging"></a>Traitement asynchrone en arrière-plan et messagerie

Messagerie asynchrone et le traitement en arrière-plan permettent aux applications amorcer le processus sans attendre. Un exemple de traitement asynchrone est une application de reconnaissance optique de caractères. Une image est envoyée et en attente de traitement. Analyse de l’image pour extraire le texte peut prendre un temps et une fois qu’il a terminé une notification est envoyée. Sans serveur peut gérer l’appel et le résultat dans ce scénario.

## <a name="web-apps-and-apis"></a>API et applications web

Un scénario courant pour sans serveur est N-tier applications, généralement celles où la couche d’interface utilisateur est une application web. La popularité des Applications à Page unique (SPA) a récemment apparues. Les applications SPA restituer une page unique, puis s’appuient sur les appels d’API et les données retournées pour restituer dynamiquement la nouvelle interface utilisateur sans recharger une page complète. Rendu côté client fournit une application beaucoup plus rapide et plus réactive à l’utilisateur final.

Des points de terminaison sans serveur déclenchées par les appels HTTP peuvent être utilisés pour gérer les demandes d’API. Par exemple, une société de services ad peut appeler une fonction sans serveur avec les informations de profil utilisateur pour demander des publicités personnalisées. La fonction sans serveur retourne d’ad et rend la page web.

![API web sans serveur](./media/serverless-web-api.png)

## <a name="data-pipeline"></a>Pipeline de données

Les fonctions sans serveur peuvent être utilisées pour faciliter un pipeline de données. Dans cet exemple, un fichier déclenche une fonction pour convertir des données dans un fichier CSV pour les lignes de données dans une table. La table organisée autorise un tableau de bord Power BI à présenter analytique à l’utilisateur final.

![Pipeline de données sans serveur](./media/serverless-data-pipeline.png)

## <a name="stream-processing"></a>Traitement de Stream

Appareils et capteurs génèrent souvent des flux de données qui doivent être traitées en temps réel. Il existe un certain nombre de technologies qui peuvent capturer les messages et flux [Event Hubs](https://docs.microsoft.com/azure/event-hubs/event-hubs-what-is-event-hubs) et [IoT Hub](https://docs.microsoft.com/azure/iot-hub) à [Service Bus](/service-bus). Quel que soit le transport, sans serveur est un mécanisme idéal pour traiter les messages et les flux de données qu’ils vous parviennent. Sans serveur peut évoluer rapidement pour répondre à la demande de gros volumes de données. Le code sans serveur peut appliquer une logique métier pour analyser les données et la sortie dans un format structuré pour l’action et d’analytique.

![Traitement de flux de données sans serveur](./media/serverless-stream-processing.png)

## <a name="api-gateway"></a>Passerelle d’API

Une passerelle d’API fournit un point d’entrée unique pour les clients et puis intelligemment achemine les demandes vers les services back-end. Il est utile de gérer de grands ensembles de services. Il peut également gérer le contrôle de version et simplifient le développement en facilement clients qui se connectent à des environnements disparates. Sans serveur peut gérer principale mise à l’échelle de microservices individuels lors de la présentation d’un serveur frontal unique via une passerelle d’API.

![Passerelle d’API sans serveur](./media/serverless-api-gateway.png)

## <a name="recommended-resources"></a>Ressources recommandées

* [Azure Event Grid](https://docs.microsoft.com/azure/event-grid/overview)
* [Azure IoT Hub](https://docs.microsoft.com/azure/iot-hub)
* [Défis et solutions pour la gestion des données distribuée](../microservices-architecture/architect-microservice-container-applications/distributed-data-management.md)
* [Conception de microservices : identification des limites de microservice](https://docs.microsoft.com/azure/architecture/microservices/microservice-boundaries)
* [Event Hubs](https://docs.microsoft.com/azure/event-hubs/event-hubs-what-is-event-hubs)
* [Modèle d’approvisionnement en événements](https://docs.microsoft.com/azure/architecture/patterns/event-sourcing)
* [Implémentation du modèle de disjoncteur](../microservices-architecture/implement-resilient-applications/implement-circuit-breaker-pattern.md)
* [IoT Hub](https://docs.microsoft.com/azure/iot-hub)
* [Service Bus](https://docs.microsoft.com/azure/service-bus)
* [Utilisation de la modification de flux prise en charge dans Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/change-feed)

>[!div class="step-by-step"]
>[Précédent](serverless-architecture-considerations.md)
>[Suivant](azure-serverless-platform.md)