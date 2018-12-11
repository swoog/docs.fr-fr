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
# <a name="soa-applications"></a>Applications SOA

SOA était un terme surutilisé et signifié des choses différentes tellement à différentes personnes. Mais au minimum et comme un dénominateur commun SOA, ou l’orientation service, moyenne structure l’architecture de votre application en la décomposant en plusieurs services (généralement en tant que services HTTP) qui peuvent être classés dans les différents types, tels que les sous-systèmes ou, dans d’autres cas, en tant que niveaux.

Aujourd'hui, vous pouvez déployer ces services en tant que conteneurs Docker, ce qui résout les problèmes liés au déploiement, car toutes les dépendances sont incluses dans l’image de conteneur. Toutefois, lorsque vous avez besoin pour la montée en puissance SOA, vous pouvez rencontrer des difficultés si vous déployez des instances uniques en fonction. Il s’agit où un Docker clustering logiciel ou orchestrator vous aidera à. Nous allons examiner cela plus en détail dans la section suivante lorsque nous examinons les approches de microservices.

À la fin de la journée, les solutions de clustering de conteneur sont utiles pour les deux une architecture SOA traditionnelle ou pour une architecture de microservices plus avancée dans lesquels chaque microservice détient son modèle de données. Et grâce à plusieurs bases de données, vous également pouvez faire évoluer la couche de données au lieu de travailler avec des bases de données monolithiques partagés par les services SOA. Toutefois, la discussion sur la division des données est purement sur l’architecture et de conception.

>[!div class="step-by-step"]
>[Précédent](state-and-data-in-docker-applications.md)
>[Suivant](orchestrate-high-scalability-availability.md)