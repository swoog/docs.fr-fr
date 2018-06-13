---
title: Utilisation d’Azure Service Fabric
description: Architecture de microservices .NET pour les applications .NET en conteneur | Utilisation d’Azure Service Fabric
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/18/2017
ms.openlocfilehash: d65968e3d37f53cceee55120110ad4bb3c13d304
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33577676"
---
# <a name="using-azure-service-fabric"></a>Utilisation d’Azure Service Fabric

Azure Service Fabric est né quand Microsoft est passé des produits livrés en coffret, qui étaient généralement de style monolithique, à la fourniture de services. La création et l’exploitation de services à grande échelle, comme Azure SQL Database, Azure Cosmos DB, Azure Service Bus ou le backend de Cortana, ont façonné Service Fabric. La plateforme a évolué au fil du temps car de plus en plus de services l’ont adoptée. Surtout, Service Fabric devait s’exécuter non seulement dans Azure, mais également dans des déploiements de Windows Server autonomes.

L’objectif de Service Fabric est de résoudre les difficiles problèmes de la création et de l’exécution d’un service, et de l’utilisation efficace des ressources de l’infrastructure, afin que les équipes puissent solutionner les problèmes métier en utilisant une approche par microservices.

Service Fabric fournit deux grands composants principaux pour vous aider à créer des applications qui utilisent une approche par microservices :

-   Une plateforme qui fournit des services système pour déployer, mettre à l’échelle, mettre à niveau, détecter et redémarrer les services ayant connu une défaillance, découvrir l’emplacement des services, gérer les états et surveiller l’intégrité. Ces services système permettent de mettre en œuvre de nombreuses caractéristiques des microservices décrites précédemment.

-   Des API de programmation, ou frameworks, pour vous aider à créer des applications en tant que microservices : [des acteurs fiables et des services fiables](https://docs.microsoft.com/azure/service-fabric/service-fabric-choose-framework). Bien sûr, vous pouvez choisir n’importe quel code pour créer votre microservice, mais ces API remplissent très bien leur rôle et s’intègrent à la plateforme de façon plus étroite. De cette manière, vous pouvez obtenir des informations sur l’intégrité et les diagnostics, ou vous pouvez bénéficier d’une gestion fiable des états.

Service Fabric est agnostique quant à la façon dont vous créez votre service, et vous pouvez utiliser n’importe quelle technologie. Il fournit cependant des API de programmation intégrées qui facilitent la création de microservices.

Comme le montre la figure 4-26, vous pouvez créer et exécuter des microservices dans Service Fabric en tant que simples processus ou en tant que conteneurs Docker. Il est également possible de combiner des microservices basés sur des conteneurs avec des microservices basés sur des processus au sein du même cluster Service Fabric.

![](./media/image30.png)

**Figure 4-26**. Déploiement de microservices en tant que processus ou en tant que conteneurs dans Azure Service Fabric

Les clusters Service Fabric basés sur des hôtes Linux et Windows peuvent exécuter des conteneurs Linux Docker et des conteneurs Windows, respectivement.

Pour obtenir des informations récentes sur la prise en charge des conteneurs dans Azure Service Fabric, consultez [Service Fabric et les conteneurs](https://docs.microsoft.com/azure/service-fabric/service-fabric-containers-overview).

Service Fabric est un bon exemple d’une plateforme où vous pouvez définir une architecture logique (microservices métier ou contextes délimités) différente de l’implémentation physique, lesquelles ont été présentées dans la section [Architecture logique et architecture physique](#logical-architecture-versus-physical-architecture). Par exemple, si vous implémentez des [services fiables avec état](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-introduction) dans [Azure Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-overview), qui sont présentés plus loin dans la section [Microservices sans état et avec état](#stateless-versus-stateful-microservices), vous pouvez avoir un concept de microservice métier avec plusieurs services physiques.

Comme le montre la figure 4-27, en adoptant une perspective de microservice logique/métier, lors de l’implémentation d’un service fiable avec état Service Fabric, vous devez généralement implémenter deux niveaux de services. Le premier est le service fiable avec état backend, qui gère plusieurs partitions (chaque partition est un service avec état). Le second est le service frontal, ou service de passerelle, en charge du routage et de l’agrégation des données entre plusieurs partitions ou instances de service avec état. Ce service de passerelle gère également la communication côté client avec des boucles de nouvelles tentatives pour l’accès au service backend.
Il est appelé service de passerelle si vous implémentez votre service personnalisé, mais vous pouvez aussi utiliser le [service de proxy inverse](https://docs.microsoft.com/azure/service-fabric/service-fabric-reverseproxy) intégré de Service Fabric.

![](./media/image31.png)

**Figure 4-27**. Microservice métier avec plusieurs instances de service avec état et une passerelle personnalisée frontale

Dans tous les cas, quand vous utilisez des services fiables avec état Service Fabric, vous avez également un microservice (contexte délimité) logique ou métier qui est généralement constitué de plusieurs services physiques. Chacun d’eux, le service de passerelle et le service de partition, peuvent être implémentés en tant que services d’API web ASP.NET, comme le montre la figure 4-26.

Dans Service Fabric, vous pouvez regrouper et déployer des groupes de services sous la forme d’une [application Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-model), qui est l’unité d’empaquetage et de déploiement pour l’orchestrateur ou le cluster. Ainsi, l’application Service Fabric peut également être mappée à cette limite de microservice logique et métier autonome (ou contexte délimité) : vous pouvez donc déployer ces services de façon autonome.

## <a name="service-fabric-and-containers"></a>Service Fabric et les conteneurs

Pour ce qui est des conteneurs dans Service Fabric, vous pouvez également déployer des services dans des images de conteneur au sein d’un cluster Service Fabric. Comme le montre la figure 4-28, la plupart du temps, il n’y a qu’un seul conteneur par service.

![](./media/image32.png)

**Figure 4-28**. Microservice métier avec plusieurs services (conteneurs) dans Service Fabric

Cependant, des conteneurs appelés conteneurs « sidecar » (deux conteneurs qui doivent être déployés ensemble dans le cadre d’un service logique) sont également possibles dans Service Fabric. Le point essentiel est qu’un microservice métier est la limite logique autour de plusieurs éléments cohésifs. Dans de nombreux cas, il peut s’agit d’un seul service avec un seul modèle de données, mais dans d’autres cas, vous pouvez aussi avoir plusieurs services physiques.

En ce milieu d’année 2017, dans Service Fabric, vous ne pouvez pas déployer des services fiables avec état Service Fabric sur des conteneurs ; vous pouvez déployer seulement des services sans état et des services d’acteur dans des conteneurs. Notez cependant que vous pouvez combiner des services dans des processus et des services dans des conteneurs dans la même application Service Fabric, comme le montre la figure 4-29.

![](./media/image33.png)

**Figure 4-29**. Microservice métier mappé à une application Service Fabric avec des conteneurs et des services avec état

Pour plus informations sur la prise en charge des conteneurs dans Azure Service Fabric, consultez [Service Fabric et les conteneurs](https://docs.microsoft.com/azure/service-fabric/service-fabric-containers-overview).

## <a name="stateless-versus-stateful-microservices"></a>Microservices sans état et avec état

Comme mentionné précédemment, chaque microservice (contexte délimité logique) doit avoir son modèle de domaine (données et logique). Dans le cas de microservices sans état, les bases de données sont externes, utilisant des options relationnelles comme SQL Server, ou NoSQL, comme MongoDB ou Azure Cosmos DB.

Cependant, les services eux-mêmes peuvent également être avec état dans Service Fabric, ce qui signifie que les données se trouvent dans le microservice. Ces données peuvent exister non seulement sur le même serveur, mais aussi dans le processus du microservice et en mémoire, et être conservées sur des disques durs et répliquées sur d’autres nœuds. La figure 4-30 montre les différentes approches.

![](./media/image34.png)

**Figure 4-30**. Microservices sans état et avec état

Une approche sans état est parfaitement valide et est plus facile à implémenter que des microservices avec état, car cette approche est similaire aux modèles traditionnels bien connus. Les microservices sans état imposent cependant de la latence entre les processus et les sources de données. Ils impliquent également le déplacement de plus d’éléments quand vous essayez d’améliorer les performances avec des caches et des files d’attente supplémentaires. Le résultat est que vous pouvez vous retrouver avec des architectures complexes qui ont trop de niveaux.

En revanche, les [microservices avec état](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-introduction#when-to-use-reliable-services-apis) peuvent exceller dans des scénarios avancés, car il n’y a pas de latence entre la logique et les données du domaine. Les traitements de données lourds, les back-end de jeux, les bases de données en tant que service et tous les autres scénarios avec une latence faible tirent parti des services avec état, qui permettent un état local pour un accès plus rapide.

Les services sans état et avec état sont complémentaires. Par exemple, vous pouvez voir dans la figure 4-30, dans le diagramme de droite, qu’un service avec état peut être fractionné en plusieurs partitions. Pour accéder à ces partitions, vous pouvez avoir besoin d’un service sans état agissant comme un service de passerelle, qui sait comment atteindre chaque partition en fonction de clés de partition.

Les services avec état présentent des inconvénients. Ils imposent un niveau de complexité qui permet la montée en charge. Les fonctionnalités qui seraient habituellement implémentées par des systèmes de base de données externes doivent être fournies pour des tâches comme la réplication des données entre des microservices avec état et le partitionnement des données. C’est un des domaines où un orchestrateur comme [Azure Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-platform-architecture) avec ses [services fiables avec état](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-introduction#when-to-use-reliable-services-apis) peut être le plus utile, en simplifiant le développement et le cycle de vie des microservices avec état grâce à [l’API Reliable Services](https://docs.microsoft.com/azure/service-fabric/service-fabric-work-with-reliable-collections) et [Reliable Actors](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-actors-introduction).

Les autres frameworks de microservices qui permettent les services avec état, qui prennent en charge le modèle d’acteur et qui améliorent la tolérance de panne et la latence entre la logique métier et les données sont Microsoft [Orléans](https://github.com/dotnet/orleans) de Microsoft Research et [Akka.NET](https://getakka.net/). Les deux frameworks améliorent actuellement leur prise en charge de Docker.

Notez que les conteneurs Docker sont eux-mêmes sans état. Si vous voulez implémenter un service avec état, vous avez besoin d’un des frameworks normatifs et de plus haut niveau supplémentaires précédemment indiqués. 

>[!div class="step-by-step"]
[Précédent] (scalable-available-multi-container-microservice-applications.md) [Suivant] (../docker-application-development-process/index.md)
