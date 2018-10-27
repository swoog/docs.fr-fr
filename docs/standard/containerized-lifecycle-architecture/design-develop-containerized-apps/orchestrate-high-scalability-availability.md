---
title: Orchestration des microservices et des applications à une grande évolutivité et disponibilité
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/19/2017
ms.openlocfilehash: 993f1d18637f39b6df4d876db8a0fe86e34391e3
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50192718"
---
# <a name="orchestrating-microservices-and-multicontainer-applications-for-high-scalability-and-availability"></a>Orchestration des microservices et des applications à une grande évolutivité et disponibilité

L’utilisation d’orchestrateurs pour les applications prêtes pour la production est essentielle si votre application est basée sur des microservices ou si elle est simplement répartie entre plusieurs conteneurs. Comme expliqué précédemment, dans une approche basée sur les microservices, chaque microservice détient son modèle et ses données, ce qui le rend autonome du point de vue du développement et du déploiement. Mais même si vous avez une application plus classique est composée de plusieurs services (comme SOA), également avoir plusieurs conteneurs ou services constituant une même application métier devant être déployé comme un système distribué. Ces types de systèmes sont complexes à monter en charge et à gérer ; Par conséquent, vous avez absolument besoin un orchestrateur si vous souhaitez disposer d’une application multiconteneur prête pour la production et évolutif.

Figure 4-6 illustre un déploiement dans un cluster d’une application composée de plusieurs microservices (conteneurs).

![](./media/image6.png)

Figure 4-6 : un cluster de conteneurs

Ceci ressemble à une approche logique. Mais comment gérez-vous l’équilibrage de charge, le routage et l’orchestration de ces applications composées ?

L’interface de ligne de commande (CLI) Docker répond aux besoins de la gestion d’un conteneur sur un ordinateur hôte, mais il s’avère insuffisant lorsqu’il s’agit de la gestion de plusieurs conteneurs déployés sur plusieurs ordinateurs hôtes pour les applications distribuées plus complexes. Dans la plupart des cas, vous avez besoin d’une plateforme de gestion qui sera automatiquement démarrer les conteneurs, les suspendre, ou les arrêter si nécessaire et idéalement, contrôler comment ils accèdent aux ressources telles que le stockage réseau et les données.

Pour aller au-delà de la gestion de conteneurs individuels ou d’applications composées très simples et passer à des applications d’entreprise plus grandes avec des microservices, vous devez faire appel à l’orchestration et au clustering des plateformes.

À partir d’un point de vue architecture et le développement, si vous êtes bâtiment, grands, basé sur des microservices, applications, il est important de comprendre les plateformes et les produits qui prennent en charge des scénarios avancés suivants :

-   **Clusters et orchestrateurs** lorsque vous devez mettre à l’échelle-applications sur plusieurs hôtes Docker, comme avec une grande application basée sur des microservices, il est essentiel de pouvoir gérer tous ces hôtes comme un seul cluster par en faisant abstraction de la complexité de la plateforme sous-jacente. C’est ce que les clusters de conteneurs et les orchestrateurs permettent. Exemples d’orchestrators sont Docker Swarm, Mesosphere DC/OS, Kubernetes (les trois premiers disponibles via Azure Container Service) et Azure Service Fabric.

-   **Planificateurs** *planification* signifie la capacité d’un administrateur pour lancer des conteneurs dans un cluster afin qu’elles fournissent également une interface utilisateur. Un planificateur de cluster a plusieurs responsabilités : utiliser efficacement les ressources du cluster, pour définir les contraintes fournies par l’utilisateur, à efficacement des conteneurs d’équilibrer la charge entre les nœuds ou les hôtes et être robustes face aux erreurs, tout en offrant de haut disponibilité.

Les concepts de cluster et de planificateur sont étroitement liés : les produits fournis par les différents fournisseurs offrent souvent les deux ensembles de fonctionnalités. Tableau 4-1 répertorie les plus importants pour les plateformes et les choix d’un logiciel pour les clusters et des planificateurs. Ces clusters sont généralement proposés dans des clouds publics comme Azure.

Tableau 4-1 : les plateformes de logiciel de clustering de conteneur, d’orchestration et de planification

| Plateforme | Description |
|---|---|
| Docker Swarm<br/> ![Logo de docker Swarm](./media/image7.png) | Docker Swarm vous donne la possibilité de mettre en cluster et de planifier les conteneurs Docker. Avec Swarm, vous pouvez changer un pool d’hôtes Docker en un seul hôte Docker virtuel. Les clients peuvent envoyer des requêtes d’API à Swarm de la même façon qu’ils font à des hôtes, ce qui signifie que Swarm facilite pour les applications à l’échelle sur plusieurs hôtes. <br /><br /> Docker Swarm est un produit de la société Docker. <br /><br /> Docker v1.12 ou ultérieur peut exécuter le mode Swarm natif et intégré. |
| Mesosphere DC/OS<br/>![Logo de mesosphere DC/OS](./media/image8.png) |  Mesosphere Enterprise DC/OS (basé sur Apache Mesos) est une plateforme prête pour la production permettant d’exécuter des conteneurs et des applications distribuées. <br /><br /> DC/OS fonctionne en rendant abstraite une collection des ressources disponibles dans le cluster et en rendant ces ressources disponibles pour les composants créés sur celle-ci. Marathon est généralement utilisé comme planificateur intégré à DC/OS. |
| Google Kubernetes<br />![Logo de Google Kubernetes](./media/image9.png) | Kubernetes est un produit open source qui offre des fonctionnalités allant de l’infrastructure de cluster et la planification de conteneurs à des fonctionnalités d’orchestration. Avec elle, vous pouvez automatiser les opérations de conteneurs d’applications, de mise à l’échelle et de déploiement sur des clusters d’hôtes. <br /><br /> Kubernetes fournit une infrastructure orientée conteneur, qui regroupe des conteneurs d’application dans des unités logiques pour en faciliter la gestion et la découverte. |
| Azure Service Fabric<br />![Logo Service Fabric Azure](./media/image10.png) | [Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-overview) est une plateforme de microservices de Microsoft pour la création d’applications. Il s’agit d’un [orchestrateur](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-resource-manager-introduction) de services, qui crée des clusters de machines. Par défaut, Service Fabric déploie et Active les services en tant que processus, mais Service Fabric peut déployer des services dans les images de conteneur Docker. Plus important encore, vous pouvez combiner des services dans des processus avec les services dans des conteneurs dans la même application. <br /><br /> Depuis mai 2017, la fonctionnalité de Service Fabric qui prend en charge le déploiement des services en tant que conteneurs Docker est en état d’aperçu. <br /><br /> Vous pouvez développer des services Service Fabric de nombreuses façons, à l’aide de la [modèles de programmation Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-choose-framework) au déploiement [exécutables invités](https://docs.microsoft.com/azure/service-fabric/service-fabric-deploy-existing-app) , ainsi que des conteneurs. Service Fabric prend en charge les modèles d’application normative comme [services avec état](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-introduction) et [Reliable Actors](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-actors-introduction).

## <a name="using-container-based-orchestrators-in-azure"></a>À l’aide d’orchestrateurs basé sur des conteneurs dans Azure

Plusieurs fournisseurs de cloud offrent la prise en charge des conteneurs Docker ainsi que des clusters Docker et prise en charge de l’orchestration, y compris Azure, Amazon EC2 Container Service et Google Container Engine. Azure offre à Docker prise en charge de cluster et l’orchestrateur via Azure Container Service, comme expliqué dans la section suivante.

Un autre choix consiste à utiliser Azure Service Fabric, qui prend également en charge Docker basé sur des conteneurs Linux et Windows. Service Fabric s’exécute sur Azure ou tout autre nuage, ainsi que [local](https://docs.microsoft.com/azure/service-fabric/service-fabric-deploy-anywhere).

## <a name="using-azure-container-service"></a>Utilisation d’Azure Container Service

Un cluster Docker met en pool plusieurs hôtes Docker et les expose sous la forme d’un hôte Docker virtuel unique : vous pouvez ainsi déployer plusieurs conteneurs dans le cluster. Le cluster gère tous les éléments de gestion complexes telles que l’évolutivité et d’intégrité. Figure 4-7 représente comment un cluster Docker pour des applications composées est mappé au Service de conteneur.

Container Service fournit un moyen de simplifier la création, la configuration et la gestion d’un cluster de machines virtuelles préconfigurées pour exécuter des applications en conteneur. À l’aide d’une configuration optimisée d’outils de planification et d’orchestration open source populaires, Container Service vous donne la possibilité d’utiliser vos compétences existantes ou de dessiner sur un corps importante et croissant de la Communauté d’experts pour déployer et gérer en conteneur applications dans Azure.

Container Service optimise la configuration d’outils open source clusters de Docker et de technologies populaires spécifiquement pour Azure. Vous obtenez une solution ouverte qui offre la portabilité à la fois pour vos conteneurs et pour la configuration de votre application. Vous sélectionnez la taille, le nombre d’hôtes et les outils de l’orchestrateur, et Container Service gère tout le reste.

Container Service utilise des images Docker pour vous assurer que vos conteneurs d’applications sont entièrement portables. Il prend en charge votre choix de plateformes d’orchestration open source comme DC/OS, Kubernetes et Docker Swarm pour vous assurer que ces applications peuvent s’adapter à des milliers ou même des dizaines de milliers de conteneurs.

Avec Azure Container Service, vous pouvez tirer parti des fonctionnalités de niveau entreprise d’Azure tout en conservant la portabilité des applications, notamment au niveau des couches d’orchestration.

![](./media/image11.png)

Figure 4-7 : choix de Clustering dans Azure Container Service

Comme indiqué dans la Figure 4-8, Container Service est simplement l’infrastructure fournie par Azure pour déployer DC/OS, Kubernetes ou Docker Swarm, mais il n’implémente pas de n’importe quel orchestrateur supplémentaire. Par conséquent, Service de conteneur n’est pas un orchestrateur, par conséquent ; Il est seulement une infrastructure qui tire parti d’existants orchestrateurs open source pour les conteneurs.

![](./media/image12.png)

Figure 4-8 : les Orchestrateurs dans Container Service

À partir d’un point de vue de l’utilisation du Service de conteneur vise à fournir un environnement d’hébergement de conteneur à l’aide des technologies et des outils open source populaires. Pour cela, il expose les points de terminaison d’API standard pour l’orchestrateur que vous avez choisi. À l’aide de ces points de terminaison, vous pouvez utiliser n’importe quel logiciel capable de communiquer ces points de terminaison. Par exemple, dans le cas le point de terminaison Docker Swarm, vous pouvez choisir d’utiliser l’interface CLI Docker. Pour DC/OS, vous pouvez choisir d’utiliser l’interface de ligne de commande de DC/OS.

### <a name="getting-started-with-container-service"></a>Mise en route avec Container Service

Pour commencer à l’aide du Service de conteneur, vous déployez un cluster Container Service à partir du portail Azure à l’aide d’un modèle Azure Resource Manager ou le [CLI](https://docs.microsoft.com/cli/azure/install-azure-cli). Les modèles disponibles sont [Docker Swarm](https://github.com/Azure/azure-quickstart-templates/tree/master/101-acs-swarm), [Kubernetes](https://github.com/Azure/azure-quickstart-templates/tree/master/101-acs-kubernetes) et [DC/OS](https://github.com/Azure/azure-quickstart-templates/tree/master/101-acs-dcos). Vous pouvez modifier les modèles de démarrage rapide pour inclure la configuration Azure supplémentaire ou avancée.

**Plus d’informations** pour en savoir plus sur le déploiement d’un cluster Container Service, sur le site Web Azure, consultez [déployer un cluster Azure Container Service](https://docs.microsoft.com/azure/container-service/dcos-swarm/container-service-deployment).

Aucun coût n’est facturé pour les logiciels installés par défaut dans le cadre d’ACS. Toutes les options par défaut sont implémentées avec des logiciels open source.

Container Service est actuellement disponible pour Standard A, D, DS, G et machines virtuelles Linux de série GS dans Azure. Vous êtes facturé uniquement pour les instances de calcul que vous choisissez, ainsi que les autres ressources d’infrastructure sous-jacentes consommées, telles que la mise en réseau et de stockage. Aucuns frais ne sont incrémentielles pour Service de conteneur lui-même.

### <a name="additional-resources"></a>Ressources supplémentaires

Voici les emplacements où vous pouvez trouver des informations supplémentaires :

-   Introduction aux solutions avec Container Service d’hébergement de conteneur Docker :  
    https://docs.microsoft.com/azure/container-service/kubernetes/container-service-intro-kubernetes>

-   Vue d’ensemble de docker Swarm :  
    <https://docs.docker.com/swarm/overview/>

-   Vue d’ensemble du mode swarm :  
    <https://docs.docker.com/engine/swarm/>

-   Vue d’ensemble de mesosphere DC/OS :    
    <https://docs.mesosphere.com/1.7/overview/>

-   Kubernetes (le site officiel) :  
    <https://kubernetes.io/>

## <a name="using-service-fabric"></a>À l’aide de Service Fabric

Service Fabric a été créée à partir de la transition de Microsoft à partir de la distribution de produits « boîte », généralement de style monolithique, à la prestation de services. L’expérience de création et l’exploitation des services à grande échelle, telles que la base de données SQL Azure, Azure Document DB, Azure Service Bus ou Backend de Cortana, en forme de Service Fabric. La plateforme a évolué au fil du temps car de plus en plus de services l’ont adoptée. Surtout, Service Fabric devait s’exécuter non seulement dans Azure, mais également dans des déploiements de Windows Server autonomes.

L’objectif de Service Fabric consiste à résoudre les problèmes difficiles de génération et un service en cours d’exécution et l’utilisation des ressources d’infrastructure efficacement afin que les équipes puissent résoudre les problèmes d’entreprise à l’aide d’une approche de microservices.

Service Fabric fournit deux grands composants principaux pour vous aider à créer des applications qui utilisent une approche par microservices :

-   Une plateforme qui fournit des services système pour déployer, mettre à l’échelle, mettre à niveau, détecter et redémarrer les services ayant connu une défaillance, découvrir l’emplacement des services, gérer les états et surveiller l’intégrité. Ces services système fournissent en effet de nombreuses caractéristiques des microservices décrites précédemment.

-   Des API de programmation, ou frameworks, pour vous aider à créer des applications en tant que microservices : [des acteurs fiables et des services fiables](https://docs.microsoft.com/azure/service-fabric/service-fabric-choose-framework). Bien sûr, vous pouvez choisir n’importe quel code pour créer votre microservice, mais ces API remplissent très bien leur rôle et s’intègrent à la plateforme de façon plus étroite. De cette manière, vous pouvez obtenir des informations sur l’intégrité et les diagnostics, ou vous pouvez bénéficier d’une gestion fiable des états.

Service Fabric est agnostique quant à la façon dont vous créez votre service, et vous pouvez utiliser n’importe quelle technologie. Il fournit cependant des API de programmation intégrées qui facilitent la création de microservices.

Figure 4-9 illustre comment vous pouvez créer et exécuter des microservices dans Service Fabric en tant que processus simples ou en tant que conteneurs Docker. Il est également possible de combiner des microservices basés sur des conteneurs avec des microservices basés sur des processus au sein du même cluster Service Fabric.

![](./media/image13.png)

Figure 4-9 : déploiement de microservices en tant que processus ou en tant que conteneurs dans Azure Service Fabric

Les clusters service Fabric basés sur des hôtes Linux et Windows peuvent exécuter les conteneurs Docker Linux et Windows.

**Plus d’informations** pour des informations récentes sur la prise en charge des conteneurs dans Service Fabric, sur le site Web Azure, consultez [Service Fabric et conteneurs](https://docs.microsoft.com/azure/service-fabric/service-fabric-containers-overview).

Service Fabric est un bon exemple d’une plateforme avec laquelle vous pouvez définir une architecture logique (microservices métier ou contextes délimités) que l’implémentation physique. Par exemple, si vous implémentez [Reliable Services avec état](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-introduction) dans [Azure Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-overview), qui sont présentés dans la section suivante, «[sans état et les microservices avec état](#stateless-versus-stateful-microservices), « vous avez un concept de microservice métier avec plusieurs services physiques.

Comme indiqué dans la Figure 4-10, en adoptant une perspective de microservice logique/métier, lors de l’implémentation d’un Service avec état fiable Service Fabric, vous doit généralement implémenter deux niveaux de services. La première est le service de fiable avec état back-end, qui gère plusieurs partitions. Le second est le service frontal, ou le service de passerelle, responsable d’agrégation de données et de routage sur plusieurs partitions ou instances de service avec état. Ce service de passerelle gère également la communication côté client avec des boucles de nouvelle tentative l’accès au service principal utilisé conjointement avec le Service Fabric [proxy inverse](https://docs.microsoft.com/azure/service-fabric/service-fabric-reverseproxy).

![](./media/image14.png)

Figure 4-10 : microservice d’entreprise avec plusieurs services avec et sans état dans Service Fabric

Dans tous les cas, quand vous utilisez des services fiables avec état Service Fabric, vous avez également un microservice (contexte délimité) logique ou métier qui est généralement constitué de plusieurs services physiques. Chacun d’eux, service de passerelle et service de Partition peut être implémentée en tant que services API Web ASP.NET, comme illustré à la Figure 4-10.

Dans Service Fabric, vous pouvez regrouper et déployer des groupes de services sous la forme d’une [application Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-application-model), qui est l’unité d’empaquetage et de déploiement pour l’orchestrateur ou le cluster. Par conséquent, l’Application Service Fabric peut être mappée à cette commerciales autonomes et la limite de microservice logique ou le contexte délimité, également.

### <a name="service-fabric-and-containers"></a>Service Fabric et les conteneurs

En ce qui concerne les conteneurs dans Service Fabric, vous pouvez également déployer des services dans les images de conteneur au sein d’un cluster Service Fabric. Figure 4-11 montre que la plupart du temps, il y aura qu’un seul conteneur par service.

![](./media/image15.png)

Figure 4-11 : microservice d’entreprise avec plusieurs services (conteneurs) dans Service Fabric

Toutefois, les conteneurs de ce que l'on appelle « side-car » (deux conteneurs qui doivent être déployées ensemble dans le cadre d’un service logique) sont également possibles dans Service Fabric. Le point essentiel est qu’un microservice métier est la limite logique autour de plusieurs éléments cohésifs. Dans de nombreux cas, il peut être un seul service avec un seul modèle de données, mais dans d’autres cas, vous pouvez avoir plusieurs services physiques, également.

À ce jour (avril 2017), dans Service Fabric vous ne pouvez pas déployer les Services avec état fiable SF sur les conteneurs, vous pouvez déployer uniquement les conteneurs d’invités, les services sans état ou les services d’acteur dans des conteneurs. Notez toutefois que vous pouvez combiner des services dans des processus et services dans des conteneurs dans la même application Service Fabric, comme illustré dans la Figure 4-12.

![](./media/image16.png)

Figure 4-12 : microservice d’entreprise mappé à une application de Service Fabric avec les conteneurs et les services avec état

Prise en charge est également différent selon que vous utilisez des conteneurs Docker sur les conteneurs Windows ou Linux. Prise en charge des conteneurs dans Service Fabric s’étend dans les prochaines versions. Pour les dernières infos sur la prise en charge des conteneurs dans Service Fabric, sur le site Web Azure, consultez [Service Fabric et conteneurs](https://docs.microsoft.com/azure/service-fabric/service-fabric-containers-overview).

## <a name="stateless-versus-stateful-microservices"></a>Microservices sans état et avec état

Comme mentionné précédemment, chaque microservice (contexte délimité logique) doit avoir son modèle de domaine (données et logique). Dans le cas des microservices sans état, les bases de données sera externes, utilisant des options relationnelles comme SQL Server, ou NoSQL comme MongoDB ou Azure DocumentDB.

Mais les services eux-mêmes peuvent également être avec état, ce qui signifie que les données résident dans le microservice. Ces données peuvent exister non seulement sur le même serveur, mais dans le processus de microservice, dans la mémoire et conservées sur des lecteurs et répliquées vers d’autres nœuds. Figure 4-13 illustre les différentes approches.

![](./media/image17.png)

Figure 4-13 : sans état et les microservices avec état

Une approche sans état est parfaitement valide et est plus facile à implémenter que les microservices avec état, car l’approche est similaire aux modèles traditionnels et bien connus. Les microservices sans état imposent cependant de la latence entre les processus et les sources de données. Ils impliquent également le déplacement de plus d’éléments quand vous essayez d’améliorer les performances avec des caches et des files d’attente supplémentaires. Le résultat est que vous pouvez vous retrouver avec des architectures complexes qui ont trop de niveaux.

En revanche, [microservices avec état](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-introduction#when-to-use-reliable-services-apis) peuvent exceller dans les scénarios avancés, car il n’existe pas de latence entre la logique de domaine et les données. Traitement des données lourd, jeux principaux, comme un service et d’autres scénarios à latence faible bénéficient toutes de services avec état, qui fournissent l’état local pour un accès plus rapide des bases de données.

Les services sans état et avec état sont complémentaires. Par exemple, un service avec état peut être fractionné en plusieurs partitions. Pour accéder à ces partitions, vous pouvez avoir besoin d’un service sans état agissant comme un service de passerelle, qui sait comment atteindre chaque partition en fonction de clés de partition.

Les services avec état présentent des inconvénients. Ils imposent un niveau de complexité qui leur permet de faire monter en charge. Les fonctionnalités qui seraient habituellement implémentées par des systèmes de base de données externes doivent être fournies pour des tâches comme la réplication des données entre des microservices avec état et le partitionnement des données. Toutefois, c’est une des zones où un orchestrateur comme [Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-platform-architecture) avec son [reliable services avec état](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-introduction#when-to-use-reliable-services-apis) peut être le plus utile, en simplifiant le développement et le cycle de vie d’avec état à l’aide de microservices le [API Reliable Services](https://docs.microsoft.com/azure/service-fabric/service-fabric-work-with-reliable-collections) et [Reliable Actors](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-actors-introduction).

Les autres frameworks de microservices qui permettent les services avec état, qui prennent en charge le modèle d’acteur et qui améliorent la tolérance de panne et la latence entre la logique métier et les données sont Microsoft [Orléans](https://github.com/dotnet/orleans) de Microsoft Research et [Akka.NET](https://getakka.net/). Les deux frameworks améliorent actuellement leur prise en charge de Docker.

Notez que les conteneurs Docker sont eux-mêmes sans état. Si vous voulez implémenter un service avec état, vous avez besoin d’un des frameworks normatifs et de plus haut niveau supplémentaires précédemment indiqués. Toutefois, à ce jour, les services avec état dans Service Fabric ne sont pas pris en charge en tant que conteneurs, uniquement en tant que microservices brut. Prise en charge des services fiables dans des conteneurs sera disponible dans les prochaines versions de Service Fabric.


>[!div class="step-by-step"]
[Précédent](soa-applications.md)
[Suivant](docker-apps-development-environment.md)
