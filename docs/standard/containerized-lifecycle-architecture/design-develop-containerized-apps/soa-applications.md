---
title: Applications SOA
description: N’oubliez pas que les conteneurs peuvent être également une option de déploiement utile pour les applications SOA.
ms.date: 02/15/2019
ms.openlocfilehash: aa56ada7b14a465fb3dafd02b03b815782ac765b
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65644761"
---
# <a name="service-oriented-applications"></a>Applications orientées service

Architecture orientée services (SOA) a été un terme surutilisé qui signifiait différentes choses pour différentes personnes. Mais comme un dénominateur commun, SOA signifie que vous structurez l’architecture de votre application en la décomposant en plusieurs services (généralement en tant que services HTTP) qui peuvent être classés dans les différents types, comme des sous-systèmes ou, dans d’autres cas, sous forme de niveaux.

Aujourd'hui, vous pouvez déployer ces services en tant que conteneurs Docker, capables de résoudre les problèmes liés au déploiement, car toutes les dépendances sont inclus dans l’image de conteneur. Toutefois, lorsque vous avez besoin faire évoluer les SOA, vous pouvez rencontrer défis si vous effectuez un déploiement en fonction des instances uniques. Ce défi peut être géré à l’aide du clustering des logiciels ou un orchestrateur Docker. Nous allons examiner orchestrateurs plus en détail dans la section suivante, lorsque nous explorons les approches de microservices.

Les conteneurs Docker sont pratiques (mais pas obligatoires) pour les architectures orientées services traditionnelles et pour les architectures de microservices plus avancées.

À la fin de la journée, les solutions de clustering de conteneur sont utiles pour les deux une architecture SOA traditionnelle et une architecture de microservices plus avancée dans lesquels chaque microservice détient son modèle de données. Et grâce à plusieurs bases de données, vous également pourrez monter en charge la couche de données au lieu de travailler avec des bases de données monolithiques partagés par les services SOA. Toutefois, la discussion sur la division des données est purement sur l’architecture et de conception.

>[!div class="step-by-step"]
>[Précédent](state-and-data-in-docker-applications.md)
>[Suivant](orchestrate-high-scalability-availability.md)
