---
title: Orchestration microservices et applications multicontainer pour une haute évolutivité et la disponibilité
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/19/2017
ms.openlocfilehash: 3a505e10b2a37032a7ccfefdf4a6f4bb64d65486
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33579546"
---
# <a name="orchestrating-microservices-and-multicontainer-applications-for-high-scalability-and-availability"></a>Orchestration microservices et applications multicontainer pour une haute évolutivité et la disponibilité

L’utilisation d’orchestrateurs pour les applications prêtes pour la production est essentielle si votre application est basée sur des microservices ou si elle est simplement répartie entre plusieurs conteneurs. Comme expliqué précédemment, dans une approche basée sur les microservices, chaque microservice détient son modèle et ses données, ce qui le rend autonome du point de vue du développement et du déploiement. Mais même si vous avez une application plus classique qui est composée de plusieurs services (par exemple, SOA), également avoir plusieurs conteneurs ou services comprenant une application unique qui doivent être déployés en tant qu’un système distribué. Ces types de systèmes sont complexes à monter en charge et gérer ; Par conséquent, vous devez absolument orchestrateur si vous souhaitez disposer d’une application multicontainer opérationnelle et évolutive.

Figure 4-6 illustre le déploiement dans un cluster d’une application composée de plusieurs microservices (conteneurs).

![](./media/image6.png)

Figure 4-6 : un cluster de conteneurs

Ceci ressemble à une approche logique. Mais la façon dont vous gérez l’équilibrage de charge, de routage et d’orchestration de ces applications composées ?

L’interface de ligne de commande Docker (CLI) répond aux besoins de la gestion d’un conteneur sur un ordinateur hôte, mais il n’était pas lorsqu’il s’agit de la gestion de plusieurs conteneurs sont déployés sur plusieurs ordinateurs hôtes pour les applications distribuées plus complexes. Dans la plupart des cas, vous avez besoin d’une plateforme de gestion qui sera automatiquement démarrer conteneurs, les suspendre, ou leur arrêt si nécessaire et dans l’idéal, également contrôler comment accéder aux ressources, telles que le stockage de données et de réseau.

Pour aller au-delà de la gestion de conteneurs individuels ou d’applications composées très simples et passer à des applications d’entreprise plus grandes avec des microservices, vous devez faire appel à l’orchestration et au clustering des plateformes.

À partir d’un point de vue architecture et le développement, si vous êtes enterprise volumineux, de construction, en fonction des microservices, applications, il est important de comprendre les plateformes et les produits qui prennent en charge des scénarios avancés suivants :

-   **Clusters et orchestrators** lorsque vous devez mettre à l’échelle-applications sur plusieurs hôtes de Docker, comme avec une grande application microservices, il est essentiel de pouvoir gérer tous les ordinateurs hôtes en tant qu’un seul cluster par en faisant abstraction de la complexité de la plateforme sous-jacente. C’est ce que les clusters de conteneurs et les orchestrateurs permettent. Exemples d’orchestrators sont Docker Swarm mésosphère DC/OS, Kubernetes (les trois premières disponibles via le Service de conteneur Azure) et Azure Service Fabric.

-   **Planificateurs** *planification* signifie la capacité d’un administrateur pour lancer des conteneurs dans un cluster afin qu’elles fournissent également une interface utilisateur. Un planificateur de cluster a plusieurs responsabilités : à utiliser efficacement les ressources du cluster, pour définir les contraintes fournis par l’utilisateur, aux conteneurs efficacement d’équilibrer la charge entre les nœuds ou des ordinateurs hôtes et être robustes face à des erreurs tout en offrant une haute disponibilité.

Les concepts de cluster et de planificateur sont étroitement liés : les produits fournis par les différents fournisseurs offrent souvent les deux ensembles de fonctionnalités. Tableau 4-1 répertorie la plate-forme plus importante et les choix d’un logiciel pour les clusters et des planificateurs. Ces clusters sont généralement proposées dans des clouds publics comme Azure.

Tableau 4-1 : les plates-formes de logiciel de clustering de conteneur, d’orchestration et de planification

| Plateforme | Description |
|---|---|
| Docker Swarm<br/> ![http://rancher.com/wp-content/themes/rancher-2016/assets/images/swarm.png?v=2016-07-10-am](./media/image7.png) | Docker essaim vous donne la possibilité de mettre en cluster et planifier des conteneurs Docker. Avec Swarm, vous pouvez changer un pool d’hôtes Docker en un seul hôte Docker virtuel. Les clients peuvent effectuer des demandes de API au essaim de la même façon que pour les ordinateurs hôtes, ce qui signifie que qu’essaim facilite pour les applications à l’échelle sur plusieurs hôtes. <br /><br /> Docker Swarm est un produit de la société Docker. <br /><br /> Docker v1.12 ou ultérieur peut exécuter le mode Swarm natif et intégré. |
| Mesosphere DC/OS<br/>![https://mesosphere.com/wp-content/uploads/2016/04/logo-horizontal-styled.png](./media/image8.png) |  Mesosphere Enterprise DC/OS (basé sur Apache Mesos) est une plateforme prête pour la production permettant d’exécuter des conteneurs et des applications distribuées. <br /><br /> DC/OS fonctionne en rendant abstraite une collection des ressources disponibles dans le cluster et en rendant ces ressources disponibles pour les composants créés sur celle-ci. Marathon est généralement utilisé comme planificateur intégré à DC/OS. |
| Google Kubernetes<br />![https://pbs.twimg.com/media/Bt\_pEfqCAAAiVyz.png](./media/image9.png) | Kubernetes est un produit open source qui offre des fonctionnalités allant de l’infrastructure de cluster et la planification de conteneurs à des fonctionnalités d’orchestration. Avec lui, vous pouvez automatiser les opérations de conteneurs d’applications, de mise à l’échelle et de déploiement sur tous les clusters d’ordinateurs hôtes. <br /><br /> Kubernetes fournit une infrastructure orientée conteneur, qui regroupe des conteneurs d’application dans des unités logiques pour en faciliter la gestion et la découverte. |
| Azure Service Fabric<br />![https://azure.microsoft.com/svghandler/service-fabric?width=600&height=315](./media/image10.png) | [Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-overview) est une plateforme de microservices de Microsoft pour la création d’applications. Il s’agit d’un [orchestrateur](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-resource-manager-introduction) de services, qui crée des clusters de machines. Par défaut, Service Fabric déploie et active des services en tant que processus, mais l’infrastructure de Service peut déployer des services dans les images de conteneur Docker. Plus important, vous pouvez combiner des services dans des processus avec les services dans des conteneurs dans la même application. <br /><br /> À compter de mai 2017, la fonctionnalité de l’infrastructure de Service qui prend en charge le déploiement des services en tant que conteneurs Docker est dans un état d’aperçu. <br /><br /> Vous pouvez développer des services de l’infrastructure de Service de nombreuses façons, à l’aide de la [Service Fabric, modèles de programmation](https://docs.microsoft.com/azure/service-fabric/service-fabric-choose-framework) au déploiement [invité exécutables](https://docs.microsoft.com/azure/service-fabric/service-fabric-deploy-existing-app) , ainsi que des conteneurs. Service Fabric prend en charge les modèles d’application normative comme [services avec état](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-introduction) et [Reliable Actors](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-actors-introduction).

## <a name="using-container-based-orchestrators-in-azure"></a>À l’aide basée sur le conteneur d’orchestrators dans Azure

Plusieurs fournisseurs de cloud computing proposent une prise en charge des conteneurs Docker ainsi que les clusters de Docker et prise en charge de l’orchestration, y compris Azure, Amazon EC2 conteneur de Service et le moteur de conteneur de Google. Azure fournit Docker à la prise en charge de cluster et orchestrator via le Service de conteneur Azure, comme expliqué dans la section suivante.

Un autre choix est d’utiliser Azure Service Fabric, qui prend également en charge Docker basé sur les conteneurs Linux et Windows. L’infrastructure de service s’exécute sur Azure ou de n’importe quel autre cloud, ainsi que [local](https://docs.microsoft.com/azure/service-fabric/service-fabric-deploy-anywhere).

## <a name="using-azure-container-service"></a>Utilisation d’Azure Container Service

Un cluster Docker met en pool plusieurs hôtes Docker et les expose sous la forme d’un hôte Docker virtuel unique : vous pouvez ainsi déployer plusieurs conteneurs dans le cluster. Le cluster gère tous les éléments nécessaires gestion complexes telles que l’évolutivité et de contrôle d’intégrité. Figure 4-7 représente comment un cluster de Docker pour les applications composées est mappé au Service de conteneur.

Service de conteneur permet de simplifier la création, la configuration et la gestion d’un cluster d’ordinateurs virtuels qui sont préconfigurés pour exécuter des applications en conteneur. À l’aide d’une configuration optimisée des outils de planification et d’orchestration open source populaires, Service de conteneur vous donne la possibilité d’utiliser vos compétences ou de dessiner sur un corps important et croissant d’expertise de communauté pour déployer et gérer basé sur le conteneur applications dans Azure.

Service de conteneur optimise la configuration des outils open source de la gestion de clusters Docker populaires et les technologies spécifiquement pour Azure. Vous obtenez une solution ouverte qui offre la portabilité à la fois pour vos conteneurs et pour la configuration de votre application. Vous sélectionnez la taille, le nombre d’hôtes et les outils de l’orchestrateur, et Container Service gère tout le reste.

Service de conteneur utilise les images Docker pour vous assurer que vos conteneurs d’applications sont entièrement portables. Il prend en charge de votre choix des plateformes open source orchestration comme contrôleur de domaine/système d’exploitation, Kubernetes et Docker Swarm pour vous assurer que ces applications peuvent s’adapter à des milliers, voire même des dizaines de milliers de conteneurs.

Avec le Service de conteneur Azure, vous pouvez tirer parti des fonctionnalités de niveau entreprise de Azure tout en conservant la portabilité des applications, y compris au niveau des couches d’orchestration.

![](./media/image11.png)

Figure 4-7 : Clustering choix dans le conteneur de Service Azure

Comme indiqué dans la Figure 4-8, le Service de conteneur est simplement l’infrastructure fournie par Azure pour déployer le contrôleur de domaine/système d’exploitation, Kubernetes ou Docker Swarm, mais il n’implémente pas de n’importe quel orchestrator supplémentaire. Par conséquent, le Service de conteneur n'est pas un orchestrator, en tant que tel ; Il est uniquement une infrastructure qui tire parti d’orchestrators d’open source existants pour les conteneurs.

![](./media/image12.png)

Orchestrators figure 4-8 : dans le Service de conteneur

À partir d’un point de vue de l’utilisation, de Service de conteneur vise à fournir un environnement d’hébergement de conteneur à l’aide de technologies et outils open source populaires. Pour cela, il expose les points de terminaison d’API standard pour l’orchestrateur que vous avez choisi. À l’aide de ces points de terminaison, vous pouvez utiliser un logiciel qui peut communiquer avec ces points de terminaison. Par exemple, dans le cas le point de terminaison Docker Swarm, vous pouvez choisir d’utiliser l’interface CLI de Docker. Pour DC/OS, vous pouvez choisir d’utiliser l’interface de ligne de commande de DC/OS.

### <a name="getting-started-with-container-service"></a>Prise en main de Service de conteneur

Pour commencer à utiliser le Service de conteneur, vous déployez un cluster du Service de conteneur à partir du portail Azure à l’aide d’un modèle Azure Resource Manager ou le [CLI](https://docs.microsoft.com/cli/azure/install-azure-cli). Les modèles disponibles sont [Docker Swarm](https://github.com/Azure/azure-quickstart-templates/tree/master/101-acs-swarm), [Kubernetes](https://github.com/Azure/azure-quickstart-templates/tree/master/101-acs-kubernetes) et [DC/OS](https://github.com/Azure/azure-quickstart-templates/tree/master/101-acs-dcos). Vous pouvez modifier les modèles de démarrage rapide pour inclure la configuration d’Azure supplémentaire ou avancée.

**Plus d’informations** pour en savoir plus sur le déploiement d’un cluster du Service de conteneur, sur le site Web Azure, consultez [déployer un cluster du Service de conteneur Azure](https://docs.microsoft.com/azure/container-service/dcos-swarm/container-service-deployment).

Aucun coût n’est facturé pour les logiciels installés par défaut dans le cadre d’ACS. Toutes les options par défaut sont implémentées avec des logiciels open source.

Service de conteneur est actuellement disponible pour un Standard, D, DS, G et GS série Linux machines virtuelles dans Azure. Vous payez uniquement pour les instances de calcul que vous choisissez, ainsi que les autres ressources infrastructure sous-jacente consommés, telles que la mise en réseau et de stockage. Frais ne sont incrémentielles pour le Service de conteneur lui-même.

### <a name="additional-resources"></a>Ressources supplémentaires

Voici les emplacements où vous trouverez des informations supplémentaires :

-   Introduction au conteneur Docker solutions avec le conteneur de Service d’hébergement :  
    https://docs.microsoft.com/azure/container-service/kubernetes/container-service-intro-kubernetes>

-   Vue d’ensemble de docker essaim :  
    <https://docs.docker.com/swarm/overview/>

-   Swarm vue d’ensemble du mode :  
    <https://docs.docker.com/engine/swarm/>

-   Vue d’ensemble du contrôleur de domaine/système d’exploitation mésosphère :    
    <https://docs.mesosphere.com/1.7/overview/>

-   Kubernetes (le site officiel) :  
    <https://kubernetes.io/>

## <a name="using-service-fabric"></a>À l’aide de l’infrastructure de Service

L’infrastructure de service a été créée à partir de passage de Microsoft proposant des produits de « boîte », qui ont été généralement monolithiques dans le style, la fourniture de services. L’expérience de création et d’exploitation de grands services à grande échelle, telles que la base de données SQL Azure, base de données de Document Azure, Azure Service Bus ou principal du Cortana, la forme Service Fabric. La plateforme a évolué au fil du temps car de plus en plus de services l’ont adoptée. Surtout, Service Fabric devait s’exécuter non seulement dans Azure, mais également dans des déploiements de Windows Server autonomes.

Le Service Fabric vise à résoudre les problèmes difficiles de créer, générer et exécuter un service utilisant efficacement des ressources d’infrastructure afin que les équipes de résoudre les problèmes d’entreprise à l’aide d’une approche de microservices.

Service Fabric fournit deux grands composants principaux pour vous aider à créer des applications qui utilisent une approche par microservices :

-   Une plateforme qui fournit des services système pour déployer, mettre à l’échelle, mettre à niveau, détecter et redémarrer les services ayant connu une défaillance, découvrir l’emplacement des services, gérer les états et surveiller l’intégrité. Ces services système fournissent en vigueur la plupart des caractéristiques de microservices décrit précédemment.

-   Des API de programmation, ou frameworks, pour vous aider à créer des applications en tant que microservices : [des acteurs fiables et des services fiables](https://docs.microsoft.com/azure/service-fabric/service-fabric-choose-framework). Bien sûr, vous pouvez choisir n’importe quel code pour créer votre microservice, mais ces API remplissent très bien leur rôle et s’intègrent à la plateforme de façon plus étroite. De cette manière, vous pouvez obtenir des informations sur l’intégrité et les diagnostics, ou vous pouvez bénéficier d’une gestion fiable des états.

Service Fabric est agnostique quant à la façon dont vous créez votre service, et vous pouvez utiliser n’importe quelle technologie. Il fournit cependant des API de programmation intégrées qui facilitent la création de microservices.

Figure 4-9 illustre comment vous pouvez créer et exécuter des microservices dans l’infrastructure de Service en tant que processus simples ou en tant que conteneurs Docker. Il est également possible de combiner des microservices basés sur des conteneurs avec des microservices basés sur des processus au sein du même cluster Service Fabric.

![](./media/image13.png)

Figure 4-9 : déploiement de microservices en tant que processus ou en tant que conteneurs dans Azure Service Fabric

Les clusters service Fabric basés sur les hôtes Linux et Windows peuvent exécuter les conteneurs Docker Linux et Windows.

**Plus d’informations** pour des informations récentes sur la prise en charge des conteneurs dans l’infrastructure de Service, sur le site Web Azure, consultez [Service Fabric et conteneurs](https://docs.microsoft.com/azure/service-fabric/service-fabric-containers-overview).

Service Fabric est un bon exemple d’une plateforme avec lequel vous pouvez définir une autre architecture logique (entreprise microservices ou limitées de contextes) que l’implémentation physique. Par exemple, si vous implémentez [Reliable Services avec état](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-introduction) dans [Azure Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-overview), qui ont été introduit dans la section suivante, «[sans état et avec état microservices](#stateless-versus-stateful-microservices), « vous avez un concept de microservice métier avec plusieurs services physiques.

Comme indiqué dans la Figure 4-10, en pensant à partir d’un point de vue logique/business microservice, lors de l’implémentation d’un Service avec état fiable Service Fabric, vous généralement devrez implémenter deux niveaux de services. Le premier est le service de fiable avec état principal, qui gère plusieurs partitions. Le second est le service frontal, ou service de passerelle, en charge du routage et de l’agrégation des données entre plusieurs partitions ou instances de service avec état. Ce service de passerelle gère également la communication de côté client avec des boucles de réessayer l’accès au service principal utilisé conjointement avec le Service Fabric [proxy inverse](https://docs.microsoft.com/azure/service-fabric/service-fabric-reverseproxy).

![](./media/image14.png)

Microservice d’entreprise figure 4-10 : avec plusieurs services avec ou sans état dans le Service Fabric

Dans tous les cas, quand vous utilisez des services fiables avec état Service Fabric, vous avez également un microservice (contexte délimité) logique ou métier qui est généralement constitué de plusieurs services physiques. Chacun d'entre eux, le service de passerelle et service de Partition peut être implémentée en tant que services de l’API Web ASP.NET, comme indiqué dans la Figure 4-10.

Dans Service Fabric, vous pouvez regrouper et déployer des groupes de services sous la forme d’une [application Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-model), qui est l’unité d’empaquetage et de déploiement pour l’orchestrateur ou le cluster. Par conséquent, l’Application de l’infrastructure de Service peut être mappée à cette commerciales autonomes et la limite de microservice logique ou le contexte délimité, également.

### <a name="service-fabric-and-containers"></a>Service Fabric et les conteneurs

En ce qui concerne les conteneurs dans l’infrastructure de Service, vous pouvez également déployer services dans les images de conteneur au sein d’un cluster Service Fabric. Figure 4-11 illustre que la plupart du temps, il y aura qu’un seul conteneur par le service.

![](./media/image15.png)

Microservice d’entreprise figure 4-11 : avec plusieurs services (conteneurs) dans le Service Fabric

Toutefois, les conteneurs dite « annexe » (deux conteneurs qui doivent être déployées ensemble dans le cadre d’un service logique) sont également possibles dans le Service Fabric. Le point essentiel est qu’un microservice métier est la limite logique autour de plusieurs éléments cohésifs. Dans de nombreux cas, il peut être un service unique avec un seul modèle de données, mais dans d’autres cas, vous pouvez avoir plusieurs services physiques, ainsi.

À compter de cette écriture (avril 2017), dans l’infrastructure de Service vous ne pouvez pas déployer SF fiable avec état Services sur les conteneurs, vous pouvez déployer uniquement les conteneurs d’invité, les services sans état ou les services d’acteur dans des conteneurs. Notez toutefois que vous pouvez combiner des services dans les processus et services dans des conteneurs dans la même application de Service Fabric, comme indiqué dans la Figure 4-12.

![](./media/image16.png)

Figure 4-12 : entreprise microservice est mappée à une application de Service Fabric des conteneurs et des services avec état

Prise en charge est également différente selon que vous utilisez des conteneurs Docker sur les conteneurs Windows ou Linux. Prise en charge des conteneurs dans le Service Fabric développons dans les prochaines versions. Pour les dernières infos sur la prise en charge de conteneur dans le Service Fabric, sur le site Web Azure, consultez [Service Fabric et conteneurs](https://docs.microsoft.com/azure/service-fabric/service-fabric-containers-overview).

## <a name="stateless-versus-stateful-microservices"></a>Microservices sans état et avec état

Comme mentionné précédemment, chaque microservice (contexte délimité logique) doit avoir son modèle de domaine (données et logique). Dans le cas de microservices sans état, les bases de données sera externes, en utilisant les options relationnelles telles que SQL Server ou les options de NoSQL comme MongoDB ou Azure DocumentDB.

Mais les services eux-mêmes peuvent également être avec état, ce qui signifie que les données se trouvent dans le microservice. Ces données existe peut-être pas seulement sur le même serveur, mais dans le processus de microservice, dans la mémoire et conservées sur des lecteurs et répliquées vers d’autres nœuds. Figure 4-13 illustre les différentes approches.

![](./media/image17.png)

Figure 4-13 : sans état et avec état microservices

Une approche sans état est parfaitement valide et est plus facile à implémenter que microservices avec état, car l’approche est similaire aux modèles traditionnels et bien connus. Les microservices sans état imposent cependant de la latence entre les processus et les sources de données. Ils impliquent également le déplacement de plus d’éléments quand vous essayez d’améliorer les performances avec des caches et des files d’attente supplémentaires. Le résultat est que vous pouvez vous retrouver avec des architectures complexes qui ont trop de niveaux.

En revanche, [microservices avec état](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-introduction#when-to-use-reliable-services-apis) peut excel dans les scénarios avancés, car il n’existe pas de latence entre la logique de domaine et les données. Le traitement des données lourd, jeu back end, bases de données comme un service et d’autres scénarios de faible latence tous tirer parti des services avec état, qui fournissent l’état local pour un accès plus rapide.

Les services sans état et avec état sont complémentaires. Par exemple, un service avec état peut être fractionné en plusieurs partitions. Pour accéder à ces partitions, vous pouvez avoir besoin d’un service sans état agissant comme un service de passerelle, qui sait comment atteindre chaque partition en fonction de clés de partition.

Les services avec état présentent des inconvénients. Ils imposent un niveau de complexité qui leur permet de montée en puissance parallèle. Les fonctionnalités qui seraient habituellement implémentées par des systèmes de base de données externes doivent être fournies pour des tâches comme la réplication des données entre des microservices avec état et le partitionnement des données. Toutefois, c’est une des zones où un orchestrator que [Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-platform-architecture) avec son [des services fiables avec état](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-introduction#when-to-use-reliable-services-apis) peut aider au plus, en ce qui simplifie le développement et le cycle de vie de l’état à l’aide de microservices les [API des Services fiables](https://docs.microsoft.com/azure/service-fabric/service-fabric-work-with-reliable-collections) et [Reliable Actors](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-actors-introduction).

Les autres frameworks de microservices qui permettent les services avec état, qui prennent en charge le modèle d’acteur et qui améliorent la tolérance de panne et la latence entre la logique métier et les données sont Microsoft [Orléans](https://github.com/dotnet/orleans) de Microsoft Research et [Akka.NET](https://getakka.net/). Les deux frameworks améliorent actuellement leur prise en charge de Docker.

Notez que les conteneurs Docker sont eux-mêmes sans état. Si vous voulez implémenter un service avec état, vous avez besoin d’un des frameworks normatifs et de plus haut niveau supplémentaires précédemment indiqués. Toutefois, à ce jour, les services avec état dans l’infrastructure de Service ne sont pas pris en charge en tant que conteneurs, uniquement en tant que microservices brut. Prise en charge des services fiables dans les conteneurs sera disponible dans les prochaines versions de Service Fabric.


>[!div class="step-by-step"]
[Précédente] (soa-applications.md) [suivant] (docker-applications-développement-environment.md)
