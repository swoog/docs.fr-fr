---
title: Moment de déployer des conteneurs Windows à Azure conteneur Instances (ACI)
description: Moderniser des applications .NET existantes avec des conteneurs de Cloud Azure et Windows | Moment de déployer des conteneurs Windows à Azure conteneur Instances (ACI)
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/29/2018
ms.openlocfilehash: 3dc23c96543d9611763b571105f52b150dfec06f
ms.sourcegitcommit: 88f251b08bf0718ce119f3d7302f514b74895038
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2018
ms.locfileid: "33957949"
---
# <a name="when-to-deploy-windows-containers-to-azure-container-instances-aci"></a><span data-ttu-id="0d6be-103">Moment de déployer des conteneurs Windows à Azure conteneur Instances (ACI)</span><span class="sxs-lookup"><span data-stu-id="0d6be-103">When to deploy Windows Containers to Azure Container Instances (ACI)</span></span>

<span data-ttu-id="0d6be-104">Les Instances du conteneur Azure proposition de valeur principale est que vous pouvez immédiatement déployer des conteneurs à celui-ci et que vous n’avez pas besoin de mettre à jour cet environnement, vous n’avez pas besoin/mise à niveau de correctif du système d’exploitation sous-jacent ou les machines virtuelles, tout ce qui est transparente et que vous venez de déployer conteneurs dans un environnement de prêt à l’emploi.</span><span class="sxs-lookup"><span data-stu-id="0d6be-104">Azure Container Instances main value proposition is that you can right away deploy containers to it and you don’t need to maintain that environment, you don’t need to upgrade/patch the underlaying operating system or VMs, all that is transparent and you just deploy containers into a ready-to-use environment.</span></span>

<span data-ttu-id="0d6be-105">Les raisons et les scénarios lorsque vous ne souhaitez pas utiliser ACI sont similaires pour les principaux scénarios lorsque vous utilisez les machines virtuelles Azure avec des conteneurs, donc en fait, les principaux scénarios pour l’utilisation d’Instances de conteneurs Azure sont :</span><span class="sxs-lookup"><span data-stu-id="0d6be-105">The reasons and scenarios when you would want to use ACI are similar to the main scenarios when you use Azure VMs with containers, so basically, the main scenarios for using Azure Container Instances are:</span></span>

-   <span data-ttu-id="0d6be-106">**Scénarios de développement/Test**</span><span class="sxs-lookup"><span data-stu-id="0d6be-106">**Dev/Test scenarios**</span></span>
-   <span data-ttu-id="0d6be-107">**Automatisation des tâches**</span><span class="sxs-lookup"><span data-stu-id="0d6be-107">**Task automation**</span></span>
-   <span data-ttu-id="0d6be-108">**Agents de l’élément de configuration/CD**</span><span class="sxs-lookup"><span data-stu-id="0d6be-108">**CI/CD agents**</span></span>
-   <span data-ttu-id="0d6be-109">**Traitement par lots de petite/mise à l’échelle**</span><span class="sxs-lookup"><span data-stu-id="0d6be-109">**Small/scale batch processing**</span></span>
-   <span data-ttu-id="0d6be-110">**Applications web simples**</span><span class="sxs-lookup"><span data-stu-id="0d6be-110">**Simple web apps**</span></span>

<span data-ttu-id="0d6be-111">Le scénario d’applications web simple est un scénario juste ACI mais tiennent compte que depuis dans ACI vous ne pouvez avoir qu’une instance de conteneur unique par l’image de conteneur, vous n’avez pas une haute disponibilité et avez uniquement une évolutivité limitée.</span><span class="sxs-lookup"><span data-stu-id="0d6be-111">The simple web apps scenario is a fair scenario for ACI but take into account that since in ACI you can only have a single container instance per container image, you won’t have high availability and only have limited scalability.</span></span>

<span data-ttu-id="0d6be-112">Toutefois, même lorsque ACI est considérée comme l’infrastructure, car il fournit simplement des instances d’un conteneur unique, il est un énorme avantage par rapport à des machines virtuelles Azure régulières avec Windows Server.</span><span class="sxs-lookup"><span data-stu-id="0d6be-112">However, even when ACI is considered infrastructure because it just provides single container instances, there is a huge benefit compared to regular Azure VMs with Windows Server.</span></span> <span data-ttu-id="0d6be-113">Avec ACI, vous déployez uniquement les conteneurs dans un environnement autonome, et vous payez uniquement pour ces conteneurs.</span><span class="sxs-lookup"><span data-stu-id="0d6be-113">With ACI, you just deploy the containers into a self-maintained environment and you just pay for those containers.</span></span> <span data-ttu-id="0d6be-114">Vous n’avez pas besoin de mettre à jour/mise à jour/patch machines virtuelles, afin qu’il soit une meilleure plateforme pour la plupart des scénarios où vous utilisez peut-être machines virtuelles avec des conteneurs.</span><span class="sxs-lookup"><span data-stu-id="0d6be-114">You don’t need to maintain/update/patch VMs, so it is a much better platform for most scenarios where you might be using VMs with containers.</span></span> <span data-ttu-id="0d6be-115">À l’aide de ACI est simple, vous déployez uniquement un conteneur, il est inutile de créer un environnement de machine virtuelle que vous déployez uniquement les conteneurs.</span><span class="sxs-lookup"><span data-stu-id="0d6be-115">Using ACI is straight forward, you just deploy a container, there’s no need to create a VM environment you just deploy containers.</span></span>

<span data-ttu-id="0d6be-116">Les principaux avantages des Instances de conteneur Azure (ACI) sont :</span><span class="sxs-lookup"><span data-stu-id="0d6be-116">The main benefits of Azure Container Instances (ACI) are:</span></span>

-   <span data-ttu-id="0d6be-117">Exécuter les conteneurs sans la gestion des serveurs</span><span class="sxs-lookup"><span data-stu-id="0d6be-117">Run containers without managing servers</span></span>
-   <span data-ttu-id="0d6be-118">Augmenter la réactivité des conteneurs à la demande</span><span class="sxs-lookup"><span data-stu-id="0d6be-118">Increase agility with containers on demand</span></span>
-   <span data-ttu-id="0d6be-119">Déployer des conteneurs dans le cloud de vitesse et de simplicité sans précédent, avec une seule commande.</span><span class="sxs-lookup"><span data-stu-id="0d6be-119">Deploy containers to the cloud with unprecedented simplicity and speed—with a single command.</span></span> 
-   <span data-ttu-id="0d6be-120">Applications sécurisées avec l’isolation de l’hyperviseur</span><span class="sxs-lookup"><span data-stu-id="0d6be-120">Secure applications with hypervisor isolation</span></span>

<span data-ttu-id="0d6be-121">En résumé, vous pouvez développer des applications avec ACI rapide sans gestion des ordinateurs virtuels ou de devoir apprendre de nouveaux outils.</span><span class="sxs-lookup"><span data-stu-id="0d6be-121">In short, with ACI you can develop apps fast without managing virtual machines or having to learn new tools.</span></span> <span data-ttu-id="0d6be-122">Il s’agit simplement votre application dans un conteneur, en cours d’exécution dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="0d6be-122">It's just your application, in a container, running in the cloud.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="0d6be-123">[Précédent](when-to-deploy-windows-containers-to-azure-vms-iaas-cloud.md)
[Suivant](when-to-deploy-windows-containers-to-service-fabric.md)</span><span class="sxs-lookup"><span data-stu-id="0d6be-123">[Previous](when-to-deploy-windows-containers-to-azure-vms-iaas-cloud.md)
[Next](when-to-deploy-windows-containers-to-service-fabric.md)</span></span>
