---
title: Applications SOA
description: N’oubliez pas que les conteneurs peuvent être également une option de déploiement utile pour les applications SOA.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 02/15/2019
ms.openlocfilehash: 353ba738143b7dcd92c7c75ac27ea6a7370f9da6
ms.sourcegitcommit: 8f95d3a37e591963ebbb9af6e90686fd5f3b8707
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "56745831"
---
# <a name="service-oriented-applications"></a><span data-ttu-id="e72c1-103">Applications orientées service</span><span class="sxs-lookup"><span data-stu-id="e72c1-103">Service-oriented applications</span></span>

<span data-ttu-id="e72c1-104">Architecture orientée services (SOA) a été un terme surutilisé qui signifiait différentes choses pour différentes personnes.</span><span class="sxs-lookup"><span data-stu-id="e72c1-104">Service-Oriented Architecture (SOA) was an overused term that meant many different things to different people.</span></span> <span data-ttu-id="e72c1-105">Mais comme un dénominateur commun, SOA signifie que vous structurez l’architecture de votre application en la décomposant en plusieurs services (généralement en tant que services HTTP) qui peuvent être classés dans les différents types, comme des sous-systèmes ou, dans d’autres cas, sous forme de niveaux.</span><span class="sxs-lookup"><span data-stu-id="e72c1-105">But as a common denominator, SOA means that you structure the architecture of your application by decomposing it into several services (most commonly as HTTP services) that can be classified in different types like subsystems or, in other cases, as tiers.</span></span>

<span data-ttu-id="e72c1-106">Aujourd'hui, vous pouvez déployer ces services en tant que conteneurs Docker, capables de résoudre les problèmes liés au déploiement, car toutes les dépendances sont inclus dans l’image de conteneur.</span><span class="sxs-lookup"><span data-stu-id="e72c1-106">Today, you can deploy those services as Docker containers, which solve deployment-related issues because all of the dependencies are included in the container image.</span></span> <span data-ttu-id="e72c1-107">Toutefois, lorsque vous avez besoin faire évoluer les SOA, vous pouvez rencontrer des défis si vous déployez des instances uniques en fonction.</span><span class="sxs-lookup"><span data-stu-id="e72c1-107">However, when you need to scale out SOAs, you might encounter challenges if you are deploying based on single instances.</span></span> <span data-ttu-id="e72c1-108">Ce défi peut être géré à l’aide du clustering des logiciels ou un orchestrateur Docker.</span><span class="sxs-lookup"><span data-stu-id="e72c1-108">This challenge can be handled using Docker clustering software or an orchestrator.</span></span> <span data-ttu-id="e72c1-109">Nous allons examiner orchestrateurs plus en détail dans la section suivante, lorsque nous explorons les approches de microservices.</span><span class="sxs-lookup"><span data-stu-id="e72c1-109">We'll look at orchestrators in greater detail in the next section, when we explore microservices approaches.</span></span>

<span data-ttu-id="e72c1-110">Les conteneurs Docker sont pratiques (mais pas obligatoires) pour les architectures orientées services traditionnelles et pour les architectures de microservices plus avancées.</span><span class="sxs-lookup"><span data-stu-id="e72c1-110">Docker containers are useful (but not required) for both traditional service-oriented architectures and the more advanced microservices architectures.</span></span>

<span data-ttu-id="e72c1-111">À la fin de la journée, les solutions de clustering de conteneur sont utiles pour les deux une architecture SOA traditionnelle et une architecture de microservices plus avancée dans lesquels chaque microservice détient son modèle de données.</span><span class="sxs-lookup"><span data-stu-id="e72c1-111">At the end of the day, the container clustering solutions are useful for both a traditional SOA architecture and for a more advanced microservices architecture in which each microservice owns its data model.</span></span> <span data-ttu-id="e72c1-112">Et grâce à plusieurs bases de données, vous également pourrez monter en charge la couche de données au lieu de travailler avec des bases de données monolithiques partagés par les services SOA.</span><span class="sxs-lookup"><span data-stu-id="e72c1-112">And thanks to multiple databases, you also can scale out the data tier instead of working with monolithic databases shared by the SOA services.</span></span> <span data-ttu-id="e72c1-113">Toutefois, la discussion sur la division des données est purement sur l’architecture et de conception.</span><span class="sxs-lookup"><span data-stu-id="e72c1-113">However, the discussion about splitting the data is purely about architecture and design.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="e72c1-114">[Précédent](state-and-data-in-docker-applications.md)
>[Suivant](orchestrate-high-scalability-availability.md)</span><span class="sxs-lookup"><span data-stu-id="e72c1-114">[Previous](state-and-data-in-docker-applications.md)
[Next](orchestrate-high-scalability-availability.md)</span></span>
