---
title: Implémenter de nouvelles tentatives avec interruption exponentielle
description: Architecture des microservices .NET pour les applications .NET en conteneur | Implémentation de nouvelles tentatives avec interruption exponentielle
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 06/08/2018
ms.openlocfilehash: e0758ee8fe28cb45ecd35ad07ddc738c12614973
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53148767"
---
# <a name="implement-retries-with-exponential-backoff"></a><span data-ttu-id="d7b73-103">Implémenter de nouvelles tentatives avec interruption exponentielle</span><span class="sxs-lookup"><span data-stu-id="d7b73-103">Implement retries with exponential backoff</span></span>

<span data-ttu-id="d7b73-104">Les [*nouvelles tentatives avec interruption exponentielle*](https://docs.microsoft.com/azure/architecture/patterns/retry) sont un mécanisme qui permet de retenter une opération après un temps d’attente qui augmente de manière exponentielle, jusqu’à ce que le nombre maximal de tentatives configuré a été atteint ([l’interruption exponentielle](https://en.wikipedia.org/wiki/Exponential_backoff)).</span><span class="sxs-lookup"><span data-stu-id="d7b73-104">[*Retries with exponential backoff*](https://docs.microsoft.com/azure/architecture/patterns/retry) is a technique that attempts to retry an operation, with an exponentially increasing wait time, until a maximum retry count has been reached (the [exponential backoff](https://en.wikipedia.org/wiki/Exponential_backoff)).</span></span> <span data-ttu-id="d7b73-105">Ce mécanisme prend en compte le fait que les ressources du cloud peuvent être indisponibles par intermittence pendant plus de quelques secondes pour une raison quelconque.</span><span class="sxs-lookup"><span data-stu-id="d7b73-105">This technique embraces the fact that cloud resources might intermittently be unavailable for more than a few seconds for any reason.</span></span> <span data-ttu-id="d7b73-106">C’est le cas, par exemple, quand un orchestrateur déplace un conteneur vers un autre nœud dans un cluster pour équilibrer la charge.</span><span class="sxs-lookup"><span data-stu-id="d7b73-106">For example, an orchestrator might be moving a container to another node in a cluster for load balancing.</span></span> <span data-ttu-id="d7b73-107">Durant cette opération, certaines requêtes risquent d’échouer.</span><span class="sxs-lookup"><span data-stu-id="d7b73-107">During that time, some requests might fail.</span></span> <span data-ttu-id="d7b73-108">Cela peut aussi se produire, par exemple, quand une base de données comme SQL Azure est déplacée sur un autre serveur pour équilibrer la charge. La base de données n’est alors plus disponible pendant plusieurs secondes.</span><span class="sxs-lookup"><span data-stu-id="d7b73-108">Another example could be a database like SQL Azure, where a database can be moved to another server for load balancing, causing the database to be unavailable for a few seconds.</span></span>

<span data-ttu-id="d7b73-109">Il existe plusieurs approches possibles pour implémenter la logique de nouvelles tentatives avec interruption exponentielle.</span><span class="sxs-lookup"><span data-stu-id="d7b73-109">There are many approaches to implement retries logic with exponential backoff.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="d7b73-110">[Précédent](partial-failure-strategies.md)
>[Suivant](implement-resilient-entity-framework-core-sql-connections.md)</span><span class="sxs-lookup"><span data-stu-id="d7b73-110">[Previous](partial-failure-strategies.md)
[Next](implement-resilient-entity-framework-core-sql-connections.md)</span></span>