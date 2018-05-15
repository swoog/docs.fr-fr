---
title: Choisir des plates-formes de calcul Azure pour les applications conteneur
description: Moderniser des applications .NET existantes avec des conteneurs de Cloud Azure et Windows | Choisir des plates-formes de calcul Azure pour les applications conteneur
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/04/2018
ms.openlocfilehash: ebf022a52aaaf95ae335976f5e097921b0ac8006
ms.sourcegitcommit: 88f251b08bf0718ce119f3d7302f514b74895038
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2018
---
# <a name="choosing-azure-compute-platforms-for-container-based-applications"></a><span data-ttu-id="fb7a6-103">Choisir des plates-formes de calcul Azure pour les applications conteneur</span><span class="sxs-lookup"><span data-stu-id="fb7a6-103">Choosing Azure compute platforms for container-based applications</span></span>

<span data-ttu-id="fb7a6-104">Comme vous l’avez remarqué après avoir lu les sections précédentes, Azure est un cloud ouvert qui offre plusieurs choix.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-104">As you have noticed after reading the previous sections, Azure is an open cloud that offers multiple choices.</span></span> <span data-ttu-id="fb7a6-105">Vous pouvez utiliser le mieux à vos besoins, toutefois, il met également en évidence les questions sur les produits et technologies que vous devez utiliser pour vos applications en conteneur.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-105">You can use the best fit for your needs, however, it also surfaces questions about what product/technology you should use for your containerized applications.</span></span>

<span data-ttu-id="fb7a6-106">Comme un *par défaut* recommandation, ce qui suit est le principal critère recommandé dans ce guide :</span><span class="sxs-lookup"><span data-stu-id="fb7a6-106">As a *by-default* recommendation, the following is the main criteria recommended in this guidance:</span></span>

  - <span data-ttu-id="fb7a6-107">**Application monolithique unique :** choisissez Azure App Service</span><span class="sxs-lookup"><span data-stu-id="fb7a6-107">**Single monolithic app:** Choose Azure App Service</span></span>
  - <span data-ttu-id="fb7a6-108">**Les applications multicouches :** choisissez orchestrators comme Azure Kubernetes Service (AKS), l’infrastructure de Service (DF) ou du Service d’applications si vous avez un seul ou plusieurs services principaux</span><span class="sxs-lookup"><span data-stu-id="fb7a6-108">**N-Tier app:** Choose orchestrators such as Azure Kubernetes Service (AKS), Service Fabric (SF) or App Service if you have a single or few back-end services</span></span>
  - <span data-ttu-id="fb7a6-109">**Linux microservices :** AKS/Kubernetes choisissez</span><span class="sxs-lookup"><span data-stu-id="fb7a6-109">**Linux microservices:** Choose AKS/Kubernetes</span></span>
  - <span data-ttu-id="fb7a6-110">**Windows microservices :** choisissez Service Fabric</span><span class="sxs-lookup"><span data-stu-id="fb7a6-110">**Windows microservices:** Choose Service Fabric</span></span>
  - <span data-ttu-id="fb7a6-111">**Les fonctions sans serveur et les gestionnaires d’événements :** choisir les fonctions de Azure</span><span class="sxs-lookup"><span data-stu-id="fb7a6-111">**Serverless functions & event handlers:** Choose Azure Functions</span></span>
  - <span data-ttu-id="fb7a6-112">**Les lots à grande échelle :** choisissez Azure par lot</span><span class="sxs-lookup"><span data-stu-id="fb7a6-112">**Large-scale Batch:** Choose Azure Batch</span></span>

<span data-ttu-id="fb7a6-113">Toutefois, cette recommandation convient avec un pincement de salt, comme la sélection du produit varient selon les caractéristiques et les besoins spécifiques de votre application.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-113">However, this recommendation should be taken with a pinch of salt, as the product’s selection will depend on your specific application’s needs and characteristics.</span></span> <span data-ttu-id="fb7a6-114">Toutes les applications ne sont identiques, même lorsque initialement, il peut présenter des types semblables.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-114">Not all applications are the same even when initially they might look similar types.</span></span>

<span data-ttu-id="fb7a6-115">Après une analyse plus approfondie des besoins de l’application, le produit sélectionné peut être différent.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-115">After a deeper analysis of the application’s needs, the product selected could be different.</span></span> <span data-ttu-id="fb7a6-116">Mais, comme point de départ, il est recommandé d’avoir des recommandations initiales d’où vous pouvez commencer à évaluer et de test en fonction de certaine priorité.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-116">But, as a starting point, it is good to have initial guidance from where you can start evaluating and testing based on certain priority.</span></span>

<span data-ttu-id="fb7a6-117">Dans la figure suivante, vous pouvez analyser plus global lors de la table de décision détaillé.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-117">In the next figure, you can analyze a more global while detailed decision table.</span></span>

![](./media/image8.5.png)

<span data-ttu-id="fb7a6-118">Notez comment le sous-jacente du système d’exploitation (Windows Visual Studio. Linux) peut également être un facteur de décision que certains orchestrators sont plus matures sur les conteneurs Linux et d’autres sur les conteneurs Windows.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-118">Notice how the underlying OS (Windows vs. Linux) can also be a decision factor as some orchestrators are more mature on Linux containers and other on Windows containers.</span></span> <span data-ttu-id="fb7a6-119">Par exemple, les conteneurs Linux sont très matures dans Kubernetes (AKS dans Azure), mais moins abouti sur le Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-119">For instance, Linux containers are very mature in Kubernetes (AKS in Azure) but less mature on Service Fabric.</span></span> <span data-ttu-id="fb7a6-120">En revanche, les conteneurs Windows sont plus matures dans Service Fabric (publiée en mai 2017) et moins mature dans AKS.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-120">On the other hand, Windows Containers are more mature in Service Fabric (released in May 2017) and less mature in AKS.</span></span>

<span data-ttu-id="fb7a6-121">Cependant, ces différences de maturité de système d’exploitation seront fondu à l’avenir, plusieurs plateformes aura comparable au niveau de maturité de système d’exploitation et la décision dispose de plus d’informations sur les préférences en fonction des fonctionnalités spécifiques, votre application peut avoir besoin, ou en fonction de l’écosystème de chaque plate-forme raisons.</span><span class="sxs-lookup"><span data-stu-id="fb7a6-121">However, those differences in OS maturity will fade in the future and multiple platforms will have comparable OS maturity and the decision will lay more on preferences based on specific features your application might need or based on each platform's ecosystem reasons.</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="fb7a6-122">[Précédent](when-to-deploy-windows-containers-to-azure-container-service-kubernetes.md)
[Suivant](build-resilient-services-ready-for-the-cloud-embrace-transient-failures-in-the-cloud.md)</span><span class="sxs-lookup"><span data-stu-id="fb7a6-122">[Previous](when-to-deploy-windows-containers-to-azure-container-service-kubernetes.md)
[Next](build-resilient-services-ready-for-the-cloud-embrace-transient-failures-in-the-cloud.md)</span></span>
