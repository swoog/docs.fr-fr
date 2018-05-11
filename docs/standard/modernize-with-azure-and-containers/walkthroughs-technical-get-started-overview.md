---
title: Procédures pas à pas et les techniques obtiennent une vue d’ensemble démarrée
description: Moderniser des Applications .NET existantes avec Azure Cloud et les conteneurs Windows | Procédures pas à pas et les techniques obtiennent une vue d’ensemble démarrée
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/28/2018
ms.openlocfilehash: 27de9d1c5475855a22f2d8a3518982605277f6d9
ms.sourcegitcommit: 88f251b08bf0718ce119f3d7302f514b74895038
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2018
---
# <a name="walkthroughs-and-technical-get-started-overview"></a>Procédures pas à pas et les techniques obtiennent une vue d’ensemble démarrée

Pour limiter la taille de ce livre électronique, documentation technique supplémentaire et les procédures pas à pas complète étaient mis à disposition dans un référentiel GitHub. La série en ligne des procédures pas à pas qui est décrite dans ce chapitre traite le programme d’installation pas à pas plusieurs environnements qui sont basées sur les conteneurs Windows et le déploiement vers Azure.

Les sections suivantes expliquent ce que chaque procédure pas à pas sur ses objectifs et la vision de haut niveau et fournit un diagramme des tâches qui sont impliquées. Vous pouvez obtenir les procédures pas à pas eux-mêmes dans le *eShopModernizing* applications wiki de référentiel GitHub à [ https://github.com/dotnet-architecture/eShopModernizing/wiki ](https://github.com/dotnet-architecture/eShopModernizing/wiki).

## <a name="technical-walkthrough-list"></a>Liste des techniques de procédure pas à pas

Les procédures get-started suivantes fournissent des conseils techniques cohérent et complet des exemples d’applications que vous pouvez de courbes d’élévation et MAJ en utilisant des conteneurs et ensuite déplacer à l’aide de plusieurs options de déploiement dans Azure.

Chacun des procédures suivantes utilise les nouveaux exemples eShopLegacy et eShopModernizing d’applications, qui sont disponibles sur GitHub à l’adresse [ https://github.com/dotnet-architecture/eShopModernizing ](https://github.com/dotnet-architecture/eShopModernizing).

- **Visite guidée de shopping hérité applications (ligne de base pour moderniser)**

- **Mettez en conteneur de vos applications web ASP.NET existantes (Web Forms et MVC) avec des conteneurs Windows**

- **Mettez en conteneur vos services WCF existants (applications multicouches) avec des conteneurs Windows**

- **Déployer votre application basée sur les conteneurs de Windows pour les machines virtuelles Azure**

- **Déployer vos applications basée sur les conteneurs de Windows à Kubernetes dans le Service de conteneur Azure**

- **Déployer vos applications basée sur les conteneurs de Windows Azure Service fabric**


## <a name="walkthrough-1-tour-of-eshop-legacy-apps"></a>Procédure pas à pas 1 : Visite guidée des applications héritées de shopping

### <a name="technical-walkthrough-availability"></a>Disponibilité de la procédure pas à pas technique

La procédure pas à pas technique complet est disponible dans le wiki de référentiel GitHub eShopModernizing :

[procédures pas à pas d’eShopModernizing wiki](https://github.com/dotnet-architecture/eShopModernizing/wiki)


### <a name="overview"></a>Vue d'ensemble

Dans cette procédure pas à pas, vous pouvez explorer l’implémentation initiale de trois exemples d’applications héritées. Les deux premiers exemples d’applications web une architecture monolithique et ont été créées à l’aide d’ASP.NET classique. Une application est basée sur ASP.NET 4.x MVC ; la deuxième application est basée sur les Web Forms ASP.NET 4.x. L’application de tiers est une application à 3 couches composée d’une application Windows Forms de client et un côté serveur [Windows Communication Foundation (WCF)](../../framework/wcf/whats-wcf.md) service.

Toutes ces applications sont disponibles sur le [eShopModernizing du référentiel GitHub](https://github.com/dotnet-architecture/eShopModernizing).

### <a name="goals"></a>Objectifs

L’objectif principal de cette procédure pas à pas est simplement afin de vous familiariser avec ces applications et leur configuration et le code. Vous pouvez configurer les applications afin qu’ils génèrent et utilisent des données fictives, sans l’aide de la base de données SQL, à des fins de test. Cette configuration facultative est basée sur l’injection de dépendance, d’une manière découplée.

### <a name="scenario-1-aspnet-web-apps"></a>Scénario 1 : Les applications Web ASP.NET

La figure ci-dessous illustre le scénario simple des applications web ASP.NET existants d’origine.

> ![Scénario simple d’architecture des applications web ASP.NET existantes d’origine](./media/image5-1.png)
>

À partir d’une perspective de domaine d’entreprise, les deux applications offrent la même catalogue de fonctionnalités de gestion. Membres de l’équipe d’entreprise Shopping utiliseriez l’application pour afficher et modifier le catalogue de produits. 

La figure suivante montre les captures d’écran de l’application initiale.

![Applications ASP.NET MVC et les Web Forms ASP.NET (technologies existantes/hérité)](./media/image5-2.png)

Dépendances dans ASP.NET 4.x ou des versions antérieures (soit pour MVC ou Web Forms) signifie que ces applications ne s’exécutent sur .NET Core, sauf si le code est entièrement réécrit à l’aide d’ASP.NET MVC de base. 

### <a name="scenario-2-wcf-service-and-winforms-client-app-3-tier-app"></a>Scénario 2 : Service WCF et WinForms client application (application de niveau 3)

La figure ci-dessous illustre le scénario simple de l’application héritée à 3 couches d’origine.

> ![Scénario simple d’architecture de l’application à 3 couches héritée d’origine avec un service WCF et d’une application WinForms client](./media/image5-1.5.png)
>

### <a name="benefits"></a>Avantages

Les avantages de cette procédure pas à pas sont simples : simplement vous familiariser avec le code et les applications initiales.

### <a name="next-steps"></a>Étapes suivantes

Explorer ce contenu plus approfondi sur le wiki de GitHub :

  - [Visite guidée sur la ligne de base ASP.NET MVC et les applications Web Forms « héritées »](https://github.com/dotnet-architecture/eShopModernizing/wiki/01.-Tour-on-the-ASP.NET-MVC-and-WebForms-apps-implementation-code)
  - [Visite sur le service WCF de base et d’application WinForms « héritée » (niveau 3)](https://github.com/dotnet-architecture/eShopModernizing/wiki/21.-Tour-on-the-WCF-service-and-WinForms-apps)


## <a name="walkthrough-2-containerize-your-existing-net-applications-with-windows-containers"></a>Procédure 2 : Mettez en conteneur vos applications .NET existantes avec des conteneurs Windows

### <a name="overview"></a>Vue d'ensemble

Les conteneurs Windows permet d’améliorer le déploiement des applications .NET existantes, telles que celles basées sur MVC, Web Forms ou WCF, pour les environnements de test, de développement et de production.

### <a name="goals"></a>Objectifs

L’objectif de cette procédure pas à pas est de vous montrer plusieurs options pour containerizing une application .NET Framework existante. Vous pouvez :

- Mettez en conteneur de votre application à l’aide de [Visual Studio 2017 Tools pour Docker](/aspnet/core/host-and-deploy/docker/visual-studio-tools-for-docker) (Visual Studio 2017 ou versions ultérieures).

- Mettez en conteneur de votre application en ajoutant manuellement un [Dockerfile](https://docs.docker.com/engine/reference/builder/), puis en utilisant la [Docker CLI](https://docs.docker.com/engine/reference/commandline/cli/).

- Mettez en conteneur de votre application à l’aide de la [Img2Docker](https://github.com/docker/communitytools-image2docker-win) outil (outil open source à partir de Docker).

Cette procédure pas à pas se concentre sur les outils de 2017 Visual Studio pour l’approche de Docker, mais les deux autres approches sont relativement similaires en ce qui concerne l’utilisation des fichiers Dockerfile.

### <a name="scenario-1-containerized-aspnet-web-apps"></a>Scénario 1 : Les applications web ASP.NET en conteneur

Figure ci-dessous illustre le scénario pour les applications d’applications en conteneur Shopping web hérité.

> ![Diagramme d’architecture simplifiée de placées dans des conteneurs dans un environnement de développement des applications ASP.NET](./media/image5-3.png)
>


### <a name="scenario-2-containerized-wcf-service"></a>Scénario 2 : Service WCF en conteneur

La figure ci-dessous illustre le scénario pour une application à 3 couches avec un service WCF en conteneur. 

> ![Diagramme d’architecture du service WCF en conteneur dans un environnement de développement de simplifiée](./media/image5-3.5.png)
>

### <a name="benefits"></a>Avantages

Il existe des avantages à l’exécution de votre application monolithique dans un conteneur. Tout d’abord, vous créez une image de l’application. À ce stade, chaque déploiement s’exécute dans le même environnement. Chaque conteneur utilise la même version du système d’exploitation, a la même version de dépendances installé, utilise la même version du .NET framework et est construit à l’aide du même processus. En fait, vous contrôlez les dépendances de votre application à l’aide d’une image Docker. Lorsque vous déployez les conteneurs, les dépendances se déplacent avec l’application.

Un autre avantage est que les développeurs peuvent exécuter l’application dans l’environnement cohérent qui est fourni par les conteneurs Windows. Les problèmes qui apparaissent uniquement dans certaines versions peuvent être détectées immédiatement, au lieu de surfaces dans un environnement intermédiaire ou de production. Les différences dans les environnements de développement utilisés par les membres de l’équipe de développement a d’importance inférieure lorsque les applications s’exécutent dans des conteneurs.

Les applications en conteneur possèdent également une courbe plate de la montée en puissance parallèle. Les applications en conteneur permettent d’avoir plus d’application et les instances de service (basés sur les conteneurs) dans une machine virtuelle ou d’un ordinateur physique par rapport aux déploiements d’application normal par ordinateur. Cela se traduit par densité plus élevée et moins nécessaire des ressources, notamment lorsque vous utilisez orchestrators comme Kubernetes ou Service Fabric.

CONTENEURISATION des données, dans des situations idéale, ne nécessitent pas d’apporter des modifications au code d’application (C\#). Dans la plupart des scénarios, vous devez simplement les fichiers de métadonnées de déploiement (fichiers Dockerfile et Docker Compose) Docker.

### <a name="next-steps"></a>Étapes suivantes

Explorer ce contenu plus approfondi sur le wiki de GitHub :

  - [Comment mettez en conteneur d’applications web .NET Framework avec les conteneurs Windows et Docker](https://github.com/dotnet-architecture/eShopModernizing/wiki/02.-How-to-containerize-the-.NET-Framework-web-apps-with-Windows-Containers-and-Docker)
  - [Ajout d’un Support Docker à un service WCF](https://github.com/dotnet-architecture/eShopModernizing/wiki/22.-Adding-Docker-Support)



## <a name="walkthrough-3-deploy-your-windows-containers-based-app-to-azure-vms"></a>Procédure 3 : Déployer votre application basée sur les conteneurs de Windows sur les machines virtuelles Azure

### <a name="technical-walkthrough-availability"></a>Disponibilité de la procédure pas à pas technique

La procédure pas à pas technique complet est disponible dans le wiki de référentiel GitHub eShopModernizing : [https://github.com/dotnet-architecture/eShopModernizing/wiki/03.-How-to-deploy-your-Windows-Containers-based-app-into-Azure-VMs-(Including-CI-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/03.-How-to-deploy-your-Windows-Containers-based-app-into-Azure-VMs-(Including-CI-CD))

### <a name="overview"></a>Vue d'ensemble

Déploiement sur un hôte Docker sur un serveur Windows Server 2016 Virtual Machine (VM) dans Azure vous permet de définir rapidement des environnements de développement/test/mise en lots. Elle vous donne également un emplacement commun pour les testeurs ou les utilisateurs des activités à valider l’application. Machines virtuelles peuvent également être infrastructure valide comme les environnements de production de Service (IaaS).

### <a name="goals"></a>Objectifs

L’objectif de cette procédure pas à pas est de vous montrer les plusieurs alternatives que vous avez lorsque vous déployez les conteneurs Windows sur les machines virtuelles Azure qui sont basés sur Windows Server 2016 ou versions ultérieures.

### <a name="scenarios"></a>Scénarios

Plusieurs scénarios sont traités dans cette procédure pas à pas.

#### <a name="scenario-a-deploy-to-an-azure-vm-from-a-dev-pc-through-docker-engine-connection"></a>Scénario a : les déployer sur une machine virtuelle Azure à partir d’un ordinateur de développement via la connexion du moteur Docker

![Déployer sur une machine virtuelle Azure à partir d’un ordinateur de développement via une connexion du moteur Docker](./media/image5-4.png)

> **Figure 5-4.** Déployer sur une machine virtuelle Azure à partir d’un ordinateur de développement via une connexion du moteur Docker

#### <a name="scenario-b-deploy-to-an-azure-vm-through-a-docker-registry"></a>Scénario b : déployer sur une machine virtuelle Azure via un Registre Docker

![Déployer sur une machine virtuelle Azure via un Registre Docker](./media/image5-5.png)

> **Figure 5-5.** Déployer sur une machine virtuelle Azure via un Registre Docker

#### <a name="scenario-c-deploy-to-an-azure-vm-from-cicd-pipelines-in-visual-studio-team-services"></a>Scénario c : déployer sur une machine virtuelle Azure à partir de l’élément de configuration/CD des pipelines dans Visual Studio Team Services

![Déployer sur une machine virtuelle Azure à partir de CD / l’élément de configuration des pipelines dans Visual Studio Team Services](./media/image5-6.png)

> **Figure 5-6.** Déployer sur une machine virtuelle Azure à partir de CD / l’élément de configuration des pipelines dans Visual Studio Team Services

### <a name="azure-vms-for-windows-containers"></a>Machines virtuelles Azure pour les conteneurs Windows

Machines virtuelles Azure pour les conteneurs Windows sont basés sur Windows Server 2016, Windows 10 ou versions ultérieures de machines virtuelles, à la fois avec le moteur Docker configuré. Dans la plupart des cas, Windows Server 2016 est utilisé dans les machines virtuelles Azure.

Azure fournit actuellement une machine virtuelle nommée **Windows Server 2016 avec des conteneurs**. Vous pouvez utiliser cet ordinateur virtuel pour essayer la nouvelle fonctionnalité de conteneur Windows Server avec Windows Server Core ou Nano Server de Windows. Les images de système d’exploitation de conteneur sont installés, et ensuite l’ordinateur virtuel est prêt à être utilisé avec Docker.

### <a name="benefits"></a>Avantages

Bien que les conteneurs Windows peuvent être déployées sur local Windows Server 2016 machines virtuelles, lorsque vous déployez dans Azure, vous obtenez un moyen plus simple pour commencer, machines virtuelles de prêt à utiliser Windows Server conteneur. Vous obtenez également un emplacement commun en ligne qui est accessible aux testeurs et évolutivité automatique par le biais des machines virtuelles Azure identiques.

### <a name="next-steps"></a>Étapes suivantes

Explorer ce contenu plus approfondi sur le wiki de GitHub :

[https://github.com/dotnet-architecture/eShopModernizing/wiki/03.-How-to-deploy-your-Windows-Containers-based-app-into-Azure-VMs-(Including-CI-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/03.-How-to-deploy-your-Windows-Containers-based-app-into-Azure-VMs-(Including-CI-CD))

## <a name="walkthrough-4-deploy-your-windows-containers-based-apps-to-azure-container-instances-aci"></a>Procédure 4 : Déployer vos applications basée sur les conteneurs de Windows sur les Instances du conteneur Azure (ACI)

### <a name="technical-walkthrough-availability"></a>Disponibilité de la procédure pas à pas technique

La procédure pas à pas technique complet est disponible dans le wiki de référentiel GitHub eShopModernizing :

[Déploiement d’applications sur ACI (Instances de conteneur Azure)](https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-Deploying-the-Apps-to-ACI-(Azure-Container-Instances))

### <a name="overview"></a>Vue d'ensemble

[Instances du conteneur Azure (ACI)](https://docs.microsoft.com/en-us/azure/container-instances/) est la plus rapide pour un environnement de développement/test/mise en lots de conteneurs où vous pouvez déployer des instances uniques de conteneurs.

### <a name="goals"></a>Objectifs

Cette procédure pas à pas vous montre les principaux scénarios lors du déploiement de conteneurs Windows Azure conteneur Instances (ACI) et comment vous pouvez déployer des applications d’eShopModernizing dans ACI.

### <a name="scenarios"></a>Scénarios

Il peut y avoir des variations sur le déploiement des applications eShopModernizing dans ACI telles que le déploiement d’un ou toutes les applications (application MVC, Web Forms application ou service WCF). Dans le scénario suivant, illustré ci-dessous, vous pouvez voir l’application ASP.NET MVC ainsi que le conteneur de SQL Server que les deux déployés en tant que conteneurs dans ACI (Instances de conteneurs Azure).

![Déploiement ACI à partir d’un environnement de développement](./media/image5-3.5.6.png)

### <a name="benefits"></a>Avantages

Les Instances du conteneur Azure facilite créer et gérer des conteneurs Docker dans Azure, sans avoir à configurer des machines virtuelles ou arrêter un service de niveau supérieur. Avec ACI, vous pouvez directement déployer un conteneur Windows dans Azure et l’exposer à internet avec un nom de domaine complet (FQDN) en quelques secondes (à condition que vous avez l’image de conteneur Windows prêt dans un Registre Docker Hub d’ancrage ou conteneur Azure Registre).

### <a name="considerations"></a>Éléments à prendre en considération

Déploiement de conteneurs Windows avec le .NET Framework complet / ASP.NET ou SQL Server dans Azure conteneur Instances (ACI) n’est pas tout à fait aussi rapide que le déploiement sur un hôte Docker régulière (par exemple, Windows Server 2016 avec des conteneurs Windows), car l’image Docker doit être téléchargés à chaque fois (extraite à partir du Registre Docker) et la taille de l’image de conteneur SQL (15.1 Go) et l’image de conteneur ASP.NET (13.9 Go) est importante, mais il est beaucoup moins coûteuse que la conservation de votre propre hôte docker (définitivement en ligne Windows Server 2016 avec l’ordinateur virtuel de conteneurs Windows dans Azure) ne pas de mentionner un ensemble orchestrator comme Kubernetes dans Azure (AKS/ACS) ou de l’infrastructure de Service Azure qui sont, quant à eux, excellentes choix pour les déploiements de production.

En tant que principale conclusion, à l’aide d’Instances de conteneurs Azure est une option très intéressante pour les scénarios de développement et de Test et pour les pipelines de l’élément de configuration/CD.

## <a name="next-steps"></a>Étapes suivantes

Explorer ce contenu plus approfondi sur le wiki de GitHub : 

[https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-Deploying-the-Apps-to-ACI-(Azure-Container-Instances)](https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-Deploying-the-Apps-to-ACI-(Azure-Container-Instances)TBD)


## <a name="walkthrough-5-deploy-your-windows-containers-based-apps-to-kubernetes-in-azure-container-service"></a>Procédure 5 : Déployer vos applications de basée sur les conteneurs Windows sur Kubernetes dans le Service de conteneur Azure

### <a name="technical-walkthrough-availability"></a>Disponibilité de la procédure pas à pas technique

La procédure pas à pas technique complet est disponible dans le wiki de référentiel GitHub eShopModernizing :

[https://github.com/dotnet-architecture/eShopModernizing/wiki/04.-How-to-deploy-your-Windows-Containers-based-apps-into-Kubernetes-in-Azure-Container-Service-(Including-C-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/04.-How-to-deploy-your-Windows-Containers-based-apps-into-Kubernetes-in-Azure-Container-Service-(Including-C-CD))

### <a name="overview"></a>Vue d'ensemble

Une application qui est basée sur les conteneurs Windows devra rapidement utilisent des plateformes, éloigner encore davantage de machines virtuelles IaaS. Cela est nécessaire pour facilement atteindre une haute évolutivité et mieux automatisée de l’évolutivité et pour une amélioration significative dans automatisée déploiements et le contrôle de version. Vous pouvez atteindre ces objectifs à l’aide de l’orchestrateur [Kubernetes](https://kubernetes.io/), disponible dans [Azure conteneur Services](https://azure.microsoft.com/services/container-service/).

### <a name="goals"></a>Objectifs

L’objectif de cette procédure pas à pas est d’apprendre à déployer une application conteneur Windows – Kubernetes (également appelé *K8s*) dans le Service de conteneur Azure. Déploiement sur Kubernetes à partir de zéro est un processus en deux étapes :

1.  Déployer un cluster Kubernetes au Service de conteneur Azure.

2.  Déployer l’application et les ressources associées au cluster Kubernetes.

### <a name="scenarios"></a>Scénarios

#### <a name="scenario-a-deploy-directly-to-a-kubernetes-cluster-from-a-dev-environment"></a>Scénario a : les déployer directement vers un cluster de Kubernetes à partir d’un environnement de développement

![Déployer directement sur un cluster Kubernetes à partir d’un environnement de développement](./media/image5-7.png)

> **Figure 5-7.** Déployer directement sur un cluster Kubernetes à partir d’un environnement de développement

#### <a name="scenario-b-deploy-to-a-kubernetes-cluster-from-cicd-pipelines-in-team-services"></a>Scénario b : déployer vers un cluster Kubernetes à partir de l’élément de configuration/CD pipelines dans Team Services

![Déployer vers un cluster Kubernetes à partir de l’élément de configuration/CD des pipelines dans Team Services](./media/image5-8.png)

> **Figure 5-8.** Déployer vers un cluster Kubernetes à partir de l’élément de configuration/CD des pipelines dans Team Services

### <a name="benefits"></a>Avantages

Il existe de nombreux avantages pour le déploiement vers un cluster dans Kubernetes. Le principal avantage est que vous obtenez un environnement de l’environnement de production dans laquelle vous pouvez faire évoluer l’application en fonction du nombre d’instances de conteneurs, vous souhaitez utiliser (évolutivité interne dans les nœuds existants), en fonction du nombre de nœuds ou des machines virtuelles dans le cluster ( évolutivité globale du cluster).

Service de conteneur Azure optimise les technologies et outils open source populaires spécifiquement pour Azure. Vous obtenez une solution ouverte qui offre la portabilité de vos conteneurs et lors de la configuration de votre application. Sélectionnez la taille, le nombre d’hôtes, et le conteneur-Outils orchestrator Service gère tout le reste.

Avec Kubernetes, les développeurs peuvent progresser de réfléchir à des machines physiques et virtuelles, à la planification d’une infrastructure orientée conteneur qui facilite les fonctionnalités suivantes, entre autres :

- Applications basées sur plusieurs conteneurs

- Réplication des instances de conteneurs et d’échelle horizontale

- Attribution de noms et de découverte (par exemple, DNS interne)

- L’équilibrage de charge

- Mises à jour propagées

- Distribution de clés secrètes

- Vérifications de l’intégrité des applications

## <a name="next-steps"></a>Étapes suivantes

Explorer ce contenu plus approfondi sur le wiki de GitHub : [https://github.com/dotnet-architecture/eShopModernizing/wiki/04.-How-to-deploy-your-Windows-Containers-based-apps-into-Kubernetes-in-Azure-Container-Service-(Including-C-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/04.-How-to-deploy-your-Windows-Containers-based-apps-into-Kubernetes-in-Azure-Container-Service-(Including-C-CD))

## <a name="walkthrough-6-deploy-your-windows-containers-based-apps-to-azure-service-fabric"></a>Procédure pas à pas 6 : Déployer vos applications basée sur les conteneurs de Windows Azure Service fabric

### <a name="technical-walkthrough-availability"></a>Disponibilité de la procédure pas à pas technique

La procédure pas à pas technique complet est disponible dans le wiki de référentiel GitHub eShopModernizing :

[https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-How-to-deploy-your-Windows-Containers-based-apps-into-Azure-Service-Fabric-(Including-CI-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-How-to-deploy-your-Windows-Containers-based-apps-into-Azure-Service-Fabric-(Including-CI-CD))

### <a name="overview"></a>Vue d'ensemble

Une application basée sur les conteneurs Windows rapidement doit utiliser des plates-formes, éloigner encore davantage de machines virtuelles IaaS. Cela est nécessaire pour facilement atteindre une haute évolutivité et mieux automatisée de l’évolutivité et pour une amélioration significative dans automatisée déploiements et le contrôle de version. Vous pouvez atteindre ces objectifs à l’aide de l’orchestrateur Azure Service Fabric, qui est disponible dans le cloud Azure, mais vous pouvez également utiliser localement, ou même dans un autre cloud public.

### <a name="goals"></a>Objectifs

L’objectif de cette procédure pas à pas est d’apprendre à déployer une application conteneur Windows vers un cluster Service Fabric dans Azure. Déploiement sur l’infrastructure de Service à partir de zéro est un processus en deux étapes :

1.  Déployer un cluster Service Fabric vers Azure (ou un autre environnement).

2.  Déployer l’application et les ressources associées au cluster Service Fabric.

### <a name="scenarios"></a>Scénarios

#### <a name="scenario-a-deploy-directly-to-a-service-fabric-cluster-from-a-dev-environment"></a>Scénario a : les déployer directement à un cluster Service Fabric à partir d’un environnement de développement

![Déployer directement sur un cluster Service Fabric à partir d’un environnement de développement](./media/image5-9.png)

> **Figure 5-9**. Déployer directement sur un cluster Service Fabric à partir d’un environnement de développement

### <a name="scenario-b-deploy-to-a-service-fabric-cluster-from-cicd-pipelines-in-team-services"></a>Scénario b : déployer vers un cluster Service Fabric à partir de l’élément de configuration/CD pipelines dans Team Services

![Déployer vers un cluster Service Fabric à partir de l’élément de configuration/CD des pipelines dans Visual Studio Team Services](./media/image5-10.png)

> **Figure 5-10.** Déployer vers un cluster Service Fabric à partir de l’élément de configuration/CD des pipelines dans Visual Studio Team Services

## <a name="benefits"></a>Avantages

Les avantages du déploiement vers un cluster Service fabric sont semblables aux avantages de Kubernetes. Cependant, une différence est que le Service Fabric est un environnement de production plus mature pour les applications Windows par rapport à Kubernetes, qui se trouve dans une phase bêta pour les conteneurs Windows dans Kubernetes version 1.9 (2017 décembre). Kubernetes est un environnement plus mature pour Linux.

Le principal avantage de l’utilisation d’Azure Service Fabric est que vous obtenez un environnement de l’environnement de production dans laquelle vous pouvez faire évoluer l’application en fonction du nombre d’instances de conteneurs, vous souhaitez utiliser (évolutivité interne dans les nœuds existants), en fonction du nombre de les nœuds ou des ordinateurs virtuels du cluster (évolutivité globale du cluster).

Azure Service Fabric offre la portabilité de vos conteneurs et lors de la configuration de votre application. Vous pouvez avoir une infrastructure de Service de cluster dans Azure, ou installer localement dans votre centre de données. Vous pouvez même installer un cluster Service Fabric dans un autre cloud, tels que [Amazon AWS](https://blogs.msdn.microsoft.com/azureservicefabric/2017/05/18/tutorial-how-to-create-a-service-fabric-standalone-cluster-with-aws-ec2-instances/).

Avec Service Fabric, les développeurs peuvent progresser de réfléchir à des machines physiques et virtuelles à la planification d’une infrastructure orientée conteneur qui facilite les fonctionnalités suivantes, entre autres :

- Applications basées sur plusieurs conteneurs.

- Réplication des instances de conteneurs et d’échelle horizontale.

- Attribution de noms et de découverte (par exemple, DNS interne).

- L’équilibrage de charge.

- Mises à jour propagées.

- La distribution de clés secrètes.

- Vérifications de contrôle d’intégrité de l’application.

Les fonctionnalités suivantes sont exclusives dans Service Fabric (par rapport à d’autres orchestrators) :

- Fonctionnalité de services avec état, par le biais du modèle d’application des Services fiables.

- Modèle d’acteurs, par le biais du modèle d’application Reliable Actors.

- Déployer un processus nus, en plus des conteneurs Windows ou Linux.

- Avancé des mises à jour et les vérifications d’intégrité.

### <a name="next-steps"></a>Étapes suivantes

Explorer ce contenu plus approfondi sur le wiki de GitHub :

[https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-How-to-deploy-your-Windows-Containers-based-apps-into-Azure-Service-Fabric-(Including-CI-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-How-to-deploy-your-Windows-Containers-based-apps-into-Azure-Service-Fabric-(Including-CI-CD))

>[!div class="step-by-step"]
[Précédent](lift-and-shift-existing-apps-devops/migrate-to-hybrid-cloud-scenarios.md)
[Suivant](conclusions.md)
