---
title: Concevoir des applications Docker
description: Recherchez ici une référence à des instructions détaillées sur l’architecture de microservices, car il s’agit d’une rubrique qui n’est pas détaillé dans ce guide.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 02/15/2019
ms.openlocfilehash: 1d49f7509c0a12edfe375486429147e8fd240b2d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61799344"
---
# <a name="design-docker-applications"></a><span data-ttu-id="b4d58-103">Concevoir des applications Docker</span><span class="sxs-lookup"><span data-stu-id="b4d58-103">Design Docker applications</span></span>

<span data-ttu-id="b4d58-104">Chapitre 1 a introduit les concepts fondamentaux concernant les conteneurs et Docker.</span><span class="sxs-lookup"><span data-stu-id="b4d58-104">Chapter 1 introduced the fundamental concepts regarding containers and Docker.</span></span> <span data-ttu-id="b4d58-105">Cette information est le niveau de base des informations que vous avez besoin pour commencer.</span><span class="sxs-lookup"><span data-stu-id="b4d58-105">That information is the basic level of information you need to get started.</span></span> <span data-ttu-id="b4d58-106">Toutefois, les applications d’entreprise peuvent être complexes et composé de plusieurs services au lieu d’un service unique ou un conteneur.</span><span class="sxs-lookup"><span data-stu-id="b4d58-106">But, enterprise applications can be complex and composed of multiple services instead of a single service or container.</span></span> <span data-ttu-id="b4d58-107">Pour ces cas d’usage facultatif, vous devez connaître les autres approches de conception, telles que les Architecture orientée services (SOA) et les concepts de microservices plus avancés et conteneur concepts d’orchestration.</span><span class="sxs-lookup"><span data-stu-id="b4d58-107">For those optional use cases, you need to know additional approaches to design, such as Service-Oriented Architecture (SOA) and the more advanced microservices concepts and container orchestration concepts.</span></span> <span data-ttu-id="b4d58-108">La portée de ce document n’est pas limitée aux microservices mais à un cycle de vie application Docker, par conséquent, il ne pas Explorer architecture de microservices en profondeur, car vous également pouvez utiliser des conteneurs et Docker avec SOA régulière, les tâches en arrière-plan ou les travaux, ou même avec des approches de déploiement d’application monolithique.</span><span class="sxs-lookup"><span data-stu-id="b4d58-108">The scope of this document is not limited to microservices but to any Docker application life cycle, therefore, it does not explore microservices architecture in depth because you also can use containers and Docker with regular SOA, background tasks or jobs, or even with monolithic application deployment approaches.</span></span>

<span data-ttu-id="b4d58-109">**Plus d’informations** pour en savoir plus sur les applications d’entreprise et l’architecture de microservices en profondeur, lisez le guide [NET Microservices : Architecture pour les Applications .NET](../../microservices-architecture/index.md) que vous pouvez également télécharger à partir de <https://aka.ms/MicroservicesEbook>.</span><span class="sxs-lookup"><span data-stu-id="b4d58-109">**More info** To learn more about enterprise applications and microservices architecture in depth, read the guide [NET Microservices: Architecture for Containerized .NET Applications](../../microservices-architecture/index.md) that you can also download from <https://aka.ms/MicroservicesEbook>.</span></span>

<span data-ttu-id="b4d58-110">Toutefois, avant d’entrer dans le cycle de vie d’application et DevOps, il est important de savoir comment vous allez à la conception et de construire votre application et quelles sont vos choix de conception.</span><span class="sxs-lookup"><span data-stu-id="b4d58-110">However, before we get into the application life cycle and DevOps, it's important to know how you're going to design and construct your application and what are your design choices.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="b4d58-111">[Précédent](index.md)
>[Suivant](common-container-design-principles.md)</span><span class="sxs-lookup"><span data-stu-id="b4d58-111">[Previous](index.md)
[Next](common-container-design-principles.md)</span></span>