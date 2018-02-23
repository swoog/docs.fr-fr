---
title: Conteneurs, images et registres Docker
description: Architecture des microservices .NET pour les applications .NET en conteneur | Conteneurs, images et registres Docker
keywords: Docker, microservices, ASP.NET, conteneur
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/26/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 79dccadfba066c673e8ef7ea5eaf1051a434ff3a
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="docker-containers-images-and-registries"></a><span data-ttu-id="abe39-104">Conteneurs, images et registres Docker</span><span class="sxs-lookup"><span data-stu-id="abe39-104">Docker containers, images, and registries</span></span>

<span data-ttu-id="abe39-105">Quand un développeur utilise Docker, il crée une application ou un service, qu’il empaquette ensuite avec les dépendances associées dans une image conteneur.</span><span class="sxs-lookup"><span data-stu-id="abe39-105">When using Docker, a developer creates an app or service and packages it and its dependencies into a container image.</span></span> <span data-ttu-id="abe39-106">Une image est une représentation statique de l’application ou du service, de leur configuration et de leurs dépendances.</span><span class="sxs-lookup"><span data-stu-id="abe39-106">An image is a static representation of the app or service and its configuration and dependencies.</span></span>

<span data-ttu-id="abe39-107">Pour exécuter l’application ou le service, l’image de l’application est instanciée, créant ainsi un conteneur à exécuter sur l’hôte Docker.</span><span class="sxs-lookup"><span data-stu-id="abe39-107">To run the app or service, the app’s image is instantiated to create a container, which will be running on the Docker host.</span></span> <span data-ttu-id="abe39-108">Les conteneurs sont initialement testés sur une machine ou un environnement de développement.</span><span class="sxs-lookup"><span data-stu-id="abe39-108">Containers are initially tested in a development environment or PC.</span></span>

<span data-ttu-id="abe39-109">Les développeurs doivent stocker les images dans un registre, comparable à une bibliothèque d’images, qui est utilisé pour le déploiement sur des orchestrateurs de production.</span><span class="sxs-lookup"><span data-stu-id="abe39-109">Developers should store images in a registry, which acts as a library of images and is needed when deploying to production orchestrators.</span></span> <span data-ttu-id="abe39-110">Docker gère un registre public via [Docker Hub](https://hub.docker.com/). D’autres fournisseurs proposent des registres pour différentes collections d’images.</span><span class="sxs-lookup"><span data-stu-id="abe39-110">Docker maintains a public registry via [Docker Hub](https://hub.docker.com/); other vendors provide registries for different collections of images.</span></span> <span data-ttu-id="abe39-111">Les entreprises peuvent également gérer un registre privé local pour stocker leurs propres images Docker.</span><span class="sxs-lookup"><span data-stu-id="abe39-111">Alternatively, enterprises can have a private registry on-premises for their own Docker images.</span></span>

<span data-ttu-id="abe39-112">La figure 2-4 montre les liens entre les images et registres Docker et les autres composants.</span><span class="sxs-lookup"><span data-stu-id="abe39-112">Figure 2-4 shows how images and registries in Docker relate to other components.</span></span> <span data-ttu-id="abe39-113">Elle montre également les divers registres des autres fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="abe39-113">It also shows the multiple registry offerings from vendors.</span></span>

![](./media/image5.PNG)

<span data-ttu-id="abe39-114">**Figure 2-4**.</span><span class="sxs-lookup"><span data-stu-id="abe39-114">**Figure 2-4**.</span></span> <span data-ttu-id="abe39-115">Taxonomie des termes et concepts Docker</span><span class="sxs-lookup"><span data-stu-id="abe39-115">Taxonomy of Docker terms and concepts</span></span>

<span data-ttu-id="abe39-116">Placer des images dans un registre vous permet de stocker les bits d’application statiques et immuables, y compris toutes les dépendances au niveau du framework.</span><span class="sxs-lookup"><span data-stu-id="abe39-116">Putting images in a registry lets you store static and immutable application bits, including all their dependencies at a framework level.</span></span> <span data-ttu-id="abe39-117">Ces images peuvent ensuite être versionnées et déployées dans différents environnements, offrant ainsi une unité de déploiement cohérente.</span><span class="sxs-lookup"><span data-stu-id="abe39-117">Those images can then be versioned and deployed in multiple environments and therefore provide a consistent deployment unit.</span></span>

<span data-ttu-id="abe39-118">L’utilisation de registres d’images privés, hébergés localement ou dans le cloud, est recommandée dans les situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="abe39-118">Private image registries, either hosted on-premises or in the cloud, are recommended when:</span></span>

-   <span data-ttu-id="abe39-119">Vous ne voulez pas partager vos images publiquement pour des raisons de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="abe39-119">Your images must not be shared publicly due to confidentiality.</span></span>

-   <span data-ttu-id="abe39-120">Vous souhaitez limiter la latence du réseau entre vos images et l’environnement de déploiement choisi.</span><span class="sxs-lookup"><span data-stu-id="abe39-120">You want to have minimum network latency between your images and your chosen deployment environment.</span></span> <span data-ttu-id="abe39-121">Par exemple, si votre environnement de production est le cloud Azure, vous souhaiterez probablement stocker vos images dans Azure Container Registry pour réduire au maximum la latence du réseau.</span><span class="sxs-lookup"><span data-stu-id="abe39-121">For example, if your production environment is Azure cloud, you probably want to store your images in Azure Container Registry so that network latency will be minimal.</span></span> <span data-ttu-id="abe39-122">De la même manière, si votre environnement de production est local, vous souhaiterez peut-être disposer d’un service Docker Trusted Registry local dans le même réseau local.</span><span class="sxs-lookup"><span data-stu-id="abe39-122">In a similar way, if your production environment is on-premises, you might want to have an on-premises Docker Trusted Registry available within the same local network.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="abe39-123">[Previous] (docker-terminology.md) [Next] (../net-core-net-framework-containers/index.md)</span><span class="sxs-lookup"><span data-stu-id="abe39-123">[Previous] (docker-terminology.md) [Next] (../net-core-net-framework-containers/index.md)</span></span>
