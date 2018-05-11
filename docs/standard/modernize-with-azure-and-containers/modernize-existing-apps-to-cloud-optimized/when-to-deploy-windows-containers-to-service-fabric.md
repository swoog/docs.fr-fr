---
title: Moment de déployer des conteneurs Windows à Service Fabric
description: Moderniser des applications .NET existantes avec des conteneurs de Cloud Azure et Windows | Moment de déployer des conteneurs Windows à Service Fabric
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/30/2018
ms.openlocfilehash: c41db8b37c883f9369a6b8d1f8bccbc0535f504c
ms.sourcegitcommit: 88f251b08bf0718ce119f3d7302f514b74895038
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2018
---
# <a name="when-to-deploy-windows-containers-to-service-fabric"></a>Moment de déployer des conteneurs Windows à Service Fabric

Les applications qui reposent sur les conteneurs Windows devront rapidement utilisent des plateformes éloignez davantage de machines virtuelles IaaS. C’est pour une plus grande évolutivité automatisée et une haute évolutivité, et pour obtenir des améliorations significatives dans une expérience de gestion complète pour les déploiements, mises à niveau, le contrôle de version, de restauration et de contrôle d’intégrité. Vous pouvez atteindre ces objectifs avec l’orchestrateur Azure Service Fabric, disponible dans le cloud Microsoft Azure, mais également sur site, ou même dans un autre cloud.

De nombreuses organisations sont délibéré et décalage existantes applications monolithiques aux conteneurs pour deux raisons :

-   Réduction des coûts, soit en raison de la consolidation et la suppression du matériel existant, ou d’exécuter des applications à une densité plus élevée.

-   Un contrat d’un déploiement cohérent entre le développement et les opérations.

Poursuite des réductions de coûts est compréhensible, et il est probable que toutes les organisations sont du repérage de cet objectif. Un déploiement cohérent est plus difficile à évaluer, mais il est tout aussi comme importantes. Un contrat de déploiement cohérent indique que les développeurs sont libres de choisir d’utiliser la technologie qui correspond le mieux à leur, et l’équipe d’exploitation Obtient un moyen simple pour déployer et gérer des applications. Ce contrat réduit le travail des opérations gérer la complexité des différentes technologies d’obliger les développeurs à fonctionnent uniquement avec certaines technologies. Essentiellement, chaque application est placées dans des conteneurs dans une image de déploiement autonome.

Certaines organisations continuent de rénovation en ajoutant des microservices (applications Cloud en mode natif), mais de nombreuses autres organisations va s’arrêter ici (applications optimisée pour le Cloud). Comme indiqué dans la Figure 4-8, ces organisations n’amène pas à des architectures de microservices, car il sont inutile de. Dans tous les cas, ils obtiennent déjà les avantages qu’à l’aide de conteneurs ainsi que l’infrastructure de Service expérience fournit une gestion complète qui inclut le déploiement, la mise à niveau, le contrôle de version, restaurations et contrôle d’intégrité.

> ![Déplacer une application de Service Fabric](./media/image8.png)
>
> **Figure 4-8.** Déplacer une application de Service Fabric

Une approche clée pour l’infrastructure de Service consiste à réutiliser le code existant et de courbes d’élévation et MAJ. Par conséquent, vous pouvez migrer vos applications .NET Framework en cours, à l’aide de conteneurs Windows et les déployer sur l’infrastructure de Service. Il sera plus facile de passer rénovation, par la suite, en ajoutant de nouvelles microservices.

Lors de la comparaison de l’infrastructure de Service pour les autres orchestrators, il est important de souligner que le Service Fabric est mature au niveau de l’exécution des services et des applications Windows. L’infrastructure de service d’exécution des services Windows et les applications, y compris les produits de niveau 1, critiques de Microsoft pour les années. Il a été le premier orchestrator pour que la disponibilité générale pour les conteneurs Windows. D’autres conteneurs, tels que Kubernetes, contrôleur de domaine/système d’exploitation et Docker Swarm, sont plus matures dans Linux, mais moins abouti à Service Fabric pour des applications Windows et les conteneurs Windows.

L’objectif ultime de l’infrastructure de Service est de réduire la complexité de la création d’applications à l’aide d’une approche de microservices. Vous souhaitez par la suite un microservices pour certains types d’applications afin d’éviter de repenser coûteux. Vous pouvez commencer petit, à l’échelle lorsque nécessaire, déconseiller des services, ajouter de nouveaux services et faire évoluer votre application avec l’utilisation par le client. Il existe de nombreux autres problèmes qui ne sont pas encore être résolus pour que microservices plus abordable pour la plupart des développeurs. Si vous sont actuellement simplement délibéré et un décalage d’une application avec des conteneurs Windows, mais vous songez sur l’ajout de microservices basée sur les conteneurs dans le futur, qui est la solution idéale Service Fabric.

>[!div class="step-by-step"]
[Précédent](when-to-deploy-windows-containers-to-azure-vms-iaas-cloud.md)
[Suivant](when-to-deploy-windows-containers-to-azure-container-service-kubernetes.md)
