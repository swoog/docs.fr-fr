---
title: Procédures pas à pas et les techniques obtiennent une vue d’ensemble démarrée
description: Moderniser des Applications .NET existantes avec Azure Cloud et les conteneurs Windows | procédures pas à pas et les techniques obtiennent une vue d’ensemble démarrée
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/26/2017
ms.prod: .net
ms.topic: article
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 0bad7e3afbdf3e55c447319b3756f2235b9e0a19
ms.sourcegitcommit: 2e8acae16ae802f2d6d04e3ce0a6dbf04e476513
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2018
---
# <a name="walkthroughs-and-technical-get-started-overview"></a><span data-ttu-id="9462e-103">Procédures pas à pas et les techniques obtiennent une vue d’ensemble démarrée</span><span class="sxs-lookup"><span data-stu-id="9462e-103">Walkthroughs and technical get started overview</span></span>

<span data-ttu-id="9462e-104">Pour limiter la taille de ce livre électronique, documentation technique supplémentaire et les procédures pas à pas complète étaient mis à disposition dans un référentiel GitHub.</span><span class="sxs-lookup"><span data-stu-id="9462e-104">To limit the size of this e-book, additional technical documentation and the full walkthroughs were made available in a GitHub repository.</span></span> <span data-ttu-id="9462e-105">La série en ligne des procédures pas à pas qui est décrite dans ce chapitre traite le programme d’installation pas à pas plusieurs environnements qui sont basées sur les conteneurs Windows et le déploiement vers Azure.</span><span class="sxs-lookup"><span data-stu-id="9462e-105">The online series of walkthroughs that is described in this chapter covers the step-by-step setup of the multiple environments that are based on Windows Containers, and deployment to Azure.</span></span>

<span data-ttu-id="9462e-106">Les sections suivantes expliquent ce que chaque procédure pas à pas sur ses objectifs et la vision de haut niveau et fournit un diagramme des tâches qui sont impliquées.</span><span class="sxs-lookup"><span data-stu-id="9462e-106">The following sections explain what each walkthrough is about, its objectives and high-level vision, and provides a diagram of the tasks that are involved.</span></span> <span data-ttu-id="9462e-107">Vous pouvez obtenir les procédures pas à pas eux-mêmes dans le *eShopModernizing* applications wiki de référentiel GitHub à [ https://github.com/dotnet-architecture/eShopModernizing/wiki ](https://github.com/dotnet-architecture/eShopModernizing/wiki).</span><span class="sxs-lookup"><span data-stu-id="9462e-107">You can get the walkthroughs themselves in the *eShopModernizing* apps GitHub repo wiki at [https://github.com/dotnet-architecture/eShopModernizing/wiki](https://github.com/dotnet-architecture/eShopModernizing/wiki).</span></span>

## <a name="technical-walkthrough-list"></a><span data-ttu-id="9462e-108">Liste des techniques de procédure pas à pas</span><span class="sxs-lookup"><span data-stu-id="9462e-108">Technical walkthrough list</span></span>

<span data-ttu-id="9462e-109">Les procédures get-started suivantes fournissent des conseils techniques cohérent et complet des exemples d’applications que vous pouvez de courbes d’élévation et MAJ en utilisant des conteneurs et ensuite déplacer à l’aide de plusieurs options de déploiement dans Azure.</span><span class="sxs-lookup"><span data-stu-id="9462e-109">The following get-started walkthroughs provide consistent and comprehensive technical guidance for sample apps that you can lift and shift by using containers, and then move by using multiple deployment choices in Azure.</span></span>

<span data-ttu-id="9462e-110">Chacun des procédures suivantes utilise les nouveaux exemples eShopLegacy et eShopModernizing d’applications, qui sont disponibles sur GitHub à l’adresse [ https://github.com/dotnet-architecture/eShopModernizing ](https://github.com/dotnet-architecture/eShopModernizing).</span><span class="sxs-lookup"><span data-stu-id="9462e-110">Each of the following walkthroughs uses the new sample eShopLegacy and eShopModernizing apps, which are available on GitHub at [https://github.com/dotnet-architecture/eShopModernizing](https://github.com/dotnet-architecture/eShopModernizing).</span></span>

- <span data-ttu-id="9462e-111">**Visite guidée de shopping des applications héritées**</span><span class="sxs-lookup"><span data-stu-id="9462e-111">**Tour of eShop legacy apps**</span></span>

- <span data-ttu-id="9462e-112">**Mettez en conteneur de vos applications .NET existantes avec des conteneurs Windows**</span><span class="sxs-lookup"><span data-stu-id="9462e-112">**Containerize your existing .NET applications with Windows Containers**</span></span>

- <span data-ttu-id="9462e-113">**Déployer votre application basée sur les conteneurs de Windows pour les machines virtuelles Azure**</span><span class="sxs-lookup"><span data-stu-id="9462e-113">**Deploy your Windows Containers-based app to Azure VMs**</span></span>

- <span data-ttu-id="9462e-114">**Déployer vos applications basée sur les conteneurs de Windows à Kubernetes dans le Service de conteneur Azure**</span><span class="sxs-lookup"><span data-stu-id="9462e-114">**Deploy your Windows Containers-based apps to Kubernetes in Azure Container Service**</span></span>

- <span data-ttu-id="9462e-115">**Déployer vos applications basée sur les conteneurs de Windows Azure Service fabric**</span><span class="sxs-lookup"><span data-stu-id="9462e-115">**Deploy your Windows Containers-based apps to Azure Service Fabric**</span></span>

## <a name="walkthrough-1-tour-of-eshop-legacy-apps"></a><span data-ttu-id="9462e-116">Procédure pas à pas 1 : Visite guidée des applications héritées de shopping</span><span class="sxs-lookup"><span data-stu-id="9462e-116">Walkthrough 1: Tour of eShop legacy apps</span></span>

### <a name="technical-walkthrough-availability"></a><span data-ttu-id="9462e-117">Disponibilité de la procédure pas à pas technique</span><span class="sxs-lookup"><span data-stu-id="9462e-117">Technical walkthrough availability</span></span>

<span data-ttu-id="9462e-118">La procédure pas à pas technique complet est disponible dans le wiki de référentiel GitHub eShopModernizing :</span><span class="sxs-lookup"><span data-stu-id="9462e-118">The full technical walkthrough is available in the eShopModernizing GitHub repo wiki:</span></span>

[https://github.com/dotnet-architecture/eShopModernizing/wiki/01.-Tour-on-eShopModernizing-apps-implementation-code](https://github.com/dotnet-architecture/eShopModernizing/wiki/01.-Tour-on-eShopModernizing-apps-implementation-code)

### <a name="overview"></a><span data-ttu-id="9462e-119">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="9462e-119">Overview</span></span>

<span data-ttu-id="9462e-120">Dans cette procédure pas à pas, vous pouvez explorer l’implémentation initiale de deux exemples d’applications héritées.</span><span class="sxs-lookup"><span data-stu-id="9462e-120">In this walkthrough, you can explore the initial implementation of two sample legacy applications.</span></span> <span data-ttu-id="9462e-121">Les deux exemples d’applications une architecture monolithique et ont été créées à l’aide d’ASP.NET classique.</span><span class="sxs-lookup"><span data-stu-id="9462e-121">Both sample apps have a monolithic architecture, and were created by using classic ASP.NET.</span></span> <span data-ttu-id="9462e-122">Une application est basée sur ASP.NET 4.x MVC ; la deuxième application est basée sur les Web Forms ASP.NET 4.x.</span><span class="sxs-lookup"><span data-stu-id="9462e-122">One application is based on ASP.NET 4.x MVC; the second application is based on ASP.NET 4.x Web Forms.</span></span> <span data-ttu-id="9462e-123">Les deux applications sont dans le [eShopModernizing du référentiel GitHub](https://github.com/dotnet-architecture/eShopModernizing).</span><span class="sxs-lookup"><span data-stu-id="9462e-123">Both applications are in the [eShopModernizing GitHub repo](https://github.com/dotnet-architecture/eShopModernizing).</span></span>

<span data-ttu-id="9462e-124">Vous pouvez mettez en conteneur les deux exemples d’applications, semblable à la façon dont vous pouvez mettez en conteneur un classique [Windows Communication Foundation](../../framework/wcf/whats-wcf.md) application (WCF) à être consommés en tant qu’une application de bureau.</span><span class="sxs-lookup"><span data-stu-id="9462e-124">You can containerize both sample apps, similar to the way you can containerize a classic [Windows Communication Foundation](../../framework/wcf/whats-wcf.md) (WCF) application to be consumed as a desktop application.</span></span> <span data-ttu-id="9462e-125">Pour obtenir un exemple, consultez [eShopModernizingWCFWinForms](https://github.com/dotnet-architecture/eShopModernizingWCFWinForms).</span><span class="sxs-lookup"><span data-stu-id="9462e-125">For an example, see [eShopModernizingWCFWinForms](https://github.com/dotnet-architecture/eShopModernizingWCFWinForms).</span></span>

### <a name="goals"></a><span data-ttu-id="9462e-126">Objectifs</span><span class="sxs-lookup"><span data-stu-id="9462e-126">Goals</span></span>

<span data-ttu-id="9462e-127">L’objectif principal de cette procédure pas à pas est simplement afin de vous familiariser avec ces applications et leur configuration et le code.</span><span class="sxs-lookup"><span data-stu-id="9462e-127">The main goal of this walkthrough is simply to get familiar with these apps, and with their code and configuration.</span></span> <span data-ttu-id="9462e-128">Vous pouvez configurer les applications afin qu’ils génèrent et utilisent des données fictives, sans l’aide de la base de données SQL, à des fins de test.</span><span class="sxs-lookup"><span data-stu-id="9462e-128">You can configure the apps so that they generate and use mock data, without using the SQL database, for testing purposes.</span></span> <span data-ttu-id="9462e-129">Cette configuration facultative est basée sur l’injection de dépendance, d’une manière découplée.</span><span class="sxs-lookup"><span data-stu-id="9462e-129">This optional config is based on dependency injection, in a decoupled way.</span></span>

### <a name="scenario"></a><span data-ttu-id="9462e-130">Scénario</span><span class="sxs-lookup"><span data-stu-id="9462e-130">Scenario</span></span>

<span data-ttu-id="9462e-131">Figure 5-1 indique un scénario simple visant les applications héritées d’origine.</span><span class="sxs-lookup"><span data-stu-id="9462e-131">Figure 5-1 shows the simple scenario of the original legacy applications.</span></span>

> ![Scénario simple d’architecture des applications héritées d’origine](./media/image5-1.png)
>
> <span data-ttu-id="9462e-133">**Figure 5-1.**</span><span class="sxs-lookup"><span data-stu-id="9462e-133">**Figure 5-1.**</span></span> <span data-ttu-id="9462e-134">Scénario simple d’architecture des applications héritées d’origine</span><span class="sxs-lookup"><span data-stu-id="9462e-134">Simple architecture scenario of the original legacy applications</span></span>

<span data-ttu-id="9462e-135">À partir d’une perspective de domaine d’entreprise, les deux applications offrent la même catalogue de fonctionnalités de gestion.</span><span class="sxs-lookup"><span data-stu-id="9462e-135">From a business domain perspective, both apps offer the same catalog management features.</span></span> <span data-ttu-id="9462e-136">Membres de l’équipe d’entreprise Shopping utiliseriez l’application pour afficher et modifier le catalogue de produits.</span><span class="sxs-lookup"><span data-stu-id="9462e-136">Members of the eShop enterprise team would use the app to view and edit the product catalog.</span></span> <span data-ttu-id="9462e-137">Figure 5-2 illustre les captures d’écran de l’application initiale.</span><span class="sxs-lookup"><span data-stu-id="9462e-137">Figure 5-2 shows the initial app screenshots.</span></span>

![Applications ASP.NET MVC et les Web Forms ASP.NET (technologies existantes/hérité)](./media/image5-2.png)

> <span data-ttu-id="9462e-139">**Figure 5-2.**</span><span class="sxs-lookup"><span data-stu-id="9462e-139">**Figure 5-2.**</span></span> <span data-ttu-id="9462e-140">Applications ASP.NET MVC et les Web Forms ASP.NET (technologies existantes/hérité)</span><span class="sxs-lookup"><span data-stu-id="9462e-140">ASP.NET MVC and ASP.NET Web Forms applications (existing/legacy technologies)</span></span>

<span data-ttu-id="9462e-141">Il s’agit d’applications web qui sont utilisées pour parcourir et modifier les entrées de catalogue.</span><span class="sxs-lookup"><span data-stu-id="9462e-141">These are web applications that are used to browse and modify catalog entries.</span></span> <span data-ttu-id="9462e-142">Le fait que les deux applications fournir les mêmes fonctionnalités d’entreprise/fonctionnel est simplement à des fins de comparaison.</span><span class="sxs-lookup"><span data-stu-id="9462e-142">The fact that both apps deliver the same business/functional features is simply for comparison purposes.</span></span> <span data-ttu-id="9462e-143">Vous pouvez voir un processus modernisation similaire pour les applications qui ont été créées avec les infrastructures d’ASP.NET MVC et les Web Forms ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="9462e-143">You can see a similar modernization process for apps that were created by using the ASP.NET MVC and ASP.NET Web Forms frameworks.</span></span>

<span data-ttu-id="9462e-144">Dépendances dans ASP.NET 4.x ou des versions antérieures (soit pour MVC ou Web Forms) signifie que ces applications ne s’exécutent sur .NET Core, sauf si le code est entièrement réécrit à l’aide d’ASP.NET MVC de base.</span><span class="sxs-lookup"><span data-stu-id="9462e-144">Dependencies in ASP.NET 4.x or earlier versions (either for MVC or for Web Forms) means that these applications won't run on .NET Core unless the code is fully rewritten by using ASP.NET Core MVC.</span></span> <span data-ttu-id="9462e-145">Cela montre le point que si vous ne souhaitez pas remodéliser ou réécrire le code, vous pouvez mettez en conteneur des applications existantes et continuer à utiliser les mêmes technologies .NET et le même code.</span><span class="sxs-lookup"><span data-stu-id="9462e-145">This demonstrates the point that if you don't want to re-architect or rewrite code, you can containerize existing applications, and still use the same .NET technologies and the same code.</span></span> <span data-ttu-id="9462e-146">Vous pouvez voir comment vous pouvez exécuter des applications de ce type dans les conteneurs, sans aucune modification de code hérité.</span><span class="sxs-lookup"><span data-stu-id="9462e-146">You can see how you can run applications like these in containers, without any changes to legacy code.</span></span>

### <a name="benefits"></a><span data-ttu-id="9462e-147">Avantages</span><span class="sxs-lookup"><span data-stu-id="9462e-147">Benefits</span></span>

<span data-ttu-id="9462e-148">Les avantages de cette procédure pas à pas sont simples : simplement vous familiariser avec la configuration d’application et de code, en fonction de l’injection de dépendances.</span><span class="sxs-lookup"><span data-stu-id="9462e-148">The benefits of this walkthrough are simple: Just get familiar with the code and application configuration, based on dependency injection.</span></span> <span data-ttu-id="9462e-149">Ensuite, vous pouvez essayer avec cette approche lorsque vous mettez en conteneur et le déployez dans plusieurs environnements à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="9462e-149">Then, you can experiment with this approach when you containerize and deploy to multiple environments in the future.</span></span>

### <a name="next-steps"></a><span data-ttu-id="9462e-150">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="9462e-150">Next steps</span></span>

<span data-ttu-id="9462e-151">Explorer ce contenu plus approfondi sur le wiki de GitHub :</span><span class="sxs-lookup"><span data-stu-id="9462e-151">Explore this content more in-depth on the GitHub wiki:</span></span>

[https://github.com/dotnet-architecture/eShopModernizing/wiki/01.-Tour-on-eShopModernizing-apps-implementation-code](https://github.com/dotnet-architecture/eShopModernizing/wiki/01.-Tour-on-eShopModernizing-apps-implementation-code)

## <a name="walkthrough-2-containerize-your-existing-net-applications-with-windows-containers"></a><span data-ttu-id="9462e-152">Procédure 2 : Mettez en conteneur vos applications .NET existantes avec des conteneurs Windows</span><span class="sxs-lookup"><span data-stu-id="9462e-152">Walkthrough 2: Containerize your existing .NET applications with Windows Containers</span></span>

### <a name="technical-walkthrough-availability"></a><span data-ttu-id="9462e-153">Disponibilité de la procédure pas à pas technique</span><span class="sxs-lookup"><span data-stu-id="9462e-153">Technical walkthrough availability</span></span>

<span data-ttu-id="9462e-154">La procédure pas à pas technique complet est disponible dans le wiki de référentiel GitHub eShopModernizing :</span><span class="sxs-lookup"><span data-stu-id="9462e-154">The full technical walkthrough is available in the eShopModernizing GitHub repo wiki:</span></span>

[https://github.com/dotnet-architecture/eShopModernizing/wiki/02.-How-to-containerize-the-.NET-Framework-web-apps-with-Windows-Containers-and-Docker](https://github.com/dotnet-architecture/eShopModernizing/wiki/02.-How-to-containerize-the-.NET-Framework-web-apps-with-Windows-Containers-and-Docker)

### <a name="overview"></a><span data-ttu-id="9462e-155">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="9462e-155">Overview</span></span>

<span data-ttu-id="9462e-156">Les conteneurs Windows permet d’améliorer le déploiement des applications .NET existantes, telles que celles basées sur MVC, Web Forms ou WCF, pour les environnements de test, de développement et de production.</span><span class="sxs-lookup"><span data-stu-id="9462e-156">Use Windows Containers to improve deployment of existing .NET applications, like those based on MVC, Web Forms, or WCF, to production, development, and test environments.</span></span>

### <a name="goals"></a><span data-ttu-id="9462e-157">Objectifs</span><span class="sxs-lookup"><span data-stu-id="9462e-157">Goals</span></span>

<span data-ttu-id="9462e-158">L’objectif de cette procédure pas à pas est de vous montrer plusieurs options pour containerizing une application .NET Framework existante.</span><span class="sxs-lookup"><span data-stu-id="9462e-158">The goal of this walkthrough is to show you several options for containerizing an existing .NET Framework application.</span></span> <span data-ttu-id="9462e-159">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="9462e-159">You can:</span></span>

- <span data-ttu-id="9462e-160">Mettez en conteneur de votre application à l’aide de [Visual Studio 2017 Tools pour Docker](/aspnet/core/host-and-deploy/docker/visual-studio-tools-for-docker) (Visual Studio 2017 ou versions ultérieures).</span><span class="sxs-lookup"><span data-stu-id="9462e-160">Containerize your application by using [Visual Studio 2017 Tools for Docker](/aspnet/core/host-and-deploy/docker/visual-studio-tools-for-docker) (Visual Studio 2017 or later versions).</span></span>

- <span data-ttu-id="9462e-161">Mettez en conteneur de votre application en ajoutant manuellement un [Dockerfile](https://docs.docker.com/engine/reference/builder/), puis en utilisant la [Docker CLI](https://docs.docker.com/engine/reference/commandline/cli/).</span><span class="sxs-lookup"><span data-stu-id="9462e-161">Containerize your application by manually adding a [Dockerfile](https://docs.docker.com/engine/reference/builder/), and then using the [Docker CLI](https://docs.docker.com/engine/reference/commandline/cli/).</span></span>

- <span data-ttu-id="9462e-162">Mettez en conteneur de votre application à l’aide de la [Img2Docker](https://github.com/docker/communitytools-image2docker-win) outil (outil open source à partir de Docker).</span><span class="sxs-lookup"><span data-stu-id="9462e-162">Containerize your application by using the [Img2Docker](https://github.com/docker/communitytools-image2docker-win) tool (an open-source tool from Docker).</span></span>

<span data-ttu-id="9462e-163">Cette procédure pas à pas se concentre sur les outils de 2017 Visual Studio pour l’approche de Docker, mais les deux autres approches sont relativement similaires en ce qui concerne l’utilisation des fichiers Dockerfile.</span><span class="sxs-lookup"><span data-stu-id="9462e-163">This walkthrough focuses on the Visual Studio 2017 Tools for Docker approach, but the other two approaches are fairly similar in regard to using Dockerfiles.</span></span>

### <a name="scenario"></a><span data-ttu-id="9462e-164">Scénario</span><span class="sxs-lookup"><span data-stu-id="9462e-164">Scenario</span></span>

<span data-ttu-id="9462e-165">Figure 5-3 illustre le scénario pour les applications héritées shopping en conteneur.</span><span class="sxs-lookup"><span data-stu-id="9462e-165">Figure 5-3 shows the scenario for containerized eShop legacy applications.</span></span>

> ![Diagramme d’architecture simplifiée des applications en conteneur dans un environnement de développement](./media/image5-3.png)
>
> <span data-ttu-id="9462e-167">**Figure 5-3.**</span><span class="sxs-lookup"><span data-stu-id="9462e-167">**Figure 5-3.**</span></span> <span data-ttu-id="9462e-168">Diagramme d’architecture simplifiée des applications en conteneur dans un environnement de développement</span><span class="sxs-lookup"><span data-stu-id="9462e-168">Simplified architecture diagram of containerized applications in a development environment</span></span>

### <a name="benefits"></a><span data-ttu-id="9462e-169">Avantages</span><span class="sxs-lookup"><span data-stu-id="9462e-169">Benefits</span></span>

<span data-ttu-id="9462e-170">Il existe des avantages à l’exécution de votre application monolithique dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="9462e-170">There are advantages to running your monolithic application in a container.</span></span> <span data-ttu-id="9462e-171">Tout d’abord, vous créez une image de l’application.</span><span class="sxs-lookup"><span data-stu-id="9462e-171">First, you create an image for the application.</span></span> <span data-ttu-id="9462e-172">À ce stade, chaque déploiement s’exécute dans le même environnement.</span><span class="sxs-lookup"><span data-stu-id="9462e-172">From that point on, every deployment runs in the same environment.</span></span> <span data-ttu-id="9462e-173">Chaque conteneur utilise la même version du système d’exploitation, a la même version de dépendances installé, utilise la même version du .NET framework et est construit à l’aide du même processus.</span><span class="sxs-lookup"><span data-stu-id="9462e-173">Every container uses the same OS version, has the same version of dependencies installed, uses the same .NET framework version, and is built by using the same process.</span></span> <span data-ttu-id="9462e-174">En fait, vous contrôlez les dépendances de votre application à l’aide d’une image Docker.</span><span class="sxs-lookup"><span data-stu-id="9462e-174">Basically, you control the dependencies of your application by using a Docker image.</span></span> <span data-ttu-id="9462e-175">Lorsque vous déployez les conteneurs, les dépendances se déplacent avec l’application.</span><span class="sxs-lookup"><span data-stu-id="9462e-175">The dependencies travel with the application when you deploy the containers.</span></span>

<span data-ttu-id="9462e-176">Un autre avantage est que les développeurs peuvent exécuter l’application dans l’environnement cohérent qui est fourni par les conteneurs Windows.</span><span class="sxs-lookup"><span data-stu-id="9462e-176">An additional benefit is that developers can run the application in the consistent environment that's provided by Windows Containers.</span></span> <span data-ttu-id="9462e-177">Les problèmes qui apparaissent uniquement dans certaines versions peuvent être détectées immédiatement, au lieu de surfaces dans un environnement intermédiaire ou de production.</span><span class="sxs-lookup"><span data-stu-id="9462e-177">Issues that appear only with certain versions can be spotted immediately, instead of surfacing in a staging or production environment.</span></span> <span data-ttu-id="9462e-178">Les différences dans les environnements de développement utilisés par les membres de l’équipe de développement a d’importance inférieure lorsque les applications s’exécutent dans des conteneurs.</span><span class="sxs-lookup"><span data-stu-id="9462e-178">Differences in development environments used by members of the development team matter less when applications run in containers.</span></span>

<span data-ttu-id="9462e-179">Les applications en conteneur possèdent également une courbe plate de la montée en puissance parallèle.</span><span class="sxs-lookup"><span data-stu-id="9462e-179">Containerized applications also have a flatter scale-out curve.</span></span> <span data-ttu-id="9462e-180">Les applications en conteneur permettent d’avoir plus d’application et les instances de service (basés sur les conteneurs) dans une machine virtuelle ou d’un ordinateur physique par rapport aux déploiements d’application normal par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="9462e-180">Containerized apps enable you to have more application and service instances (based on containers) in a VM or physical machine compared to regular application deployments per machine.</span></span> <span data-ttu-id="9462e-181">Cela se traduit par densité plus élevée et moins nécessaire des ressources, notamment lorsque vous utilisez orchestrators comme Kubernetes ou Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="9462e-181">This translates to higher density and fewer required resources, especially when you use orchestrators like Kubernetes or Service Fabric.</span></span>

<span data-ttu-id="9462e-182">CONTENEURISATION des données, dans des situations idéale, ne nécessitent pas d’apporter des modifications au code d’application (C\#).</span><span class="sxs-lookup"><span data-stu-id="9462e-182">Containerization, in ideal situations, does not require making any changes to the application code (C\#).</span></span> <span data-ttu-id="9462e-183">Dans la plupart des scénarios, vous devez simplement les fichiers de métadonnées de déploiement (fichiers Dockerfile et Docker Compose) Docker.</span><span class="sxs-lookup"><span data-stu-id="9462e-183">In most scenarios, you just need the Docker deployment metadata files (Dockerfiles and Docker Compose files).</span></span>

### <a name="next-steps"></a><span data-ttu-id="9462e-184">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="9462e-184">Next steps</span></span>

<span data-ttu-id="9462e-185">Explorer ce contenu plus approfondi sur le wiki de GitHub : [https://github.com/dotnet-architecture/eShopModernizing/wiki/02.-How-to-containerize-the-.NET-Framework-web-apps-with-Windows-Containers-and-Docker](https://github.com/dotnet-architecture/eShopModernizing/wiki/02.-How-to-containerize-the-.NET-Framework-web-apps-with-Windows-Containers-and-Docker)</span><span class="sxs-lookup"><span data-stu-id="9462e-185">Explore this content more in-depth on the GitHub wiki: [https://github.com/dotnet-architecture/eShopModernizing/wiki/02.-How-to-containerize-the-.NET-Framework-web-apps-with-Windows-Containers-and-Docker](https://github.com/dotnet-architecture/eShopModernizing/wiki/02.-How-to-containerize-the-.NET-Framework-web-apps-with-Windows-Containers-and-Docker)</span></span>

## <a name="walkthrough-3-deploy-your-windows-containers-based-app-to-azure-vms"></a><span data-ttu-id="9462e-186">Procédure 3 : Déployer votre application basée sur les conteneurs de Windows sur les machines virtuelles Azure</span><span class="sxs-lookup"><span data-stu-id="9462e-186">Walkthrough 3: Deploy your Windows Containers-based app to Azure VMs</span></span>

### <a name="technical-walkthrough-availability"></a><span data-ttu-id="9462e-187">Disponibilité de la procédure pas à pas technique</span><span class="sxs-lookup"><span data-stu-id="9462e-187">Technical walkthrough availability</span></span>

<span data-ttu-id="9462e-188">La procédure pas à pas technique complet est disponible dans le wiki de référentiel GitHub eShopModernizing :</span><span class="sxs-lookup"><span data-stu-id="9462e-188">The full technical walkthrough is available in the eShopModernizing GitHub repo wiki:</span></span>

[https://github.com/dotnet-architecture/eShopModernizing/wiki/03.-How-to-deploy-your-Windows-Containers-based-app-into-Azure-VMs-(Including-CI-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/03.-How-to-deploy-your-Windows-Containers-based-app-into-Azure-VMs-(Including-CI-CD))

### <a name="overview"></a><span data-ttu-id="9462e-189">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="9462e-189">Overview</span></span>

<span data-ttu-id="9462e-190">Déploiement sur un hôte Docker sur un serveur Windows Server 2016 Virtual Machine (VM) dans Azure vous permet de définir rapidement des environnements de développement/test/mise en lots.</span><span class="sxs-lookup"><span data-stu-id="9462e-190">Deploying to a Docker host on a Windows Server 2016 Virtual Machine (VM) in Azure lets you quickly set up development/test/staging environments.</span></span> <span data-ttu-id="9462e-191">Elle vous donne également un emplacement commun pour les testeurs ou les utilisateurs des activités à valider l’application.</span><span class="sxs-lookup"><span data-stu-id="9462e-191">It also gives you a common place for testers or business users to validate the app.</span></span> <span data-ttu-id="9462e-192">Machines virtuelles peuvent également être infrastructure valide comme les environnements de production de Service (IaaS).</span><span class="sxs-lookup"><span data-stu-id="9462e-192">VMs also can be valid Infrastucture as a Service (IaaS) production environments.</span></span>

### <a name="goals"></a><span data-ttu-id="9462e-193">Objectifs</span><span class="sxs-lookup"><span data-stu-id="9462e-193">Goals</span></span>

<span data-ttu-id="9462e-194">L’objectif de cette procédure pas à pas est de vous montrer les plusieurs alternatives que vous avez lorsque vous déployez les conteneurs Windows sur les machines virtuelles Azure qui sont basés sur Windows Server 2016 ou versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="9462e-194">The goal of this walkthrough is to show you the multiple alternatives you have when you deploy Windows Containers to Azure VMs that are based on Windows Server 2016 or later versions.</span></span>

### <a name="scenarios"></a><span data-ttu-id="9462e-195">Scénarios</span><span class="sxs-lookup"><span data-stu-id="9462e-195">Scenarios</span></span>

<span data-ttu-id="9462e-196">Plusieurs scénarios sont traités dans cette procédure pas à pas.</span><span class="sxs-lookup"><span data-stu-id="9462e-196">Several scenarios are covered in this walkthrough.</span></span>

#### <a name="scenario-a-deploy-to-an-azure-vm-from-a-dev-pc-through-docker-engine-connection"></a><span data-ttu-id="9462e-197">Scénario a : les déployer sur une machine virtuelle Azure à partir d’un ordinateur de développement via la connexion du moteur Docker</span><span class="sxs-lookup"><span data-stu-id="9462e-197">Scenario A: Deploy to an Azure VM from a dev PC through Docker Engine connection</span></span>

![Déployer sur une machine virtuelle Azure à partir d’un ordinateur de développement via une connexion du moteur Docker](./media/image5-4.png)

> <span data-ttu-id="9462e-199">**Figure 5-4.**</span><span class="sxs-lookup"><span data-stu-id="9462e-199">**Figure 5-4.**</span></span> <span data-ttu-id="9462e-200">Déployer sur une machine virtuelle Azure à partir d’un ordinateur de développement via une connexion du moteur Docker</span><span class="sxs-lookup"><span data-stu-id="9462e-200">Deploy to an Azure VM from a dev PC through a Docker Engine connection</span></span>

#### <a name="scenario-b-deploy-to-an-azure-vm-through-a-docker-registry"></a><span data-ttu-id="9462e-201">Scénario b : déployer sur une machine virtuelle Azure via un Registre Docker</span><span class="sxs-lookup"><span data-stu-id="9462e-201">Scenario B: Deploy to an Azure VM through a Docker Registry</span></span>

![Déployer sur une machine virtuelle Azure via un Registre Docker](./media/image5-5.png)

> <span data-ttu-id="9462e-203">**Figure 5-5.**</span><span class="sxs-lookup"><span data-stu-id="9462e-203">**Figure 5-5.**</span></span> <span data-ttu-id="9462e-204">Déployer sur une machine virtuelle Azure via un Registre Docker</span><span class="sxs-lookup"><span data-stu-id="9462e-204">Deploy to an Azure VM through a Docker Registry</span></span>

#### <a name="scenario-c-deploy-to-an-azure-vm-from-cicd-pipelines-in-visual-studio-team-services"></a><span data-ttu-id="9462e-205">Scénario c : déployer sur une machine virtuelle Azure à partir de l’élément de configuration/CD des pipelines dans Visual Studio Team Services</span><span class="sxs-lookup"><span data-stu-id="9462e-205">Scenario C: Deploy to an Azure VM from CI/CD pipelines in Visual Studio Team Services</span></span>

![Déployer sur une machine virtuelle Azure à partir de CD / l’élément de configuration des pipelines dans Visual Studio Team Services](./media/image5-6.png)

> <span data-ttu-id="9462e-207">**Figure 5-6.**</span><span class="sxs-lookup"><span data-stu-id="9462e-207">**Figure 5-6.**</span></span> <span data-ttu-id="9462e-208">Déployer sur une machine virtuelle Azure à partir de CD / l’élément de configuration des pipelines dans Visual Studio Team Services</span><span class="sxs-lookup"><span data-stu-id="9462e-208">Deploy to an Azure VM from CI/CD pipelines in Visual Studio Team Services</span></span>

### <a name="azure-vms-for-windows-containers"></a><span data-ttu-id="9462e-209">Machines virtuelles Azure pour les conteneurs Windows</span><span class="sxs-lookup"><span data-stu-id="9462e-209">Azure VMs for Windows Containers</span></span>

<span data-ttu-id="9462e-210">Machines virtuelles Azure pour les conteneurs Windows sont basés sur Windows Server 2016, Windows 10 ou versions ultérieures de machines virtuelles, à la fois avec le moteur Docker configuré.</span><span class="sxs-lookup"><span data-stu-id="9462e-210">Azure VMs for Windows Containers are VMs based on Windows Server 2016, Windows 10, or later versions, both with Docker Engine set up.</span></span> <span data-ttu-id="9462e-211">Dans la plupart des cas, Windows Server 2016 est utilisé dans les machines virtuelles Azure.</span><span class="sxs-lookup"><span data-stu-id="9462e-211">In most cases, Windows Server 2016 is used in the Azure VMs.</span></span>

<span data-ttu-id="9462e-212">Azure fournit actuellement une machine virtuelle nommée **Windows Server 2016 avec des conteneurs**.</span><span class="sxs-lookup"><span data-stu-id="9462e-212">Azure currently provides a VM named **Windows Server 2016 with Containers**.</span></span> <span data-ttu-id="9462e-213">Vous pouvez utiliser cet ordinateur virtuel pour essayer la nouvelle fonctionnalité de conteneur Windows Server avec Windows Server Core ou Nano Server de Windows.</span><span class="sxs-lookup"><span data-stu-id="9462e-213">You can use this VM to try the new Windows Server Container feature, with either Windows Server Core or Windows Nano Server.</span></span> <span data-ttu-id="9462e-214">Les images de système d’exploitation de conteneur sont installés, et ensuite l’ordinateur virtuel est prêt à être utilisé avec Docker.</span><span class="sxs-lookup"><span data-stu-id="9462e-214">Container OS images are installed, and then the VM is ready to use with Docker.</span></span>

### <a name="benefits"></a><span data-ttu-id="9462e-215">Avantages</span><span class="sxs-lookup"><span data-stu-id="9462e-215">Benefits</span></span>

<span data-ttu-id="9462e-216">Bien que les conteneurs Windows peuvent être déployées sur local Windows Server 2016 machines virtuelles, lorsque vous déployez dans Azure, vous obtenez un moyen plus simple pour commencer, machines virtuelles de prêt à utiliser Windows Server conteneur.</span><span class="sxs-lookup"><span data-stu-id="9462e-216">Although Windows Containers can be deployed to on-premises Windows Server 2016 VMs, when you deploy to Azure, you get an easier way to get started, with ready-to-use Windows Server Container VMs.</span></span> <span data-ttu-id="9462e-217">Vous obtenez également un emplacement commun en ligne qui est accessible aux testeurs et évolutivité automatique par le biais des machines virtuelles Azure identiques.</span><span class="sxs-lookup"><span data-stu-id="9462e-217">You also get a common online location that’s accessible to testers, and automatic scalability through Azure virtual machine scale sets.</span></span>

### <a name="next-steps"></a><span data-ttu-id="9462e-218">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="9462e-218">Next steps</span></span>

<span data-ttu-id="9462e-219">Explorer ce contenu plus approfondi sur le wiki de GitHub :</span><span class="sxs-lookup"><span data-stu-id="9462e-219">Explore this content more in-depth on the GitHub wiki:</span></span>

[https://github.com/dotnet-architecture/eShopModernizing/wiki/03.-How-to-deploy-your-Windows-Containers-based-app-into-Azure-VMs-(Including-CI-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/03.-How-to-deploy-your-Windows-Containers-based-app-into-Azure-VMs-(Including-CI-CD))

## <a name="walkthrough-4-deploy-your-windows-containers-based-apps-to-kubernetes-in-azure-container-service"></a><span data-ttu-id="9462e-220">Procédure pas à pas 4 : Déployer vos applications de basée sur les conteneurs Windows sur Kubernetes dans le Service de conteneur Azure</span><span class="sxs-lookup"><span data-stu-id="9462e-220">Walkthrough 4: Deploy your Windows Containers-based apps to Kubernetes in Azure Container Service</span></span>

### <a name="technical-walkthrough-availability"></a><span data-ttu-id="9462e-221">Disponibilité de la procédure pas à pas technique</span><span class="sxs-lookup"><span data-stu-id="9462e-221">Technical walkthrough availability</span></span>

<span data-ttu-id="9462e-222">La procédure pas à pas technique complet est disponible dans le wiki de référentiel GitHub eShopModernizing :</span><span class="sxs-lookup"><span data-stu-id="9462e-222">The full technical walkthrough is available in the eShopModernizing GitHub repo wiki:</span></span>

[https://github.com/dotnet-architecture/eShopModernizing/wiki/04.-How-to-deploy-your-Windows-Containers-based-apps-into-Kubernetes-in-Azure-Container-Service-(Including-C-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/04.-How-to-deploy-your-Windows-Containers-based-apps-into-Kubernetes-in-Azure-Container-Service-(Including-C-CD))

### <a name="overview"></a><span data-ttu-id="9462e-223">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="9462e-223">Overview</span></span>

<span data-ttu-id="9462e-224">Une application qui est basée sur les conteneurs Windows devra rapidement utilisent des plateformes, éloigner encore davantage de machines virtuelles IaaS.</span><span class="sxs-lookup"><span data-stu-id="9462e-224">An application that's based on Windows Containers will quickly need to use platforms, moving even further away from IaaS VMs.</span></span> <span data-ttu-id="9462e-225">Cela est nécessaire pour facilement atteindre une haute évolutivité et mieux automatisée de l’évolutivité et pour une amélioration significative dans automatisée déploiements et le contrôle de version.</span><span class="sxs-lookup"><span data-stu-id="9462e-225">This is needed to easily achieve high scalability and better automated scalability, and for a significant improvement in automated deployments and versioning.</span></span> <span data-ttu-id="9462e-226">Vous pouvez atteindre ces objectifs à l’aide de l’orchestrateur [Kubernetes](https://kubernetes.io/), disponible dans [Azure conteneur Services](https://azure.microsoft.com/services/container-service/).</span><span class="sxs-lookup"><span data-stu-id="9462e-226">You can achieve these goals by using the orchestrator [Kubernetes](https://kubernetes.io/), available in [Azure Container Services](https://azure.microsoft.com/services/container-service/).</span></span>

### <a name="goals"></a><span data-ttu-id="9462e-227">Objectifs</span><span class="sxs-lookup"><span data-stu-id="9462e-227">Goals</span></span>

<span data-ttu-id="9462e-228">L’objectif de cette procédure pas à pas est d’apprendre à déployer une application conteneur Windows – Kubernetes (également appelé *K8s*) dans le Service de conteneur Azure.</span><span class="sxs-lookup"><span data-stu-id="9462e-228">The goal of this walkthrough is to learn how to deploy a Windows Container–based application to Kubernetes (also called *K8s*) in Azure Container Service.</span></span> <span data-ttu-id="9462e-229">Déploiement sur Kubernetes à partir de zéro est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="9462e-229">Deploying to Kubernetes from scratch is a two-step process:</span></span>

1.  <span data-ttu-id="9462e-230">Déployer un cluster Kubernetes au Service de conteneur Azure.</span><span class="sxs-lookup"><span data-stu-id="9462e-230">Deploy a Kubernetes cluster to Azure Container Service.</span></span>

2.  <span data-ttu-id="9462e-231">Déployer l’application et les ressources associées au cluster Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="9462e-231">Deploy the application and related resources to the Kubernetes cluster.</span></span>

### <a name="scenarios"></a><span data-ttu-id="9462e-232">Scénarios</span><span class="sxs-lookup"><span data-stu-id="9462e-232">Scenarios</span></span>

#### <a name="scenario-a-deploy-directly-to-a-kubernetes-cluster-from-a-dev-environment"></a><span data-ttu-id="9462e-233">Scénario a : les déployer directement vers un cluster de Kubernetes à partir d’un environnement de développement</span><span class="sxs-lookup"><span data-stu-id="9462e-233">Scenario A: Deploy directly to a Kubernetes cluster from a dev environment</span></span>

![Déployer directement sur un cluster Kubernetes à partir d’un environnement de développement](./media/image5-7.png)

> <span data-ttu-id="9462e-235">**Figure 5-7.**</span><span class="sxs-lookup"><span data-stu-id="9462e-235">**Figure 5-7.**</span></span> <span data-ttu-id="9462e-236">Déployer directement sur un cluster Kubernetes à partir d’un environnement de développement</span><span class="sxs-lookup"><span data-stu-id="9462e-236">Deploy directly to a Kubernetes cluster from a development environment</span></span>

#### <a name="scenario-b-deploy-to-a-kubernetes-cluster-from-cicd-pipelines-in-team-services"></a><span data-ttu-id="9462e-237">Scénario b : déployer vers un cluster Kubernetes à partir de l’élément de configuration/CD pipelines dans Team Services</span><span class="sxs-lookup"><span data-stu-id="9462e-237">Scenario B: Deploy to a Kubernetes cluster from CI/CD pipelines in Team Services</span></span>

![Déployer vers un cluster Kubernetes à partir de l’élément de configuration/CD des pipelines dans Team Services](./media/image5-8.png)

> <span data-ttu-id="9462e-239">**Figure 5-8.**</span><span class="sxs-lookup"><span data-stu-id="9462e-239">**Figure 5-8.**</span></span> <span data-ttu-id="9462e-240">Déployer vers un cluster Kubernetes à partir de l’élément de configuration/CD des pipelines dans Team Services</span><span class="sxs-lookup"><span data-stu-id="9462e-240">Deploy to a Kubernetes cluster from CI/CD pipelines in Team Services</span></span>

### <a name="benefits"></a><span data-ttu-id="9462e-241">Avantages</span><span class="sxs-lookup"><span data-stu-id="9462e-241">Benefits</span></span>

<span data-ttu-id="9462e-242">Il existe de nombreux avantages pour le déploiement vers un cluster dans Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="9462e-242">There are many benefits to deploying to a cluster in Kubernetes.</span></span> <span data-ttu-id="9462e-243">Le principal avantage est que vous obtenez un environnement de l’environnement de production dans laquelle vous pouvez faire évoluer l’application en fonction du nombre d’instances de conteneurs, vous souhaitez utiliser (évolutivité interne dans les nœuds existants), en fonction du nombre de nœuds ou des machines virtuelles dans le cluster ( évolutivité globale du cluster).</span><span class="sxs-lookup"><span data-stu-id="9462e-243">The biggest benefit is that you get a production-ready environment in which you can scale out the application based on the number of container instances you want to use (inner-scalability in the existing nodes), and based on the number of nodes or VMs in the cluster (global scalability of the cluster).</span></span>

<span data-ttu-id="9462e-244">Service de conteneur Azure optimise les technologies et outils open source populaires spécifiquement pour Azure.</span><span class="sxs-lookup"><span data-stu-id="9462e-244">Azure Container Service optimizes popular open-source tools and technologies specifically for Azure.</span></span> <span data-ttu-id="9462e-245">Vous obtenez une solution ouverte qui offre la portabilité de vos conteneurs et lors de la configuration de votre application.</span><span class="sxs-lookup"><span data-stu-id="9462e-245">You get an open solution that offers portability, both for your containers and for your application configuration.</span></span> <span data-ttu-id="9462e-246">Sélectionnez la taille, le nombre d’hôtes, et le conteneur-Outils orchestrator Service gère tout le reste.</span><span class="sxs-lookup"><span data-stu-id="9462e-246">You select the size, the number of hosts, and the orchestrator tools-Container Service handles everything else.</span></span>

<span data-ttu-id="9462e-247">Avec Kubernetes, les développeurs peuvent progresser de réfléchir à des machines physiques et virtuelles, à la planification d’une infrastructure orientée conteneur qui facilite les fonctionnalités suivantes, entre autres :</span><span class="sxs-lookup"><span data-stu-id="9462e-247">With Kubernetes, developers can progress from thinking about physical and virtual machines, to planning a container-centric infrastructure that facilitates the following capabilities, among others:</span></span>

- <span data-ttu-id="9462e-248">Applications basées sur plusieurs conteneurs</span><span class="sxs-lookup"><span data-stu-id="9462e-248">Applications based on multiple containers</span></span>

- <span data-ttu-id="9462e-249">Réplication des instances de conteneurs et d’échelle horizontale</span><span class="sxs-lookup"><span data-stu-id="9462e-249">Replicating container instances and horizontal autoscaling</span></span>

- <span data-ttu-id="9462e-250">Attribution de noms et de découverte (par exemple, DNS interne)</span><span class="sxs-lookup"><span data-stu-id="9462e-250">Naming and discovering (for example, internal DNS)</span></span>

- <span data-ttu-id="9462e-251">L’équilibrage de charge</span><span class="sxs-lookup"><span data-stu-id="9462e-251">Balancing loads</span></span>

- <span data-ttu-id="9462e-252">Mises à jour propagées</span><span class="sxs-lookup"><span data-stu-id="9462e-252">Rolling updates</span></span>

- <span data-ttu-id="9462e-253">Distribution de clés secrètes</span><span class="sxs-lookup"><span data-stu-id="9462e-253">Distributing secrets</span></span>

- <span data-ttu-id="9462e-254">Vérifications de l’intégrité des applications</span><span class="sxs-lookup"><span data-stu-id="9462e-254">Application health checks</span></span>

## <a name="next-steps"></a><span data-ttu-id="9462e-255">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="9462e-255">Next steps</span></span>

<span data-ttu-id="9462e-256">Explorer ce contenu plus approfondi sur le wiki de GitHub : [https://github.com/dotnet-architecture/eShopModernizing/wiki/04.-How-to-deploy-your-Windows-Containers-based-apps-into-Kubernetes-in-Azure-Container-Service-(Including-C-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/04.-How-to-deploy-your-Windows-Containers-based-apps-into-Kubernetes-in-Azure-Container-Service-(Including-C-CD))</span><span class="sxs-lookup"><span data-stu-id="9462e-256">Explore this content more in-depth on the GitHub wiki: [https://github.com/dotnet-architecture/eShopModernizing/wiki/04.-How-to-deploy-your-Windows-Containers-based-apps-into-Kubernetes-in-Azure-Container-Service-(Including-C-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/04.-How-to-deploy-your-Windows-Containers-based-apps-into-Kubernetes-in-Azure-Container-Service-(Including-C-CD))</span></span>

## <a name="walkthrough-5-deploy-your-windows-containers-based-apps-to-azure-service-fabric"></a><span data-ttu-id="9462e-257">Procédure 5 : Déployer vos applications basée sur les conteneurs de Windows Azure Service fabric</span><span class="sxs-lookup"><span data-stu-id="9462e-257">Walkthrough 5: Deploy your Windows Containers-based apps to Azure Service Fabric</span></span>

### <a name="technical-walkthrough-availability"></a><span data-ttu-id="9462e-258">Disponibilité de la procédure pas à pas technique</span><span class="sxs-lookup"><span data-stu-id="9462e-258">Technical walkthrough availability</span></span>

<span data-ttu-id="9462e-259">La procédure pas à pas technique complet est disponible dans le wiki de référentiel GitHub eShopModernizing :</span><span class="sxs-lookup"><span data-stu-id="9462e-259">The full technical walkthrough is available in the eShopModernizing GitHub repo wiki:</span></span>

[https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-How-to-deploy-your-Windows-Containers-based-apps-into-Azure-Service-Fabric-(Including-CI-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-How-to-deploy-your-Windows-Containers-based-apps-into-Azure-Service-Fabric-(Including-CI-CD))

### <a name="overview"></a><span data-ttu-id="9462e-260">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="9462e-260">Overview</span></span>

<span data-ttu-id="9462e-261">Une application basée sur les conteneurs Windows rapidement doit utiliser des plates-formes, éloigner encore davantage de machines virtuelles IaaS.</span><span class="sxs-lookup"><span data-stu-id="9462e-261">An application based on Windows Containers quickly needs to use platforms, moving even further away from IaaS VMs.</span></span> <span data-ttu-id="9462e-262">Cela est nécessaire pour facilement atteindre une haute évolutivité et mieux automatisée de l’évolutivité et pour une amélioration significative dans automatisée déploiements et le contrôle de version.</span><span class="sxs-lookup"><span data-stu-id="9462e-262">This is needed to easily achieve high scalability and better automated scalability, and for a significant improvement in automated deployments and versioning.</span></span> <span data-ttu-id="9462e-263">Vous pouvez atteindre ces objectifs à l’aide de l’orchestrateur Azure Service Fabric, qui est disponible dans le cloud Azure, mais vous pouvez également utiliser localement, ou même dans un autre cloud public.</span><span class="sxs-lookup"><span data-stu-id="9462e-263">You can achieve these goals by using the orchestrator Azure Service Fabric, which is available in the Azure cloud, but also available to use on-premises, or even in a different public cloud.</span></span>

### <a name="goals"></a><span data-ttu-id="9462e-264">Objectifs</span><span class="sxs-lookup"><span data-stu-id="9462e-264">Goals</span></span>

<span data-ttu-id="9462e-265">L’objectif de cette procédure pas à pas est d’apprendre à déployer une application conteneur Windows vers un cluster Service Fabric dans Azure.</span><span class="sxs-lookup"><span data-stu-id="9462e-265">The goal of this walkthrough is to learn how to deploy a Windows Container–based application to a Service Fabric cluster in Azure.</span></span> <span data-ttu-id="9462e-266">Déploiement sur l’infrastructure de Service à partir de zéro est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="9462e-266">Deploying to Service Fabric from scratch is a two-step process:</span></span>

1.  <span data-ttu-id="9462e-267">Déployer un cluster Service Fabric vers Azure (ou un autre environnement).</span><span class="sxs-lookup"><span data-stu-id="9462e-267">Deploy a Service Fabric cluster to Azure (or to a different environment).</span></span>

2.  <span data-ttu-id="9462e-268">Déployer l’application et les ressources associées au cluster Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="9462e-268">Deploy the application and related resources to the Service Fabric cluster.</span></span>

### <a name="scenarios"></a><span data-ttu-id="9462e-269">Scénarios</span><span class="sxs-lookup"><span data-stu-id="9462e-269">Scenarios</span></span>

#### <a name="scenario-a-deploy-directly-to-a-service-fabric-cluster-from-a-dev-environment"></a><span data-ttu-id="9462e-270">Scénario a : les déployer directement à un cluster Service Fabric à partir d’un environnement de développement</span><span class="sxs-lookup"><span data-stu-id="9462e-270">Scenario A: Deploy directly to a Service Fabric cluster from a dev environment</span></span>

![Déployer directement sur un cluster Service Fabric à partir d’un environnement de développement](./media/image5-9.png)

> <span data-ttu-id="9462e-272">**Figure 5-9**.</span><span class="sxs-lookup"><span data-stu-id="9462e-272">**Figure 5-9.**</span></span> <span data-ttu-id="9462e-273">Déployer directement sur un cluster Service Fabric à partir d’un environnement de développement</span><span class="sxs-lookup"><span data-stu-id="9462e-273">Deploy directly to a Service Fabric cluster from a development environment</span></span>

### <a name="scenario-b-deploy-to-a-service-fabric-cluster-from-cicd-pipelines-in-team-services"></a><span data-ttu-id="9462e-274">Scénario b : déployer vers un cluster Service Fabric à partir de l’élément de configuration/CD pipelines dans Team Services</span><span class="sxs-lookup"><span data-stu-id="9462e-274">Scenario B: Deploy to a Service Fabric cluster from CI/CD pipelines in Team Services</span></span>

![Déployer vers un cluster Service Fabric à partir de l’élément de configuration/CD des pipelines dans Visual Studio Team Services](./media/image5-10.png)

> <span data-ttu-id="9462e-276">**Figure 5-10.**</span><span class="sxs-lookup"><span data-stu-id="9462e-276">**Figure 5-10.**</span></span> <span data-ttu-id="9462e-277">Déployer vers un cluster Service Fabric à partir de l’élément de configuration/CD des pipelines dans Visual Studio Team Services</span><span class="sxs-lookup"><span data-stu-id="9462e-277">Deploy to a Service Fabric cluster from CI/CD pipelines in Visual Studio Team Services</span></span>

## <a name="benefits"></a><span data-ttu-id="9462e-278">Avantages</span><span class="sxs-lookup"><span data-stu-id="9462e-278">Benefits</span></span>

<span data-ttu-id="9462e-279">Les avantages du déploiement vers un cluster Service fabric sont semblables aux avantages de Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="9462e-279">The benefits of deploying to a cluster in Service Fabric are similar to the benefits of using Kubernetes.</span></span> <span data-ttu-id="9462e-280">Cependant, une différence est que le Service Fabric est un environnement de production plus mature pour les applications Windows par rapport à Kubernetes, qui se trouve dans une phase bêta pour les conteneurs Windows dans Kubernetes version 1.9 (2017 décembre).</span><span class="sxs-lookup"><span data-stu-id="9462e-280">One difference, though, is that Service Fabric is a more mature production environment for Windows applications compared to Kubernetes, which is in a beta phase for Windows Containers in Kubernetes version 1.9 (December 2017).</span></span> <span data-ttu-id="9462e-281">Kubernetes est un environnement plus mature pour Linux.</span><span class="sxs-lookup"><span data-stu-id="9462e-281">Kubernetes is a more mature environment for Linux.</span></span>

<span data-ttu-id="9462e-282">Le principal avantage de l’utilisation d’Azure Service Fabric est que vous obtenez un environnement de l’environnement de production dans laquelle vous pouvez faire évoluer l’application en fonction du nombre d’instances de conteneurs, vous souhaitez utiliser (évolutivité interne dans les nœuds existants), en fonction du nombre de les nœuds ou des ordinateurs virtuels du cluster (évolutivité globale du cluster).</span><span class="sxs-lookup"><span data-stu-id="9462e-282">The main benefit of using Azure Service Fabric is that you get a production-ready environment in which you can scale out the application based on the number of container instances you want to use (inner-scalability in the existing nodes), and based on the number of nodes or VMs in the cluster (global scalability of the cluster).</span></span>

<span data-ttu-id="9462e-283">Azure Service Fabric offre la portabilité de vos conteneurs et lors de la configuration de votre application.</span><span class="sxs-lookup"><span data-stu-id="9462e-283">Azure Service Fabric offers portability both for your containers and for your application configuration.</span></span> <span data-ttu-id="9462e-284">Vous pouvez avoir une infrastructure de Service de cluster dans Azure, ou installer localement dans votre centre de données.</span><span class="sxs-lookup"><span data-stu-id="9462e-284">You can have a Service Fabric cluster in Azure, or install it on-premises in your own datacenter.</span></span> <span data-ttu-id="9462e-285">Vous pouvez même installer un cluster Service Fabric dans un autre cloud, tels que [Amazon AWS](https://blogs.msdn.microsoft.com/azureservicefabric/2017/05/18/tutorial-how-to-create-a-service-fabric-standalone-cluster-with-aws-ec2-instances/).</span><span class="sxs-lookup"><span data-stu-id="9462e-285">You can even install a Service Fabric cluster in a different cloud, like [Amazon AWS](https://blogs.msdn.microsoft.com/azureservicefabric/2017/05/18/tutorial-how-to-create-a-service-fabric-standalone-cluster-with-aws-ec2-instances/).</span></span>

<span data-ttu-id="9462e-286">Avec Service Fabric, les développeurs peuvent progresser de réfléchir à des machines physiques et virtuelles à la planification d’une infrastructure orientée conteneur qui facilite les fonctionnalités suivantes, entre autres :</span><span class="sxs-lookup"><span data-stu-id="9462e-286">With Service Fabric, developers can progress from thinking about physical and virtual machines to planning a container-centric infrastructure that facilitates the following capabilities, among others:</span></span>

- <span data-ttu-id="9462e-287">Applications basées sur plusieurs conteneurs.</span><span class="sxs-lookup"><span data-stu-id="9462e-287">Applications based on multiple containers.</span></span>

- <span data-ttu-id="9462e-288">Réplication des instances de conteneurs et d’échelle horizontale.</span><span class="sxs-lookup"><span data-stu-id="9462e-288">Replicating container instances and horizontal autoscaling.</span></span>

- <span data-ttu-id="9462e-289">Attribution de noms et de découverte (par exemple, DNS interne).</span><span class="sxs-lookup"><span data-stu-id="9462e-289">Naming and discovering (for example, internal DNS).</span></span>

- <span data-ttu-id="9462e-290">L’équilibrage de charge.</span><span class="sxs-lookup"><span data-stu-id="9462e-290">Balancing loads.</span></span>

- <span data-ttu-id="9462e-291">Mises à jour propagées.</span><span class="sxs-lookup"><span data-stu-id="9462e-291">Rolling updates.</span></span>

- <span data-ttu-id="9462e-292">La distribution de clés secrètes.</span><span class="sxs-lookup"><span data-stu-id="9462e-292">Distributing secrets.</span></span>

- <span data-ttu-id="9462e-293">Vérifications de contrôle d’intégrité de l’application.</span><span class="sxs-lookup"><span data-stu-id="9462e-293">Application health checks.</span></span>

<span data-ttu-id="9462e-294">Les fonctionnalités suivantes sont exclusives dans Service Fabric (par rapport à d’autres orchestrators) :</span><span class="sxs-lookup"><span data-stu-id="9462e-294">The following capabilities are exclusive in Service Fabric (compared to other orchestrators):</span></span>

- <span data-ttu-id="9462e-295">Fonctionnalité de services avec état, par le biais du modèle d’application des Services fiables.</span><span class="sxs-lookup"><span data-stu-id="9462e-295">Stateful services capability, through the Reliable Services application model.</span></span>

- <span data-ttu-id="9462e-296">Modèle d’acteurs, par le biais du modèle d’application Reliable Actors.</span><span class="sxs-lookup"><span data-stu-id="9462e-296">Actors pattern, through the Reliable Actors application model.</span></span>

- <span data-ttu-id="9462e-297">Déployer un processus nus, en plus des conteneurs Windows ou Linux.</span><span class="sxs-lookup"><span data-stu-id="9462e-297">Deploy bare-bone processes, in addition to Windows or Linux containers.</span></span>

- <span data-ttu-id="9462e-298">Avancé des mises à jour et les vérifications d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="9462e-298">Advanced rolling updates and health checks.</span></span>

### <a name="next-steps"></a><span data-ttu-id="9462e-299">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="9462e-299">Next steps</span></span>

<span data-ttu-id="9462e-300">Explorer ce contenu plus approfondi sur le wiki de GitHub :</span><span class="sxs-lookup"><span data-stu-id="9462e-300">Explore this content more in-depth on the GitHub wiki:</span></span>

[https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-How-to-deploy-your-Windows-Containers-based-apps-into-Azure-Service-Fabric-(Including-CI-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-How-to-deploy-your-Windows-Containers-based-apps-into-Azure-Service-Fabric-(Including-CI-CD))

>[!div class="step-by-step"]
<span data-ttu-id="9462e-301">[Précédent](lift-and-shift-existing-apps-devops/migrate-to-hybrid-cloud-scenarios.md)
[Suivant](conclusions.md)</span><span class="sxs-lookup"><span data-stu-id="9462e-301">[Previous](lift-and-shift-existing-apps-devops/migrate-to-hybrid-cloud-scenarios.md)
[Next](conclusions.md)</span></span>
