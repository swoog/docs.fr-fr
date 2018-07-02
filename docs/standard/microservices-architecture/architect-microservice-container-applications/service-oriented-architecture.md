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
# <a name="service-oriented-architecture"></a>Architecture orientée services 

SOA, ou Architecture orientée services, est un terme qui a été trop utilisé et qui a signifié des choses différentes pour différentes personnes. Un dénominateur commun est néanmoins que SOA signifie que vous structurez votre application en la décomposant en plusieurs services (la plupart du temps en services HTTP) qui peuvent être classés selon différents types, comme des sous-systèmes ou des niveaux.

Ces services peuvent désormais être déployés en tant que conteneurs Docker, ce qui résout les problèmes de déploiement, car toutes les dépendances sont incluses dans l’image du conteneur. Cependant, quand vous devez faire monter en charge des applications SOA, vous pouvez rencontrer des problèmes de scalabilité et de disponibilité si vous déployez sur des hôtes Docker simples. C’est là où les logiciels de clustering Docker ou un orchestrateur peuvent vous aider, comme c’est expliqué dans les sections suivantes, où nous décrivons les approches du déploiement pour les microservices.

Les conteneurs Docker sont pratiques (mais pas obligatoires) pour les architectures orientées services traditionnelles et pour les architectures de microservices plus avancées.

Les microservices dérivent de SOA, mais SOA est différent de l’architecture de microservices. Des fonctionnalités comme les grands courtiers centralisés, les orchestrateurs centralisés au niveau de l’organisation et [ESB (Enterprise Service Bus)](https://en.wikipedia.org/wiki/Enterprise_service_bus) sont habituelles dans SOA. Dans la plupart des cas cependant, celles-ci sont des antimodèles dans la communauté des microservices. En fait, certaines personnes affirment que « l’architecture de microservice est une architecture SOA bien conçue ».

Ce guide se concentre sur les microservices, car une approche SOA est moins stricte que la configuration requise et les techniques utilisées dans une architecture de microservices. Si vous savez créer une application basée sur des microservices, vous savez également créer une application orientée services plus simple.




>[!div class="step-by-step"]
[Précédent](docker-application-state-data.md)
[Suivant](microservices-architecture.md)
