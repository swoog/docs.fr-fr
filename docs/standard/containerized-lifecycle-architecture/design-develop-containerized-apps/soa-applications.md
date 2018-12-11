---
title: Applications SOA
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: 7f88daaf0787cf780e7ab9602f35ae4e6ab8308c
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53155312"
---
# <a name="soa-applications"></a><span data-ttu-id="aaf64-103">Applications SOA</span><span class="sxs-lookup"><span data-stu-id="aaf64-103">SOA applications</span></span>

<span data-ttu-id="aaf64-104">SOA était un terme surutilisé et signifié des choses différentes tellement à différentes personnes.</span><span class="sxs-lookup"><span data-stu-id="aaf64-104">SOA was an overused term and meant so many different things to different people.</span></span> <span data-ttu-id="aaf64-105">Mais au minimum et comme un dénominateur commun SOA, ou l’orientation service, moyenne structure l’architecture de votre application en la décomposant en plusieurs services (généralement en tant que services HTTP) qui peuvent être classés dans les différents types, tels que les sous-systèmes ou, dans d’autres cas, en tant que niveaux.</span><span class="sxs-lookup"><span data-stu-id="aaf64-105">But at a minimum and as a common denominator, SOA, or service orientation, mean that you structure the architecture of your application by decomposing it in multiple services (most commonly as HTTP services) that can be classified in different types like subsystems or, in other cases, as tiers.</span></span>

<span data-ttu-id="aaf64-106">Aujourd'hui, vous pouvez déployer ces services en tant que conteneurs Docker, ce qui résout les problèmes liés au déploiement, car toutes les dépendances sont incluses dans l’image de conteneur.</span><span class="sxs-lookup"><span data-stu-id="aaf64-106">Today, you can deploy those services as Docker containers, which solves deployment-related issues because all of the dependencies are included within the container image.</span></span> <span data-ttu-id="aaf64-107">Toutefois, lorsque vous avez besoin pour la montée en puissance SOA, vous pouvez rencontrer des difficultés si vous déployez des instances uniques en fonction.</span><span class="sxs-lookup"><span data-stu-id="aaf64-107">However, when you need to scale-out SOAs, you might encounter challenges if you are deploying based on single instances.</span></span> <span data-ttu-id="aaf64-108">Il s’agit où un Docker clustering logiciel ou orchestrator vous aidera à.</span><span class="sxs-lookup"><span data-stu-id="aaf64-108">This is where a Docker clustering software or orchestrator will help you.</span></span> <span data-ttu-id="aaf64-109">Nous allons examiner cela plus en détail dans la section suivante lorsque nous examinons les approches de microservices.</span><span class="sxs-lookup"><span data-stu-id="aaf64-109">We'll look at this in greater detail in the next section when we examine microservices approaches.</span></span>

<span data-ttu-id="aaf64-110">À la fin de la journée, les solutions de clustering de conteneur sont utiles pour les deux une architecture SOA traditionnelle ou pour une architecture de microservices plus avancée dans lesquels chaque microservice détient son modèle de données.</span><span class="sxs-lookup"><span data-stu-id="aaf64-110">At the end of the day, the container clustering solutions are useful for both a traditional SOA architecture or for a more advanced microservices architecture in which each microservice owns its data model.</span></span> <span data-ttu-id="aaf64-111">Et grâce à plusieurs bases de données, vous également pouvez faire évoluer la couche de données au lieu de travailler avec des bases de données monolithiques partagés par les services SOA.</span><span class="sxs-lookup"><span data-stu-id="aaf64-111">And, thanks to multiple databases, you also can scale-out the data tier instead of working with monolithic databases shared by the SOA services.</span></span> <span data-ttu-id="aaf64-112">Toutefois, la discussion sur la division des données est purement sur l’architecture et de conception.</span><span class="sxs-lookup"><span data-stu-id="aaf64-112">However, the discussion about splitting the data is purely about architecture and design.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="aaf64-113">[Précédent](state-and-data-in-docker-applications.md)
>[Suivant](orchestrate-high-scalability-availability.md)</span><span class="sxs-lookup"><span data-stu-id="aaf64-113">[Previous](state-and-data-in-docker-applications.md)
[Next](orchestrate-high-scalability-availability.md)</span></span>