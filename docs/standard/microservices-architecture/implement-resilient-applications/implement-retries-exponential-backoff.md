---
title: Implémentation de nouvelles tentatives avec interruption exponentielle
description: Architecture des microservices .NET pour les applications .NET en conteneur | Implémentation de nouvelles tentatives avec interruption exponentielle
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/26/2017
ms.openlocfilehash: ee5dd711484ba7861eedbd9613fda1209736d5b6
ms.sourcegitcommit: 979597cd8055534b63d2c6ee8322938a27d0c87b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2018
ms.locfileid: "37106916"
---
# <a name="implementing-retries-with-exponential-backoff"></a>Implémentation de nouvelles tentatives avec interruption exponentielle

Les [*nouvelles tentatives avec interruption exponentielle*](https://docs.microsoft.com/azure/architecture/patterns/retry) sont un mécanisme qui permet de retenter une opération après un temps d’attente qui augmente de manière exponentielle, jusqu’à ce que le nombre maximal de tentatives configuré a été atteint ([l’interruption exponentielle](https://en.wikipedia.org/wiki/Exponential_backoff)). Ce mécanisme prend en compte le fait que les ressources du cloud peuvent être indisponibles par intermittence pendant plus de quelques secondes pour une raison quelconque. C’est le cas, par exemple, quand un orchestrateur déplace un conteneur vers un autre nœud dans un cluster pour équilibrer la charge. Durant cette opération, certaines requêtes risquent d’échouer. Cela peut aussi se produire, par exemple, quand une base de données comme SQL Azure est déplacée sur un autre serveur pour équilibrer la charge. La base de données n’est alors plus disponible pendant plusieurs secondes.

Il existe plusieurs approches possibles pour implémenter la logique de nouvelles tentatives avec interruption exponentielle.


>[!div class="step-by-step"]
[Précédent](partial-failure-strategies.md)
[Suivant](implement-resilient-entity-framework-core-sql-connections.md)
