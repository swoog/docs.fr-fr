---
title: "Recommandations générales"
description: "Architecture de microservices .NET pour les applications .NET en conteneur | Recommandations générales"
keywords: Docker, microservices, ASP.NET, conteneur
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/18/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: fa58d1d81b2d1523baf123d4963db2ca00fee15d
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="general-guidance"></a><span data-ttu-id="b6041-104">Recommandations générales</span><span class="sxs-lookup"><span data-stu-id="b6041-104">General guidance</span></span>

<span data-ttu-id="b6041-105">Cette section indique brièvement dans quels cas choisir .NET Core ou .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="b6041-105">This section provides a summary of when to choose .NET Core or .NET Framework.</span></span> <span data-ttu-id="b6041-106">Vous trouverez des détails complémentaires sur ces choix dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="b6041-106">We provide more details about these choices in the sections that follow.</span></span>

<span data-ttu-id="b6041-107">Vous avez tout intérêt à utiliser .NET Core, avec des conteneurs Windows ou Linux, pour votre application serveur Docker en conteneur dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="b6041-107">You should use .NET Core, with Linux or Windows Containers, for your containerized Docker server application when:</span></span>

-   <span data-ttu-id="b6041-108">Vous avez des besoins multiplateformes.</span><span class="sxs-lookup"><span data-stu-id="b6041-108">You have cross-platform needs.</span></span> <span data-ttu-id="b6041-109">Par exemple, vous souhaitez utiliser à la fois des conteneurs Linux et Windows.</span><span class="sxs-lookup"><span data-stu-id="b6041-109">For example, you want to use both Linux and Windows Containers.</span></span>

-   <span data-ttu-id="b6041-110">L’architecture de votre application est basée sur des microservices.</span><span class="sxs-lookup"><span data-stu-id="b6041-110">Your application architecture is based on microservices.</span></span>

-   <span data-ttu-id="b6041-111">Vous avez besoin de démarrer les conteneurs rapidement et souhaitez un faible encombrement par conteneur pour profiter d’une meilleure densité ou davantage de conteneurs par unité matérielle afin de réduire les coûts.</span><span class="sxs-lookup"><span data-stu-id="b6041-111">You need to start containers fast and want a small footprint per container to achieve better density or more containers per hardware unit in order to lower your costs.</span></span>

<span data-ttu-id="b6041-112">En somme, quand il s’agit de créer des applications .NET en conteneur, vous devez envisager .NET Core comme le choix par défaut.</span><span class="sxs-lookup"><span data-stu-id="b6041-112">In short, when you create new containerized .NET applications, you should consider .NET Core as the default choice.</span></span> <span data-ttu-id="b6041-113">Il offre de nombreux avantages et correspond le mieux à la philosophie et au type de fonctionnement des conteneurs.</span><span class="sxs-lookup"><span data-stu-id="b6041-113">It has many benefits and fits best with the containers philosophy and style of working.</span></span>

<span data-ttu-id="b6041-114">L’autre avantage de .NET Core est lié au fait que vous pouvez exécuter différentes versions de .NET côte à côte pour les applications présentes sur une même machine.</span><span class="sxs-lookup"><span data-stu-id="b6041-114">An additional benefit of using .NET Core is that you can run side by side .NET versions for applications within the same machine.</span></span> <span data-ttu-id="b6041-115">Cet avantage est plus important pour les serveurs ou les machines virtuelles qui n’utilisent pas de conteneurs, car les conteneurs isolent les versions de .NET dont l’application a besoin.</span><span class="sxs-lookup"><span data-stu-id="b6041-115">This benefit is more important for servers or VMs that do not use containers, because containers isolate the versions of .NET that the app needs.</span></span> <span data-ttu-id="b6041-116">(Du moment qu’elles sont compatibles avec le système d’exploitation sous-jacent.)</span><span class="sxs-lookup"><span data-stu-id="b6041-116">(As long as they are compatible with the underlying OS.)</span></span>

<span data-ttu-id="b6041-117">Vous avez tout intérêt à utiliser le .NET Framework avec des conteneurs Windows pour votre application serveur Docker en conteneur dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="b6041-117">You should use .NET Framework, with Windows Containers, for your containerized Docker server application when:</span></span>

-   <span data-ttu-id="b6041-118">Votre application utilise actuellement le .NET Framework et présente de fortes dépendances vis-à-vis de Windows.</span><span class="sxs-lookup"><span data-stu-id="b6041-118">Your application currently uses .NET Framework and has strong dependencies on Windows.</span></span>

-   <span data-ttu-id="b6041-119">Vous avez besoin d’utiliser des API Windows qui ne sont pas prises en charge par .NET Core.</span><span class="sxs-lookup"><span data-stu-id="b6041-119">You need to use Windows APIs that are not supported by .NET Core.</span></span>

-   <span data-ttu-id="b6041-120">Vous avez besoin d’utiliser des bibliothèques .NET ou des packages NuGet tiers qui ne sont pas disponibles pour .NET Core.</span><span class="sxs-lookup"><span data-stu-id="b6041-120">You need to use third-party .NET libraries or NuGet packages that are not available for .NET Core.</span></span>

<span data-ttu-id="b6041-121">Le fait d’utiliser le .NET Framework sur Docker peut améliorer vos expériences de déploiement en limitant les problèmes de déploiement.</span><span class="sxs-lookup"><span data-stu-id="b6041-121">Using .NET Framework on Docker can improve your deployment experiences by minimizing deployment issues.</span></span> <span data-ttu-id="b6041-122">Ce [*scénario « lift-and-shift »* ](https://aka.ms/liftandshiftwithcontainersebook) est important pour la mise en conteneur d’applications existantes qui ont été développées à l’origine avec le .NET Framework classique, comme les applications Web Forms ASP.NET, les applications web MVC ou les services WCF (Windows Communication Foundation).</span><span class="sxs-lookup"><span data-stu-id="b6041-122">This [*"lift and shift" scenario*](https://aka.ms/liftandshiftwithcontainersebook) is important for containerizing legacy applications that were originally developed with the traditional .NET Framework, like ASP.NET WebForms, MVC web apps or WCF (Windows Communication Foundation) services.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="b6041-123">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="b6041-123">Additional resources</span></span>

-   <span data-ttu-id="b6041-124">**Livre électronique : Modernize existing .NET Framework applications with Azure and Windows Containers**
    [*https://aka.ms/liftandshiftwithcontainersebook*](https://aka.ms/liftandshiftwithcontainersebook)</span><span class="sxs-lookup"><span data-stu-id="b6041-124">**e-book: Modernize existing .NET Framework applications with Azure and Windows Containers**
[*https://aka.ms/liftandshiftwithcontainersebook*](https://aka.ms/liftandshiftwithcontainersebook)</span></span>

-   <span data-ttu-id="b6041-125">**Exemples d’applications : Modernization of legacy ASP.NET web apps by using Windows Containers**
    [*https://aka.ms/eshopmodernizing*](https://aka.ms/eshopmodernizing)</span><span class="sxs-lookup"><span data-stu-id="b6041-125">**Sample apps: Modernization of legacy ASP.NET web apps by using Windows Containers**
[*https://aka.ms/eshopmodernizing*](https://aka.ms/eshopmodernizing)</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="b6041-126">[Précédent] (index.md) [Suivant] (net-core-container-scenarios.md)</span><span class="sxs-lookup"><span data-stu-id="b6041-126">[Previous] (index.md) [Next] (net-core-container-scenarios.md)</span></span>
