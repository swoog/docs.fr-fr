---
title: Moment de déployer des conteneurs Windows dans le Service de conteneur Azure (autrement dit, Kubernetes)
description: Moderniser des applications .NET existantes avec des conteneurs de Cloud Azure et Windows | Moment de déployer des conteneurs Windows dans le Service de conteneur Azure (autrement dit, Kubernetes)
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/30/2018
ms.openlocfilehash: b7f106e2b79a2c6bb24733debf7f4828505d66a6
ms.sourcegitcommit: 88f251b08bf0718ce119f3d7302f514b74895038
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2018
ms.locfileid: "33958169"
---
# <a name="when-to-deploy-windows-containers-to-azure-container-service-that-is-kubernetes"></a>Moment de déployer des conteneurs Windows dans le Service de conteneur Azure (autrement dit, Kubernetes)

Service de conteneur Azure permet d’optimiser la configuration des outils open source populaires et technologies utilisées spécifiquement pour Azure. Vous obtenez une solution ouverte qui offre la portabilité de vos conteneurs et lors de la configuration de votre application. Vous sélectionnez la taille, le nombre d’hôtes et les outils d’orchestrator. Service de conteneur Azure gère l’infrastructure pour vous.

Si vous utilisez déjà orchestrators open source comme Kubernetes, Docker Swarm ou contrôleur de domaine/système d’exploitation, vous n’avez pas besoin de modifier vos méthodes de gestion existant pour déplacer les charges de travail conteneur dans le cloud. Utilisez les outils de gestion d’application que vous êtes déjà familiarisé avec et se connecter via les points de terminaison API standards pour l’orchestrateur de votre choix.

Tous ces orchestrators sont déjà rodées environnements Si vous utilisez des conteneurs Docker de Linux, mais il pouvez uniquement être dans un état d’aperçu pour les conteneurs Windows.

Par exemple, dans Kubernetes, prise en charge les conteneurs est natif (acteur), à l’aide de conteneurs Windows sur Kubernetes est également efficace (version préliminaire dans ACS à partir des premières 2018).

Remarque importante : l’ont évolué et « PaaS plus » version des services ACS (Service de conteneur Azure) pour Kubernetes est AKS (Service de Kubernetes Azure), les conteneurs Windows sont toujours pas pris en charge à compter de Q2 2018, toutefois, il sera être bientôt pris en charge.

>[!div class="step-by-step"]
[Précédent](when-to-deploy-windows-containers-to-service-fabric.md)
[Suivant](choosing-azure-compute-options-for-container-based-applications.md)
