---
title: Gérer les environnements de production Docker
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: 3bafdd9f6a6aa4f850fd28b6315e68c643d1f8c0
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/29/2018
ms.locfileid: "50202853"
---
# <a name="manage-production-docker-environments"></a>Gérer les environnements de production Docker

Gestion du cluster et l’orchestration est le processus de contrôle d’un groupe d’hôtes. Cela peut impliquer d’ajout et suppression d’ordinateurs hôtes à partir d’un cluster, l’obtention d’informations sur l’état actuel des hôtes et des conteneurs et de démarrage et arrêt des processus. Orchestration et la gestion du cluster sont étroitement liés à la planification, car le planificateur doit avoir accès à chaque hôte dans le cluster afin de planifier les services. Pour cette raison, le même outil est souvent utilisé pour les deux fonctions.

## <a name="container-service-and-management-tools"></a>Outils de gestion des services et du conteneur

Container Service assure le déploiement rapide de solutions de clustering et d’orchestration de conteneur open source populaire. Il utilise des images Docker pour vous assurer que vos conteneurs d’applications sont entièrement portables. À l’aide de Container Service, vous pouvez déployer (s’appuyant Mesosphere et Apache Mesos) DC/OS et Docker Swarm clusters à l’aide de modèles Azure Resource Manager ou le portail Azure pour vous assurer que vous pouvez faire évoluer ces applications à des milliers, même des dizaines de milliers, de conteneurs.

Vous déployez ces clusters à l’aide d’Azure Virtual Machine Scale Sets, et les clusters tirent parti des offres de mise en réseau et stockage Azure. Pour accéder au Service de conteneur, vous avez besoin d’un abonnement Azure. Avec Container Service, vous pouvez tirer parti des fonctionnalités de niveau entreprise d’Azure tout en conservant la portabilité des applications, notamment au niveau des couches d’orchestration.

Tableau 6-1 répertorie les outils de gestion courants liés à leurs orchestrateurs, planificateurs et de plateforme de clustering.

Outils de gestion Docker tableau 6-1 :


| Outils de gestion      | Description           | Orchestrateurs connexes |
|-----------------------|-----------------------|-----------------------|
| Service de conteneur\(gestion de l’interface utilisateur dans le portail Azure) | [Service de conteneur](https://azure.microsoft.com/services/container-service/) fournit un permet d’obtenir facilement démarré de façon à [déployer un cluster de conteneur dans Azure](https://docs.microsoft.com/azure/container-service/dcos-swarm/container-service-deployment) basée sur des orchestrateurs populaires comme Mesosphere DC/OS, Kubernetes et Docker Swarm. <br /><br /> Container Service optimise la configuration de ces plateformes. Vous devez simplement sélectionner la taille, le nombre d’hôtes et le choix d’outils d’orchestrateur et Container Service gère tout le reste. | Mesosphere DC/OS <br /><br /> Kubernetes <br /><br /> Docker Swarm |
| Plan de contrôle universel docker\(en local ou cloud) | [Plan de contrôle universel docker](https://docs.docker.com/v1.11/ucp/overview/) est la solution de gestion du cluster de niveau entreprise à partir de Docker. Il vous permet de gérer votre cluster à partir d’un emplacement unique. <br /><br /> Plan de contrôle universel docker est inclus dans le produit commercial nommé Docker Datacenter, qui propose Docker Swarm, plan de contrôle universel de Docker et Docker Trusted Registry. <br /><br /> Centre de données de docker peut être installé en local ou configuré à partir d’un cloud public comme Azure. | Docker Swarm\(pris en charge par le Service de conteneur) |
| Docker Cloud\(également appelé Tutum ; cloud SaaS) | [Docker Cloud](https://docs.docker.com/docker-cloud/) est un service hébergé de gestion (SaaS) qui fournit des capacités d’orchestration et d’un Registre Docker avec la build et des fonctions de test pour les images d’application Dockerisée, outils pour vous aider à configurer et gérer votre infrastructure de l’hôte, fonctionnalités et de déploiement pour vous aider à automatiser le déploiement de vos images à votre infrastructure concrète. Vous pouvez vous connecter à votre compte Docker SaaS Cloud à votre infrastructure dans Container Service exécutant un cluster Docker Swarm. | Docker Swarm\(pris en charge par le Service de conteneur) |
| Mesosphere Marathon\(en local ou cloud) | [Marathon](https://mesosphere.github.io/marathon/docs/marathon-ui.html) est un conteneur d’orchestration et le Planificateur de plateforme de production pour de Mesosphere DC/OS et Apache Mesos. <br /><br /> Il fonctionne avec Mesos (DC/OS est basé sur Apache Mesos) à long terme de contrôle des services et fournit un [l’interface utilisateur web pour la gestion des processus et conteneur](https://mesosphere.github.io/marathon/docs/marathon-ui.html). Il fournit un outil de gestion de l’interface utilisateur web | Mesosphere DC/OS\(basé sur Apache Mesos ; pris en charge par le Service de conteneur) |
| Google Kubernetes | [Kubernetes](https://kubernetes.io/docs/user-guide/ui/#dashboard-access) couvre l’orchestration, la planification et infrastructure de cluster. Il est une plateforme open source pour l’automatisation des opérations de conteneurs d’applications, de mise à l’échelle et de déploiement sur des clusters d’hôtes, en fournissant une infrastructure orientée conteneur. | Google Kubernetes\(pris en charge par le Service de conteneur) |

## <a name="azure-service-fabric"></a>Azure Service Fabric

Un autre choix pour la gestion et de déploiement de cluster est Azure Service Fabric. [Service Fabric](https://azure.microsoft.com/services/service-fabric/) est une plateforme de microservices de Microsoft qui inclut l’orchestration de conteneur, ainsi que des développeurs programmation de modèles pour créer des applications de microservices hautement évolutif. Service Fabric prend en charge Docker dans les versions Linux en version préliminaire actuelles, comme dans le [en version préliminaire de Service Fabric sur Linux](https://docs.microsoft.com/azure/service-fabric/service-fabric-deploy-anywhere)et pour les conteneurs Windows [dans la prochaine version](https://docs.microsoft.com/azure/service-fabric/service-fabric-containers-overview).

Voici les outils de gestion de Service Fabric :

-   [Portail Azure pour Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-creation-via-portal) associés au cluster operations (création/mise à jour/suppression) un cluster ou de configurer son infrastructure (machines virtuelles, équilibrage de charge, la mise en réseau, etc.)

-   [Azure Service Fabric Explorer](https://docs.microsoft.com/azure/service-fabric/service-fabric-visualizing-your-cluster) est un outil d’interface utilisateur web spécialisées qui fournit des insights et certaines opérations sur le cluster Service Fabric à partir du point de vue de nœuds/machines virtuelles et à partir de l’application et les services de point de vue.


>[!div class="step-by-step"]
[Précédent](run-microservices-based-applications-in-production.md)
[Suivant](monitor-containerized-application-services.md)
