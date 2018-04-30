---
title: Création d’images Docker .NET Core
description: Présentation des images Docker et de .NET Core
author: jralexander
ms.author: johalex
ms.date: 11/06/2017
ms.topic: tutorial
ms.prod: dotnet-core
ms.technology: dotnet-docker
ms.devlang: dotnet
ms.custom: mvc
manager: wpickett
ms.workload:
- dotnetcore
ms.openlocfilehash: c1983be59b4a961cabd94915852e0cab7811682c
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="building-docker-images-for-net-core-applications"></a><span data-ttu-id="c286f-103">Création d’images Docker pour les applications .NET Core</span><span class="sxs-lookup"><span data-stu-id="c286f-103">Building Docker Images for .NET Core Applications</span></span>

 <span data-ttu-id="c286f-104">Dans ce didacticiel, nous nous concentrons sur l’utilisation de .NET Core sur Docker.</span><span class="sxs-lookup"><span data-stu-id="c286f-104">In this tutorial, We focus on how to use .NET Core on Docker.</span></span> <span data-ttu-id="c286f-105">Tout d’abord, nous explorons les différentes images Docker proposées et gérées par Microsoft, ainsi que les cas d’usage.</span><span class="sxs-lookup"><span data-stu-id="c286f-105">First, we explore the different Docker images offered and maintained by Microsoft, and use cases.</span></span> <span data-ttu-id="c286f-106">Nous découvrons ensuite comment générer et dockeriser une application ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="c286f-106">We then learn how to build and dockerize an ASP.NET Core app.</span></span>

<span data-ttu-id="c286f-107">Au cours de ce didacticiel, vous apprenez à :</span><span class="sxs-lookup"><span data-stu-id="c286f-107">During the course of this tutorial, you learn:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="c286f-108">Découvrir les images Docker Microsoft .NET Core</span><span class="sxs-lookup"><span data-stu-id="c286f-108">Learn about Microsoft .NET Core Docker images</span></span> 
> * <span data-ttu-id="c286f-109">Obtenir un exemple d’application ASP.NET Core à dockeriser</span><span class="sxs-lookup"><span data-stu-id="c286f-109">Get an ASP.NET Core sample app to Dockerize</span></span>
> * <span data-ttu-id="c286f-110">Exécuter l’exemple d’application ASP.NET localement</span><span class="sxs-lookup"><span data-stu-id="c286f-110">Run the ASP.NET sample app locally</span></span>
> * <span data-ttu-id="c286f-111">Générer et exécuter l’exemple avec Docker pour des conteneurs Linux</span><span class="sxs-lookup"><span data-stu-id="c286f-111">Build and run the sample with Docker for Linux containers</span></span>
> * <span data-ttu-id="c286f-112">Générer et exécuter l’exemple avec Docker pour des conteneurs Windows</span><span class="sxs-lookup"><span data-stu-id="c286f-112">Build and run the sample with Docker for Windows containers</span></span>

## <a name="docker-image-optimizations"></a><span data-ttu-id="c286f-113">Optimisations des images Docker</span><span class="sxs-lookup"><span data-stu-id="c286f-113">Docker Image Optimizations</span></span>

<span data-ttu-id="c286f-114">Lors de la création d’images Docker pour les développeurs, nous nous sommes concentrés sur trois scénarios principaux :</span><span class="sxs-lookup"><span data-stu-id="c286f-114">When building Docker images for developers, we focused on three main scenarios:</span></span>

* <span data-ttu-id="c286f-115">Images utilisées pour développer des applications .NET Core</span><span class="sxs-lookup"><span data-stu-id="c286f-115">Images used to develop .NET Core apps</span></span>
* <span data-ttu-id="c286f-116">Images utilisées pour générer des applications .NET Core</span><span class="sxs-lookup"><span data-stu-id="c286f-116">Images used to build .NET Core apps</span></span>
* <span data-ttu-id="c286f-117">Images utilisées pour exécuter des applications .NET Core</span><span class="sxs-lookup"><span data-stu-id="c286f-117">Images used to run .NET Core apps</span></span>

<span data-ttu-id="c286f-118">Pourquoi trois images ?</span><span class="sxs-lookup"><span data-stu-id="c286f-118">Why three images?</span></span>
<span data-ttu-id="c286f-119">Lors du développement, de la génération et de l’exécution d’applications en conteneur, nous avons des priorités différentes.</span><span class="sxs-lookup"><span data-stu-id="c286f-119">When developing, building, and running containerized applications, we have different priorities.</span></span>

* <span data-ttu-id="c286f-120">**Développement :** la priorité porte sur la rapidité avec laquelle vous pouvez apporter des modifications de façon itérative, et la possibilité de déboguer les modifications.</span><span class="sxs-lookup"><span data-stu-id="c286f-120">**Development:**  The priority focuses on quickly iterate changes, and the ability to debug the changes.</span></span> <span data-ttu-id="c286f-121">La taille de l’image est moins importante que la possibilité d’apporter des modifications à votre code et de les voir rapidement.</span><span class="sxs-lookup"><span data-stu-id="c286f-121">The size of the image isn't as important, rather can you make changes to your code and see them quickly?</span></span>

* <span data-ttu-id="c286f-122">**Génération :** cette image contient tous les éléments nécessaires pour compiler votre application, ce qui inclut le compilateur et toutes les autres dépendances pour optimiser les fichiers binaires.</span><span class="sxs-lookup"><span data-stu-id="c286f-122">**Build:** This image contains everything needed to compile your app, which includes the compiler and any other dependencies to optimize the binaries.</span></span>  <span data-ttu-id="c286f-123">L’image de build vous permet de créer les ressources que vous placez dans une image de production.</span><span class="sxs-lookup"><span data-stu-id="c286f-123">You use the build image to create the assets you place into a production image.</span></span> <span data-ttu-id="c286f-124">Cette image est destinée à être utilisée dans une intégration continue ou dans un environnement de génération.</span><span class="sxs-lookup"><span data-stu-id="c286f-124">The build image would be used for continuous integration, or in a build environment.</span></span> <span data-ttu-id="c286f-125">Cette approche permet à un agent de build de compiler et générer l’application (avec toutes les dépendances requises) dans une instance d’image de build.</span><span class="sxs-lookup"><span data-stu-id="c286f-125">This approach allows a build agent to compile and build the application (with all the required dependencies) in a build image instance.</span></span> <span data-ttu-id="c286f-126">L’agent de build doit seulement savoir comment exécuter cette image Docker.</span><span class="sxs-lookup"><span data-stu-id="c286f-126">Your build agent only needs to know how to run this Docker image.</span></span>

* <span data-ttu-id="c286f-127">**Production :** la rapidité avec laquelle vous pouvez déployer et démarrer votre image.</span><span class="sxs-lookup"><span data-stu-id="c286f-127">**Production:** How fast you can deploy and start your image?</span></span> <span data-ttu-id="c286f-128">Comme cette image est de petite taille, les performances réseau entre votre Registre Docker et vos hôtes Docker sont optimisées.</span><span class="sxs-lookup"><span data-stu-id="c286f-128">This image is small so network performance from your Docker Registry to your Docker hosts is optimized.</span></span> <span data-ttu-id="c286f-129">Le contenu est prêt à s’exécuter, ce qui permet d’obtenir le temps le plus court entre l’exécution Docker et les résultats du traitement.</span><span class="sxs-lookup"><span data-stu-id="c286f-129">The contents are ready to run enabling the fastest time from Docker run to processing results.</span></span> <span data-ttu-id="c286f-130">La compilation de code dynamique n’est pas nécessaire dans le modèle Docker.</span><span class="sxs-lookup"><span data-stu-id="c286f-130">Dynamic code compilation isn't needed in the Docker model.</span></span> <span data-ttu-id="c286f-131">Le contenu que vous placez dans cette image est limité aux fichiers binaires et au contenu nécessaires pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="c286f-131">The content you place in this image would be limited to the binaries and content needed to run the application.</span></span>

    <span data-ttu-id="c286f-132">Par exemple, la sortie `dotnet publish` contient :</span><span class="sxs-lookup"><span data-stu-id="c286f-132">For example, the `dotnet publish` output contains:</span></span>

    * <span data-ttu-id="c286f-133">les fichiers binaires compilés</span><span class="sxs-lookup"><span data-stu-id="c286f-133">the compiled binaries</span></span>
    * <span data-ttu-id="c286f-134">les fichiers .js et .css</span><span class="sxs-lookup"><span data-stu-id="c286f-134">.js and .css files</span></span>


<span data-ttu-id="c286f-135">Il est utile d’inclure la sortie de la commande `dotnet publish` dans votre image de production si vous voulez conserver sa taille au minimum.</span><span class="sxs-lookup"><span data-stu-id="c286f-135">The reason to include the `dotnet publish` command output in your production image is to keep its' size to a minimum.</span></span>

<span data-ttu-id="c286f-136">Certaines images .NET Core partagent des couches entre différentes balises pour que le téléchargement de la dernière balise soit un processus relativement simple.</span><span class="sxs-lookup"><span data-stu-id="c286f-136">Some .NET Core images share layers between different tags so downloading the latest tag is a relatively lightweight process.</span></span> <span data-ttu-id="c286f-137">Si vous avez déjà une version antérieure sur votre ordinateur, cette architecture diminue l’espace disque nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c286f-137">If you already have an older version on your machine, this architecture decreases the needed disk space.</span></span>

<span data-ttu-id="c286f-138">Quand plusieurs applications utilisent des images communes sur le même ordinateur, la mémoire est partagée entre ces images.</span><span class="sxs-lookup"><span data-stu-id="c286f-138">When multiple applications use common images on the same machine, memory is shared between the common images.</span></span> <span data-ttu-id="c286f-139">Les images doivent être identiques pour être partagées.</span><span class="sxs-lookup"><span data-stu-id="c286f-139">The images must be the same to be shared.</span></span>

## <a name="docker-image-variations"></a><span data-ttu-id="c286f-140">Variantes des images Docker</span><span class="sxs-lookup"><span data-stu-id="c286f-140">Docker image variations</span></span>

<span data-ttu-id="c286f-141">Pour atteindre les objectifs ci-dessus, nous fournissons des variantes d’images sous [`microsoft/dotnet`](https://hub.docker.com/r/microsoft/dotnet/).</span><span class="sxs-lookup"><span data-stu-id="c286f-141">To achieve the goals above, we provide image variants under [`microsoft/dotnet`](https://hub.docker.com/r/microsoft/dotnet/).</span></span>

* <span data-ttu-id="c286f-142">`microsoft/dotnet:<version>-sdk`(`microsoft/dotnet:2.0.0-sdk`) Cette image contient le kit SDK .NET Core, qui inclut .NET Core et les outils en ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="c286f-142">`microsoft/dotnet:<version>-sdk`(`microsoft/dotnet:2.0.0-sdk`) This image contains the .NET Core SDK, which includes the .NET Core and Command Line Tools (CLI).</span></span> <span data-ttu-id="c286f-143">Cette image est adaptée au **scénario de développement**.</span><span class="sxs-lookup"><span data-stu-id="c286f-143">This image maps to the **development scenario**.</span></span> <span data-ttu-id="c286f-144">Vous utilisez cette image pour le développement local, le débogage et les tests unitaires.</span><span class="sxs-lookup"><span data-stu-id="c286f-144">You use this image for local development, debugging, and unit testing.</span></span> <span data-ttu-id="c286f-145">Cette image peut également être utilisée pour vos scénarios de **génération**.</span><span class="sxs-lookup"><span data-stu-id="c286f-145">This image can also be used for your **build** scenarios.</span></span> <span data-ttu-id="c286f-146">L’utilisation de `microsoft/dotnet:sdk` vous donne toujours la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="c286f-146">Using `microsoft/dotnet:sdk` always gives you the latest version.</span></span>

> [!TIP]
> <span data-ttu-id="c286f-147">Si vous ne savez pas de quoi vous avez besoin, vous pouvez utiliser l’image `microsoft/dotnet:<version>-sdk`.</span><span class="sxs-lookup"><span data-stu-id="c286f-147">If you are unsure about your needs, you want to use the `microsoft/dotnet:<version>-sdk` image.</span></span> <span data-ttu-id="c286f-148">En tant qu’image « de facto », elle est conçue pour être utilisée comme conteneur jetable (montez votre code source et démarrez le conteneur pour démarrer votre application) et comme image de base à partir de laquelle générer d’autres images.</span><span class="sxs-lookup"><span data-stu-id="c286f-148">As the "de facto" image, it's designed to be used as a throw away container (mount your source code and start the container to start your app), and as the base image to build other images from.</span></span>

* <span data-ttu-id="c286f-149">`microsoft/dotnet:<version>-runtime` : cette image contient .NET Core (runtime et bibliothèques) et est optimisée pour l’exécution des applications .NET Core en **production**.</span><span class="sxs-lookup"><span data-stu-id="c286f-149">`microsoft/dotnet:<version>-runtime`: This image contains the .NET Core (runtime and libraries) and is optimized for running .NET Core apps in **production**.</span></span>

## <a name="alternative-images"></a><span data-ttu-id="c286f-150">Images alternatives</span><span class="sxs-lookup"><span data-stu-id="c286f-150">Alternative images</span></span>

<span data-ttu-id="c286f-151">En plus des scénarios de développement, de génération et de production optimisés, nous fournissons des images supplémentaires :</span><span class="sxs-lookup"><span data-stu-id="c286f-151">In addition to the optimized scenarios of development, build and production, we provide additional images:</span></span>

* <span data-ttu-id="c286f-152">`microsoft/dotnet:<version>-runtime-deps` : l’image **runtime-deps** contient le système d’exploitation avec toutes les dépendances natives nécessaires à .NET Core.</span><span class="sxs-lookup"><span data-stu-id="c286f-152">`microsoft/dotnet:<version>-runtime-deps`: The **runtime-deps** image contains the operating system with all of the native dependencies needed by .NET Core.</span></span> <span data-ttu-id="c286f-153">Cette image est destinée aux [applications autonomes](../deploying/index.md).</span><span class="sxs-lookup"><span data-stu-id="c286f-153">This image is for [self-contained applications](../deploying/index.md).</span></span>

<span data-ttu-id="c286f-154">Versions les plus récentes de chaque variante :</span><span class="sxs-lookup"><span data-stu-id="c286f-154">Latest versions of each variant:</span></span>

* <span data-ttu-id="c286f-155">`microsoft/dotnet` ou `microsoft/dotnet:latest` (alias pour l’image du kit SDK)</span><span class="sxs-lookup"><span data-stu-id="c286f-155">`microsoft/dotnet` or `microsoft/dotnet:latest` (alias for the SDK image)</span></span>
* `microsoft/dotnet:sdk`
* `microsoft/dotnet:runtime`
* `microsoft/dotnet:runtime-deps`

## <a name="samples-to-explore"></a><span data-ttu-id="c286f-156">Exemples à explorer</span><span class="sxs-lookup"><span data-stu-id="c286f-156">Samples to explore</span></span>

* <span data-ttu-id="c286f-157">[Cet exemple d’ASP.NET Core Docker](https://github.com/dotnet/dotnet-docker-samples/tree/master/aspnetapp) montre un modèle des meilleures pratiques pour la création d’images Docker pour les applications ASP.NET Core pour la production.</span><span class="sxs-lookup"><span data-stu-id="c286f-157">[This ASP.NET Core Docker sample](https://github.com/dotnet/dotnet-docker-samples/tree/master/aspnetapp) demonstrates a best practice pattern for building Docker images for ASP.NET Core apps for production.</span></span> <span data-ttu-id="c286f-158">L’exemple s’applique aux conteneurs Linux et Windows.</span><span class="sxs-lookup"><span data-stu-id="c286f-158">The sample works with both Linux and Windows containers.</span></span>

* <span data-ttu-id="c286f-159">Cet exemple de Docker .NET Core montre un modèle des meilleures pratiques pour la [création d’images Docker pour les applications .NET Core pour la production.](https://github.com/dotnet/dotnet-docker-samples/tree/master/dotnetapp-prod)</span><span class="sxs-lookup"><span data-stu-id="c286f-159">This .NET Core Docker sample demonstrates a best practice pattern for [building Docker images for .NET Core apps for production.](https://github.com/dotnet/dotnet-docker-samples/tree/master/dotnetapp-prod)</span></span>

## <a name="your-first-aspnet-core-docker-app"></a><span data-ttu-id="c286f-160">Votre première application Docker ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="c286f-160">Your first ASP.NET Core Docker app</span></span>

<span data-ttu-id="c286f-161">Pour ce didacticiel, utilisons un exemple d’application Docker ASP.NET Core pour l’application à dockeriser.</span><span class="sxs-lookup"><span data-stu-id="c286f-161">For this tutorial, lets use an ASP.NET Core Docker sample application for the app we want to dockerize.</span></span> <span data-ttu-id="c286f-162">Cet exemple d’application Docker ASP.NET Core montre un modèle de bonnes pratiques de création d’images Docker pour les applications ASP.NET Core destinées à la production.</span><span class="sxs-lookup"><span data-stu-id="c286f-162">This ASP.NET Core Docker sample application demonstrates a best practice pattern for building Docker images for ASP.NET Core apps for production.</span></span> <span data-ttu-id="c286f-163">L’exemple s’applique aux conteneurs Linux et Windows.</span><span class="sxs-lookup"><span data-stu-id="c286f-163">The sample works with both Linux and Windows containers.</span></span>

<span data-ttu-id="c286f-164">L’exemple de fichier Dockerfile crée une image Docker d’application ASP.NET Core basée sur l’image de base Docker de runtime ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="c286f-164">The sample Dockerfile creates an ASP.NET Core application Docker image based off of the ASP.NET Core Runtime Docker base image.</span></span>

<span data-ttu-id="c286f-165">Il utilise la [fonctionnalité de build en plusieurs étapes Docker](https://docs.docker.com/engine/userguide/eng-image/multistage-build/) pour :</span><span class="sxs-lookup"><span data-stu-id="c286f-165">It uses the [Docker multi-stage build feature](https://docs.docker.com/engine/userguide/eng-image/multistage-build/) to:</span></span>

* <span data-ttu-id="c286f-166">Générer l’exemple dans un conteneur selon l’image de base Docker de build ASP.NET Core **la plus grande**</span><span class="sxs-lookup"><span data-stu-id="c286f-166">build the sample in a container based on the **larger** ASP.NET Core Build Docker base image</span></span> 
* <span data-ttu-id="c286f-167">Copier le résultat de la build finale dans une image Docker basée sur l’image de base Docker de runtime ASP.NET Core **la plus petite**</span><span class="sxs-lookup"><span data-stu-id="c286f-167">copies the final build result into a Docker image based on the **smaller** ASP.NET Core Docker Runtime base image</span></span>

> [!NOTE]
> <span data-ttu-id="c286f-168">L’image de build contient les outils requis pour créer des applications, contrairement à l’image de runtime.</span><span class="sxs-lookup"><span data-stu-id="c286f-168">The build image contains required tools to build applications while the runtime image does not.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="c286f-169">Prérequis</span><span class="sxs-lookup"><span data-stu-id="c286f-169">Prerequisites</span></span>

<span data-ttu-id="c286f-170">Pour générer et exécuter, installez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="c286f-170">To build and run, install the following items:</span></span>

#### <a name="net-core-20-sdk"></a><span data-ttu-id="c286f-171">Kit SDK .NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="c286f-171">.NET Core 2.0 SDK</span></span>

* <span data-ttu-id="c286f-172">Installez le [Kit SDK .NET Core 2.0](https://www.microsoft.com/net/core).</span><span class="sxs-lookup"><span data-stu-id="c286f-172">Install [.NET Core SDK 2.0](https://www.microsoft.com/net/core).</span></span>

* <span data-ttu-id="c286f-173">Installez votre éditeur de code favori, si ce n’est pas déjà fait.</span><span class="sxs-lookup"><span data-stu-id="c286f-173">Install your favorite code editor, if you haven't already.</span></span>

> [!TIP]
> <span data-ttu-id="c286f-174">Vous avez besoin d’installer un éditeur de code ?</span><span class="sxs-lookup"><span data-stu-id="c286f-174">Need to install a code editor?</span></span> <span data-ttu-id="c286f-175">Essayez [Visual Studio](https://visualstudio.com/downloads) !</span><span class="sxs-lookup"><span data-stu-id="c286f-175">Try [Visual Studio](https://visualstudio.com/downloads)!</span></span>

#### <a name="installing-docker-client"></a><span data-ttu-id="c286f-176">Installation du client Docker</span><span class="sxs-lookup"><span data-stu-id="c286f-176">Installing Docker Client</span></span>

<span data-ttu-id="c286f-177">Installez la version [Docker 17.06](https://docs.docker.com/release-notes/docker-ce/) ou ultérieure du client Docker.</span><span class="sxs-lookup"><span data-stu-id="c286f-177">Install [Docker 17.06](https://docs.docker.com/release-notes/docker-ce/) or later of the Docker client.</span></span>

<span data-ttu-id="c286f-178">Le client Docker peut être installé dans :</span><span class="sxs-lookup"><span data-stu-id="c286f-178">The Docker client can be installed in:</span></span>

* <span data-ttu-id="c286f-179">Distributions Linux</span><span class="sxs-lookup"><span data-stu-id="c286f-179">Linux distributions</span></span>

   * [<span data-ttu-id="c286f-180">CentOS</span><span class="sxs-lookup"><span data-stu-id="c286f-180">CentOS</span></span>](https://www.docker.com/docker-centos-distribution)

   * [<span data-ttu-id="c286f-181">Debian</span><span class="sxs-lookup"><span data-stu-id="c286f-181">Debian</span></span>](https://www.docker.com/docker-debian)

   * [<span data-ttu-id="c286f-182">Fedora</span><span class="sxs-lookup"><span data-stu-id="c286f-182">Fedora</span></span>](https://www.docker.com/docker-fedora)

   * [<span data-ttu-id="c286f-183">Ubuntu</span><span class="sxs-lookup"><span data-stu-id="c286f-183">Ubuntu</span></span>](https://www.docker.com/docker-ubuntu)

* [<span data-ttu-id="c286f-184">macOS</span><span class="sxs-lookup"><span data-stu-id="c286f-184">macOS</span></span>](https://docs.docker.com/docker-for-mac/)

* <span data-ttu-id="c286f-185">[Windows](https://docs.docker.com/docker-for-windows/).</span><span class="sxs-lookup"><span data-stu-id="c286f-185">[Windows](https://docs.docker.com/docker-for-windows/).</span></span>

#### <a name="installing-git-for-sample-repository"></a><span data-ttu-id="c286f-186">Installation de Git pour un dépôt d’exemples</span><span class="sxs-lookup"><span data-stu-id="c286f-186">Installing Git for sample repository</span></span>

* <span data-ttu-id="c286f-187">Installez [git](https://git-scm.com/download) si vous souhaitez cloner le dépôt.</span><span class="sxs-lookup"><span data-stu-id="c286f-187">Install [git](https://git-scm.com/download) if you wish to clone the repository.</span></span>

### <a name="getting-the-sample-application"></a><span data-ttu-id="c286f-188">Obtention de l’exemple d’application</span><span class="sxs-lookup"><span data-stu-id="c286f-188">Getting the sample application</span></span>

<span data-ttu-id="c286f-189">La façon la plus simple d’obtenir l’exemple consiste à cloner le [dépôt d’exemples](https://github.com/dotnet/dotnet-docker-samples) avec git, en utilisant les instructions suivantes :</span><span class="sxs-lookup"><span data-stu-id="c286f-189">The easiest way to get the sample is by cloning the [samples repository](https://github.com/dotnet/dotnet-docker-samples) with git, using the following instructions:</span></span> 

```console
git clone https://github.com/dotnet/dotnet-docker-samples/
```

<span data-ttu-id="c286f-190">Vous pouvez également télécharger le dépôt (qui est petit) comme un fichier zip à partir du dépôt d’exemples Docker .NET Core.</span><span class="sxs-lookup"><span data-stu-id="c286f-190">You can also download the repository (it is small) as a zip from the .NET Core Docker samples repository.</span></span>

### <a name="run-the-aspnet-app-locally"></a><span data-ttu-id="c286f-191">Exécuter l’application ASP.NET localement</span><span class="sxs-lookup"><span data-stu-id="c286f-191">Run the ASP.NET app locally</span></span>

<span data-ttu-id="c286f-192">Pour établir un point de référence, avant de mettre l’application dans un conteneur, exécutez l’application localement.</span><span class="sxs-lookup"><span data-stu-id="c286f-192">For a reference point, before we containerize the application, first run the application locally.</span></span>

<span data-ttu-id="c286f-193">Vous pouvez générer et exécuter l’application localement avec le kit SDK .NET Core 2.0 à l’aide des commandes suivantes (les instructions supposent la racine du dépôt) :</span><span class="sxs-lookup"><span data-stu-id="c286f-193">You can build and run the application locally with the .NET Core 2.0 SDK using the following commands (The instructions assume the root of the repository):</span></span>

```console
cd aspnetapp
dotnet run
```

<span data-ttu-id="c286f-194">Une fois que l’application démarre, accédez à **http://localhost:5000** dans votre navigateur web.</span><span class="sxs-lookup"><span data-stu-id="c286f-194">After the application starts, visit **http://localhost:5000** in your web browser.</span></span>

### <a name="build-and-run-the-sample-with-docker-for-linux-containers"></a><span data-ttu-id="c286f-195">Générer et exécuter l’exemple avec Docker pour des conteneurs Linux</span><span class="sxs-lookup"><span data-stu-id="c286f-195">Build and run the sample with Docker for Linux containers</span></span>

<span data-ttu-id="c286f-196">Vous pouvez générer et exécuter l’exemple dans Docker avec des conteneurs Linux à l’aide des commandes suivantes (les instructions supposent la racine du dépôt) :</span><span class="sxs-lookup"><span data-stu-id="c286f-196">You can build and run the sample in Docker using Linux containers using the following commands (The instructions assume the root of the repository):</span></span>

```console
cd aspnetapp
docker build -t aspnetapp .
docker run -it --rm -p 5000:80 --name aspnetcore_sample aspnetapp
```

> [!NOTE]
> <span data-ttu-id="c286f-197">L’argument `docker run` '-p' mappe le port 5000 sur votre ordinateur local au port 80 dans le conteneur (la forme de mappage de port est `host:container`).</span><span class="sxs-lookup"><span data-stu-id="c286f-197">The `docker run` '-p' argument maps port 5000 on your local machine to port 80 in the container (the port mapping form is `host:container`).</span></span> <span data-ttu-id="c286f-198">Pour plus d’informations, consultez la référence [docker run](https://docs.docker.com/engine/reference/commandline/exec/) dans les paramètres de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="c286f-198">For more information, see the [docker run](https://docs.docker.com/engine/reference/commandline/exec/) reference on command-line parameters.</span></span>

<span data-ttu-id="c286f-199">Une fois que l’application démarre, accédez à **http://localhost:5000** dans votre navigateur web.</span><span class="sxs-lookup"><span data-stu-id="c286f-199">After the application starts, visit **http://localhost:5000** in your web browser.</span></span>

### <a name="build-and-run-the-sample-with-docker-for-windows-containers"></a><span data-ttu-id="c286f-200">Générer et exécuter l’exemple avec Docker pour des conteneurs Windows</span><span class="sxs-lookup"><span data-stu-id="c286f-200">Build and run the sample with Docker for Windows containers</span></span>

<span data-ttu-id="c286f-201">Vous pouvez générer et exécuter l’exemple dans Docker avec des conteneurs Windows à l’aide des commandes suivantes (les instructions supposent la racine du dépôt) :</span><span class="sxs-lookup"><span data-stu-id="c286f-201">You can build and run the sample in Docker using Windows containers using the following commands (The instructions assume the root of the repository):</span></span>

```console
cd aspnetapp
docker build -t aspnetapp .
docker run -it --rm --name aspnetcore_sample aspnetapp
```

> [!IMPORTANT]
> <span data-ttu-id="c286f-202">Vous devez accéder directement à **l’adresse IP de conteneur** (par opposition à http://localhost)) dans votre navigateur lors de l’utilisation de conteneurs Windows.</span><span class="sxs-lookup"><span data-stu-id="c286f-202">You must navigate to the **container IP address** (as opposed to http://localhost) in your browser directly when using Windows containers.</span></span> <span data-ttu-id="c286f-203">Vous pouvez obtenir l’adresse IP de votre conteneur en effectuant les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="c286f-203">You can get the IP address of your container with the following steps:</span></span>

* <span data-ttu-id="c286f-204">Ouvrez une autre invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="c286f-204">Open up another command prompt.</span></span>
* <span data-ttu-id="c286f-205">Exécutez `docker ps` pour voir vos conteneurs en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c286f-205">Run `docker ps` to see your running containers.</span></span> <span data-ttu-id="c286f-206">Le conteneur « aspnetcore_sample » doit être visible.</span><span class="sxs-lookup"><span data-stu-id="c286f-206">The "aspnetcore_sample" container should be there.</span></span>
* <span data-ttu-id="c286f-207">Exécutez `docker exec aspnetcore_sample ipconfig`.</span><span class="sxs-lookup"><span data-stu-id="c286f-207">Run `docker exec aspnetcore_sample ipconfig`.</span></span>
* <span data-ttu-id="c286f-208">Copiez l’adresse IP de conteneur et collez-la dans votre navigateur (par exemple, 172.29.245.43).</span><span class="sxs-lookup"><span data-stu-id="c286f-208">Copy the container IP address and paste into your browser (for example, 172.29.245.43).</span></span>

> [!NOTE]
> <span data-ttu-id="c286f-209">Docker exec prend en charge l’identification des conteneurs avec le nom ou le hachage.</span><span class="sxs-lookup"><span data-stu-id="c286f-209">Docker exec supports identifying containers with name or hash.</span></span> <span data-ttu-id="c286f-210">Dans notre exemple, le nom (aspnetcore_sample) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="c286f-210">The name (aspnetcore_sample) is used in our example.</span></span>

<span data-ttu-id="c286f-211">Consultez l’exemple suivant illustrant comment obtenir l’adresse IP d’un conteneur Windows en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c286f-211">See the following example of how to get the IP address of a running Windows container.</span></span>

```console
docker exec aspnetcore_sample ipconfig

Windows IP Configuration

Ethernet adapter Ethernet:

   Connection-specific DNS Suffix  . : contoso.com
   Link-local IPv6 Address . . . . . : fe80::1967:6598:124:cfa3%4
   IPv4 Address. . . . . . . . . . . : 172.29.245.43
   Subnet Mask . . . . . . . . . . . : 255.255.240.0
   Default Gateway . . . . . . . . . : 172.29.240.1
```

> [!NOTE]
> <span data-ttu-id="c286f-212">Docker exec exécute une nouvelle commande dans un conteneur en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c286f-212">Docker exec runs a new command in a running container.</span></span> <span data-ttu-id="c286f-213">Pour plus d’informations, consultez la [référence docker exec](https://docs.docker.com/engine/reference/commandline/exec/) dans les paramètres de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="c286f-213">For more information, see the [docker exec reference](https://docs.docker.com/engine/reference/commandline/exec/) on command-line parameters.</span></span>

<span data-ttu-id="c286f-214">Vous pouvez générer une application qui est prête à être déployée en production localement à l’aide de la commande [dotnet publish](../tools/dotnet-publish.md).</span><span class="sxs-lookup"><span data-stu-id="c286f-214">You can produce an application that is ready to deploy to production locally using the [dotnet publish](../tools/dotnet-publish.md) command.</span></span>

```console
dotnet publish -c release -o published
```

> [!NOTE]
> <span data-ttu-id="c286f-215">L’argument -c release génère l’application en mode mise en production (la valeur par défaut est le mode débogage).</span><span class="sxs-lookup"><span data-stu-id="c286f-215">The -c release argument builds the application in release mode (the default is debug mode).</span></span> <span data-ttu-id="c286f-216">Pour plus d’informations, consultez la [référence dotnet run](../tools/dotnet-run.md) dans les paramètres de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="c286f-216">For more information, see the [dotnet run reference](../tools/dotnet-run.md) on command-line parameters.</span></span>

<span data-ttu-id="c286f-217">Vous pouvez exécuter l’application sur **Windows** à l’aide de la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="c286f-217">You can run the application on **Windows** using the following command.</span></span>

```console
dotnet published\aspnetapp.dll
```

<span data-ttu-id="c286f-218">Vous pouvez exécuter l’application sur **Linux** ou **macOS** à l’aide de la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="c286f-218">You can run the application on **Linux** or **macOS** using the following command.</span></span>

```bash
dotnet published/aspnetapp.dll
```

### <a name="docker-images-used-in-this-sample"></a><span data-ttu-id="c286f-219">Images Docker utilisées dans cet exemple</span><span class="sxs-lookup"><span data-stu-id="c286f-219">Docker Images used in this sample</span></span>

<span data-ttu-id="c286f-220">Les images Docker suivantes sont utilisées dans cet exemple</span><span class="sxs-lookup"><span data-stu-id="c286f-220">The following Docker images are used in this sample</span></span>

* `microsoft/aspnetcore-build:2.0`
* `microsoft/aspnetcore:2.0`

<span data-ttu-id="c286f-221">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="c286f-221">Congratulations!</span></span> <span data-ttu-id="c286f-222">Vous venez de :</span><span class="sxs-lookup"><span data-stu-id="c286f-222">you have just:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="c286f-223">Découvrir les images Docker Microsoft .NET Core</span><span class="sxs-lookup"><span data-stu-id="c286f-223">Learned about Microsoft .NET Core Docker images</span></span>
> * <span data-ttu-id="c286f-224">Obtenir un exemple d’application ASP.NET Core à dockeriser</span><span class="sxs-lookup"><span data-stu-id="c286f-224">Got an ASP.NET Core sample app to Dockerize</span></span>
> * <span data-ttu-id="c286f-225">Exécuter l’exemple d’application ASP.NET localement</span><span class="sxs-lookup"><span data-stu-id="c286f-225">Ran the ASP.NET sample app locally</span></span>
> * <span data-ttu-id="c286f-226">Générer et exécuter l’exemple avec Docker pour des conteneurs Linux</span><span class="sxs-lookup"><span data-stu-id="c286f-226">Built and ran the sample with Docker for Linux containers</span></span>
> * <span data-ttu-id="c286f-227">Générer et exécuter l’exemple avec Docker pour des conteneurs Windows</span><span class="sxs-lookup"><span data-stu-id="c286f-227">Built and ran the sample with Docker for Windows containers</span></span>


<span data-ttu-id="c286f-228">**Étapes suivantes**</span><span class="sxs-lookup"><span data-stu-id="c286f-228">**Next Steps**</span></span>

<span data-ttu-id="c286f-229">Voici quelques étapes suivantes que vous pouvez effectuer :</span><span class="sxs-lookup"><span data-stu-id="c286f-229">Here are some next steps you can take:</span></span>

* [<span data-ttu-id="c286f-230">Utilisation des outils Docker dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c286f-230">Working with Visual Studio Docker Tools</span></span>](https://docs.microsoft.com/aspnet/core/publishing/visual-studio-tools-for-docker)
* [<span data-ttu-id="c286f-231">Déploiement d’images Docker à partir du Registre de conteneurs Azure dans Azure Container Instances</span><span class="sxs-lookup"><span data-stu-id="c286f-231">Deploying Docker Images from the Azure Container Registry to Azure Container Instances</span></span>](https://blogs.msdn.microsoft.com/stevelasker/2017/07/28/deploying-docker-images-from-the-azure-container-registry-to-azure-container-instances/)
* [<span data-ttu-id="c286f-232">Débogage avec Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="c286f-232">Debugging with Visual Studio Code</span></span>](https://code.visualstudio.com/docs/nodejs/debugging-recipes#_nodejs-typescript-docker-container) 
* [<span data-ttu-id="c286f-233">Prise en main de Visual Studio pour Mac, les conteneurs et le code serverless dans le cloud</span><span class="sxs-lookup"><span data-stu-id="c286f-233">Getting hands on with Visual Studio for Mac, containers, and serverless code in the cloud</span></span>](https://blogs.msdn.microsoft.com/visualstudio/2017/08/31/hands-on-with-visual-studio-for-mac-containers-serverless-code-in-the-cloud/#comments)
* [<span data-ttu-id="c286f-234">Bien démarrer avec Docker et Visual Studio pour Mac Lab</span><span class="sxs-lookup"><span data-stu-id="c286f-234">Getting Started with Docker and Visual Studio for Mac Lab</span></span>](https://github.com/Microsoft/vs4mac-labs/tree/master/Docker/Getting-Started)

> [!NOTE]
> <span data-ttu-id="c286f-235">Si vous ne disposez pas d’abonnement Azure, [inscrivez-vous dès aujourd'hui](https://azure.microsoft.com/free/?b=16.48) pour obtenir un compte gratuit pendant 30 jours et 200 dollars US en crédits Azure pour essayer une combinaison quelconque de services Azure.</span><span class="sxs-lookup"><span data-stu-id="c286f-235">If you do not have an Azure subscription, [sign up today](https://azure.microsoft.com/free/?b=16.48) for a free 30-day account and get $200 in Azure Credits to try out any combination of Azure services.</span></span>
