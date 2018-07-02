---
title: Conteneurs, images et registres Docker
description: Architecture des microservices .NET pour les applications .NET en conteneur | Conteneurs, images et registres Docker
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/26/2017
ms.openlocfilehash: 4716159d052fd8e229ac42e5d17c72717ac86d9f
ms.sourcegitcommit: 979597cd8055534b63d2c6ee8322938a27d0c87b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2018
ms.locfileid: "37106458"
---
# <a name="docker-containers-images-and-registries"></a>Conteneurs, images et registres Docker

Quand un développeur utilise Docker, il crée une application ou un service, qu’il empaquette ensuite avec les dépendances associées dans une image conteneur. Une image est une représentation statique de l’application ou du service, de leur configuration et de leurs dépendances.

Pour exécuter l’application ou le service, l’image de l’application est instanciée, créant ainsi un conteneur à exécuter sur l’hôte Docker. Les conteneurs sont initialement testés sur une machine ou un environnement de développement.

Les développeurs doivent stocker les images dans un registre, comparable à une bibliothèque d’images, qui est utilisé pour le déploiement sur des orchestrateurs de production. Docker gère un registre public via [Docker Hub](https://hub.docker.com/). D’autres fournisseurs proposent des registres pour différentes collections d’images. Les entreprises peuvent également gérer un registre privé local pour stocker leurs propres images Docker.

La figure 2-4 montre les liens entre les images et registres Docker et les autres composants. Elle montre également les divers registres des autres fournisseurs.

![](./media/image5.PNG)

**Figure 2-4**. Taxonomie des termes et concepts Docker

Placer des images dans un registre vous permet de stocker les bits d’application statiques et immuables, y compris toutes les dépendances au niveau du framework. Ces images peuvent ensuite être versionnées et déployées dans différents environnements, offrant ainsi une unité de déploiement cohérente.

L’utilisation de registres d’images privés, hébergés localement ou dans le cloud, est recommandée dans les situations suivantes :

-   Vous ne voulez pas partager vos images publiquement pour des raisons de confidentialité.

-   Vous souhaitez limiter la latence du réseau entre vos images et l’environnement de déploiement choisi. Par exemple, si votre environnement de production est le cloud Azure, vous souhaiterez probablement stocker vos images dans Azure Container Registry pour réduire au maximum la latence du réseau. De la même manière, si votre environnement de production est local, vous souhaiterez peut-être disposer d’un service Docker Trusted Registry local dans le même réseau local.

>[!div class="step-by-step"]
[Précédent](docker-terminology.md)
[Suivant](../net-core-net-framework-containers/index.md)
