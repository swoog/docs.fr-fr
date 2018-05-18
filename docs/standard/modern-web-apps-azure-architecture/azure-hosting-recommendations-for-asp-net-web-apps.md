---
title: Recommandations sur l’hébergement Azure pour les applications web ASP.NET Core
description: Architecturer des applications web modernes avec ASP.NET Core et Azure | Recommandations sur l’hébergement Azure pour les applications web ASP.NET
author: ardalis
ms.author: wiwagn
ms.date: 10/07/2017
ms.openlocfilehash: aea8a54bdee7eebd977f8b67d9888c2288dcd26d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="azure-hosting-recommendations-for-aspnet-core-web-apps"></a>Recommandations sur l’hébergement Azure pour les applications web ASP.NET Core

> « Les leaders métier ne passent plus par les départements informatiques pour obtenir des applications du cloud (également appelé SaaS) et les paient comme ils paient un abonnement à un magazine. Quand ils n’ont plus besoin du service, ils peuvent annuler l’abonnement sans se retrouver avec du matériel inutilisé dans un coin. »  
> _\- Daryl Plummer, analyste chez Gartner_

## <a name="summary"></a>Récapitulatif

Quels que soient les besoins et l’architecture de votre application, Microsoft Azure peut la prendre en charge. Vos besoins d’hébergement peuvent être aussi simples que ceux d’un site web statique et aussi complexes que ceux d’une application extrêmement sophistiquée constituée de dizaines de services. Pour les applications ASP.NET Core monolithiques et les services qui les prennent en charge, il existe plusieurs configurations connues qui sont recommandées. Les recommandations ci-dessous sont regroupées en fonction du type de ressource à héberger, qu’il s’agisse d’applications complètes, de processus individuels ou de données.

## <a name="web-applications"></a>Applications Web

Les applications web peuvent être hébergées avec :

-   App Service Web Apps

-   Conteneurs

-   Azure Service Fabric

-   Des machines virtuelles

Entre tous, App Service Web Apps constitue l’approche recommandée pour la plupart des scénarios. Pour les architectures de microservices, envisagez une approche basée sur les conteneurs ou Service Fabric. Si vous avez besoin de contrôler davantage les machines qui exécutent votre application, envisagez le service Machines virtuelles Azure.

### <a name="app-service-web-apps"></a>App Service Web Apps

App Service Web Apps offre une plateforme entièrement managée, optimisée pour l’hébergement d’applications web. Il s’agit d’une offre de plateforme PaaS qui vous permet de vous concentrer sur votre logique métier, tandis qu’Azure fournit l’infrastructure nécessaire pour exécuter et mettre à l’échelle l’application. Voici quelques fonctionnalités clés d’App Service Web Apps :

-   Optimisation de DevOps (intégration et livraison continues, environnements multiples, tests A/B, prise en charge des scripts)

-   Échelle globale et haute disponibilité

-   Connexions aux plateformes SaaS et à vos données locales

-   Sécurité et conformité

-   Visual Studio, intégration

Azure App Service est le meilleur choix pour la plupart des applications web. Le déploiement et la gestion sont intégrés à la plateforme, les sites peuvent évoluer rapidement pour gérer des charges de trafic élevées, et l’équilibrage de charge et le gestionnaire de trafic intégrés offrent une haute disponibilité. Vous pouvez déplacer facilement des sites existants vers Azure App Service avec un outil de migration en ligne, utiliser une application open source de la galerie d’applications web, ou créer un site en utilisant le framework et les outils de votre choix. La fonctionnalité WebJobs facilite l’ajout du traitement de travaux en arrière-plan à votre application web App Service.

### <a name="containers-and-azure-container-service"></a>Conteneurs et Azure Container Service

Azure Container Service facilite la création, la configuration et la gestion d’un cluster de machines virtuelles qui sont préconfigurées pour exécuter des applications en conteneur. Il utilise une configuration optimisée d’outils de planification et d’orchestration open source connus. Vous pouvez ainsi faire appel à vos compétences existantes ou profiter de l’expertise vaste et toujours croissante de la communauté pour déployer et gérer sur Microsoft Azure des applications basées sur des conteneurs.

Azure Container Service facilite la création, la configuration et la gestion d’un cluster de machines virtuelles qui sont préconfigurées pour exécuter des applications en conteneur. Il utilise une configuration optimisée d’outils de planification et d’orchestration open source connus. Vous pouvez ainsi faire appel à vos compétences existantes ou profiter de l’expertise vaste et toujours croissante de la communauté pour déployer et gérer sur Microsoft Azure des applications basées sur des conteneurs.

Un des objectifs d’Azure Container Service est de fournir un environnement d’hébergement de conteneurs avec des technologies et des outils open source aujourd’hui répandus parmi les clients de Microsoft. À cette fin, Azure Container Service expose les points de terminaison d’API standard pour l’orchestrateur de votre choix (DC/OS, Docker Swarm ou Kubernetes). En utilisant ces points de terminaison, vous pouvez exploiter n’importe quel logiciel capable de communiquer avec ces points de terminaison. Par exemple, dans le cas du point de terminaison Docker Swarm, vous pouvez choisir d’utiliser l’interface de ligne de commande de Docker. Pour DC/OS, vous pouvez choisir l’interface de ligne de commande DCOS. Pour Kubernetes, vous pouvez choisir kubectl. La figure 11-1 montre comment utiliser ces points de terminaison pour gérer vos clusters de conteneurs.

![](./media/image11-1.png)

**Figure 11-1.** Gestion d’Azure Container Service avec des points de terminaison Docker, Kubernetes ou DC/OS.

### <a name="azure-service-fabric"></a>Azure Service Fabric

Service Fabric est un bon choix si vous créez une application ou que vous réécrivez une application existante pour utiliser une architecture de microservices. Les applications, qui s’exécutent sur un pool partagé de machines, peuvent commencer à une petite échelle et croître jusqu’à atteindre une échelle réellement massive, avec des centaines ou des milliers d’ordinateurs, en fonction des besoins. Les services avec état permettent de stocker de façon cohérente et fiable l’état de l’application, et Service Fabric gère automatiquement pour vous le partitionnement, la mise à l’échelle et la disponibilité des services. Service Fabric prend également en charge WebAPI avec Open Web Interface pour .NET (OWIN) et ASP.NET Core. Par rapport à App Service, Service Fabric offre plus de contrôle sur l’infrastructure sous-jacente, ou un accès direct à celle-ci. Vous pouvez vous connecter à distance à vos serveurs ou y configurer des tâches de démarrage.

### <a name="azure-virtual-machines"></a>Machines virtuelles Azure

Si vous avez une application existante qui nécessite des modifications substantielles pour s’exécuter dans App Service ou Service Fabric, vous pouvez choisir Machines virtuelles afin de simplifier la migration vers le cloud. Cependant, la configuration, la sécurisation et la gestion des machines virtuelles nécessitent beaucoup plus de temps et d’expertise en informatique comparé à Azure App Service et de Service Fabric. Si vous envisagez d’utiliser Machines virtuelles Azure, veillez à prendre en compte le travail continu de maintenance nécessaire pour appliquer les correctifs, mettre à jour et gérer votre environnement de machines virtuelles. Machines virtuelles Azure est une infrastructure IaaS, tandis qu’App Service et Service Fabric sont des plateformes Paas.

#### <a name="feature-comparison"></a>Comparaison des fonctionnalités

| Fonctionnalité App Service | Service Fabric | Machine virtuelle |
|---------|----------|----------|
| Déploiement quasi instantané | X | X | |
| Mise à l’échelle (scale up) vers des machines plus puissantes sans redéploiement | X | X | |
| Les instances partagent le contenu et la configuration ; pas de redéploiement ou de reconfiguration nécessaire lors d’une mise à l’échelle | X | X | |
| Plusieurs environnements de déploiement (production, préproduction) | X | X | |
| Gestion automatique de la mise à jour du système d’exploitation | X | | |
| Passage fluide entre les plateformes 32/64 bits | X | | |
| Déploiement du code avec Git, FTP | X | | X |
| Déploiement du code avec WebDeploy | X | | X |
| Déploiement du code avec TFS | X | X | X |
| Hébergement de niveau web ou service web, avec une architecture multiniveau | X | X | X |
| Accès à des services Azure comme Service Bus, Stockage, SQL Database | X | X | X |
| Installation de n’importe quel MSI personnalisé | | X | X |

## <a name="logical-processes"></a>Processus logiques

Les processus logiques individuels qui peuvent être dissociés du reste de l’application peuvent être déployés indépendamment sur Azure Functions de manière « serveless ». Azure Functions vous permet de simplement écrire le code dont vous avez besoin pour un problème donné, sans se préoccuper de l’application ou de l’infrastructure pour l’exécuter. Vous pouvez choisir parmi une variété de langages de programmation, notamment C\#, F\#, Node.js, Python et PHP, ce qui vous permet de choisir le langage le plus productif pour la tâche à traiter. Comme la plupart des solutions cloud, vous payez seulement pour la durée de votre utilisation, et vous pouvez faire confiance à Azure Functions pour monter en puissance au fil des besoins.

## <a name="data"></a>Données

Azure propose un large éventail d’options de stockage des données, afin que votre application puisse utiliser le fournisseur de données approprié pour les données en question.

Pour les données transactionnelles relationnelles, les bases de données Azure SQL Database sont la meilleure option. Pour de hautes performances avec les données qui sont principalement en lecture, un cache Redis s’appuyant sur une base de données Azure SQL Database est une bonne solution.

Les données JSON non structurées peuvent être stockées de différentes façons : colonnes SQL Database, objets blob ou tables dans Stockage Azure, ou encore DocumentDB. Parmi ces possibilités, DocumentDB offre les meilleures fonctionnalités de requête et il s’agit de l’option recommandée pour de grandes quantités de documents JSON qui doivent prendre en charge les requêtes.

Les données basées sur des commandes ou des événements transitoires pour orchestrer le comportement des applications peuvent utiliser Azure Service Bus ou Stockage File d’attente Azure. Azure Service Bus offre davantage de souplesse et est le service recommandé pour les échanges complexes de messages au sein des applications et entre elles.

## <a name="architecture-recommendations"></a>Recommandations en matière d’architecture

Les exigences de votre application doivent dicter son architecture. De nombreux services Azure différents sont disponibles : le choix du bon service est une décision importante. Microsoft propose une galerie d’architectures de référence pour aider à identifier des architectures classiques optimisées pour les scénarios courants. Vous pouvez adopter une architecture de référence qui correspond étroitement aux exigences de votre application ou qui offre au moins un point de départ.

La figure 11-2 montre un exemple d’architecture de référence. Ce diagramme décrit une approche recommandée pour l’architecture d’un site web de système de gestion de contenu Sitecore optimisé pour le marketing.

![](./media/image11-2.png)

**Figure 11-2.** Architecture de référence d’un site web de marketing Sitecore.

**Informations de référence : recommandations sur l’hébergement Azure**

-   Architectures de solutions Azure\
    <https://azure.microsoft.com/solutions/architecture/>

-   Guide du développeur Azure\
    <https://azure.microsoft.com/campaigns/developer-guide/>

-   Présentation d’Azure App Service\
    <https://docs.microsoft.com/azure/app-service/app-service-value-prop-what-is>

-   Comparaison entre Azure App Service, Machines virtuelles, Service Fabric et Services cloud\
    <https://docs.microsoft.com/azure/app-service-web/choose-web-site-cloud-service-vm>

>[!div class="step-by-step"]
[Précédent] (development-process-for-azure.md)
