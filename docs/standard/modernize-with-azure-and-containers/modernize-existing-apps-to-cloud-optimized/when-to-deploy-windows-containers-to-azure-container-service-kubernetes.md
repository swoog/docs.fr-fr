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
# <a name="when-to-deploy-windows-containers-to-azure-container-service-that-is-kubernetes"></a><span data-ttu-id="d75b3-103">Moment de déployer des conteneurs Windows dans le Service de conteneur Azure (autrement dit, Kubernetes)</span><span class="sxs-lookup"><span data-stu-id="d75b3-103">When to deploy Windows Containers to Azure Container Service (that is, Kubernetes)</span></span>

<span data-ttu-id="d75b3-104">Service de conteneur Azure permet d’optimiser la configuration des outils open source populaires et technologies utilisées spécifiquement pour Azure.</span><span class="sxs-lookup"><span data-stu-id="d75b3-104">Azure Container Service optimizes the configuration of popular open-source tools and technologies specifically for Azure.</span></span> <span data-ttu-id="d75b3-105">Vous obtenez une solution ouverte qui offre la portabilité de vos conteneurs et lors de la configuration de votre application.</span><span class="sxs-lookup"><span data-stu-id="d75b3-105">You get an open solution that offers portability both for your containers and for your application configuration.</span></span> <span data-ttu-id="d75b3-106">Vous sélectionnez la taille, le nombre d’hôtes et les outils d’orchestrator.</span><span class="sxs-lookup"><span data-stu-id="d75b3-106">You select the size, the number of hosts, and the orchestrator tools.</span></span> <span data-ttu-id="d75b3-107">Service de conteneur Azure gère l’infrastructure pour vous.</span><span class="sxs-lookup"><span data-stu-id="d75b3-107">Azure Container Service handles the infrastructure for you.</span></span>

<span data-ttu-id="d75b3-108">Si vous utilisez déjà orchestrators open source comme Kubernetes, Docker Swarm ou contrôleur de domaine/système d’exploitation, vous n’avez pas besoin de modifier vos méthodes de gestion existant pour déplacer les charges de travail conteneur dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="d75b3-108">If you are already working with open-source orchestrators like Kubernetes, Docker Swarm, or DC/OS, you don't need to change your existing management practices to move container workloads to the cloud.</span></span> <span data-ttu-id="d75b3-109">Utilisez les outils de gestion d’application que vous êtes déjà familiarisé avec et se connecter via les points de terminaison API standards pour l’orchestrateur de votre choix.</span><span class="sxs-lookup"><span data-stu-id="d75b3-109">Use the application management tools that you're already familiar with and connect via the standard API endpoints for the orchestrator of your choice.</span></span>

<span data-ttu-id="d75b3-110">Tous ces orchestrators sont déjà rodées environnements Si vous utilisez des conteneurs Docker de Linux, mais il pouvez uniquement être dans un état d’aperçu pour les conteneurs Windows.</span><span class="sxs-lookup"><span data-stu-id="d75b3-110">All these orchestrators are mature environments if you are using Linux Docker containers, but might only be in Preview state for Windows Containers.</span></span>

<span data-ttu-id="d75b3-111">Par exemple, dans Kubernetes, prise en charge les conteneurs est natif (acteur), à l’aide de conteneurs Windows sur Kubernetes est également efficace (version préliminaire dans ACS à partir des premières 2018).</span><span class="sxs-lookup"><span data-stu-id="d75b3-111">For example, in Kubernetes, support for containers is native (first-class citizen), so using Windows Containers on Kubernetes is also effective (in preview in ACS as of early 2018).</span></span>

<span data-ttu-id="d75b3-112">Remarque importante : l’ont évolué et « PaaS plus » version des services ACS (Service de conteneur Azure) pour Kubernetes est AKS (Service de Kubernetes Azure), les conteneurs Windows sont toujours pas pris en charge à compter de Q2 2018, toutefois, il sera être bientôt pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d75b3-112">Important note: The evolved and “more PaaS” version of ACS (Azure Container Service) for Kubernetes is AKS (Azure Kubernetes Service), however, Windows Containers are still not supported as of Q2 2018, but it will be supported soon.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="d75b3-113">[Précédent](when-to-deploy-windows-containers-to-service-fabric.md)
[Suivant](choosing-azure-compute-options-for-container-based-applications.md)</span><span class="sxs-lookup"><span data-stu-id="d75b3-113">[Previous](when-to-deploy-windows-containers-to-service-fabric.md)
[Next](choosing-azure-compute-options-for-container-based-applications.md)</span></span>
