---
title: Quand déployer des conteneurs Windows sur Service Fabric
description: Moderniser des applications .NET existantes avec des conteneurs de Cloud Azure et Windows | Quand déployer les conteneurs Windows sur Service Fabric
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/30/2018
ms.openlocfilehash: 01d76f325480c7cf09fef36b02589a602e3ee11e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61973658"
---
# <a name="when-to-deploy-windows-containers-to-service-fabric"></a>Quand déployer des conteneurs Windows sur Service Fabric

Les applications qui reposent sur les conteneurs Windows devront rapidement utiliser plateformes éloignez davantage de machines virtuelles IaaS. Il s’agit d’améliore l’évolutivité automatique et d’évolutivité élevée et pour obtenir des améliorations significatives dans une expérience de gestion complète pour les déploiements, mises à niveau, le contrôle de version, vous permettez ainsi l’intégrité. Vous pouvez atteindre ces objectifs avec l’orchestrateur Azure Service Fabric, disponible dans le cloud Microsoft Azure, mais également en local, ou même dans un autre cloud.

De nombreuses organisations sont soulever et déplacent des applications monolithiques existantes vers les conteneurs pour deux raisons :

- Réductions de coûts, soit en raison de la consolidation et la suppression de matériel existant, ou à partir de l’exécution des applications à une densité plus élevée.

- Un contrat d’un déploiement cohérent entre le développement et les opérations.

Poursuite de réductions de coûts est compréhensible, et il est probable que toutes les organisations sont repérage de cet objectif. Un déploiement cohérent est plus difficile à évaluer, mais il est tout aussi comme importantes. Un contrat d’un déploiement cohérent indique que les développeurs sont libres de choisir d’utiliser la technologie qui leur convient, et l’équipe d’exploitation Obtient un moyen simple pour déployer et gérer des applications. Le présent contrat inconfortable d’avoir des opérations de gérer la complexité de nombreuses technologies différentes, ou forcer les développeurs à travailler uniquement avec certaines technologies. En fait, chaque application est placée dans une image de déploiement autonome.

Certaines organisations continueront de modernisation en ajoutant des microservices (applications Cloud natives), mais de nombreuses autres organisations va s’arrêter ici (optimisé pour le Cloud des applications). Comme indiqué dans la Figure 4-8, ces organisations n’amène pas à des architectures de microservices, car ils ont ne peut-être pas besoin. Dans tous les cas, ils obtenez déjà les avantages qu’à l’aide de conteneurs ainsi que Service Fabric expérience fournit une gestion complète qui inclut le déploiement, met à niveau, le contrôle de version, restaurations et l’analyse du fonctionnement.

> ![Élever et déplacer une application de Service Fabric](./media/image8.png)
>
> **Figure 4-8.** Élever et déplacer une application de Service Fabric

Une approche clé de Service Fabric consiste à réutiliser le code existant et lift- and -shift. Par conséquent, vous pouvez migrer vos applications .NET Framework en cours, en utilisant des conteneurs de Windows et les déployer sur Service Fabric. Il sera plus facile de passer modernisation, finalement, en ajoutant de nouveaux microservices.

Lors de la comparaison de Service Fabric aux autres utilisateurs d’Orchestrator, il est important de souligner que le Service Fabric est mature à l’exécution des services et applications basées sur Windows. Service Fabric a été exécuté services basés sur Windows et des applications, y compris les produits de niveau 1, critiques de Microsoft depuis des années. Il a été le premier orchestrator à disponibilité générale pour les conteneurs Windows. D’autres conteneurs, tels que Kubernetes, DC/OS et Docker Swarm, sont plus matures dans Linux, mais moins reconnue que les conteneurs Windows et des applications Service Fabric pour Windows.

L’objectif ultime de Service Fabric consiste à réduire la complexité de la création d’applications à l’aide d’une approche de microservices. Vous souhaitez par la suite une microservices pour certains types d’applications afin d’éviter de coûteux repenser le modèle. Vous pouvez commencer à petite échelle, mettre à l’échelle si nécessaire, Déconseillez les services inutiles, ajouter de nouveaux services et faire évoluer votre application avec l’utilisation par le client. Il existe de nombreux autres problèmes qui ne sont pas encore être résolus pour que les microservices plus abordables pour la plupart des développeurs. Si vous actuellement sont simplement soulever et le décalage d’une application avec les conteneurs Windows, mais vous vous focalisez sur l’ajout de microservices basées sur les conteneurs à l’avenir, qui est la zone de confort de Service Fabric.

>[!div class="step-by-step"]
>[Précédent](when-to-deploy-windows-containers-to-azure-vms-iaas-cloud.md)
>[Suivant](when-to-deploy-windows-containers-to-azure-container-service-kubernetes.md)