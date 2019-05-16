---
title: Choix des plateformes de calcul Azure pour les applications basées sur des conteneurs
description: Moderniser des applications .NET existantes avec des conteneurs de Cloud Azure et Windows | Choisir des plates-formes de calcul Azure pour les applications en conteneur
ms.date: 05/04/2018
ms.openlocfilehash: 28e103c67f47d63582384c9ab468a5f631b5ce9e
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65638977"
---
# <a name="choosing-azure-compute-platforms-for-container-based-applications"></a><span data-ttu-id="ba614-103">Choix des plateformes de calcul Azure pour les applications basées sur des conteneurs</span><span class="sxs-lookup"><span data-stu-id="ba614-103">Choosing Azure compute platforms for container-based applications</span></span>

<span data-ttu-id="ba614-104">Comme vous l’avez remarqué après avoir lu les sections précédentes, Azure est un cloud ouverte qui offre plusieurs choix.</span><span class="sxs-lookup"><span data-stu-id="ba614-104">As you have noticed after reading the previous sections, Azure is an open cloud that offers multiple choices.</span></span> <span data-ttu-id="ba614-105">Vous pouvez utiliser la mieux adaptée à vos besoins, toutefois, il met également en évidence questions sur les produits et technologies que vous devez utiliser pour vos applications en conteneur.</span><span class="sxs-lookup"><span data-stu-id="ba614-105">You can use the best fit for your needs, however, it also surfaces questions about what product/technology you should use for your containerized applications.</span></span>

<span data-ttu-id="ba614-106">Comme un *par défaut* recommandation, ce qui suit est le principal critère recommandé dans ce guide :</span><span class="sxs-lookup"><span data-stu-id="ba614-106">As a *by-default* recommendation, the following is the main criteria recommended in this guidance:</span></span>

- <span data-ttu-id="ba614-107">**Application monolithique unique :** Choisissez Azure App Service</span><span class="sxs-lookup"><span data-stu-id="ba614-107">**Single monolithic app:** Choose Azure App Service</span></span>
- <span data-ttu-id="ba614-108">**Application multiniveau :** Choisissez des orchestrateurs tels que App Service, Service Fabric (SF) ou Azure Kubernetes Service (AKS) si vous avez un seul ou plusieurs services back-end</span><span class="sxs-lookup"><span data-stu-id="ba614-108">**N-Tier app:** Choose orchestrators such as Azure Kubernetes Service (AKS), Service Fabric (SF) or App Service if you have a single or few back-end services</span></span>
- <span data-ttu-id="ba614-109">**Microservices de Linux :** Choisissez AKS/Kubernetes</span><span class="sxs-lookup"><span data-stu-id="ba614-109">**Linux microservices:** Choose AKS/Kubernetes</span></span>
- <span data-ttu-id="ba614-110">**Microservices de Windows :** Choisissez Service Fabric</span><span class="sxs-lookup"><span data-stu-id="ba614-110">**Windows microservices:** Choose Service Fabric</span></span>
- <span data-ttu-id="ba614-111">**& Gestionnaires d’événements de fonctions sans serveur :** Choisissez Azure Functions</span><span class="sxs-lookup"><span data-stu-id="ba614-111">**Serverless functions & event handlers:** Choose Azure Functions</span></span>
- <span data-ttu-id="ba614-112">**Lots à grande échelle :** Choisissez Azure Batch</span><span class="sxs-lookup"><span data-stu-id="ba614-112">**Large-scale Batch:** Choose Azure Batch</span></span>

<span data-ttu-id="ba614-113">Toutefois, cette recommandation à entreprendre avec une pincée de salt, comme la sélection du produit varie selon les besoins spécifiques de votre application et de caractéristiques.</span><span class="sxs-lookup"><span data-stu-id="ba614-113">However, this recommendation should be taken with a pinch of salt, as the product’s selection will depend on your specific application’s needs and characteristics.</span></span> <span data-ttu-id="ba614-114">Pas toutes les applications sont les mêmes, même lorsque initialement, il peut présenter des types similaires.</span><span class="sxs-lookup"><span data-stu-id="ba614-114">Not all applications are the same even when initially they might look similar types.</span></span>

<span data-ttu-id="ba614-115">Après une analyse plus approfondie des besoins de l’application, le produit sélectionné peut être différent.</span><span class="sxs-lookup"><span data-stu-id="ba614-115">After a deeper analysis of the application’s needs, the product selected could be different.</span></span> <span data-ttu-id="ba614-116">Mais, en tant que point de départ, il est judicieux d’avoir des recommandations initiales relatives à partir d’où vous pouvez commencer à évaluer et de test en fonction de certaine priorité.</span><span class="sxs-lookup"><span data-stu-id="ba614-116">But, as a starting point, it is good to have initial guidance from where you can start evaluating and testing based on certain priority.</span></span>

<span data-ttu-id="ba614-117">Dans la figure suivante, vous pouvez analyser plus global lors de la table de prise de décision détaillé.</span><span class="sxs-lookup"><span data-stu-id="ba614-117">In the next figure, you can analyze a more global while detailed decision table.</span></span>

![](./media/image8.5.png)

<span data-ttu-id="ba614-118">Notez comment la sous-jacente du système d’exploitation (Windows Visual Studio. Linux) peut également être un facteur de décision que certains orchestrateurs sont plus mature sur des conteneurs Linux et d’autres sur les conteneurs Windows.</span><span class="sxs-lookup"><span data-stu-id="ba614-118">Notice how the underlying OS (Windows vs. Linux) can also be a decision factor as some orchestrators are more mature on Linux containers and other on Windows containers.</span></span> <span data-ttu-id="ba614-119">Par exemple, les conteneurs Linux sont parvenues à maturité dans Kubernetes (AKS dans Azure), mais moins reconnue sur Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="ba614-119">For instance, Linux containers are very mature in Kubernetes (AKS in Azure) but less mature on Service Fabric.</span></span> <span data-ttu-id="ba614-120">En revanche, les conteneurs Windows sont plus mature dans Service Fabric (publiée en mai 2017) et moins reconnue dans ACS.</span><span class="sxs-lookup"><span data-stu-id="ba614-120">On the other hand, Windows Containers are more mature in Service Fabric (released in May 2017) and less mature in AKS.</span></span>

<span data-ttu-id="ba614-121">Cependant, ces différences de maturité de système d’exploitation seront estompe à l’avenir, plusieurs plateformes auront comparable maturité du système d’exploitation et la décision sera mise en page plus sur les préférences en fonction des fonctionnalités spécifiques, votre application peut avoir besoin, ou en fonction de l’écosystème de chaque plateforme raisons.</span><span class="sxs-lookup"><span data-stu-id="ba614-121">However, those differences in OS maturity will fade in the future and multiple platforms will have comparable OS maturity and the decision will lay more on preferences based on specific features your application might need or based on each platform's ecosystem reasons.</span></span>

> [!div class="step-by-step"]
> <span data-ttu-id="ba614-122">[Précédent](when-to-deploy-windows-containers-to-azure-container-service-kubernetes.md)
> [Suivant](build-resilient-services-ready-for-the-cloud-embrace-transient-failures-in-the-cloud.md)</span><span class="sxs-lookup"><span data-stu-id="ba614-122">[Previous](when-to-deploy-windows-containers-to-azure-container-service-kubernetes.md)
[Next](build-resilient-services-ready-for-the-cloud-embrace-transient-failures-in-the-cloud.md)</span></span>
