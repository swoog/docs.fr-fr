---
title: Conteneurs, images et registres Docker
description: Découvrez le rôle de clé que les registres lire globales de la façon de Docker du déploiement d’applications.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.openlocfilehash: 7a2e20e09561a5cc91aa29059fb8d19a14205bb5
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56221197"
---
# <a name="docker-containers-images-and-registries"></a>Conteneurs, images et registres Docker

Lorsque vous utilisez Docker, vous créez une application ou le service et le package elle et ses dépendances dans une image de conteneur. Une image est une représentation statique de l’application ou du service, de leur configuration et de leurs dépendances.

Pour exécuter l’application ou le service, l’image de l’application est instanciée, créant ainsi un conteneur à exécuter sur l’hôte Docker. Les conteneurs sont initialement testés sur une machine ou un environnement de développement.

Vous stockez des images dans un Registre, qui agit en tant que bibliothèque d’images. Vous avez besoin d’un Registre lors du déploiement vers des orchestrateurs de production. Docker gère un registre public via [Docker Hub](https://hub.docker.com/). D’autres fournisseurs proposent des registres pour différentes collections d’images. Les entreprises peuvent également gérer un registre privé local pour stocker leurs propres images Docker.

Figure 1-4 illustre comment les images et registres Docker sont liés à d’autres composants. Elle montre également les divers registres des autres fournisseurs.

![](./media/image4.png)

Figure 1-4 : Taxonomie des termes et concepts Docker

En plaçant des images dans un Registre, vous pouvez stocker les bits d’application statiques et immuables, y compris toutes leurs dépendances, au niveau du framework. Vous pouvez version et déployer des images dans plusieurs environnements, puis fournir ainsi une unité de déploiement cohérent.

Registres d’images privés, hébergés localement ou dans le cloud, sont recommandés pour les situations suivantes :

-   Vous ne voulez pas partager vos images publiquement pour des raisons de confidentialité.

-   Vous souhaitez limiter la latence du réseau entre vos images et l’environnement de déploiement choisi. Par exemple, si votre environnement de production est Azure, vous souhaiterez probablement stocker vos images dans Azure Container Registry, afin que la latence du réseau sera minime. De la même manière, si votre environnement de production est local, vous souhaiterez peut-être disposer d’un service Docker Trusted Registry local dans le même réseau local.

>[!div class="step-by-step"]
>[Précédent](docker-terminology.md)
>[Suivant](road-to-modern-applications-based-on-containers.md)
