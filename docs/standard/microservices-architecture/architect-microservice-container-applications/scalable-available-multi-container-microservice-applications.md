---
title: Orchestration des microservices et des applications à plusieurs conteneurs pour une grande scalabilité et une haute disponibilité
description: Architecture de microservices .NET pour les applications .NET en conteneur | Orchestration des microservices et des applications à plusieurs conteneurs pour une grande scalabilité et une haute disponibilité
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/18/2017
ms.openlocfilehash: e8552f79a4196c161ec70d7ea46156215e52db26
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33578883"
---
# <a name="orchestrating-microservices-and-multi-container-applications-for-high-scalability-and-availability"></a>Orchestration des microservices et des applications à plusieurs conteneurs pour une grande scalabilité et une haute disponibilité

L’utilisation d’orchestrateurs pour les applications prêtes pour la production est essentielle si votre application est basée sur des microservices ou si elle est simplement répartie entre plusieurs conteneurs. Comme expliqué précédemment, dans une approche basée sur les microservices, chaque microservice détient son modèle et ses données, ce qui le rend autonome du point de vue du développement et du déploiement. Cependant, même si vous avez une application plus classique composée de plusieurs services (comme SOA), vous aurez également plusieurs conteneurs ou services constituant une même application métier, qui doivent être déployés en tant que système distribué. Ces types de systèmes sont complexes à monter en charge et à gérer : pour cette raison, vous avez absolument besoin d’un orchestrateur si vous voulez disposer d’une application multiconteneur prête pour la production et scalable.

La figure 4-23 illustre un déploiement dans un cluster d’une application composée de plusieurs microservices (conteneurs).

![](./media/image23.PNG)

**Figure 4-23**. Un cluster de conteneurs

Ceci ressemble à une approche logique. Mais comment gérez-vous l’équilibrage de charge, le routage et l’orchestration de ces applications composées ?

Le moteur Docker standard dans des hôtes Docker individuels répond aux besoins de la gestion des instances avec une seule image sur un seul hôte, mais il ne peut pas faire face quand il s’agit de gérer plusieurs conteneurs déployés sur plusieurs hôtes pour des applications distribuées plus complexes. Dans la plupart des cas, vous avez besoin d’une plateforme de gestion qui va démarrer automatiquement les conteneurs, monter en charge les conteneurs avec plusieurs instances par image, les suspendre ou les arrêter si nécessaire, et idéalement, contrôler comment ils accèdent à des ressources comme le réseau et le stockage de données.

Pour aller au-delà de la gestion de conteneurs individuels ou d’applications composées très simples et passer à des applications d’entreprise plus grandes avec des microservices, vous devez faire appel à l’orchestration et au clustering des plateformes.

Du point de vue de l’architecture et du développement, si vous créez de grandes applications d’entreprise basées sur des microservices, il est important de comprendre les plateformes et les produits suivants, qui prennent en charge des scénarios avancés :

**Clusters et orchestrateurs**. Quand vous devez monter en charge (scale out) des applications sur plusieurs hôtes Docker, comme dans le cas d’une grande application basée sur des microservices, il est essentiel de pouvoir gérer tous ces hôtes sous la forme d’un seul cluster, en faisant abstraction de la complexité de la plateforme sous-jacente. C’est ce que les clusters de conteneurs et les orchestrateurs permettent. Azure Service Fabric, Kubernetes, Docker Swarm et Mesosphere DC/OS sont des exemples d’orchestrateurs. Les trois derniers orchestrateurs open source sont disponibles dans Azure via Azure Container Service.

**Planificateurs**. La *planification* signifie qu’un administrateur a la possibilité de lancer des conteneurs dans un cluster : ils doivent donc également fournir une interface utilisateur. Un planificateur de cluster a plusieurs responsabilités : utiliser efficacement les ressources du cluster, définir les contraintes fournies par l’utilisateur, équilibrer efficacement la charge des conteneurs entre les nœuds ou les hôtes, et être robustes face aux erreurs, tout en offrant une haute disponibilité.

Les concepts de cluster et de planificateur sont étroitement liés : les produits fournis par les différents fournisseurs offrent souvent les deux ensembles de fonctionnalités. La liste suivante montre les choix les plus importants pour les plateformes et les logiciels dont vous disposez pour les clusters et les planificateurs. Ces orchestrateurs sont généralement proposés dans des clouds publics comme Azure.

## <a name="software-platforms-for-container-clustering-orchestration-and-scheduling"></a>Plateformes logicielles pour le clustering, l’orchestration et la planification de conteneurs

Kubernetes

![https://pbs.twimg.com/media/Bt\_pEfqCAAAiVyz.png](./media/image24.png)

> Kubernetes est un produit open source qui offre des fonctionnalités allant de l’infrastructure de cluster et la planification de conteneurs à des fonctionnalités d’orchestration. Il vous permet d’automatiser le déploiement, la mise à l’échelle et le fonctionnement de conteneurs d’application entre des clusters d’hôtes.
>
> Kubernetes fournit une infrastructure orientée conteneur, qui regroupe des conteneurs d’application dans des unités logiques pour en faciliter la gestion et la découverte.
>
> Kubernetes est suffisamment mature dans Linux, mais il l’est moins dans Windows.

Docker Swarm

![http://rancher.com/wp-content/themes/rancher-2016/assets/images/swarm.png?v=2016-07-10-am](./media/image25.png)

> Docker Swarm vous permet de placer des conteneurs Docker dans un cluster et de les planifier. Avec Swarm, vous pouvez changer un pool d’hôtes Docker en un seul hôte Docker virtuel. Les clients peuvent envoyer des demandes d’API à Swarm de la même façon qu’ils le font à des hôtes, ce qui signifie que Swarm facilite la mise à l’échelle des applications sur plusieurs hôtes.
>
> Docker Swarm est un produit de la société Docker.
>
> Docker v1.12 ou ultérieur peut exécuter le mode Swarm natif et intégré.

Mesosphere DC/OS

![https://mesosphere.com/wp-content/uploads/2016/04/logo-horizontal-styled.png](./media/image26.png)

> Mesosphere Enterprise DC/OS (basé sur Apache Mesos) est une plateforme prête pour la production permettant d’exécuter des conteneurs et des applications distribuées.
>
> DC/OS fonctionne en rendant abstraite une collection des ressources disponibles dans le cluster et en rendant ces ressources disponibles pour les composants créés sur celle-ci. Marathon est généralement utilisé comme planificateur intégré à DC/OS.
>
> DC/OS est suffisamment mature dans Linux, mais il l’est moins dans Windows.

Azure Service Fabric

![https://azure.microsoft.com/svghandler/service-fabric?width=600&height=315](./media/image27.png)

> [Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-overview) est une plateforme de microservices de Microsoft pour la création d’applications. Il s’agit d’un [orchestrateur](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-resource-manager-introduction) de services, qui crée des clusters de machines. Service Fabric peut déployer des services en tant que conteneurs ou en tant que processus standard. Il peut même combiner des services dans des processus avec des services dans des conteneurs au sein de la même application et du même cluster.
>
> Service Fabric fournit des [modèles de programmation Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-choose-framework) supplémentaires prescriptifs et facultatifs, comme des [services avec état](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-introduction) et [Reliable Actors](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-actors-introduction).
>
> Service Fabric est mature dans Windows (plusieurs années d’évolution dans Windows), mais il l’est moins dans Linux. 
> Les conteneurs Linux et Windows sont pris en charge dans Service Fabric depuis 2017.

## <a name="using-container-based-orchestrators-in-microsoft-azure"></a>Utilisation d’orchestrateurs basés sur des conteneurs dans Microsoft Azure

Plusieurs fournisseurs de cloud offrent la prise en charge des conteneurs Docker, ainsi que celle des clusters et de l’orchestration Docker, notamment Microsoft Azure, Amazon EC2 Container Service et Google Container Engine. Microsoft Azure offre la prise en charge des clusters et de l’orchestrateur Docker via Azure Container Service, comme expliqué dans la section suivante.

Un autre choix est d’utiliser Microsoft Azure Service Fabric (plateforme de microservices), qui prend également en charge Docker avec des conteneurs Linux et Windows. Service Fabric s’exécute sur Azure ou sur n’importe quel autre cloud, et s’exécute également [localement](https://docs.microsoft.com/azure/service-fabric/service-fabric-deploy-anywhere).

## <a name="using-azure-container-service"></a>Utilisation d’Azure Container Service

Un cluster Docker met en pool plusieurs hôtes Docker et les expose sous la forme d’un hôte Docker virtuel unique : vous pouvez ainsi déployer plusieurs conteneurs dans le cluster. Le cluster prend en charge tous les détails complexes de la gestion, comme la scalabilité , l’intégrité, etc. La figure 4-24 représente la façon dont un cluster Docker pour des applications composées est mappé à Azure Container Service.

ACS offre un moyen de simplifier la création, la configuration et la gestion d’un cluster de machines virtuelles qui sont préconfigurées pour exécuter des applications en conteneur. Avec une configuration optimisée d’outils open source courants de planification et d’orchestration, ACS vous permet d’utiliser vos compétences existantes ou de profiter de l’expertise importante et toujours croissante de la communauté pour déployer et gérer sur Microsoft Azure des applications basées sur des conteneurs.

Azure Container Service optimise la configuration des outils open source et des technologies courants de mise en cluster Docker spécifiquement pour Azure. Vous obtenez une solution ouverte qui offre la portabilité à la fois pour vos conteneurs et pour la configuration de votre application. Vous sélectionnez la taille, le nombre d’hôtes et les outils de l’orchestrateur, et Container Service gère tout le reste.

![](./media/image28.png)

**Figure 4-24**. Choix de clustering dans Azure Container Service

ACS tire parti des images Docker pour garantir la portabilité complète de vos conteneurs d’application. Il prend en charge votre choix de plateformes d’orchestration open source comme DC/OS (technologie Apache Mesos), Kubernetes (créé à l’origine par Google) et Docker Swarm, pour garantir que ces applications peuvent être mises à l’échelle en milliers ou même en dizaines de milliers de conteneurs.

Azure Container Service vous permet de bénéficier des fonctionnalités de niveau entreprise d’Azure, tout en conservant la portabilité des applications, notamment au niveau des couches d’orchestration.

![](./media/image29.png)

**Figure 4-25**. Orchestrateurs dans ACS

Comme le montre la figure 4-25, Azure Container Service est simplement l’infrastructure fournie par Azure pour déployer DC/OS, Kubernetes ou Docker Swarm : il n’implémente aucun autre orchestrateur. Ainsi, ACS n’est pas un orchestrateur en tant que tel. C’est seulement une infrastructure qui tire parti d’orchestrateurs open source existants pour les conteneurs.

Du point de vue de l’utilisation, l’objectif d’Azure Container Service est de fournir un environnement d’hébergement de conteneurs avec des technologies et des outils open source répandus. Pour cela, il expose les points de terminaison d’API standard pour l’orchestrateur que vous avez choisi. En utilisant ces points de terminaison, vous pouvez exploiter n’importe quel logiciel qui peut communiquer avec ces points de terminaison. Par exemple, dans le cas du point de terminaison Docker Swarm, vous pouvez choisir d’utiliser l’interface de ligne de commande de Docker. Pour DC/OS, vous pouvez choisir d’utiliser l’interface de ligne de commande de DC/OS.

### <a name="getting-started-with-azure-container-service"></a>Bien démarrer avec Azure Container Service 

Pour commencer à utiliser Azure Container Service, déployez un cluster Azure Container Service à partir du portail Azure en utilisant un modèle Azure Resource Manager ou [l’interface CLI](https://docs.microsoft.com/cli/azure/install-azure-cli). Les modèles disponibles sont [Docker Swarm](https://github.com/Azure/azure-quickstart-templates/tree/master/101-acs-swarm), [Kubernetes](https://github.com/Azure/azure-quickstart-templates/tree/master/101-acs-kubernetes) et [DC/OS](https://github.com/Azure/azure-quickstart-templates/tree/master/101-acs-dcos). Les modèles de démarrage rapide peuvent être modifiés pour inclure des configurations Azure supplémentaires ou avancées. Pour plus d’informations sur le déploiement d’un cluster Azure Container Service, consultez [Déployer un cluster Azure Container Service](https://docs.microsoft.com/azure/container-service/container-service-deployment) sur le site web Azure.

Aucun coût n’est facturé pour les logiciels installés par défaut dans le cadre d’ACS. Toutes les options par défaut sont implémentées avec des logiciels open source.

ACS est actuellement disponible pour les machines virtuelles Linux de la série Standard A, D, DS, G et GS dans Azure. Vous payez seulement pour les instances de calcul que vous choisissez, ainsi que pour les autres ressources de l’infrastructure sous-jacente consommées, comme le stockage et la mise en réseau. Aucun coût supplémentaire n’est facturé pour ACS lui-même.

## <a name="additional-resources"></a>Ressources supplémentaires

-   **Présentation d’Azure Container Service pour Kubernetes**
    [*https://docs.microsoft.com/azure/container-service/container-service-intro*](https://docs.microsoft.com/azure/container-service/container-service-intro)

-   **Docker Swarm overview**
    [*https://docs.docker.com/swarm/overview/*](https://docs.docker.com/swarm/overview/)

-   **Swarm mode overview**
    [*https://docs.docker.com/engine/swarm/*](https://docs.docker.com/engine/swarm/)

-   **Mesosphere DC/OS Overview**
    [*https://docs.mesosphere.com/1.7/overview/*](https://docs.mesosphere.com/1.7/overview/)

-   **Kubernetes.** Le site officiel.\
    [*https://kubernetes.io/*](https://kubernetes.io/)


>[!div class="step-by-step"]
[Précédent] (resilient-high-availability-microservices.md) [Suivant] (using-azure-service-fabric.md)
