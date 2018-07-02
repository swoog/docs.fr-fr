---
title: Architecture orientée services
description: Architecture de microservices .NET pour les applications .NET en conteneur | Architecture orientée services
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/26/2017
ms.openlocfilehash: 67560cc93b3d147be36a691af440bb78f2315557
ms.sourcegitcommit: 979597cd8055534b63d2c6ee8322938a27d0c87b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2018
ms.locfileid: "37105002"
---
# <a name="service-oriented-architecture"></a><span data-ttu-id="e7a23-103">Architecture orientée services</span><span class="sxs-lookup"><span data-stu-id="e7a23-103">Service-oriented architecture</span></span> 

<span data-ttu-id="e7a23-104">SOA, ou Architecture orientée services, est un terme qui a été trop utilisé et qui a signifié des choses différentes pour différentes personnes.</span><span class="sxs-lookup"><span data-stu-id="e7a23-104">Service-oriented architecture (SOA) was an overused term and has meant different things to different people.</span></span> <span data-ttu-id="e7a23-105">Un dénominateur commun est néanmoins que SOA signifie que vous structurez votre application en la décomposant en plusieurs services (la plupart du temps en services HTTP) qui peuvent être classés selon différents types, comme des sous-systèmes ou des niveaux.</span><span class="sxs-lookup"><span data-stu-id="e7a23-105">But as a common denominator, SOA means that you structure your application by decomposing it into multiple services (most commonly as HTTP services) that can be classified as different types like subsystems or tiers.</span></span>

<span data-ttu-id="e7a23-106">Ces services peuvent désormais être déployés en tant que conteneurs Docker, ce qui résout les problèmes de déploiement, car toutes les dépendances sont incluses dans l’image du conteneur.</span><span class="sxs-lookup"><span data-stu-id="e7a23-106">Those services can now be deployed as Docker containers, which solves deployment issues, because all the dependencies are included in the container image.</span></span> <span data-ttu-id="e7a23-107">Cependant, quand vous devez faire monter en charge des applications SOA, vous pouvez rencontrer des problèmes de scalabilité et de disponibilité si vous déployez sur des hôtes Docker simples.</span><span class="sxs-lookup"><span data-stu-id="e7a23-107">However, when you need to scale up SOA applications, you might have scalability and availability challenges if you are deploying based on single Docker hosts.</span></span> <span data-ttu-id="e7a23-108">C’est là où les logiciels de clustering Docker ou un orchestrateur peuvent vous aider, comme c’est expliqué dans les sections suivantes, où nous décrivons les approches du déploiement pour les microservices.</span><span class="sxs-lookup"><span data-stu-id="e7a23-108">This is where Docker clustering software or an orchestrator will help you out, as explained in later sections where we describe deployment approaches for microservices.</span></span>

<span data-ttu-id="e7a23-109">Les conteneurs Docker sont pratiques (mais pas obligatoires) pour les architectures orientées services traditionnelles et pour les architectures de microservices plus avancées.</span><span class="sxs-lookup"><span data-stu-id="e7a23-109">Docker containers are useful (but not required) for both traditional service-oriented architectures and the more advanced microservices architectures.</span></span>

<span data-ttu-id="e7a23-110">Les microservices dérivent de SOA, mais SOA est différent de l’architecture de microservices.</span><span class="sxs-lookup"><span data-stu-id="e7a23-110">Microservices derive from SOA, but SOA is different from microservices architecture.</span></span> <span data-ttu-id="e7a23-111">Des fonctionnalités comme les grands courtiers centralisés, les orchestrateurs centralisés au niveau de l’organisation et [ESB (Enterprise Service Bus)](https://en.wikipedia.org/wiki/Enterprise_service_bus) sont habituelles dans SOA.</span><span class="sxs-lookup"><span data-stu-id="e7a23-111">Features like big central brokers, central orchestrators at the organization level, and the [Enterprise Service Bus (ESB)](https://en.wikipedia.org/wiki/Enterprise_service_bus) are typical in SOA.</span></span> <span data-ttu-id="e7a23-112">Dans la plupart des cas cependant, celles-ci sont des antimodèles dans la communauté des microservices.</span><span class="sxs-lookup"><span data-stu-id="e7a23-112">But in most cases, these are anti-patterns in the microservice community.</span></span> <span data-ttu-id="e7a23-113">En fait, certaines personnes affirment que « l’architecture de microservice est une architecture SOA bien conçue ».</span><span class="sxs-lookup"><span data-stu-id="e7a23-113">In fact, some people argue that “The microservice architecture is SOA done right.”</span></span>

<span data-ttu-id="e7a23-114">Ce guide se concentre sur les microservices, car une approche SOA est moins stricte que la configuration requise et les techniques utilisées dans une architecture de microservices.</span><span class="sxs-lookup"><span data-stu-id="e7a23-114">This guide focuses on microservices, because a SOA approach is less prescriptive than the requirements and techniques used in a microservice architecture.</span></span> <span data-ttu-id="e7a23-115">Si vous savez créer une application basée sur des microservices, vous savez également créer une application orientée services plus simple.</span><span class="sxs-lookup"><span data-stu-id="e7a23-115">If you know how to build a microservice-based application, you also know how to build a simpler service-oriented application.</span></span>




>[!div class="step-by-step"]
<span data-ttu-id="e7a23-116">[Précédent](docker-application-state-data.md)
[Suivant](microservices-architecture.md)</span><span class="sxs-lookup"><span data-stu-id="e7a23-116">[Previous](docker-application-state-data.md)
[Next](microservices-architecture.md)</span></span>
