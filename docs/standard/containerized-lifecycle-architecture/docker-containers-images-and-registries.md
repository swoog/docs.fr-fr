---
title: Conteneurs, images et registres Docker
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: af235280c985d20f9e6a2ee6096edbe6c3aad63a
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53142747"
---
# <a name="docker-containers-images-and-registries"></a><span data-ttu-id="4dfb1-103">Conteneurs, images et registres Docker</span><span class="sxs-lookup"><span data-stu-id="4dfb1-103">Docker containers, images, and registries</span></span>

<span data-ttu-id="4dfb1-104">Lorsque vous utilisez Docker, vous créez une application ou le service et le package elle et ses dépendances dans une image de conteneur.</span><span class="sxs-lookup"><span data-stu-id="4dfb1-104">When using Docker, you create an app or service and package it and its dependencies into a container image.</span></span> <span data-ttu-id="4dfb1-105">Une image est une représentation statique de l’application ou du service, de leur configuration et de leurs dépendances.</span><span class="sxs-lookup"><span data-stu-id="4dfb1-105">An image is a static representation of the app or service and its configuration and dependencies.</span></span>

<span data-ttu-id="4dfb1-106">Pour exécuter l’application ou le service, l’image de l’application est instanciée, créant ainsi un conteneur à exécuter sur l’hôte Docker.</span><span class="sxs-lookup"><span data-stu-id="4dfb1-106">To run the app or service, the app's image is instantiated to create a container, which will be running on the Docker host.</span></span> <span data-ttu-id="4dfb1-107">Les conteneurs sont initialement testés sur une machine ou un environnement de développement.</span><span class="sxs-lookup"><span data-stu-id="4dfb1-107">Containers are initially tested in a development environment or PC.</span></span>

<span data-ttu-id="4dfb1-108">Vous stockez des images dans un Registre, qui agit en tant que bibliothèque d’images.</span><span class="sxs-lookup"><span data-stu-id="4dfb1-108">You store images in a registry, which acts as a library of images.</span></span> <span data-ttu-id="4dfb1-109">Vous avez besoin d’un Registre lors du déploiement vers des orchestrateurs de production.</span><span class="sxs-lookup"><span data-stu-id="4dfb1-109">You need a registry when deploying to production orchestrators.</span></span> <span data-ttu-id="4dfb1-110">Docker gère un registre public via [Docker Hub](https://hub.docker.com/). D’autres fournisseurs proposent des registres pour différentes collections d’images.</span><span class="sxs-lookup"><span data-stu-id="4dfb1-110">Docker maintains a public registry via [Docker Hub](https://hub.docker.com/); other vendors provide registries for different collections of images.</span></span> <span data-ttu-id="4dfb1-111">Les entreprises peuvent également gérer un registre privé local pour stocker leurs propres images Docker.</span><span class="sxs-lookup"><span data-stu-id="4dfb1-111">Alternatively, enterprises can have a private registry on-premises for their own Docker images.</span></span>

<span data-ttu-id="4dfb1-112">Figure 1-4 illustre comment les images et registres Docker sont liés à d’autres composants.</span><span class="sxs-lookup"><span data-stu-id="4dfb1-112">Figure 1-4 shows how images and registries in Docker relate to other components.</span></span> <span data-ttu-id="4dfb1-113">Elle montre également les divers registres des autres fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="4dfb1-113">It also shows the multiple registry offerings from vendors.</span></span>

![](./media/image4.png)

<span data-ttu-id="4dfb1-114">Figure 1-4 : Taxonomie des termes et concepts Docker</span><span class="sxs-lookup"><span data-stu-id="4dfb1-114">Figure 1-4: Taxonomy of Docker terms and concepts</span></span>

<span data-ttu-id="4dfb1-115">En plaçant des images dans un Registre, vous pouvez stocker les bits d’application statiques et immuables, y compris toutes leurs dépendances, au niveau du framework.</span><span class="sxs-lookup"><span data-stu-id="4dfb1-115">By putting images in a registry, you can store static and immutable application bits, including all of their dependencies, at a framework level.</span></span> <span data-ttu-id="4dfb1-116">Vous pouvez version et déployer des images dans plusieurs environnements, puis fournir ainsi une unité de déploiement cohérent.</span><span class="sxs-lookup"><span data-stu-id="4dfb1-116">You then can version and deploy images in multiple environments and thus provide a consistent deployment unit.</span></span>

<span data-ttu-id="4dfb1-117">Registres d’images privés, hébergés localement ou dans le cloud, sont recommandés pour les situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="4dfb1-117">Private image registries, either hosted on-premises or in the cloud, are recommended for the following situations:</span></span>

-   <span data-ttu-id="4dfb1-118">Vous ne voulez pas partager vos images publiquement pour des raisons de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="4dfb1-118">Your images must not be shared publicly due to confidentiality.</span></span>

-   <span data-ttu-id="4dfb1-119">Vous souhaitez limiter la latence du réseau entre vos images et l’environnement de déploiement choisi.</span><span class="sxs-lookup"><span data-stu-id="4dfb1-119">You want to have minimum network latency between your images and your chosen deployment environment.</span></span> <span data-ttu-id="4dfb1-120">Par exemple, si votre environnement de production est Azure, vous souhaiterez probablement stocker vos images dans Azure Container Registry, afin que la latence du réseau sera minime.</span><span class="sxs-lookup"><span data-stu-id="4dfb1-120">For example, if your production environment is Azure, you probably want to store your images in Azure Container Registry so that network latency will be minimal.</span></span> <span data-ttu-id="4dfb1-121">De la même manière, si votre environnement de production est local, vous souhaiterez peut-être disposer d’un service Docker Trusted Registry local dans le même réseau local.</span><span class="sxs-lookup"><span data-stu-id="4dfb1-121">In a similar way, if your production environment is on-premises, you might want to have an on-premises Docker Trusted Registry available within the same local network.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="4dfb1-122">[Précédent](docker-terminology.md)
>[Suivant](Docker-application-lifecycle/index.md)</span><span class="sxs-lookup"><span data-stu-id="4dfb1-122">[Previous](docker-terminology.md)
[Next](Docker-application-lifecycle/index.md)</span></span>