---
title: Conteneurs, images et registres Docker
description: Découvrez le rôle de clé que les registres lire globales de la façon de Docker du déploiement d’applications.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 02/15/2019
ms.openlocfilehash: e69490734a03cf58bf8534bc9e31110a11d44c58
ms.sourcegitcommit: 07c4368273b446555cb2c85397ea266b39d5fe50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56583314"
---
# <a name="docker-containers-images-and-registries"></a><span data-ttu-id="65eb7-103">Conteneurs, images et registres Docker</span><span class="sxs-lookup"><span data-stu-id="65eb7-103">Docker containers, images, and registries</span></span>

<span data-ttu-id="65eb7-104">Lorsque vous utilisez Docker, vous créez une application ou le service et le package elle et ses dépendances dans une image de conteneur.</span><span class="sxs-lookup"><span data-stu-id="65eb7-104">When using Docker, you create an app or service and package it and its dependencies into a container image.</span></span> <span data-ttu-id="65eb7-105">Une image est une représentation statique de l’application ou du service, de leur configuration et de leurs dépendances.</span><span class="sxs-lookup"><span data-stu-id="65eb7-105">An image is a static representation of the app or service and its configuration and dependencies.</span></span>

<span data-ttu-id="65eb7-106">Pour exécuter l’application ou le service, l’image de l’application est instanciée, créant ainsi un conteneur à exécuter sur l’hôte Docker.</span><span class="sxs-lookup"><span data-stu-id="65eb7-106">To run the app or service, the app's image is instantiated to create a container, which will be running on the Docker host.</span></span> <span data-ttu-id="65eb7-107">Les conteneurs sont initialement testés sur une machine ou un environnement de développement.</span><span class="sxs-lookup"><span data-stu-id="65eb7-107">Containers are initially tested in a development environment or PC.</span></span>

<span data-ttu-id="65eb7-108">Vous stockez des images dans un Registre, qui agit en tant que bibliothèque d’images.</span><span class="sxs-lookup"><span data-stu-id="65eb7-108">You store images in a registry, that acts as a library of images.</span></span> <span data-ttu-id="65eb7-109">Vous avez besoin d’un Registre lors du déploiement vers des orchestrateurs de production.</span><span class="sxs-lookup"><span data-stu-id="65eb7-109">You need a registry when deploying to production orchestrators.</span></span> <span data-ttu-id="65eb7-110">Docker gère un registre public via [Docker Hub](https://hub.docker.com/). D’autres fournisseurs proposent des registres pour différentes collections d’images, notamment [Azure Container Registry](https://azure.microsoft.com/services/container-registry/).</span><span class="sxs-lookup"><span data-stu-id="65eb7-110">Docker maintains a public registry via [Docker Hub](https://hub.docker.com/); other vendors provide registries for different collections of images, including [Azure Container Registry](https://azure.microsoft.com/services/container-registry/).</span></span> <span data-ttu-id="65eb7-111">Les entreprises peuvent également gérer un registre privé local pour stocker leurs propres images Docker.</span><span class="sxs-lookup"><span data-stu-id="65eb7-111">Alternatively, enterprises can have a private registry on-premises for their own Docker images.</span></span>

<span data-ttu-id="65eb7-112">Figure 1-4 illustre comment les images et registres Docker sont liés à d’autres composants.</span><span class="sxs-lookup"><span data-stu-id="65eb7-112">Figure 1-4 shows how images and registries in Docker relate to other components.</span></span> <span data-ttu-id="65eb7-113">Elle montre également les divers registres des autres fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="65eb7-113">It also shows the multiple registry offerings from vendors.</span></span>

![Taxonomie de base dans Docker : Le Registre est comme une bibliothèque où les images sont stockées et peut être extrait pour la génération de conteneurs pour exécuter les services ou applications web.](./media/image4.png)

<span data-ttu-id="65eb7-118">**Figure 1-4**.</span><span class="sxs-lookup"><span data-stu-id="65eb7-118">**Figure 1-4**.</span></span> <span data-ttu-id="65eb7-119">Taxonomie des termes et concepts Docker</span><span class="sxs-lookup"><span data-stu-id="65eb7-119">Taxonomy of Docker terms and concepts</span></span>

<span data-ttu-id="65eb7-120">En plaçant des images dans un Registre, vous pouvez stocker les bits d’application statiques et immuables, y compris toutes leurs dépendances, au niveau du framework.</span><span class="sxs-lookup"><span data-stu-id="65eb7-120">By putting images in a registry, you can store static and immutable application bits, including all of their dependencies, at a framework level.</span></span> <span data-ttu-id="65eb7-121">Vous pouvez version et déployer des images dans plusieurs environnements, puis fournir ainsi une unité de déploiement cohérent.</span><span class="sxs-lookup"><span data-stu-id="65eb7-121">You then can version and deploy images in multiple environments and thus provide a consistent deployment unit.</span></span>

<span data-ttu-id="65eb7-122">L’utilisation de registres d’images privés, hébergés localement ou dans le cloud, est recommandée dans les situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="65eb7-122">Private image registries, either hosted on-premises or in the cloud, are recommended when:</span></span>

- <span data-ttu-id="65eb7-123">Vous ne voulez pas partager vos images publiquement pour des raisons de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="65eb7-123">Your images must not be shared publicly due to confidentiality.</span></span>

- <span data-ttu-id="65eb7-124">Vous souhaitez limiter la latence du réseau entre vos images et l’environnement de déploiement choisi.</span><span class="sxs-lookup"><span data-stu-id="65eb7-124">You want to have minimum network latency between your images and your chosen deployment environment.</span></span> <span data-ttu-id="65eb7-125">Par exemple, si votre environnement de production est Azure, vous souhaiterez probablement stocker vos images dans [Azure Container Registry](https://azure.microsoft.com/services/container-registry/) afin que la latence du réseau est minime.</span><span class="sxs-lookup"><span data-stu-id="65eb7-125">For example, if your production environment is Azure, you probably want to store your images in [Azure Container Registry](https://azure.microsoft.com/services/container-registry/) so that network latency is minimal.</span></span> <span data-ttu-id="65eb7-126">De la même manière, si votre environnement de production est local, vous souhaiterez peut-être disposer d’un service Docker Trusted Registry local dans le même réseau local.</span><span class="sxs-lookup"><span data-stu-id="65eb7-126">In a similar way, if your production environment is on-premises, you might want to have an on-premises Docker Trusted Registry available within the same local network.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="65eb7-127">[Précédent](docker-terminology.md)
>[Suivant](road-to-modern-applications-based-on-containers.md)</span><span class="sxs-lookup"><span data-stu-id="65eb7-127">[Previous](docker-terminology.md)
[Next](road-to-modern-applications-based-on-containers.md)</span></span>
