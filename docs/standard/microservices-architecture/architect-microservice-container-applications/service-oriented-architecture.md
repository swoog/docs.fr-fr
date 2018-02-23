---
title: "Architecture orientée services"
description: "Architecture de microservices .NET pour les applications .NET en conteneur | Architecture orientée services"
keywords: Docker, microservices, ASP.NET, conteneur
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/26/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 6a5f0f53f4208c9944adea33fe1aa3f35fed81ab
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="service-oriented-architecture"></a><span data-ttu-id="7a101-104">Architecture orientée services</span><span class="sxs-lookup"><span data-stu-id="7a101-104">Service-oriented architecture</span></span> 

<span data-ttu-id="7a101-105">SOA, ou Architecture orientée services, est un terme qui a été trop utilisé et qui a signifié des choses différentes pour différentes personnes.</span><span class="sxs-lookup"><span data-stu-id="7a101-105">Service-oriented architecture (SOA) was an overused term and has meant different things to different people.</span></span> <span data-ttu-id="7a101-106">Un dénominateur commun est néanmoins que SOA signifie que vous structurez votre application en la décomposant en plusieurs services (la plupart du temps en services HTTP) qui peuvent être classés selon différents types, comme des sous-systèmes ou des niveaux.</span><span class="sxs-lookup"><span data-stu-id="7a101-106">But as a common denominator, SOA means that you structure your application by decomposing it into multiple services (most commonly as HTTP services) that can be classified as different types like subsystems or tiers.</span></span>

<span data-ttu-id="7a101-107">Ces services peuvent désormais être déployés en tant que conteneurs Docker, ce qui résout les problèmes de déploiement, car toutes les dépendances sont incluses dans l’image du conteneur.</span><span class="sxs-lookup"><span data-stu-id="7a101-107">Those services can now be deployed as Docker containers, which solves deployment issues, because all the dependencies are included in the container image.</span></span> <span data-ttu-id="7a101-108">Cependant, quand vous devez faire monter en charge des applications SOA, vous pouvez rencontrer des problèmes de scalabilité et de disponibilité si vous déployez sur des hôtes Docker simples.</span><span class="sxs-lookup"><span data-stu-id="7a101-108">However, when you need to scale up SOA applications, you might have scalability and availability challenges if you are deploying based on single Docker hosts.</span></span> <span data-ttu-id="7a101-109">C’est là où les logiciels de clustering Docker ou un orchestrateur peuvent vous aider, comme c’est expliqué dans les sections suivantes, où nous décrivons les approches du déploiement pour les microservices.</span><span class="sxs-lookup"><span data-stu-id="7a101-109">This is where Docker clustering software or an orchestrator will help you out, as explained in later sections where we describe deployment approaches for microservices.</span></span>

<span data-ttu-id="7a101-110">Les conteneurs Docker sont pratiques (mais pas obligatoires) pour les architectures orientées services traditionnelles et pour les architectures de microservices plus avancées.</span><span class="sxs-lookup"><span data-stu-id="7a101-110">Docker containers are useful (but not required) for both traditional service-oriented architectures and the more advanced microservices architectures.</span></span>

<span data-ttu-id="7a101-111">Les microservices dérivent de SOA, mais SOA est différent de l’architecture de microservices.</span><span class="sxs-lookup"><span data-stu-id="7a101-111">Microservices derive from SOA, but SOA is different from microservices architecture.</span></span> <span data-ttu-id="7a101-112">Des fonctionnalités comme les grands courtiers centralisés, les orchestrateurs centralisés au niveau de l’organisation et [ESB (Enterprise Service Bus)](https://en.wikipedia.org/wiki/Enterprise_service_bus) sont habituelles dans SOA.</span><span class="sxs-lookup"><span data-stu-id="7a101-112">Features like big central brokers, central orchestrators at the organization level, and the [Enterprise Service Bus (ESB)](https://en.wikipedia.org/wiki/Enterprise_service_bus) are typical in SOA.</span></span> <span data-ttu-id="7a101-113">Dans la plupart des cas cependant, celles-ci sont des antimodèles dans la communauté des microservices.</span><span class="sxs-lookup"><span data-stu-id="7a101-113">But in most cases, these are anti-patterns in the microservice community.</span></span> <span data-ttu-id="7a101-114">En fait, certaines personnes affirment que « l’architecture de microservice est une architecture SOA bien conçue ».</span><span class="sxs-lookup"><span data-stu-id="7a101-114">In fact, some people argue that “The microservice architecture is SOA done right.”</span></span>

<span data-ttu-id="7a101-115">Ce guide se concentre sur les microservices, car une approche SOA est moins stricte que la configuration requise et les techniques utilisées dans une architecture de microservices.</span><span class="sxs-lookup"><span data-stu-id="7a101-115">This guide focuses on microservices, because a SOA approach is less prescriptive than the requirements and techniques used in a microservice architecture.</span></span> <span data-ttu-id="7a101-116">Si vous savez créer une application basée sur des microservices, vous savez également créer une application orientée services plus simple.</span><span class="sxs-lookup"><span data-stu-id="7a101-116">If you know how to build a microservice-based application, you also know how to build a simpler service-oriented application.</span></span>




>[!div class="step-by-step"]
<span data-ttu-id="7a101-117">[Précédent] (docker-application-state-data.md) [Suivant] (microservices-architecture.md)</span><span class="sxs-lookup"><span data-stu-id="7a101-117">[Previous] (docker-application-state-data.md) [Next] (microservices-architecture.md)</span></span>
