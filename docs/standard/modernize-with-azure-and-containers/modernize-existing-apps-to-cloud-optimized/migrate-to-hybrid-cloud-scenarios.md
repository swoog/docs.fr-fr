---
title: Scénarios de migration vers le cloud hybride
description: Moderniser des applications .NET existantes avec des conteneurs de Cloud Azure et Windows | Migrer vers les scénarios de cloud hybride
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/30/2018
ms.openlocfilehash: b04c6edecf5b63f191cb2e0f808fb1d0f801d0a3
ms.sourcegitcommit: 438919211260bb415fc8f96ca3eabc33cf2d681d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2019
ms.locfileid: "59612574"
---
# <a name="migrate-to-hybrid-cloud-scenarios"></a><span data-ttu-id="3ef9c-103">Scénarios de migration vers le cloud hybride</span><span class="sxs-lookup"><span data-stu-id="3ef9c-103">Migrate to hybrid cloud scenarios</span></span>

<span data-ttu-id="3ef9c-104">Certaines organisations et les entreprises ne peuvent pas migrer certaines de leurs applications à des clouds publics comme Microsoft Azure ou n’importe quel autre cloud public en raison des réglementations ou leurs propres stratégies.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-104">Some organizations and enterprises can't migrate some of their applications to public clouds like Microsoft Azure or any other public cloud due to regulations or their own policies.</span></span> <span data-ttu-id="3ef9c-105">Toutefois, il est probable que n’importe quelle organisation peut bénéficier d’avoir certaines de leurs applications dans le cloud public et d’autres applications en local.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-105">However, it's likely that any organization might benefit from having some of their applications in the public cloud and other applications on-premises.</span></span> <span data-ttu-id="3ef9c-106">Mais un environnement mixte peut conduire à l’excès de complexité dans les environnements en raison des différentes plateformes et technologies utilisées dans des clouds publics et les environnements locaux.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-106">But a mixed environment can lead to excessive complexity in environments due to different platforms and technologies used in public clouds versus on-premises environments.</span></span>

<span data-ttu-id="3ef9c-107">Microsoft fournit la meilleure solution de cloud hybride, un dans lequel vous pouvez optimiser vos actifs existants en local et dans le cloud public, alors que vous garantir la cohérence dans un cloud hybride Azure.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-107">Microsoft provides the best hybrid cloud solution, one in which you can optimize your existing assets on-premises and in the public cloud, while you ensure consistency in an Azure hybrid cloud.</span></span> <span data-ttu-id="3ef9c-108">Vous pouvez optimiser les compétences et bénéficiez d’une approche flexible et unifiée pour la création d’applications pouvant s’exécuter dans le cloud ou sur site, grâce à Azure Stack (local) et Azure (cloud public).</span><span class="sxs-lookup"><span data-stu-id="3ef9c-108">You can maximize existing skills, and get a flexible, unified approach to building apps that can run in the cloud or on-premises, thanks to Azure Stack (on-premises) and Azure (public cloud).</span></span>

<span data-ttu-id="3ef9c-109">Lorsqu’il s’agit à la sécurité, vous pouvez centraliser la gestion et la sécurité dans votre cloud hybride.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-109">When it comes to security, you can centralize management and security across your hybrid cloud.</span></span> <span data-ttu-id="3ef9c-110">Vous pouvez obtenir un contrôle sur toutes les ressources, à partir de votre centre de données dans le cloud, en fournissant l’authentification unique au niveau local et les applications cloud.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-110">You can get control over all assets, from your datacenter to the cloud, by providing single sign-on to on-premises and cloud apps.</span></span> <span data-ttu-id="3ef9c-111">Vous y parvenir en étendant Active Directory à un cloud hybride et à l’aide de la gestion des identités.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-111">You accomplish this by extending Active Directory to a hybrid cloud, and by using identity management.</span></span>

<span data-ttu-id="3ef9c-112">Enfin, vous pouvez distribuer analyser les données en toute transparence, utiliser les mêmes langages de requête pour les ressources cloud et locales et s’appliquent aux analytique et l’apprentissage profond dans Azure pour enrichir vos données, quelle que soit sa source.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-112">Finally, you can distribute and analyze data seamlessly, use the same query languages for cloud and on-premises assets, and apply analytics and deep learning in Azure to enrich your data, regardless of its source.</span></span>

## <a name="azure-stack"></a><span data-ttu-id="3ef9c-113">Azure Stack</span><span class="sxs-lookup"><span data-stu-id="3ef9c-113">Azure Stack</span></span>

<span data-ttu-id="3ef9c-114">Azure Stack est une plateforme de cloud hybride qui vous permet de fournir des services Azure à partir du centre de données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-114">Azure Stack is a hybrid cloud platform that lets you deliver Azure services from your organization's datacenter.</span></span> <span data-ttu-id="3ef9c-115">Azure Stack est conçu pour prendre en charge de nouvelles options pour vos applications modernes dans des scénarios clés, telles qu’edge et les environnements non connectés ou les exigences de sécurité et de conformité spécifiques de réunion.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-115">Azure Stack is designed to support new options for your modern applications in key scenarios, like edge and unconnected environments, or meeting specific security and compliance requirements.</span></span>

<span data-ttu-id="3ef9c-116">Figure 4-13 montre une vue d’ensemble de la plateforme de cloud hybride true proposées par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-116">Figure 4-13 shows an overview of the true hybrid cloud platform that Microsoft offers.</span></span>

![Plateforme de cloud hybride de Microsoft avec Azure Stack et Azure](./media/image13.jpg)

> <span data-ttu-id="3ef9c-118">**Figure 4-13.**</span><span class="sxs-lookup"><span data-stu-id="3ef9c-118">**Figure 4-13.**</span></span> <span data-ttu-id="3ef9c-119">Plateforme de cloud hybride de Microsoft avec Azure Stack et Azure</span><span class="sxs-lookup"><span data-stu-id="3ef9c-119">Microsoft hybrid cloud platform with Azure Stack and Azure</span></span>

<span data-ttu-id="3ef9c-120">Azure Stack est proposé en deux options de déploiement, à vos besoins :</span><span class="sxs-lookup"><span data-stu-id="3ef9c-120">Azure Stack is offered in two deployment options, to meet your needs:</span></span>

-   <span data-ttu-id="3ef9c-121">Systèmes intégrés Azure Stack</span><span class="sxs-lookup"><span data-stu-id="3ef9c-121">Azure Stack integrated systems</span></span>

-   <span data-ttu-id="3ef9c-122">Kit de développement Azure Stack</span><span class="sxs-lookup"><span data-stu-id="3ef9c-122">Azure Stack Development Kit</span></span>

### <a name="azure-stack-integrated-systems"></a><span data-ttu-id="3ef9c-123">Systèmes intégrés Azure Stack</span><span class="sxs-lookup"><span data-stu-id="3ef9c-123">Azure Stack integrated systems</span></span>

<span data-ttu-id="3ef9c-124">Systèmes intégrés Azure Stack sont proposées grâce à un partenariat de partenaires matériels et de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-124">Azure Stack integrated systems are offered through a partnership of Microsoft and hardware partners.</span></span> <span data-ttu-id="3ef9c-125">Le partenariat crée une solution qui offre l’innovation cloud-à un rythme qui est équilibrée et simplicité de gestion.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-125">The partnership creates a solution that offers cloud-paced innovation that is balanced with simplicity in management.</span></span> <span data-ttu-id="3ef9c-126">Car Azure Stack est proposé comme un système intégré de matériels et logiciels, vous obtenez la quantité exacte de flexibilité et de contrôle, tout en adoptant toujours l’innovation à partir du cloud.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-126">Because Azure Stack is offered as an integrated system of hardware and software, you get the right amount of flexibility and control, while still adopting innovation from the cloud.</span></span> <span data-ttu-id="3ef9c-127">Systèmes intégrés Azure Stack taille comprise entre 4 à 12 nœuds et sont pris en charge conjointement par le fournisseur de matériel partenaire et Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-127">Azure Stack integrated systems range in size from 4 to 12 nodes, and are jointly supported by the hardware partner and Microsoft.</span></span> <span data-ttu-id="3ef9c-128">Utiliser des systèmes intégrés Azure Stack pour implémenter les nouveaux scénarios pour vos charges de travail de production.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-128">Use Azure Stack integrated systems to implement new scenarios for your production workloads.</span></span>

### <a name="azure-stack-development-kit"></a><span data-ttu-id="3ef9c-129">Kit de développement Azure Stack</span><span class="sxs-lookup"><span data-stu-id="3ef9c-129">Azure Stack Development Kit</span></span>

<span data-ttu-id="3ef9c-130">Kit de développement Microsoft Azure Stack est un déploiement à nœud unique d’Azure Stack, que vous pouvez utiliser pour évaluer et d’en savoir plus sur Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-130">Microsoft Azure Stack Development Kit is a single-node deployment of Azure Stack, which you can use to evaluate and learn about Azure Stack.</span></span> <span data-ttu-id="3ef9c-131">Vous pouvez également utiliser le Kit de développement Azure Stack comme environnement de développement, où vous pouvez développer à l’aide des API et des outils qui sont compatibles avec Azure.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-131">You can also use Azure Stack Development Kit as a developer environment, where you can develop using APIs and tooling that are consistent with Azure.</span></span> <span data-ttu-id="3ef9c-132">Kit de développement Azure Stack n’est pas destiné à être utilisé comme un environnement de production.</span><span class="sxs-lookup"><span data-stu-id="3ef9c-132">Azure Stack Development Kit is not intended to be used as a production environment.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="3ef9c-133">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="3ef9c-133">Additional resources</span></span>

-   <span data-ttu-id="3ef9c-134">**Cloud hybride Azure**</span><span class="sxs-lookup"><span data-stu-id="3ef9c-134">**Azure hybrid cloud**</span></span>

    <https://azure.microsoft.com/overview/hybrid-cloud/>

-   <span data-ttu-id="3ef9c-135">**Azure Stack**</span><span class="sxs-lookup"><span data-stu-id="3ef9c-135">**Azure Stack**</span></span>

    <https://azure.microsoft.com/overview/azure-stack/>

-   <span data-ttu-id="3ef9c-136">**Comptes de Service de Active Directory pour les conteneurs Windows**</span><span class="sxs-lookup"><span data-stu-id="3ef9c-136">**Active Directory Service Accounts for Windows Containers**</span></span>

    <https://docs.microsoft.com/virtualization/windowscontainers/manage-containers/manage-serviceaccounts>

-   <span data-ttu-id="3ef9c-137">**Créer un conteneur avec prise en charge d’Active Directory**</span><span class="sxs-lookup"><span data-stu-id="3ef9c-137">**Create a container with Active Directory support**</span></span>

    <https://blogs.msdn.microsoft.com/containerstuff/2017/01/30/create-a-container-with-active-directory-support/>

-   <span data-ttu-id="3ef9c-138">**Licences Azure Hybrid Benefit**</span><span class="sxs-lookup"><span data-stu-id="3ef9c-138">**Azure Hybrid Benefit licensing**</span></span>

    <https://azure.microsoft.com/pricing/hybrid-benefit/>

>[!div class="step-by-step"]
><span data-ttu-id="3ef9c-139">[Précédent](modernize-your-apps-lifecycle-with-ci-cd-pipelines-and-devops-tools-in-the-cloud.md)
>[Suivant](../walkthroughs-technical-get-started-overview.md)</span><span class="sxs-lookup"><span data-stu-id="3ef9c-139">[Previous](modernize-your-apps-lifecycle-with-ci-cd-pipelines-and-devops-tools-in-the-cloud.md)
[Next](../walkthroughs-technical-get-started-overview.md)</span></span>
