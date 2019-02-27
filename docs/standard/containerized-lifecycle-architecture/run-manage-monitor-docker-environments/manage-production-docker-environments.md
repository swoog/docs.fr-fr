---
title: Gérer les environnements de production Docker
description: Découvrez les points clés de gestion d’un environnement de production basées sur le conteneur.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 02/15/2019
ms.openlocfilehash: f3cf9bc281e94f342cecb1083d886daba03c019d
ms.sourcegitcommit: bd28ff1e312eaba9718c4f7ea272c2d4781a7cac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "56836615"
---
# <a name="manage-production-docker-environments"></a>Gérer les environnements de production Docker

Gestion du cluster et l’orchestration est le processus de contrôle d’un groupe d’hôtes. Cela peut impliquer d’ajout et suppression d’ordinateurs hôtes à partir d’un cluster, l’obtention d’informations sur l’état actuel des hôtes et des conteneurs et de démarrage et arrêt des processus. Orchestration et la gestion du cluster sont étroitement liés à la planification, car le planificateur doit avoir accès à chaque hôte dans le cluster afin de planifier les services. Pour cette raison, le même outil est souvent utilisé pour les deux fonctions.

## <a name="container-service-and-management-tools"></a>Outils de gestion des services et du conteneur

Container Service assure le déploiement rapide de solutions de clustering et d’orchestration de conteneur open source populaire. Il utilise des images Docker pour vous assurer que vos conteneurs d’applications sont entièrement portables. À l’aide de Container Service, vous pouvez déployer (s’appuyant Mesosphere et Apache Mesos) DC/OS et Docker Swarm clusters à l’aide de modèles Azure Resource Manager ou le portail Azure pour vous assurer que vous pouvez faire évoluer ces applications à des milliers, même des dizaines de milliers, de conteneurs.

Vous déployez ces clusters à l’aide d’Azure Virtual Machine Scale Sets, et les clusters tirent parti des offres de mise en réseau et stockage Azure. Pour accéder au Service de conteneur, vous avez besoin d’un abonnement Azure. Avec Container Service, vous pouvez tirer parti des fonctionnalités de niveau entreprise d’Azure tout en conservant la portabilité des applications, notamment au niveau des couches d’orchestration.

Tableau 6-1 répertorie les outils de gestion courants liés à leurs orchestrateurs, planificateurs et de plateforme de clustering.

**Tableau 6-1**. Outils de gestion de docker

| Outils de gestion | Description | Orchestrateurs connexes |
|------------------|-------------|-----------------------|
| [Azure Monitor pour les conteneurs](https://docs.microsoft.com/azure/monitoring/monitoring-container-insights-overview) | Outil de gestion dédié Kubernetes Azure | Services de Azure Kubernetes (AKS) |
| [Interface utilisateur Web Kubernetes (tableau de bord)](https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/) | Outil de gestion de Kubernetes, peut surveiller et gérer des clusters Kubernetes local | Azure Kubernetes Service (AKS)<br/>Kubernetes local |
| [Portail Azure pour Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-creation-via-portal)<br/>[Azure Service Fabric Explorer](https://docs.microsoft.com/azure/service-fabric/service-fabric-visualizing-your-cluster) | Version en ligne et de bureau pour la gestion des clusters Service Fabric, sur Azure, sur site, de développement local et d’autres clouds | Azure Service Fabric |
| [Conteneur de surveillance (Analytique de journal)](https://docs.microsoft.com/azure/azure-monitor/insights/containers) | Conteneur général gestion y est solution de surveillance. Peut gérer des clusters Kubernetes via [Azure Monitor pour les conteneurs](https://docs.microsoft.com/azure/monitoring/monitoring-container-insights-overview). | Azure Service Fabric<br/>Azure Kubernetes Service (AKS)<br/>Mesosphere DC/OS et autres utilisateurs. |

## <a name="azure-service-fabric"></a>Azure Service Fabric

Un autre choix pour la gestion et de déploiement de cluster est Azure Service Fabric. [Service Fabric](https://azure.microsoft.com/services/service-fabric/) est une plateforme de microservices de Microsoft qui inclut l’orchestration de conteneur, ainsi que des développeurs programmation de modèles pour créer des applications de microservices hautement évolutif. Service Fabric prend en charge de Docker dans des conteneurs Linux et Windows et peuvent s’exécuter dans les serveurs Windows et Linux.

Voici les outils de gestion de Service Fabric :

- [Portail Azure pour Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-cluster-creation-via-portal) associés au cluster operations (création/mise à jour/suppression) un cluster ou de configurer son infrastructure (machines virtuelles, équilibrage de charge, la mise en réseau, etc.)

- [Azure Service Fabric Explorer](https://docs.microsoft.com/azure/service-fabric/service-fabric-visualizing-your-cluster) est spécialisé UI et outil de bureau multiplateforme qui fournit des insights et certaines opérations sur le cluster Service Fabric, à partir du point de vue de nœuds/machines virtuelles et à partir du point de vue application et les services web.

>[!div class="step-by-step"]
>[Précédent](run-microservices-based-applications-in-production.md)
>[Suivant](monitor-containerized-application-services.md)
