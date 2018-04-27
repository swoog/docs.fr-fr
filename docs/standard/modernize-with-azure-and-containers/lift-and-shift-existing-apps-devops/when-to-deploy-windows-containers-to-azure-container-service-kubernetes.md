---
title: Moment de déployer des conteneurs Windows dans le Service de conteneur Azure (autrement dit, Kubernetes)
description: Architecture de Microservices .NET pour les Applications .NET en conteneur | Moment de déployer des conteneurs Windows dans le Service de conteneur Azure (autrement dit, Kubernetes)
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/26/2017
ms.prod: .net
ms.topic: article
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: cccf78ef5b7683a2eefa3efab50a7bbe1bffda18
ms.sourcegitcommit: 2e8acae16ae802f2d6d04e3ce0a6dbf04e476513
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2018
---
# <a name="when-to-deploy-windows-containers-to-azure-container-service-that-is-kubernetes"></a>Moment de déployer des conteneurs Windows dans le Service de conteneur Azure (autrement dit, Kubernetes)

Service de conteneur Azure permet d’optimiser la configuration des outils open source populaires et technologies utilisées spécifiquement pour Azure. Vous obtenez une solution ouverte qui offre la portabilité de vos conteneurs et lors de la configuration de votre application. Vous sélectionnez la taille, le nombre d’hôtes et les outils d’orchestrator. Service de conteneur Azure gère l’infrastructure pour vous.

Si vous utilisez déjà orchestrators open source comme Kubernetes, Docker Swarm ou contrôleur de domaine/système d’exploitation, vous n’avez pas besoin de modifier vos méthodes de gestion existant pour déplacer les charges de travail conteneur dans le cloud. Utilisez les outils de gestion d’application que vous êtes déjà familiarisé avec et se connectez via les points de terminaison API standards pour l’orchestrateur de votre choix.

Tous ces orchestrators sont déjà rodées environnements Si vous utilisez des conteneurs Linux Docker, mais ils également prise en charge des conteneurs Windows comme de 2017 (certaines précédemment, d’autres plus récente, en fonction de l’orchestrateur).

Par exemple, dans Kubernetes, prise en charge les conteneurs est natif (acteur), à l’aide de conteneurs Windows sur Kubernetes est également très efficace et fiable (dans l’aperçu jusqu’au début se situent 2017).

>[!div class="step-by-step"]
[Précédent](when-to-deploy-windows-containers-to-service-fabric.md)
[Suivant](build-resilient-services-ready-for-the-cloud-embrace-transient-failures-in-the-cloud.md)
