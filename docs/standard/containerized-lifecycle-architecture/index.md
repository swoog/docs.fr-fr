---
title: Introduction aux conteneurs et à Docker
description: Obtenir une vue d’ensemble globale des principaux avantages de l’utilisation de Docker.
ms.date: 02/15/2019
ms.openlocfilehash: a03c67ed4fbc55c84e69fba5b7978863c8305e00
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65644953"
---
# <a name="introduction-to-containers-and-docker"></a>Présentation des conteneurs et de Docker

*Mise en conteneur est une approche de développement logiciel dans lequel une application ou service, ses dépendances et sa configuration (extraits sous forme de fichiers manifeste de déploiement) sont regroupés comme une image de conteneur. Vous pouvez ensuite tester l’application en conteneur en tant qu’unité et déployez-la en tant qu’une instance d’image de conteneur au système d’exploitation hôte (système d’exploitation).*

De la même manière que les conteneurs de transport permettent de transporter des marchandises par bateau, par train ou par camion indépendamment de la nature de la cargaison, les conteneurs logiciels agissent comme une unité de déploiement logiciel standard qui peut contenir du code et des dépendances différents. Cette façon de mettre les logiciels en conteneur permet aux développeurs et aux informaticiens de les déployer dans les environnements avec peu ou pas de modifications.

Par ailleurs, les conteneurs isolent les applications les unes des autres sur un SE partagé. Les applications en conteneur s’exécutent sur un hôte de conteneurs qui à son tour s’exécute sur le SE (Linux ou Windows). Par conséquent, les conteneurs ont beaucoup moins encombrantes que les images de machine virtuelle (VM).

Chaque conteneur peut exécuter une application web entière ou un service, comme indiqué dans la Figure 1-1. Dans cet exemple, hôte Docker est un hôte de conteneur, et App1, App2, Svc1 et Svc2 sont des applications ou services.

![Deux applications et deux services s’exécutant sur le système d’exploitation dans une machine virtuelle ou un serveur physique](./media/image1.png)

**Figure 1-1**. plusieurs conteneurs s’exécutant sur un hôte de conteneurs

L’autre avantage qui dérive de la mise en conteneur est la scalabilité. Vous pouvez rapidement monter en charge en créant des conteneurs pour des tâches à court terme. Du point de vue de l’application, instancier une image (c.-à-d., créer un conteneur) revient à instancier un processus comme un service ou une application web. Cependant, dans un souci de fiabilité, quand il s’agit d’exécuter plusieurs instances d’une même image sur plusieurs serveurs hôtes, il est en principe préférable que chaque conteneur (instance d’image) s’exécute sur un serveur hôte différent ou sur une machine virtuelle dans différents domaines d’erreur.

En bref, les conteneurs offrent les avantages de l’isolation, portabilité, flexibilité, évolutivité et de contrôle dans le flux de travail du cycle de vie ensemble de l’application. L’avantage le plus important est effectuée entre les services de développement et l’isolation de l’environnement.

>[!div class="step-by-step"]
>[Next](what-is-docker.md)
