---
title: Gestion d’une défaillance partielle
description: Architecture des microservices .NET pour les applications .NET en conteneur | Gestion d’une défaillance partielle
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/26/2017
ms.openlocfilehash: 957a0b1b8b4d217fac591db54e4ee053098bc7da
ms.sourcegitcommit: 979597cd8055534b63d2c6ee8322938a27d0c87b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2018
ms.locfileid: "37105193"
---
# <a name="handling-partial-failure"></a>Gestion d’une défaillance partielle

Dans les systèmes distribués tels que les applications basées sur des microservices, le risque de défaillance partielle est omniprésent. Par exemple, un microservice ou un conteneur peut échouer ou ne pas être disponible pour répondre pendant un court instant, ou une machine virtuelle ou un serveur peut connaître un incident. Étant donné que les clients et les services sont des processus distincts, il peut arriver qu’un service ne puisse pas répondre à temps à une requête d’un client. Le service peut être surchargé et répondre très lentement aux requêtes, ou il peut simplement ne pas être accessible pendant un bref laps de temps à cause de problèmes réseau.

Prenons la page des détails de commande dans l’exemple d’application eShopOnContainers. Si le microservice Ordering ne répond pas quand l’utilisateur tente d’envoyer sa commande, une mauvaise implémentation du processus client (l’application web MVC) peut bloquer indéfiniment les threads en attente d’une réponse. C’est le cas, par exemple, si le code client est défini pour utiliser des RPC synchrones sans délai d’expiration. Outre la mauvaise expérience que cela représente pour l’utilisateur, chaque attente de réponse consomme ou bloque un thread. Or les applications hautement évolutives ont besoin de beaucoup de threads. Si de nombreux threads sont bloqués, le runtime de l’application peut finir par ne plus disposer de suffisamment de threads. Si cela se produit, l’application risque de ne plus répondre du tout au lieu de ne plus répondre simplement partiellement, comme cela est illustré à la figure 10-1.

![](./media/image1.png)

**Figure 10-1**. Défaillances partielles dues à des dépendances qui impactent la disponibilité des threads du service

Dans une large application basée sur des microservices, une défaillance partielle peut avoir un impact plus global, surtout si la plupart des interactions de microservices internes sont basées sur des appels HTTP synchrones (ce qui est considéré comme anti-modèle). Pensez à un système qui reçoit des millions d’appels par jour. Si votre système a une mauvaise conception basée sur de longues chaînes d’appels HTTP synchrones, ces appels entrants peuvent provoquer des millions d’appels sortants supplémentaires (avec un ratio estimé de 1 pour 4) vers des dizaines de microservices internes et dépendances synchrones. Cette situation est illustrée à la figure 10-2, en particulier la dépendance \#3.

![](./media/image2.png)

**Figure 10-2**. Impact d’une mauvaise conception avec de longues chaînes de requêtes HTTP

Une défaillance intermittente est quasiment inévitable dans un système cloud et distribué, même si les dépendances présentent individuellement une haute disponibilité. C’est un point important à prendre en compte.

Si vous ne concevez pas et n’implémentez pas de techniques de tolérance de panne, même de courts temps d’arrêt peuvent avoir des répercussions amplifiées. Par exemple, l’existence de 50 dépendances avec 99,99 % de disponibilité se traduit par plusieurs heures d’arrêt chaque mois en raison de cet effet amplificateur. En cas d’échec d’une dépendance de microservice pendant le traitement d’un grand nombre de requêtes, cette défaillance peut rapidement saturer tous les threads de requête disponibles dans chaque service et entraîner le blocage de l’application entière.

![](./media/image3.png)

**Figure 10-3**. Défaillance partielle amplifiée par les microservices avec de longues chaînes d’appels HTTP synchrones

Pour limiter ce problème, nous vous recommandons d’utiliser la communication asynchrone entre les microservices internes, comme cela est expliqué dans la section *Asynchronous microservice integration enforce microservice’s autonomy* (dans le chapitre sur l’architecture). Nous expliquerons un peu plus ce point dans la section suivante.

De plus, il est essentiel de concevoir vos microservices et applications clientes pour gérer les défaillances partielles, et ainsi les rendre résilients.


>[!div class="step-by-step"]
[Précédent](index.md)
[Suivant](partial-failure-strategies.md)
