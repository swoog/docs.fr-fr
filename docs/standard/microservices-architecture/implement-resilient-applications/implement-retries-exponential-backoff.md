---
title: "Implémentation de nouvelles tentatives avec interruption exponentielle"
description: "Architecture des microservices .NET pour les applications .NET en conteneur | Implémentation de nouvelles tentatives avec interruption exponentielle"
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
ms.openlocfilehash: 7ed97b750d6e3f2aa5def72e90e070a49a7c0e63
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="implementing-retries-with-exponential-backoff"></a>Implémentation de nouvelles tentatives avec interruption exponentielle

Les [*nouvelles tentatives avec interruption exponentielle*](https://docs.microsoft.com/azure/architecture/patterns/retry) sont un mécanisme qui permet de retenter une opération après un temps d’attente qui augmente de manière exponentielle, jusqu’à ce que le nombre maximal de tentatives configuré a été atteint ([l’interruption exponentielle](https://en.wikipedia.org/wiki/Exponential_backoff)). Ce mécanisme prend en compte le fait que les ressources du cloud peuvent être indisponibles par intermittence pendant plus de quelques secondes pour une raison quelconque. C’est le cas, par exemple, quand un orchestrateur déplace un conteneur vers un autre nœud dans un cluster pour équilibrer la charge. Durant cette opération, certaines requêtes risquent d’échouer. Cela peut aussi se produire, par exemple, quand une base de données comme SQL Azure est déplacée sur un autre serveur pour équilibrer la charge. La base de données n’est alors plus disponible pendant plusieurs secondes.

Il existe plusieurs approches possibles pour implémenter la logique de nouvelles tentatives avec interruption exponentielle.


>[!div class="step-by-step"]
[Previous] (partial-failure-strategies.md) [Next] (implement-resilient-entity-framework-core-sql-connections.md)
