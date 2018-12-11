---
title: Concevoir des applications Docker
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/21/2017
ms.openlocfilehash: d02cec0595024eb7bd7c0ac46df093359680da74
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53155377"
---
# <a name="design-docker-applications"></a><span data-ttu-id="c8f2d-103">Concevoir des applications Docker</span><span class="sxs-lookup"><span data-stu-id="c8f2d-103">Design Docker applications</span></span>

<span data-ttu-id="c8f2d-104">Chapitre 1 a introduit les concepts fondamentaux concernant les conteneurs et Docker.</span><span class="sxs-lookup"><span data-stu-id="c8f2d-104">Chapter 1 introduced the fundamental concepts regarding containers and Docker.</span></span> <span data-ttu-id="c8f2d-105">Cette information est le niveau de base des informations que vous avez besoin pour commencer.</span><span class="sxs-lookup"><span data-stu-id="c8f2d-105">That information is the basic level of information you need to get started.</span></span> <span data-ttu-id="c8f2d-106">Toutefois, les applications d’entreprise peuvent être complexes et composé de plusieurs services au lieu d’un service unique ou un conteneur.</span><span class="sxs-lookup"><span data-stu-id="c8f2d-106">But, enterprise applications can be complex and composed of multiple services instead of a single service or container.</span></span> <span data-ttu-id="c8f2d-107">Pour ces cas d’usage facultatif, vous devez connaître les autres approches de conception, telles que les Architecture orientée services (SOA) et les concepts de microservices plus avancés et conteneur concepts d’orchestration.</span><span class="sxs-lookup"><span data-stu-id="c8f2d-107">For those optional use cases, you need to know additional approaches to design, such as Service-Oriented Architecture (SOA) and the more advanced microservices concepts and container orchestration concepts.</span></span> <span data-ttu-id="c8f2d-108">La portée de ce document n’est pas limitée aux microservices mais à un cycle de vie application Docker, par conséquent, il ne pas Explorer architecture de microservices en profondeur, car vous également pouvez utiliser des conteneurs et Docker avec SAO régulière, les tâches en arrière-plan ou les travaux, ou même avec des approches de déploiement d’application monolithique.</span><span class="sxs-lookup"><span data-stu-id="c8f2d-108">The scope of this document is not limited to microservices but to any Docker application life cycle, therefore, it does not explore microservices architecture in depth because you also can use containers and Docker with regular SAO, background tasks or jobs, or even with monolithic application deployment approaches.</span></span>

<span data-ttu-id="c8f2d-109">Toutefois, avant d’entrer dans le cycle de vie d’application et DevOps, il est important de savoir comment vous allez à la conception et de construire votre application et quelles sont vos choix de conception.</span><span class="sxs-lookup"><span data-stu-id="c8f2d-109">However, before we get into the application life cycle and DevOps, it is important to know how you are going to design and construct your application and what are your design choices.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="c8f2d-110">[Précédent](index.md)
>[Suivant](common-container-design-principles.md)</span><span class="sxs-lookup"><span data-stu-id="c8f2d-110">[Previous](index.md)
[Next](common-container-design-principles.md)</span></span>