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
# <a name="soa-applications"></a>Applications SOA

SOA était un terme surutilisé et signifié des choses différentes tellement à différentes personnes. Mais au minimum et comme un dénominateur commun SOA, ou l’orientation service, moyenne structure l’architecture de votre application en la décomposant en plusieurs services (généralement en tant que services HTTP) qui peuvent être classés dans les différents types, tels que les sous-systèmes ou, dans d’autres cas, en tant que niveaux.

Aujourd'hui, vous pouvez déployer ces services en tant que conteneurs Docker, ce qui résout les problèmes liés au déploiement, car toutes les dépendances sont incluses dans l’image de conteneur. Toutefois, lorsque vous avez besoin pour la montée en puissance SOA, vous pouvez rencontrer des difficultés si vous déployez des instances uniques en fonction. Il s’agit où un Docker clustering logiciel ou orchestrator vous aidera à. Nous allons examiner cela plus en détail dans la section suivante lorsque nous examinons les approches de microservices.

À la fin de la journée, les solutions de clustering de conteneur sont utiles pour les deux une architecture SOA traditionnelle ou pour une architecture de microservices plus avancée dans lesquels chaque microservice détient son modèle de données. Et grâce à plusieurs bases de données, vous également pouvez faire évoluer la couche de données au lieu de travailler avec des bases de données monolithiques partagés par les services SOA. Toutefois, la discussion sur la division des données est purement sur l’architecture et de conception.

>[!div class="step-by-step"]
>[Précédent](state-and-data-in-docker-applications.md)
>[Suivant](orchestrate-high-scalability-availability.md)