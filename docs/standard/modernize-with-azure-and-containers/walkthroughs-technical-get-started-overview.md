---
title: Procédures pas à pas et les techniques obtiennent une vue d’ensemble démarrée
description: Moderniser des Applications .NET existantes avec Azure Cloud et les conteneurs Windows | Procédures pas à pas et les techniques obtiennent une vue d’ensemble démarrée
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/28/2018
ms.openlocfilehash: 27de9d1c5475855a22f2d8a3518982605277f6d9
ms.sourcegitcommit: 88f251b08bf0718ce119f3d7302f514b74895038
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2018
---
# <a name="walkthroughs-and-technical-get-started-overview"></a><span data-ttu-id="eaec5-103">Procédures pas à pas et les techniques obtiennent une vue d’ensemble démarrée</span><span class="sxs-lookup"><span data-stu-id="eaec5-103">Walkthroughs and technical get started overview</span></span>

<span data-ttu-id="eaec5-104">Pour limiter la taille de ce livre électronique, documentation technique supplémentaire et les procédures pas à pas complète étaient mis à disposition dans un référentiel GitHub.</span><span class="sxs-lookup"><span data-stu-id="eaec5-104">To limit the size of this e-book, additional technical documentation and the full walkthroughs were made available in a GitHub repository.</span></span> <span data-ttu-id="eaec5-105">La série en ligne des procédures pas à pas qui est décrite dans ce chapitre traite le programme d’installation pas à pas plusieurs environnements qui sont basées sur les conteneurs Windows et le déploiement vers Azure.</span><span class="sxs-lookup"><span data-stu-id="eaec5-105">The online series of walkthroughs that is described in this chapter covers the step-by-step setup of the multiple environments that are based on Windows Containers, and deployment to Azure.</span></span>

<span data-ttu-id="eaec5-106">Les sections suivantes expliquent ce que chaque procédure pas à pas sur ses objectifs et la vision de haut niveau et fournit un diagramme des tâches qui sont impliquées.</span><span class="sxs-lookup"><span data-stu-id="eaec5-106">The following sections explain what each walkthrough is about, its objectives and high-level vision, and provides a diagram of the tasks that are involved.</span></span> <span data-ttu-id="eaec5-107">Vous pouvez obtenir les procédures pas à pas eux-mêmes dans le *eShopModernizing* applications wiki de référentiel GitHub à [ https://github.com/dotnet-architecture/eShopModernizing/wiki ](https://github.com/dotnet-architecture/eShopModernizing/wiki).</span><span class="sxs-lookup"><span data-stu-id="eaec5-107">You can get the walkthroughs themselves in the *eShopModernizing* apps GitHub repo wiki at [https://github.com/dotnet-architecture/eShopModernizing/wiki](https://github.com/dotnet-architecture/eShopModernizing/wiki).</span></span>

## <a name="technical-walkthrough-list"></a><span data-ttu-id="eaec5-108">Liste des techniques de procédure pas à pas</span><span class="sxs-lookup"><span data-stu-id="eaec5-108">Technical walkthrough list</span></span>

<span data-ttu-id="eaec5-109">Les procédures get-started suivantes fournissent des conseils techniques cohérent et complet des exemples d’applications que vous pouvez de courbes d’élévation et MAJ en utilisant des conteneurs et ensuite déplacer à l’aide de plusieurs options de déploiement dans Azure.</span><span class="sxs-lookup"><span data-stu-id="eaec5-109">The following get-started walkthroughs provide consistent and comprehensive technical guidance for sample apps that you can lift and shift by using containers, and then move by using multiple deployment choices in Azure.</span></span>

<span data-ttu-id="eaec5-110">Chacun des procédures suivantes utilise les nouveaux exemples eShopLegacy et eShopModernizing d’applications, qui sont disponibles sur GitHub à l’adresse [ https://github.com/dotnet-architecture/eShopModernizing ](https://github.com/dotnet-architecture/eShopModernizing).</span><span class="sxs-lookup"><span data-stu-id="eaec5-110">Each of the following walkthroughs uses the new sample eShopLegacy and eShopModernizing apps, which are available on GitHub at [https://github.com/dotnet-architecture/eShopModernizing](https://github.com/dotnet-architecture/eShopModernizing).</span></span>

- <span data-ttu-id="eaec5-111">**Visite guidée de shopping hérité applications (ligne de base pour moderniser)**</span><span class="sxs-lookup"><span data-stu-id="eaec5-111">**Tour of eShop legacy apps (baseline apps to modernize)**</span></span>

- <span data-ttu-id="eaec5-112">**Mettez en conteneur de vos applications web ASP.NET existantes (Web Forms et MVC) avec des conteneurs Windows**</span><span class="sxs-lookup"><span data-stu-id="eaec5-112">**Containerize your existing ASP.NET web apps (WebForms & MVC) with Windows Containers**</span></span>

- <span data-ttu-id="eaec5-113">**Mettez en conteneur vos services WCF existants (applications multicouches) avec des conteneurs Windows**</span><span class="sxs-lookup"><span data-stu-id="eaec5-113">**Containerize your existing WCF services (N-Tier apps) with Windows Containers**</span></span>

- <span data-ttu-id="eaec5-114">**Déployer votre application basée sur les conteneurs de Windows pour les machines virtuelles Azure**</span><span class="sxs-lookup"><span data-stu-id="eaec5-114">**Deploy your Windows Containers-based app to Azure VMs**</span></span>

- <span data-ttu-id="eaec5-115">**Déployer vos applications basée sur les conteneurs de Windows à Kubernetes dans le Service de conteneur Azure**</span><span class="sxs-lookup"><span data-stu-id="eaec5-115">**Deploy your Windows Containers-based apps to Kubernetes in Azure Container Service**</span></span>

- <span data-ttu-id="eaec5-116">**Déployer vos applications basée sur les conteneurs de Windows Azure Service fabric**</span><span class="sxs-lookup"><span data-stu-id="eaec5-116">**Deploy your Windows Containers-based apps to Azure Service Fabric**</span></span>


## <a name="walkthrough-1-tour-of-eshop-legacy-apps"></a><span data-ttu-id="eaec5-117">Procédure pas à pas 1 : Visite guidée des applications héritées de shopping</span><span class="sxs-lookup"><span data-stu-id="eaec5-117">Walkthrough 1: Tour of eShop legacy apps</span></span>

### <a name="technical-walkthrough-availability"></a><span data-ttu-id="eaec5-118">Disponibilité de la procédure pas à pas technique</span><span class="sxs-lookup"><span data-stu-id="eaec5-118">Technical walkthrough availability</span></span>

<span data-ttu-id="eaec5-119">La procédure pas à pas technique complet est disponible dans le wiki de référentiel GitHub eShopModernizing :</span><span class="sxs-lookup"><span data-stu-id="eaec5-119">The full technical walkthrough is available in the eShopModernizing GitHub repo wiki:</span></span>

[<span data-ttu-id="eaec5-120">procédures pas à pas d’eShopModernizing wiki</span><span class="sxs-lookup"><span data-stu-id="eaec5-120">eShopModernizing wiki walkthroughs</span></span>](https://github.com/dotnet-architecture/eShopModernizing/wiki)


### <a name="overview"></a><span data-ttu-id="eaec5-121">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="eaec5-121">Overview</span></span>

<span data-ttu-id="eaec5-122">Dans cette procédure pas à pas, vous pouvez explorer l’implémentation initiale de trois exemples d’applications héritées.</span><span class="sxs-lookup"><span data-stu-id="eaec5-122">In this walkthrough, you can explore the initial implementation of three sample legacy applications.</span></span> <span data-ttu-id="eaec5-123">Les deux premiers exemples d’applications web une architecture monolithique et ont été créées à l’aide d’ASP.NET classique.</span><span class="sxs-lookup"><span data-stu-id="eaec5-123">The first two sample web apps have a monolithic architecture, and were created by using classic ASP.NET.</span></span> <span data-ttu-id="eaec5-124">Une application est basée sur ASP.NET 4.x MVC ; la deuxième application est basée sur les Web Forms ASP.NET 4.x.</span><span class="sxs-lookup"><span data-stu-id="eaec5-124">One application is based on ASP.NET 4.x MVC; the second application is based on ASP.NET 4.x Web Forms.</span></span> <span data-ttu-id="eaec5-125">L’application de tiers est une application à 3 couches composée d’une application Windows Forms de client et un côté serveur [Windows Communication Foundation (WCF)](../../framework/wcf/whats-wcf.md) service.</span><span class="sxs-lookup"><span data-stu-id="eaec5-125">The third app is a 3-Tier app composed by a client WinForms app and a server-side [Windows Communication Foundation (WCF)](../../framework/wcf/whats-wcf.md) service.</span></span>

<span data-ttu-id="eaec5-126">Toutes ces applications sont disponibles sur le [eShopModernizing du référentiel GitHub](https://github.com/dotnet-architecture/eShopModernizing).</span><span class="sxs-lookup"><span data-stu-id="eaec5-126">All these applications are available at the [eShopModernizing GitHub repo](https://github.com/dotnet-architecture/eShopModernizing).</span></span>

### <a name="goals"></a><span data-ttu-id="eaec5-127">Objectifs</span><span class="sxs-lookup"><span data-stu-id="eaec5-127">Goals</span></span>

<span data-ttu-id="eaec5-128">L’objectif principal de cette procédure pas à pas est simplement afin de vous familiariser avec ces applications et leur configuration et le code.</span><span class="sxs-lookup"><span data-stu-id="eaec5-128">The main goal of this walkthrough is simply to get familiar with these apps, and with their code and configuration.</span></span> <span data-ttu-id="eaec5-129">Vous pouvez configurer les applications afin qu’ils génèrent et utilisent des données fictives, sans l’aide de la base de données SQL, à des fins de test.</span><span class="sxs-lookup"><span data-stu-id="eaec5-129">You can configure the apps so that they generate and use mock data, without using the SQL database, for testing purposes.</span></span> <span data-ttu-id="eaec5-130">Cette configuration facultative est basée sur l’injection de dépendance, d’une manière découplée.</span><span class="sxs-lookup"><span data-stu-id="eaec5-130">This optional config is based on dependency injection, in a decoupled way.</span></span>

### <a name="scenario-1-aspnet-web-apps"></a><span data-ttu-id="eaec5-131">Scénario 1 : Les applications Web ASP.NET</span><span class="sxs-lookup"><span data-stu-id="eaec5-131">Scenario 1: ASP.NET Web apps</span></span>

<span data-ttu-id="eaec5-132">La figure ci-dessous illustre le scénario simple des applications web ASP.NET existants d’origine.</span><span class="sxs-lookup"><span data-stu-id="eaec5-132">The figure below shows the simple scenario of the original legacy ASP.NET web applications.</span></span>

> ![Scénario simple d’architecture des applications web ASP.NET existantes d’origine](./media/image5-1.png)
>

<span data-ttu-id="eaec5-134">À partir d’une perspective de domaine d’entreprise, les deux applications offrent la même catalogue de fonctionnalités de gestion.</span><span class="sxs-lookup"><span data-stu-id="eaec5-134">From a business domain perspective, both apps offer the same catalog management features.</span></span> <span data-ttu-id="eaec5-135">Membres de l’équipe d’entreprise Shopping utiliseriez l’application pour afficher et modifier le catalogue de produits.</span><span class="sxs-lookup"><span data-stu-id="eaec5-135">Members of the eShop enterprise team would use the app to view and edit the product catalog.</span></span> 

<span data-ttu-id="eaec5-136">La figure suivante montre les captures d’écran de l’application initiale.</span><span class="sxs-lookup"><span data-stu-id="eaec5-136">The next figure shows the initial app screenshots.</span></span>

![Applications ASP.NET MVC et les Web Forms ASP.NET (technologies existantes/hérité)](./media/image5-2.png)

<span data-ttu-id="eaec5-138">Dépendances dans ASP.NET 4.x ou des versions antérieures (soit pour MVC ou Web Forms) signifie que ces applications ne s’exécutent sur .NET Core, sauf si le code est entièrement réécrit à l’aide d’ASP.NET MVC de base.</span><span class="sxs-lookup"><span data-stu-id="eaec5-138">Dependencies in ASP.NET 4.x or earlier versions (either for MVC or for Web Forms) means that these applications won’t run on .NET Core unless the code is fully rewritten by using ASP.NET Core MVC.</span></span> 

### <a name="scenario-2-wcf-service-and-winforms-client-app-3-tier-app"></a><span data-ttu-id="eaec5-139">Scénario 2 : Service WCF et WinForms client application (application de niveau 3)</span><span class="sxs-lookup"><span data-stu-id="eaec5-139">Scenario 2: WCF service and WinForms client app (3-Tier app)</span></span>

<span data-ttu-id="eaec5-140">La figure ci-dessous illustre le scénario simple de l’application héritée à 3 couches d’origine.</span><span class="sxs-lookup"><span data-stu-id="eaec5-140">The figure below shows the simple scenario of the original 3-Tier legacy application.</span></span>

> ![Scénario simple d’architecture de l’application à 3 couches héritée d’origine avec un service WCF et d’une application WinForms client](./media/image5-1.5.png)
>

### <a name="benefits"></a><span data-ttu-id="eaec5-142">Avantages</span><span class="sxs-lookup"><span data-stu-id="eaec5-142">Benefits</span></span>

<span data-ttu-id="eaec5-143">Les avantages de cette procédure pas à pas sont simples : simplement vous familiariser avec le code et les applications initiales.</span><span class="sxs-lookup"><span data-stu-id="eaec5-143">The benefits of this walkthrough are simple: Just get familiar with the code and initial apps.</span></span>

### <a name="next-steps"></a><span data-ttu-id="eaec5-144">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="eaec5-144">Next steps</span></span>

<span data-ttu-id="eaec5-145">Explorer ce contenu plus approfondi sur le wiki de GitHub :</span><span class="sxs-lookup"><span data-stu-id="eaec5-145">Explore this content more in-depth on the GitHub wiki:</span></span>

  - [<span data-ttu-id="eaec5-146">Visite guidée sur la ligne de base ASP.NET MVC et les applications Web Forms « héritées »</span><span class="sxs-lookup"><span data-stu-id="eaec5-146">Tour on the baseline ASP.NET MVC and Web Forms “legacy” apps</span></span>](https://github.com/dotnet-architecture/eShopModernizing/wiki/01.-Tour-on-the-ASP.NET-MVC-and-WebForms-apps-implementation-code)
  - [<span data-ttu-id="eaec5-147">Visite sur le service WCF de base et d’application WinForms « héritée » (niveau 3)</span><span class="sxs-lookup"><span data-stu-id="eaec5-147">Tour on the baseline WCF service and WinForms (3-Tier) “legacy” app</span></span>](https://github.com/dotnet-architecture/eShopModernizing/wiki/21.-Tour-on-the-WCF-service-and-WinForms-apps)


## <a name="walkthrough-2-containerize-your-existing-net-applications-with-windows-containers"></a><span data-ttu-id="eaec5-148">Procédure 2 : Mettez en conteneur vos applications .NET existantes avec des conteneurs Windows</span><span class="sxs-lookup"><span data-stu-id="eaec5-148">Walkthrough 2: Containerize your existing .NET applications with Windows Containers</span></span>

### <a name="overview"></a><span data-ttu-id="eaec5-149">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="eaec5-149">Overview</span></span>

<span data-ttu-id="eaec5-150">Les conteneurs Windows permet d’améliorer le déploiement des applications .NET existantes, telles que celles basées sur MVC, Web Forms ou WCF, pour les environnements de test, de développement et de production.</span><span class="sxs-lookup"><span data-stu-id="eaec5-150">Use Windows Containers to improve deployment of existing .NET applications, like those based on MVC, Web Forms, or WCF, to production, development, and test environments.</span></span>

### <a name="goals"></a><span data-ttu-id="eaec5-151">Objectifs</span><span class="sxs-lookup"><span data-stu-id="eaec5-151">Goals</span></span>

<span data-ttu-id="eaec5-152">L’objectif de cette procédure pas à pas est de vous montrer plusieurs options pour containerizing une application .NET Framework existante.</span><span class="sxs-lookup"><span data-stu-id="eaec5-152">The goal of this walkthrough is to show you several options for containerizing an existing .NET Framework application.</span></span> <span data-ttu-id="eaec5-153">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="eaec5-153">You can:</span></span>

- <span data-ttu-id="eaec5-154">Mettez en conteneur de votre application à l’aide de [Visual Studio 2017 Tools pour Docker](/aspnet/core/host-and-deploy/docker/visual-studio-tools-for-docker) (Visual Studio 2017 ou versions ultérieures).</span><span class="sxs-lookup"><span data-stu-id="eaec5-154">Containerize your application by using [Visual Studio 2017 Tools for Docker](/aspnet/core/host-and-deploy/docker/visual-studio-tools-for-docker) (Visual Studio 2017 or later versions).</span></span>

- <span data-ttu-id="eaec5-155">Mettez en conteneur de votre application en ajoutant manuellement un [Dockerfile](https://docs.docker.com/engine/reference/builder/), puis en utilisant la [Docker CLI](https://docs.docker.com/engine/reference/commandline/cli/).</span><span class="sxs-lookup"><span data-stu-id="eaec5-155">Containerize your application by manually adding a [Dockerfile](https://docs.docker.com/engine/reference/builder/), and then using the [Docker CLI](https://docs.docker.com/engine/reference/commandline/cli/).</span></span>

- <span data-ttu-id="eaec5-156">Mettez en conteneur de votre application à l’aide de la [Img2Docker](https://github.com/docker/communitytools-image2docker-win) outil (outil open source à partir de Docker).</span><span class="sxs-lookup"><span data-stu-id="eaec5-156">Containerize your application by using the [Img2Docker](https://github.com/docker/communitytools-image2docker-win) tool (an open-source tool from Docker).</span></span>

<span data-ttu-id="eaec5-157">Cette procédure pas à pas se concentre sur les outils de 2017 Visual Studio pour l’approche de Docker, mais les deux autres approches sont relativement similaires en ce qui concerne l’utilisation des fichiers Dockerfile.</span><span class="sxs-lookup"><span data-stu-id="eaec5-157">This walkthrough focuses on the Visual Studio 2017 Tools for Docker approach, but the other two approaches are fairly similar in regard to using Dockerfiles.</span></span>

### <a name="scenario-1-containerized-aspnet-web-apps"></a><span data-ttu-id="eaec5-158">Scénario 1 : Les applications web ASP.NET en conteneur</span><span class="sxs-lookup"><span data-stu-id="eaec5-158">Scenario 1: Containerized ASP.NET web apps</span></span>

<span data-ttu-id="eaec5-159">Figure ci-dessous illustre le scénario pour les applications d’applications en conteneur Shopping web hérité.</span><span class="sxs-lookup"><span data-stu-id="eaec5-159">Figure below shows the scenario for containerized eShop legacy web apps applications.</span></span>

> ![Diagramme d’architecture simplifiée de placées dans des conteneurs dans un environnement de développement des applications ASP.NET](./media/image5-3.png)
>


### <a name="scenario-2-containerized-wcf-service"></a><span data-ttu-id="eaec5-161">Scénario 2 : Service WCF en conteneur</span><span class="sxs-lookup"><span data-stu-id="eaec5-161">Scenario 2: Containerized WCF service</span></span>

<span data-ttu-id="eaec5-162">La figure ci-dessous illustre le scénario pour une application à 3 couches avec un service WCF en conteneur.</span><span class="sxs-lookup"><span data-stu-id="eaec5-162">Figure below shows the scenario for a 3-Tier app with a containerized WCF service.</span></span> 

> ![Diagramme d’architecture du service WCF en conteneur dans un environnement de développement de simplifiée](./media/image5-3.5.png)
>

### <a name="benefits"></a><span data-ttu-id="eaec5-164">Avantages</span><span class="sxs-lookup"><span data-stu-id="eaec5-164">Benefits</span></span>

<span data-ttu-id="eaec5-165">Il existe des avantages à l’exécution de votre application monolithique dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="eaec5-165">There are advantages to running your monolithic application in a container.</span></span> <span data-ttu-id="eaec5-166">Tout d’abord, vous créez une image de l’application.</span><span class="sxs-lookup"><span data-stu-id="eaec5-166">First, you create an image for the application.</span></span> <span data-ttu-id="eaec5-167">À ce stade, chaque déploiement s’exécute dans le même environnement.</span><span class="sxs-lookup"><span data-stu-id="eaec5-167">From that point on, every deployment runs in the same environment.</span></span> <span data-ttu-id="eaec5-168">Chaque conteneur utilise la même version du système d’exploitation, a la même version de dépendances installé, utilise la même version du .NET framework et est construit à l’aide du même processus.</span><span class="sxs-lookup"><span data-stu-id="eaec5-168">Every container uses the same OS version, has the same version of dependencies installed, uses the same .NET framework version, and is built by using the same process.</span></span> <span data-ttu-id="eaec5-169">En fait, vous contrôlez les dépendances de votre application à l’aide d’une image Docker.</span><span class="sxs-lookup"><span data-stu-id="eaec5-169">Basically, you control the dependencies of your application by using a Docker image.</span></span> <span data-ttu-id="eaec5-170">Lorsque vous déployez les conteneurs, les dépendances se déplacent avec l’application.</span><span class="sxs-lookup"><span data-stu-id="eaec5-170">The dependencies travel with the application when you deploy the containers.</span></span>

<span data-ttu-id="eaec5-171">Un autre avantage est que les développeurs peuvent exécuter l’application dans l’environnement cohérent qui est fourni par les conteneurs Windows.</span><span class="sxs-lookup"><span data-stu-id="eaec5-171">An additional benefit is that developers can run the application in the consistent environment that's provided by Windows Containers.</span></span> <span data-ttu-id="eaec5-172">Les problèmes qui apparaissent uniquement dans certaines versions peuvent être détectées immédiatement, au lieu de surfaces dans un environnement intermédiaire ou de production.</span><span class="sxs-lookup"><span data-stu-id="eaec5-172">Issues that appear only with certain versions can be spotted immediately, instead of surfacing in a staging or production environment.</span></span> <span data-ttu-id="eaec5-173">Les différences dans les environnements de développement utilisés par les membres de l’équipe de développement a d’importance inférieure lorsque les applications s’exécutent dans des conteneurs.</span><span class="sxs-lookup"><span data-stu-id="eaec5-173">Differences in development environments used by members of the development team matter less when applications run in containers.</span></span>

<span data-ttu-id="eaec5-174">Les applications en conteneur possèdent également une courbe plate de la montée en puissance parallèle.</span><span class="sxs-lookup"><span data-stu-id="eaec5-174">Containerized applications also have a flatter scale-out curve.</span></span> <span data-ttu-id="eaec5-175">Les applications en conteneur permettent d’avoir plus d’application et les instances de service (basés sur les conteneurs) dans une machine virtuelle ou d’un ordinateur physique par rapport aux déploiements d’application normal par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="eaec5-175">Containerized apps enable you to have more application and service instances (based on containers) in a VM or physical machine compared to regular application deployments per machine.</span></span> <span data-ttu-id="eaec5-176">Cela se traduit par densité plus élevée et moins nécessaire des ressources, notamment lorsque vous utilisez orchestrators comme Kubernetes ou Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="eaec5-176">This translates to higher density and fewer required resources, especially when you use orchestrators like Kubernetes or Service Fabric.</span></span>

<span data-ttu-id="eaec5-177">CONTENEURISATION des données, dans des situations idéale, ne nécessitent pas d’apporter des modifications au code d’application (C\#).</span><span class="sxs-lookup"><span data-stu-id="eaec5-177">Containerization, in ideal situations, does not require making any changes to the application code (C\#).</span></span> <span data-ttu-id="eaec5-178">Dans la plupart des scénarios, vous devez simplement les fichiers de métadonnées de déploiement (fichiers Dockerfile et Docker Compose) Docker.</span><span class="sxs-lookup"><span data-stu-id="eaec5-178">In most scenarios, you just need the Docker deployment metadata files (Dockerfiles and Docker Compose files).</span></span>

### <a name="next-steps"></a><span data-ttu-id="eaec5-179">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="eaec5-179">Next steps</span></span>

<span data-ttu-id="eaec5-180">Explorer ce contenu plus approfondi sur le wiki de GitHub :</span><span class="sxs-lookup"><span data-stu-id="eaec5-180">Explore this content more in-depth on the GitHub wiki:</span></span>

  - [<span data-ttu-id="eaec5-181">Comment mettez en conteneur d’applications web .NET Framework avec les conteneurs Windows et Docker</span><span class="sxs-lookup"><span data-stu-id="eaec5-181">How to containerize the .NET Framework web apps with Windows Containers and Docker</span></span>](https://github.com/dotnet-architecture/eShopModernizing/wiki/02.-How-to-containerize-the-.NET-Framework-web-apps-with-Windows-Containers-and-Docker)
  - [<span data-ttu-id="eaec5-182">Ajout d’un Support Docker à un service WCF</span><span class="sxs-lookup"><span data-stu-id="eaec5-182">Adding Docker Support to a WCF service</span></span>](https://github.com/dotnet-architecture/eShopModernizing/wiki/22.-Adding-Docker-Support)



## <a name="walkthrough-3-deploy-your-windows-containers-based-app-to-azure-vms"></a><span data-ttu-id="eaec5-183">Procédure 3 : Déployer votre application basée sur les conteneurs de Windows sur les machines virtuelles Azure</span><span class="sxs-lookup"><span data-stu-id="eaec5-183">Walkthrough 3: Deploy your Windows Containers-based app to Azure VMs</span></span>

### <a name="technical-walkthrough-availability"></a><span data-ttu-id="eaec5-184">Disponibilité de la procédure pas à pas technique</span><span class="sxs-lookup"><span data-stu-id="eaec5-184">Technical walkthrough availability</span></span>

<span data-ttu-id="eaec5-185">La procédure pas à pas technique complet est disponible dans le wiki de référentiel GitHub eShopModernizing : [https://github.com/dotnet-architecture/eShopModernizing/wiki/03.-How-to-deploy-your-Windows-Containers-based-app-into-Azure-VMs-(Including-CI-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/03.-How-to-deploy-your-Windows-Containers-based-app-into-Azure-VMs-(Including-CI-CD))</span><span class="sxs-lookup"><span data-stu-id="eaec5-185">The full technical walkthrough is available in the eShopModernizing GitHub repo wiki: [https://github.com/dotnet-architecture/eShopModernizing/wiki/03.-How-to-deploy-your-Windows-Containers-based-app-into-Azure-VMs-(Including-CI-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/03.-How-to-deploy-your-Windows-Containers-based-app-into-Azure-VMs-(Including-CI-CD))</span></span>

### <a name="overview"></a><span data-ttu-id="eaec5-186">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="eaec5-186">Overview</span></span>

<span data-ttu-id="eaec5-187">Déploiement sur un hôte Docker sur un serveur Windows Server 2016 Virtual Machine (VM) dans Azure vous permet de définir rapidement des environnements de développement/test/mise en lots.</span><span class="sxs-lookup"><span data-stu-id="eaec5-187">Deploying to a Docker host on a Windows Server 2016 Virtual Machine (VM) in Azure lets you quickly set up development/test/staging environments.</span></span> <span data-ttu-id="eaec5-188">Elle vous donne également un emplacement commun pour les testeurs ou les utilisateurs des activités à valider l’application.</span><span class="sxs-lookup"><span data-stu-id="eaec5-188">It also gives you a common place for testers or business users to validate the app.</span></span> <span data-ttu-id="eaec5-189">Machines virtuelles peuvent également être infrastructure valide comme les environnements de production de Service (IaaS).</span><span class="sxs-lookup"><span data-stu-id="eaec5-189">VMs also can be valid Infrastucture as a Service (IaaS) production environments.</span></span>

### <a name="goals"></a><span data-ttu-id="eaec5-190">Objectifs</span><span class="sxs-lookup"><span data-stu-id="eaec5-190">Goals</span></span>

<span data-ttu-id="eaec5-191">L’objectif de cette procédure pas à pas est de vous montrer les plusieurs alternatives que vous avez lorsque vous déployez les conteneurs Windows sur les machines virtuelles Azure qui sont basés sur Windows Server 2016 ou versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="eaec5-191">The goal of this walkthrough is to show you the multiple alternatives you have when you deploy Windows Containers to Azure VMs that are based on Windows Server 2016 or later versions.</span></span>

### <a name="scenarios"></a><span data-ttu-id="eaec5-192">Scénarios</span><span class="sxs-lookup"><span data-stu-id="eaec5-192">Scenarios</span></span>

<span data-ttu-id="eaec5-193">Plusieurs scénarios sont traités dans cette procédure pas à pas.</span><span class="sxs-lookup"><span data-stu-id="eaec5-193">Several scenarios are covered in this walkthrough.</span></span>

#### <a name="scenario-a-deploy-to-an-azure-vm-from-a-dev-pc-through-docker-engine-connection"></a><span data-ttu-id="eaec5-194">Scénario a : les déployer sur une machine virtuelle Azure à partir d’un ordinateur de développement via la connexion du moteur Docker</span><span class="sxs-lookup"><span data-stu-id="eaec5-194">Scenario A: Deploy to an Azure VM from a dev PC through Docker Engine connection</span></span>

![Déployer sur une machine virtuelle Azure à partir d’un ordinateur de développement via une connexion du moteur Docker](./media/image5-4.png)

> <span data-ttu-id="eaec5-196">**Figure 5-4.**</span><span class="sxs-lookup"><span data-stu-id="eaec5-196">**Figure 5-4.**</span></span> <span data-ttu-id="eaec5-197">Déployer sur une machine virtuelle Azure à partir d’un ordinateur de développement via une connexion du moteur Docker</span><span class="sxs-lookup"><span data-stu-id="eaec5-197">Deploy to an Azure VM from a dev PC through a Docker Engine connection</span></span>

#### <a name="scenario-b-deploy-to-an-azure-vm-through-a-docker-registry"></a><span data-ttu-id="eaec5-198">Scénario b : déployer sur une machine virtuelle Azure via un Registre Docker</span><span class="sxs-lookup"><span data-stu-id="eaec5-198">Scenario B: Deploy to an Azure VM through a Docker Registry</span></span>

![Déployer sur une machine virtuelle Azure via un Registre Docker](./media/image5-5.png)

> <span data-ttu-id="eaec5-200">**Figure 5-5.**</span><span class="sxs-lookup"><span data-stu-id="eaec5-200">**Figure 5-5.**</span></span> <span data-ttu-id="eaec5-201">Déployer sur une machine virtuelle Azure via un Registre Docker</span><span class="sxs-lookup"><span data-stu-id="eaec5-201">Deploy to an Azure VM through a Docker Registry</span></span>

#### <a name="scenario-c-deploy-to-an-azure-vm-from-cicd-pipelines-in-visual-studio-team-services"></a><span data-ttu-id="eaec5-202">Scénario c : déployer sur une machine virtuelle Azure à partir de l’élément de configuration/CD des pipelines dans Visual Studio Team Services</span><span class="sxs-lookup"><span data-stu-id="eaec5-202">Scenario C: Deploy to an Azure VM from CI/CD pipelines in Visual Studio Team Services</span></span>

![Déployer sur une machine virtuelle Azure à partir de CD / l’élément de configuration des pipelines dans Visual Studio Team Services](./media/image5-6.png)

> <span data-ttu-id="eaec5-204">**Figure 5-6.**</span><span class="sxs-lookup"><span data-stu-id="eaec5-204">**Figure 5-6.**</span></span> <span data-ttu-id="eaec5-205">Déployer sur une machine virtuelle Azure à partir de CD / l’élément de configuration des pipelines dans Visual Studio Team Services</span><span class="sxs-lookup"><span data-stu-id="eaec5-205">Deploy to an Azure VM from CI/CD pipelines in Visual Studio Team Services</span></span>

### <a name="azure-vms-for-windows-containers"></a><span data-ttu-id="eaec5-206">Machines virtuelles Azure pour les conteneurs Windows</span><span class="sxs-lookup"><span data-stu-id="eaec5-206">Azure VMs for Windows Containers</span></span>

<span data-ttu-id="eaec5-207">Machines virtuelles Azure pour les conteneurs Windows sont basés sur Windows Server 2016, Windows 10 ou versions ultérieures de machines virtuelles, à la fois avec le moteur Docker configuré.</span><span class="sxs-lookup"><span data-stu-id="eaec5-207">Azure VMs for Windows Containers are VMs based on Windows Server 2016, Windows 10, or later versions, both with Docker Engine set up.</span></span> <span data-ttu-id="eaec5-208">Dans la plupart des cas, Windows Server 2016 est utilisé dans les machines virtuelles Azure.</span><span class="sxs-lookup"><span data-stu-id="eaec5-208">In most cases, Windows Server 2016 is used in the Azure VMs.</span></span>

<span data-ttu-id="eaec5-209">Azure fournit actuellement une machine virtuelle nommée **Windows Server 2016 avec des conteneurs**.</span><span class="sxs-lookup"><span data-stu-id="eaec5-209">Azure currently provides a VM named **Windows Server 2016 with Containers**.</span></span> <span data-ttu-id="eaec5-210">Vous pouvez utiliser cet ordinateur virtuel pour essayer la nouvelle fonctionnalité de conteneur Windows Server avec Windows Server Core ou Nano Server de Windows.</span><span class="sxs-lookup"><span data-stu-id="eaec5-210">You can use this VM to try the new Windows Server Container feature, with either Windows Server Core or Windows Nano Server.</span></span> <span data-ttu-id="eaec5-211">Les images de système d’exploitation de conteneur sont installés, et ensuite l’ordinateur virtuel est prêt à être utilisé avec Docker.</span><span class="sxs-lookup"><span data-stu-id="eaec5-211">Container OS images are installed, and then the VM is ready to use with Docker.</span></span>

### <a name="benefits"></a><span data-ttu-id="eaec5-212">Avantages</span><span class="sxs-lookup"><span data-stu-id="eaec5-212">Benefits</span></span>

<span data-ttu-id="eaec5-213">Bien que les conteneurs Windows peuvent être déployées sur local Windows Server 2016 machines virtuelles, lorsque vous déployez dans Azure, vous obtenez un moyen plus simple pour commencer, machines virtuelles de prêt à utiliser Windows Server conteneur.</span><span class="sxs-lookup"><span data-stu-id="eaec5-213">Although Windows Containers can be deployed to on-premises Windows Server 2016 VMs, when you deploy to Azure, you get an easier way to get started, with ready-to-use Windows Server Container VMs.</span></span> <span data-ttu-id="eaec5-214">Vous obtenez également un emplacement commun en ligne qui est accessible aux testeurs et évolutivité automatique par le biais des machines virtuelles Azure identiques.</span><span class="sxs-lookup"><span data-stu-id="eaec5-214">You also get a common online location that’s accessible to testers, and automatic scalability through Azure virtual machine scale sets.</span></span>

### <a name="next-steps"></a><span data-ttu-id="eaec5-215">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="eaec5-215">Next steps</span></span>

<span data-ttu-id="eaec5-216">Explorer ce contenu plus approfondi sur le wiki de GitHub :</span><span class="sxs-lookup"><span data-stu-id="eaec5-216">Explore this content more in-depth on the GitHub wiki:</span></span>

[https://github.com/dotnet-architecture/eShopModernizing/wiki/03.-How-to-deploy-your-Windows-Containers-based-app-into-Azure-VMs-(Including-CI-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/03.-How-to-deploy-your-Windows-Containers-based-app-into-Azure-VMs-(Including-CI-CD))

## <a name="walkthrough-4-deploy-your-windows-containers-based-apps-to-azure-container-instances-aci"></a><span data-ttu-id="eaec5-217">Procédure 4 : Déployer vos applications basée sur les conteneurs de Windows sur les Instances du conteneur Azure (ACI)</span><span class="sxs-lookup"><span data-stu-id="eaec5-217">Walkthrough 4: Deploy your Windows Containers-based apps to Azure Container Instances (ACI)</span></span>

### <a name="technical-walkthrough-availability"></a><span data-ttu-id="eaec5-218">Disponibilité de la procédure pas à pas technique</span><span class="sxs-lookup"><span data-stu-id="eaec5-218">Technical walkthrough availability</span></span>

<span data-ttu-id="eaec5-219">La procédure pas à pas technique complet est disponible dans le wiki de référentiel GitHub eShopModernizing :</span><span class="sxs-lookup"><span data-stu-id="eaec5-219">The full technical walkthrough is available in the eShopModernizing GitHub repo wiki:</span></span>

<span data-ttu-id="eaec5-220">[Déploiement d’applications sur ACI (Instances de conteneur Azure)](https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-Deploying-the-Apps-to-ACI-(Azure-Container-Instances))</span><span class="sxs-lookup"><span data-stu-id="eaec5-220">[Deploying the Apps to ACI (Azure Container Instances)](https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-Deploying-the-Apps-to-ACI-(Azure-Container-Instances))</span></span>

### <a name="overview"></a><span data-ttu-id="eaec5-221">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="eaec5-221">Overview</span></span>

<span data-ttu-id="eaec5-222">[Instances du conteneur Azure (ACI)](https://docs.microsoft.com/en-us/azure/container-instances/) est la plus rapide pour un environnement de développement/test/mise en lots de conteneurs où vous pouvez déployer des instances uniques de conteneurs.</span><span class="sxs-lookup"><span data-stu-id="eaec5-222">[Azure Container Instances (ACI)](https://docs.microsoft.com/en-us/azure/container-instances/) is the quickest way to have a Containers dev/test/staging environment where you can deploy single instances of containers.</span></span>

### <a name="goals"></a><span data-ttu-id="eaec5-223">Objectifs</span><span class="sxs-lookup"><span data-stu-id="eaec5-223">Goals</span></span>

<span data-ttu-id="eaec5-224">Cette procédure pas à pas vous montre les principaux scénarios lors du déploiement de conteneurs Windows Azure conteneur Instances (ACI) et comment vous pouvez déployer des applications d’eShopModernizing dans ACI.</span><span class="sxs-lookup"><span data-stu-id="eaec5-224">This walkthrough shows you the main scenarios when deploying Windows Containers to Azure Container Instances (ACI) and how you can deploy eShopModernizing Apps into ACI.</span></span>

### <a name="scenarios"></a><span data-ttu-id="eaec5-225">Scénarios</span><span class="sxs-lookup"><span data-stu-id="eaec5-225">Scenarios</span></span>

<span data-ttu-id="eaec5-226">Il peut y avoir des variations sur le déploiement des applications eShopModernizing dans ACI telles que le déploiement d’un ou toutes les applications (application MVC, Web Forms application ou service WCF).</span><span class="sxs-lookup"><span data-stu-id="eaec5-226">There can be variations about deploying the eShopModernizing apps into ACI such as deploying just one or all of the apps (MVC app, WebForms app or WCF service).</span></span> <span data-ttu-id="eaec5-227">Dans le scénario suivant, illustré ci-dessous, vous pouvez voir l’application ASP.NET MVC ainsi que le conteneur de SQL Server que les deux déployés en tant que conteneurs dans ACI (Instances de conteneurs Azure).</span><span class="sxs-lookup"><span data-stu-id="eaec5-227">In the following scenario shown below you can see the ASP.NET MVC app plus the SQL Server container both of them deployed as containers into ACI (Azure Container Instances).</span></span>

![Déploiement ACI à partir d’un environnement de développement](./media/image5-3.5.6.png)

### <a name="benefits"></a><span data-ttu-id="eaec5-229">Avantages</span><span class="sxs-lookup"><span data-stu-id="eaec5-229">Benefits</span></span>

<span data-ttu-id="eaec5-230">Les Instances du conteneur Azure facilite créer et gérer des conteneurs Docker dans Azure, sans avoir à configurer des machines virtuelles ou arrêter un service de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="eaec5-230">Azure Container Instances makes it easy to create and manage Docker containers in Azure, without having to provision virtual machines or adopt a higher-level service.</span></span> <span data-ttu-id="eaec5-231">Avec ACI, vous pouvez directement déployer un conteneur Windows dans Azure et l’exposer à internet avec un nom de domaine complet (FQDN) en quelques secondes (à condition que vous avez l’image de conteneur Windows prêt dans un Registre Docker Hub d’ancrage ou conteneur Azure Registre).</span><span class="sxs-lookup"><span data-stu-id="eaec5-231">With ACI, you can directly deploy a Windows container in Azure and expose it to the internet with a fully qualified domain name (FQDN) in a matter of seconds (Provided that you have the Windows Container image ready in a Docker registry like Docker Hub or Azure Container Registry).</span></span>

### <a name="considerations"></a><span data-ttu-id="eaec5-232">Éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="eaec5-232">Considerations</span></span>

<span data-ttu-id="eaec5-233">Déploiement de conteneurs Windows avec le .NET Framework complet / ASP.NET ou SQL Server dans Azure conteneur Instances (ACI) n’est pas tout à fait aussi rapide que le déploiement sur un hôte Docker régulière (par exemple, Windows Server 2016 avec des conteneurs Windows), car l’image Docker doit être téléchargés à chaque fois (extraite à partir du Registre Docker) et la taille de l’image de conteneur SQL (15.1 Go) et l’image de conteneur ASP.NET (13.9 Go) est importante, mais il est beaucoup moins coûteuse que la conservation de votre propre hôte docker (définitivement en ligne Windows Server 2016 avec l’ordinateur virtuel de conteneurs Windows dans Azure) ne pas de mentionner un ensemble orchestrator comme Kubernetes dans Azure (AKS/ACS) ou de l’infrastructure de Service Azure qui sont, quant à eux, excellentes choix pour les déploiements de production.</span><span class="sxs-lookup"><span data-stu-id="eaec5-233">Deploying Windows Containers with either full .NET Framework / ASP.NET or SQL Server into Azure Container Instances (ACI) is not quite as fast as deploying to a regular Docker Host (like a Windows Server 2016 with Windows Containers) because the Docker image has to be downloaded (pulled from the Docker registry) every time and the sizes of the SQL container image (15.1 GB) and the ASP.NET container image (13.9 GB) are significantly large, however it is much cheaper than maintaining your own docker host (permanently on-line Windows Server 2016 with Windows Containers VM in Azure) not to mention a whole orchestrator like Kubernetes in Azure (AKS/ACS) or Azure Service Fabric which are, on the other hand, great choices for production deployments.</span></span>

<span data-ttu-id="eaec5-234">En tant que principale conclusion, à l’aide d’Instances de conteneurs Azure est une option très intéressante pour les scénarios de développement et de Test et pour les pipelines de l’élément de configuration/CD.</span><span class="sxs-lookup"><span data-stu-id="eaec5-234">As main conclusion, using Azure Container Instances is a very compelling option for Dev/Test scenarios and for CI/CD pipelines.</span></span>

## <a name="next-steps"></a><span data-ttu-id="eaec5-235">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="eaec5-235">Next steps</span></span>

<span data-ttu-id="eaec5-236">Explorer ce contenu plus approfondi sur le wiki de GitHub :</span><span class="sxs-lookup"><span data-stu-id="eaec5-236">Explore this content more in-depth on the GitHub wiki:</span></span> 

[https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-Deploying-the-Apps-to-ACI-(Azure-Container-Instances)](https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-Deploying-the-Apps-to-ACI-(Azure-Container-Instances)TBD)


## <a name="walkthrough-5-deploy-your-windows-containers-based-apps-to-kubernetes-in-azure-container-service"></a><span data-ttu-id="eaec5-237">Procédure 5 : Déployer vos applications de basée sur les conteneurs Windows sur Kubernetes dans le Service de conteneur Azure</span><span class="sxs-lookup"><span data-stu-id="eaec5-237">Walkthrough 5: Deploy your Windows Containers-based apps to Kubernetes in Azure Container Service</span></span>

### <a name="technical-walkthrough-availability"></a><span data-ttu-id="eaec5-238">Disponibilité de la procédure pas à pas technique</span><span class="sxs-lookup"><span data-stu-id="eaec5-238">Technical walkthrough availability</span></span>

<span data-ttu-id="eaec5-239">La procédure pas à pas technique complet est disponible dans le wiki de référentiel GitHub eShopModernizing :</span><span class="sxs-lookup"><span data-stu-id="eaec5-239">The full technical walkthrough is available in the eShopModernizing GitHub repo wiki:</span></span>

[https://github.com/dotnet-architecture/eShopModernizing/wiki/04.-How-to-deploy-your-Windows-Containers-based-apps-into-Kubernetes-in-Azure-Container-Service-(Including-C-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/04.-How-to-deploy-your-Windows-Containers-based-apps-into-Kubernetes-in-Azure-Container-Service-(Including-C-CD))

### <a name="overview"></a><span data-ttu-id="eaec5-240">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="eaec5-240">Overview</span></span>

<span data-ttu-id="eaec5-241">Une application qui est basée sur les conteneurs Windows devra rapidement utilisent des plateformes, éloigner encore davantage de machines virtuelles IaaS.</span><span class="sxs-lookup"><span data-stu-id="eaec5-241">An application that's based on Windows Containers will quickly need to use platforms, moving even further away from IaaS VMs.</span></span> <span data-ttu-id="eaec5-242">Cela est nécessaire pour facilement atteindre une haute évolutivité et mieux automatisée de l’évolutivité et pour une amélioration significative dans automatisée déploiements et le contrôle de version.</span><span class="sxs-lookup"><span data-stu-id="eaec5-242">This is needed to easily achieve high scalability and better automated scalability, and for a significant improvement in automated deployments and versioning.</span></span> <span data-ttu-id="eaec5-243">Vous pouvez atteindre ces objectifs à l’aide de l’orchestrateur [Kubernetes](https://kubernetes.io/), disponible dans [Azure conteneur Services](https://azure.microsoft.com/services/container-service/).</span><span class="sxs-lookup"><span data-stu-id="eaec5-243">You can achieve these goals by using the orchestrator [Kubernetes](https://kubernetes.io/), available in [Azure Container Services](https://azure.microsoft.com/services/container-service/).</span></span>

### <a name="goals"></a><span data-ttu-id="eaec5-244">Objectifs</span><span class="sxs-lookup"><span data-stu-id="eaec5-244">Goals</span></span>

<span data-ttu-id="eaec5-245">L’objectif de cette procédure pas à pas est d’apprendre à déployer une application conteneur Windows – Kubernetes (également appelé *K8s*) dans le Service de conteneur Azure.</span><span class="sxs-lookup"><span data-stu-id="eaec5-245">The goal of this walkthrough is to learn how to deploy a Windows Container–based application to Kubernetes (also called *K8s*) in Azure Container Service.</span></span> <span data-ttu-id="eaec5-246">Déploiement sur Kubernetes à partir de zéro est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="eaec5-246">Deploying to Kubernetes from scratch is a two-step process:</span></span>

1.  <span data-ttu-id="eaec5-247">Déployer un cluster Kubernetes au Service de conteneur Azure.</span><span class="sxs-lookup"><span data-stu-id="eaec5-247">Deploy a Kubernetes cluster to Azure Container Service.</span></span>

2.  <span data-ttu-id="eaec5-248">Déployer l’application et les ressources associées au cluster Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="eaec5-248">Deploy the application and related resources to the Kubernetes cluster.</span></span>

### <a name="scenarios"></a><span data-ttu-id="eaec5-249">Scénarios</span><span class="sxs-lookup"><span data-stu-id="eaec5-249">Scenarios</span></span>

#### <a name="scenario-a-deploy-directly-to-a-kubernetes-cluster-from-a-dev-environment"></a><span data-ttu-id="eaec5-250">Scénario a : les déployer directement vers un cluster de Kubernetes à partir d’un environnement de développement</span><span class="sxs-lookup"><span data-stu-id="eaec5-250">Scenario A: Deploy directly to a Kubernetes cluster from a dev environment</span></span>

![Déployer directement sur un cluster Kubernetes à partir d’un environnement de développement](./media/image5-7.png)

> <span data-ttu-id="eaec5-252">**Figure 5-7.**</span><span class="sxs-lookup"><span data-stu-id="eaec5-252">**Figure 5-7.**</span></span> <span data-ttu-id="eaec5-253">Déployer directement sur un cluster Kubernetes à partir d’un environnement de développement</span><span class="sxs-lookup"><span data-stu-id="eaec5-253">Deploy directly to a Kubernetes cluster from a development environment</span></span>

#### <a name="scenario-b-deploy-to-a-kubernetes-cluster-from-cicd-pipelines-in-team-services"></a><span data-ttu-id="eaec5-254">Scénario b : déployer vers un cluster Kubernetes à partir de l’élément de configuration/CD pipelines dans Team Services</span><span class="sxs-lookup"><span data-stu-id="eaec5-254">Scenario B: Deploy to a Kubernetes cluster from CI/CD pipelines in Team Services</span></span>

![Déployer vers un cluster Kubernetes à partir de l’élément de configuration/CD des pipelines dans Team Services](./media/image5-8.png)

> <span data-ttu-id="eaec5-256">**Figure 5-8.**</span><span class="sxs-lookup"><span data-stu-id="eaec5-256">**Figure 5-8.**</span></span> <span data-ttu-id="eaec5-257">Déployer vers un cluster Kubernetes à partir de l’élément de configuration/CD des pipelines dans Team Services</span><span class="sxs-lookup"><span data-stu-id="eaec5-257">Deploy to a Kubernetes cluster from CI/CD pipelines in Team Services</span></span>

### <a name="benefits"></a><span data-ttu-id="eaec5-258">Avantages</span><span class="sxs-lookup"><span data-stu-id="eaec5-258">Benefits</span></span>

<span data-ttu-id="eaec5-259">Il existe de nombreux avantages pour le déploiement vers un cluster dans Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="eaec5-259">There are many benefits to deploying to a cluster in Kubernetes.</span></span> <span data-ttu-id="eaec5-260">Le principal avantage est que vous obtenez un environnement de l’environnement de production dans laquelle vous pouvez faire évoluer l’application en fonction du nombre d’instances de conteneurs, vous souhaitez utiliser (évolutivité interne dans les nœuds existants), en fonction du nombre de nœuds ou des machines virtuelles dans le cluster ( évolutivité globale du cluster).</span><span class="sxs-lookup"><span data-stu-id="eaec5-260">The biggest benefit is that you get a production-ready environment in which you can scale out the application based on the number of container instances you want to use (inner-scalability in the existing nodes), and based on the number of nodes or VMs in the cluster (global scalability of the cluster).</span></span>

<span data-ttu-id="eaec5-261">Service de conteneur Azure optimise les technologies et outils open source populaires spécifiquement pour Azure.</span><span class="sxs-lookup"><span data-stu-id="eaec5-261">Azure Container Service optimizes popular open-source tools and technologies specifically for Azure.</span></span> <span data-ttu-id="eaec5-262">Vous obtenez une solution ouverte qui offre la portabilité de vos conteneurs et lors de la configuration de votre application.</span><span class="sxs-lookup"><span data-stu-id="eaec5-262">You get an open solution that offers portability, both for your containers and for your application configuration.</span></span> <span data-ttu-id="eaec5-263">Sélectionnez la taille, le nombre d’hôtes, et le conteneur-Outils orchestrator Service gère tout le reste.</span><span class="sxs-lookup"><span data-stu-id="eaec5-263">You select the size, the number of hosts, and the orchestrator tools-Container Service handles everything else.</span></span>

<span data-ttu-id="eaec5-264">Avec Kubernetes, les développeurs peuvent progresser de réfléchir à des machines physiques et virtuelles, à la planification d’une infrastructure orientée conteneur qui facilite les fonctionnalités suivantes, entre autres :</span><span class="sxs-lookup"><span data-stu-id="eaec5-264">With Kubernetes, developers can progress from thinking about physical and virtual machines, to planning a container-centric infrastructure that facilitates the following capabilities, among others:</span></span>

- <span data-ttu-id="eaec5-265">Applications basées sur plusieurs conteneurs</span><span class="sxs-lookup"><span data-stu-id="eaec5-265">Applications based on multiple containers</span></span>

- <span data-ttu-id="eaec5-266">Réplication des instances de conteneurs et d’échelle horizontale</span><span class="sxs-lookup"><span data-stu-id="eaec5-266">Replicating container instances and horizontal autoscaling</span></span>

- <span data-ttu-id="eaec5-267">Attribution de noms et de découverte (par exemple, DNS interne)</span><span class="sxs-lookup"><span data-stu-id="eaec5-267">Naming and discovering (for example, internal DNS)</span></span>

- <span data-ttu-id="eaec5-268">L’équilibrage de charge</span><span class="sxs-lookup"><span data-stu-id="eaec5-268">Balancing loads</span></span>

- <span data-ttu-id="eaec5-269">Mises à jour propagées</span><span class="sxs-lookup"><span data-stu-id="eaec5-269">Rolling updates</span></span>

- <span data-ttu-id="eaec5-270">Distribution de clés secrètes</span><span class="sxs-lookup"><span data-stu-id="eaec5-270">Distributing secrets</span></span>

- <span data-ttu-id="eaec5-271">Vérifications de l’intégrité des applications</span><span class="sxs-lookup"><span data-stu-id="eaec5-271">Application health checks</span></span>

## <a name="next-steps"></a><span data-ttu-id="eaec5-272">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="eaec5-272">Next steps</span></span>

<span data-ttu-id="eaec5-273">Explorer ce contenu plus approfondi sur le wiki de GitHub : [https://github.com/dotnet-architecture/eShopModernizing/wiki/04.-How-to-deploy-your-Windows-Containers-based-apps-into-Kubernetes-in-Azure-Container-Service-(Including-C-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/04.-How-to-deploy-your-Windows-Containers-based-apps-into-Kubernetes-in-Azure-Container-Service-(Including-C-CD))</span><span class="sxs-lookup"><span data-stu-id="eaec5-273">Explore this content more in-depth on the GitHub wiki: [https://github.com/dotnet-architecture/eShopModernizing/wiki/04.-How-to-deploy-your-Windows-Containers-based-apps-into-Kubernetes-in-Azure-Container-Service-(Including-C-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/04.-How-to-deploy-your-Windows-Containers-based-apps-into-Kubernetes-in-Azure-Container-Service-(Including-C-CD))</span></span>

## <a name="walkthrough-6-deploy-your-windows-containers-based-apps-to-azure-service-fabric"></a><span data-ttu-id="eaec5-274">Procédure pas à pas 6 : Déployer vos applications basée sur les conteneurs de Windows Azure Service fabric</span><span class="sxs-lookup"><span data-stu-id="eaec5-274">Walkthrough 6: Deploy your Windows Containers-based apps to Azure Service Fabric</span></span>

### <a name="technical-walkthrough-availability"></a><span data-ttu-id="eaec5-275">Disponibilité de la procédure pas à pas technique</span><span class="sxs-lookup"><span data-stu-id="eaec5-275">Technical walkthrough availability</span></span>

<span data-ttu-id="eaec5-276">La procédure pas à pas technique complet est disponible dans le wiki de référentiel GitHub eShopModernizing :</span><span class="sxs-lookup"><span data-stu-id="eaec5-276">The full technical walkthrough is available in the eShopModernizing GitHub repo wiki:</span></span>

[https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-How-to-deploy-your-Windows-Containers-based-apps-into-Azure-Service-Fabric-(Including-CI-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-How-to-deploy-your-Windows-Containers-based-apps-into-Azure-Service-Fabric-(Including-CI-CD))

### <a name="overview"></a><span data-ttu-id="eaec5-277">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="eaec5-277">Overview</span></span>

<span data-ttu-id="eaec5-278">Une application basée sur les conteneurs Windows rapidement doit utiliser des plates-formes, éloigner encore davantage de machines virtuelles IaaS.</span><span class="sxs-lookup"><span data-stu-id="eaec5-278">An application based on Windows Containers quickly needs to use platforms, moving even further away from IaaS VMs.</span></span> <span data-ttu-id="eaec5-279">Cela est nécessaire pour facilement atteindre une haute évolutivité et mieux automatisée de l’évolutivité et pour une amélioration significative dans automatisée déploiements et le contrôle de version.</span><span class="sxs-lookup"><span data-stu-id="eaec5-279">This is needed to easily achieve high scalability and better automated scalability, and for a significant improvement in automated deployments and versioning.</span></span> <span data-ttu-id="eaec5-280">Vous pouvez atteindre ces objectifs à l’aide de l’orchestrateur Azure Service Fabric, qui est disponible dans le cloud Azure, mais vous pouvez également utiliser localement, ou même dans un autre cloud public.</span><span class="sxs-lookup"><span data-stu-id="eaec5-280">You can achieve these goals by using the orchestrator Azure Service Fabric, which is available in the Azure cloud, but also available to use on-premises, or even in a different public cloud.</span></span>

### <a name="goals"></a><span data-ttu-id="eaec5-281">Objectifs</span><span class="sxs-lookup"><span data-stu-id="eaec5-281">Goals</span></span>

<span data-ttu-id="eaec5-282">L’objectif de cette procédure pas à pas est d’apprendre à déployer une application conteneur Windows vers un cluster Service Fabric dans Azure.</span><span class="sxs-lookup"><span data-stu-id="eaec5-282">The goal of this walkthrough is to learn how to deploy a Windows Container–based application to a Service Fabric cluster in Azure.</span></span> <span data-ttu-id="eaec5-283">Déploiement sur l’infrastructure de Service à partir de zéro est un processus en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="eaec5-283">Deploying to Service Fabric from scratch is a two-step process:</span></span>

1.  <span data-ttu-id="eaec5-284">Déployer un cluster Service Fabric vers Azure (ou un autre environnement).</span><span class="sxs-lookup"><span data-stu-id="eaec5-284">Deploy a Service Fabric cluster to Azure (or to a different environment).</span></span>

2.  <span data-ttu-id="eaec5-285">Déployer l’application et les ressources associées au cluster Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="eaec5-285">Deploy the application and related resources to the Service Fabric cluster.</span></span>

### <a name="scenarios"></a><span data-ttu-id="eaec5-286">Scénarios</span><span class="sxs-lookup"><span data-stu-id="eaec5-286">Scenarios</span></span>

#### <a name="scenario-a-deploy-directly-to-a-service-fabric-cluster-from-a-dev-environment"></a><span data-ttu-id="eaec5-287">Scénario a : les déployer directement à un cluster Service Fabric à partir d’un environnement de développement</span><span class="sxs-lookup"><span data-stu-id="eaec5-287">Scenario A: Deploy directly to a Service Fabric cluster from a dev environment</span></span>

![Déployer directement sur un cluster Service Fabric à partir d’un environnement de développement](./media/image5-9.png)

> <span data-ttu-id="eaec5-289">**Figure 5-9**.</span><span class="sxs-lookup"><span data-stu-id="eaec5-289">**Figure 5-9.**</span></span> <span data-ttu-id="eaec5-290">Déployer directement sur un cluster Service Fabric à partir d’un environnement de développement</span><span class="sxs-lookup"><span data-stu-id="eaec5-290">Deploy directly to a Service Fabric cluster from a development environment</span></span>

### <a name="scenario-b-deploy-to-a-service-fabric-cluster-from-cicd-pipelines-in-team-services"></a><span data-ttu-id="eaec5-291">Scénario b : déployer vers un cluster Service Fabric à partir de l’élément de configuration/CD pipelines dans Team Services</span><span class="sxs-lookup"><span data-stu-id="eaec5-291">Scenario B: Deploy to a Service Fabric cluster from CI/CD pipelines in Team Services</span></span>

![Déployer vers un cluster Service Fabric à partir de l’élément de configuration/CD des pipelines dans Visual Studio Team Services](./media/image5-10.png)

> <span data-ttu-id="eaec5-293">**Figure 5-10.**</span><span class="sxs-lookup"><span data-stu-id="eaec5-293">**Figure 5-10.**</span></span> <span data-ttu-id="eaec5-294">Déployer vers un cluster Service Fabric à partir de l’élément de configuration/CD des pipelines dans Visual Studio Team Services</span><span class="sxs-lookup"><span data-stu-id="eaec5-294">Deploy to a Service Fabric cluster from CI/CD pipelines in Visual Studio Team Services</span></span>

## <a name="benefits"></a><span data-ttu-id="eaec5-295">Avantages</span><span class="sxs-lookup"><span data-stu-id="eaec5-295">Benefits</span></span>

<span data-ttu-id="eaec5-296">Les avantages du déploiement vers un cluster Service fabric sont semblables aux avantages de Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="eaec5-296">The benefits of deploying to a cluster in Service Fabric are similar to the benefits of using Kubernetes.</span></span> <span data-ttu-id="eaec5-297">Cependant, une différence est que le Service Fabric est un environnement de production plus mature pour les applications Windows par rapport à Kubernetes, qui se trouve dans une phase bêta pour les conteneurs Windows dans Kubernetes version 1.9 (2017 décembre).</span><span class="sxs-lookup"><span data-stu-id="eaec5-297">One difference, though, is that Service Fabric is a more mature production environment for Windows applications compared to Kubernetes, which is in a beta phase for Windows Containers in Kubernetes version 1.9 (December 2017).</span></span> <span data-ttu-id="eaec5-298">Kubernetes est un environnement plus mature pour Linux.</span><span class="sxs-lookup"><span data-stu-id="eaec5-298">Kubernetes is a more mature environment for Linux.</span></span>

<span data-ttu-id="eaec5-299">Le principal avantage de l’utilisation d’Azure Service Fabric est que vous obtenez un environnement de l’environnement de production dans laquelle vous pouvez faire évoluer l’application en fonction du nombre d’instances de conteneurs, vous souhaitez utiliser (évolutivité interne dans les nœuds existants), en fonction du nombre de les nœuds ou des ordinateurs virtuels du cluster (évolutivité globale du cluster).</span><span class="sxs-lookup"><span data-stu-id="eaec5-299">The main benefit of using Azure Service Fabric is that you get a production-ready environment in which you can scale out the application based on the number of container instances you want to use (inner-scalability in the existing nodes), and based on the number of nodes or VMs in the cluster (global scalability of the cluster).</span></span>

<span data-ttu-id="eaec5-300">Azure Service Fabric offre la portabilité de vos conteneurs et lors de la configuration de votre application.</span><span class="sxs-lookup"><span data-stu-id="eaec5-300">Azure Service Fabric offers portability both for your containers and for your application configuration.</span></span> <span data-ttu-id="eaec5-301">Vous pouvez avoir une infrastructure de Service de cluster dans Azure, ou installer localement dans votre centre de données.</span><span class="sxs-lookup"><span data-stu-id="eaec5-301">You can have a Service Fabric cluster in Azure, or install it on-premises in your own datacenter.</span></span> <span data-ttu-id="eaec5-302">Vous pouvez même installer un cluster Service Fabric dans un autre cloud, tels que [Amazon AWS](https://blogs.msdn.microsoft.com/azureservicefabric/2017/05/18/tutorial-how-to-create-a-service-fabric-standalone-cluster-with-aws-ec2-instances/).</span><span class="sxs-lookup"><span data-stu-id="eaec5-302">You can even install a Service Fabric cluster in a different cloud, like [Amazon AWS](https://blogs.msdn.microsoft.com/azureservicefabric/2017/05/18/tutorial-how-to-create-a-service-fabric-standalone-cluster-with-aws-ec2-instances/).</span></span>

<span data-ttu-id="eaec5-303">Avec Service Fabric, les développeurs peuvent progresser de réfléchir à des machines physiques et virtuelles à la planification d’une infrastructure orientée conteneur qui facilite les fonctionnalités suivantes, entre autres :</span><span class="sxs-lookup"><span data-stu-id="eaec5-303">With Service Fabric, developers can progress from thinking about physical and virtual machines to planning a container-centric infrastructure that facilitates the following capabilities, among others:</span></span>

- <span data-ttu-id="eaec5-304">Applications basées sur plusieurs conteneurs.</span><span class="sxs-lookup"><span data-stu-id="eaec5-304">Applications based on multiple containers.</span></span>

- <span data-ttu-id="eaec5-305">Réplication des instances de conteneurs et d’échelle horizontale.</span><span class="sxs-lookup"><span data-stu-id="eaec5-305">Replicating container instances and horizontal autoscaling.</span></span>

- <span data-ttu-id="eaec5-306">Attribution de noms et de découverte (par exemple, DNS interne).</span><span class="sxs-lookup"><span data-stu-id="eaec5-306">Naming and discovering (for example, internal DNS).</span></span>

- <span data-ttu-id="eaec5-307">L’équilibrage de charge.</span><span class="sxs-lookup"><span data-stu-id="eaec5-307">Balancing loads.</span></span>

- <span data-ttu-id="eaec5-308">Mises à jour propagées.</span><span class="sxs-lookup"><span data-stu-id="eaec5-308">Rolling updates.</span></span>

- <span data-ttu-id="eaec5-309">La distribution de clés secrètes.</span><span class="sxs-lookup"><span data-stu-id="eaec5-309">Distributing secrets.</span></span>

- <span data-ttu-id="eaec5-310">Vérifications de contrôle d’intégrité de l’application.</span><span class="sxs-lookup"><span data-stu-id="eaec5-310">Application health checks.</span></span>

<span data-ttu-id="eaec5-311">Les fonctionnalités suivantes sont exclusives dans Service Fabric (par rapport à d’autres orchestrators) :</span><span class="sxs-lookup"><span data-stu-id="eaec5-311">The following capabilities are exclusive in Service Fabric (compared to other orchestrators):</span></span>

- <span data-ttu-id="eaec5-312">Fonctionnalité de services avec état, par le biais du modèle d’application des Services fiables.</span><span class="sxs-lookup"><span data-stu-id="eaec5-312">Stateful services capability, through the Reliable Services application model.</span></span>

- <span data-ttu-id="eaec5-313">Modèle d’acteurs, par le biais du modèle d’application Reliable Actors.</span><span class="sxs-lookup"><span data-stu-id="eaec5-313">Actors pattern, through the Reliable Actors application model.</span></span>

- <span data-ttu-id="eaec5-314">Déployer un processus nus, en plus des conteneurs Windows ou Linux.</span><span class="sxs-lookup"><span data-stu-id="eaec5-314">Deploy bare-bone processes, in addition to Windows or Linux containers.</span></span>

- <span data-ttu-id="eaec5-315">Avancé des mises à jour et les vérifications d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="eaec5-315">Advanced rolling updates and health checks.</span></span>

### <a name="next-steps"></a><span data-ttu-id="eaec5-316">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="eaec5-316">Next steps</span></span>

<span data-ttu-id="eaec5-317">Explorer ce contenu plus approfondi sur le wiki de GitHub :</span><span class="sxs-lookup"><span data-stu-id="eaec5-317">Explore this content more in-depth on the GitHub wiki:</span></span>

[https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-How-to-deploy-your-Windows-Containers-based-apps-into-Azure-Service-Fabric-(Including-CI-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-How-to-deploy-your-Windows-Containers-based-apps-into-Azure-Service-Fabric-(Including-CI-CD))

>[!div class="step-by-step"]
<span data-ttu-id="eaec5-318">[Précédent](lift-and-shift-existing-apps-devops/migrate-to-hybrid-cloud-scenarios.md)
[Suivant](conclusions.md)</span><span class="sxs-lookup"><span data-stu-id="eaec5-318">[Previous](lift-and-shift-existing-apps-devops/migrate-to-hybrid-cloud-scenarios.md)
[Next](conclusions.md)</span></span>
