---
title: Applications SOA
description: N’oubliez pas que les conteneurs peuvent être également une option de déploiement utile pour les applications SOA.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.openlocfilehash: 4fd39e075c5730cf7fddb0138cdb5267a914c91f
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56221262"
---
# <a name="soa-applications"></a><span data-ttu-id="1195c-103">Applications SOA</span><span class="sxs-lookup"><span data-stu-id="1195c-103">SOA applications</span></span>

<span data-ttu-id="1195c-104">SOA était un terme surutilisé et signifié des choses différentes tellement à différentes personnes.</span><span class="sxs-lookup"><span data-stu-id="1195c-104">SOA was an overused term and meant so many different things to different people.</span></span> <span data-ttu-id="1195c-105">Mais au minimum et comme un dénominateur commun SOA, ou l’orientation service, moyenne structure l’architecture de votre application en la décomposant en plusieurs services (généralement en tant que services HTTP) qui peuvent être classés dans les différents types, tels que les sous-systèmes ou, dans d’autres cas, en tant que niveaux.</span><span class="sxs-lookup"><span data-stu-id="1195c-105">But at a minimum and as a common denominator, SOA, or service orientation, mean that you structure the architecture of your application by decomposing it in multiple services (most commonly as HTTP services) that can be classified in different types like subsystems or, in other cases, as tiers.</span></span>

<span data-ttu-id="1195c-106">Aujourd'hui, vous pouvez déployer ces services en tant que conteneurs Docker, ce qui résout les problèmes liés au déploiement, car toutes les dépendances sont incluses dans l’image de conteneur.</span><span class="sxs-lookup"><span data-stu-id="1195c-106">Today, you can deploy those services as Docker containers, which solves deployment-related issues because all of the dependencies are included within the container image.</span></span> <span data-ttu-id="1195c-107">Toutefois, lorsque vous avez besoin pour la montée en puissance SOA, vous pouvez rencontrer des difficultés si vous déployez des instances uniques en fonction.</span><span class="sxs-lookup"><span data-stu-id="1195c-107">However, when you need to scale-out SOAs, you might encounter challenges if you are deploying based on single instances.</span></span> <span data-ttu-id="1195c-108">Il s’agit où un Docker clustering logiciel ou orchestrator vous aidera à.</span><span class="sxs-lookup"><span data-stu-id="1195c-108">This is where a Docker clustering software or orchestrator will help you.</span></span> <span data-ttu-id="1195c-109">Nous allons examiner cela plus en détail dans la section suivante lorsque nous examinons les approches de microservices.</span><span class="sxs-lookup"><span data-stu-id="1195c-109">We'll look at this in greater detail in the next section when we examine microservices approaches.</span></span>

<span data-ttu-id="1195c-110">À la fin de la journée, les solutions de clustering de conteneur sont utiles pour les deux une architecture SOA traditionnelle ou pour une architecture de microservices plus avancée dans lesquels chaque microservice détient son modèle de données.</span><span class="sxs-lookup"><span data-stu-id="1195c-110">At the end of the day, the container clustering solutions are useful for both a traditional SOA architecture or for a more advanced microservices architecture in which each microservice owns its data model.</span></span> <span data-ttu-id="1195c-111">Et grâce à plusieurs bases de données, vous également pouvez faire évoluer la couche de données au lieu de travailler avec des bases de données monolithiques partagés par les services SOA.</span><span class="sxs-lookup"><span data-stu-id="1195c-111">And, thanks to multiple databases, you also can scale-out the data tier instead of working with monolithic databases shared by the SOA services.</span></span> <span data-ttu-id="1195c-112">Toutefois, la discussion sur la division des données est purement sur l’architecture et de conception.</span><span class="sxs-lookup"><span data-stu-id="1195c-112">However, the discussion about splitting the data is purely about architecture and design.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="1195c-113">[Précédent](state-and-data-in-docker-applications.md)
>[Suivant](orchestrate-high-scalability-availability.md)</span><span class="sxs-lookup"><span data-stu-id="1195c-113">[Previous](state-and-data-in-docker-applications.md)
[Next](orchestrate-high-scalability-availability.md)</span></span>