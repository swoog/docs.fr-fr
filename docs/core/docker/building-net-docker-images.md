---
title: Vue d’ensemble des images Docker
description: Découvrez comment utiliser les images Docker .NET Core publiées à partir du Registre Docker. Vous apprendrez également à extraire des images et à créer les vôtres.
ms.date: 11/06/2017
ms.topic: tutorial
ms.custom: mvc, seodec18
ms.openlocfilehash: dd8c6c500dc2177768e6cba0c1e303950e20d4f3
ms.sourcegitcommit: 3d0c29b878f00caec288dfecb3a5c959de5aa629
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/20/2018
ms.locfileid: "53656035"
---
# <a name="learn-about-docker-images-for-net-core"></a><span data-ttu-id="6d89d-104">Découvrir les images Docker pour .NET Core</span><span class="sxs-lookup"><span data-stu-id="6d89d-104">Learn about Docker images for .NET Core</span></span>

<span data-ttu-id="6d89d-105">Dans ce didacticiel, nous nous concentrons sur l’utilisation de .NET Core sur Docker.</span><span class="sxs-lookup"><span data-stu-id="6d89d-105">In this tutorial, We focus on how to use .NET Core on Docker.</span></span> <span data-ttu-id="6d89d-106">Tout d’abord, nous explorons les différentes images Docker proposées et gérées par Microsoft, ainsi que les cas d’usage.</span><span class="sxs-lookup"><span data-stu-id="6d89d-106">First, we explore the different Docker images offered and maintained by Microsoft, and use cases.</span></span> <span data-ttu-id="6d89d-107">Nous découvrons ensuite comment générer et dockeriser une application ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="6d89d-107">We then learn how to build and dockerize an ASP.NET Core app.</span></span>

<span data-ttu-id="6d89d-108">Au cours de ce didacticiel, vous apprenez à :</span><span class="sxs-lookup"><span data-stu-id="6d89d-108">During the course of this tutorial, you learn:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="6d89d-109">Découvrir les images Docker Microsoft .NET Core</span><span class="sxs-lookup"><span data-stu-id="6d89d-109">Learn about Microsoft .NET Core Docker images</span></span> 
> * <span data-ttu-id="6d89d-110">Obtenir un exemple d’application ASP.NET Core à dockeriser</span><span class="sxs-lookup"><span data-stu-id="6d89d-110">Get an ASP.NET Core sample app to Dockerize</span></span>
> * <span data-ttu-id="6d89d-111">Exécuter l’exemple d’application ASP.NET localement</span><span class="sxs-lookup"><span data-stu-id="6d89d-111">Run the ASP.NET sample app locally</span></span>
> * <span data-ttu-id="6d89d-112">Générer et exécuter l’exemple avec Docker pour des conteneurs Linux</span><span class="sxs-lookup"><span data-stu-id="6d89d-112">Build and run the sample with Docker for Linux containers</span></span>
> * <span data-ttu-id="6d89d-113">Générer et exécuter l’exemple avec Docker pour des conteneurs Windows</span><span class="sxs-lookup"><span data-stu-id="6d89d-113">Build and run the sample with Docker for Windows containers</span></span>

## <a name="docker-image-optimizations"></a><span data-ttu-id="6d89d-114">Optimisations des images Docker</span><span class="sxs-lookup"><span data-stu-id="6d89d-114">Docker Image Optimizations</span></span>

<span data-ttu-id="6d89d-115">Lors de la création d’images Docker pour les développeurs, nous nous sommes concentrés sur trois scénarios principaux :</span><span class="sxs-lookup"><span data-stu-id="6d89d-115">When building Docker images for developers, we focused on three main scenarios:</span></span>

* <span data-ttu-id="6d89d-116">Images utilisées pour développer des applications .NET Core</span><span class="sxs-lookup"><span data-stu-id="6d89d-116">Images used to develop .NET Core apps</span></span>
* <span data-ttu-id="6d89d-117">Images utilisées pour générer des applications .NET Core</span><span class="sxs-lookup"><span data-stu-id="6d89d-117">Images used to build .NET Core apps</span></span>
* <span data-ttu-id="6d89d-118">Images utilisées pour exécuter des applications .NET Core</span><span class="sxs-lookup"><span data-stu-id="6d89d-118">Images used to run .NET Core apps</span></span>

<span data-ttu-id="6d89d-119">Pourquoi trois images ?</span><span class="sxs-lookup"><span data-stu-id="6d89d-119">Why three images?</span></span>
<span data-ttu-id="6d89d-120">Lors du développement, de la génération et de l’exécution d’applications en conteneur, nous avons des priorités différentes.</span><span class="sxs-lookup"><span data-stu-id="6d89d-120">When developing, building, and running containerized applications, we have different priorities.</span></span>

* <span data-ttu-id="6d89d-121">**Développement :**  la priorité porte sur la rapidité avec laquelle vous pouvez apporter des modifications de façon itérative, et la possibilité de déboguer les modifications.</span><span class="sxs-lookup"><span data-stu-id="6d89d-121">**Development:**  The priority focuses on quickly iterate changes, and the ability to debug the changes.</span></span> <span data-ttu-id="6d89d-122">La taille de l’image est moins importante que la possibilité d’apporter des modifications à votre code et de les voir rapidement.</span><span class="sxs-lookup"><span data-stu-id="6d89d-122">The size of the image isn't as important, rather can you make changes to your code and see them quickly?</span></span>

* <span data-ttu-id="6d89d-123">**Build :** cette image contient tous les éléments nécessaires pour compiler votre application, ce qui inclut le compilateur et toutes les autres dépendances pour optimiser les fichiers binaires.</span><span class="sxs-lookup"><span data-stu-id="6d89d-123">**Build:** This image contains everything needed to compile your app, which includes the compiler and any other dependencies to optimize the binaries.</span></span>  <span data-ttu-id="6d89d-124">L’image de build vous permet de créer les ressources que vous placez dans une image de production.</span><span class="sxs-lookup"><span data-stu-id="6d89d-124">You use the build image to create the assets you place into a production image.</span></span> <span data-ttu-id="6d89d-125">Cette image est destinée à être utilisée dans une intégration continue ou dans un environnement de génération.</span><span class="sxs-lookup"><span data-stu-id="6d89d-125">The build image would be used for continuous integration, or in a build environment.</span></span> <span data-ttu-id="6d89d-126">Cette approche permet à un agent de build de compiler et générer l’application (avec toutes les dépendances requises) dans une instance d’image de build.</span><span class="sxs-lookup"><span data-stu-id="6d89d-126">This approach allows a build agent to compile and build the application (with all the required dependencies) in a build image instance.</span></span> <span data-ttu-id="6d89d-127">L’agent de build doit seulement savoir comment exécuter cette image Docker.</span><span class="sxs-lookup"><span data-stu-id="6d89d-127">Your build agent only needs to know how to run this Docker image.</span></span>

* <span data-ttu-id="6d89d-128">**Production :** la rapidité avec laquelle vous pouvez déployer et démarrer votre image.</span><span class="sxs-lookup"><span data-stu-id="6d89d-128">**Production:** How fast you can deploy and start your image?</span></span> <span data-ttu-id="6d89d-129">Comme cette image est de petite taille, les performances réseau entre votre Registre Docker et vos hôtes Docker sont optimisées.</span><span class="sxs-lookup"><span data-stu-id="6d89d-129">This image is small so network performance from your Docker Registry to your Docker hosts is optimized.</span></span> <span data-ttu-id="6d89d-130">Le contenu est prêt à s’exécuter, ce qui permet d’obtenir le temps le plus court entre l’exécution Docker et les résultats du traitement.</span><span class="sxs-lookup"><span data-stu-id="6d89d-130">The contents are ready to run enabling the fastest time from Docker run to processing results.</span></span> <span data-ttu-id="6d89d-131">La compilation de code dynamique n’est pas nécessaire dans le modèle Docker.</span><span class="sxs-lookup"><span data-stu-id="6d89d-131">Dynamic code compilation isn't needed in the Docker model.</span></span> <span data-ttu-id="6d89d-132">Le contenu que vous placez dans cette image est limité aux fichiers binaires et au contenu nécessaires pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="6d89d-132">The content you place in this image would be limited to the binaries and content needed to run the application.</span></span>

    <span data-ttu-id="6d89d-133">Par exemple, la sortie `dotnet publish` contient :</span><span class="sxs-lookup"><span data-stu-id="6d89d-133">For example, the `dotnet publish` output contains:</span></span>

    * <span data-ttu-id="6d89d-134">les fichiers binaires compilés</span><span class="sxs-lookup"><span data-stu-id="6d89d-134">the compiled binaries</span></span>
    * <span data-ttu-id="6d89d-135">les fichiers .js et .css</span><span class="sxs-lookup"><span data-stu-id="6d89d-135">.js and .css files</span></span>


<span data-ttu-id="6d89d-136">Il est utile d’inclure la sortie de la commande `dotnet publish` dans votre image de production si vous voulez conserver sa taille au minimum.</span><span class="sxs-lookup"><span data-stu-id="6d89d-136">The reason to include the `dotnet publish` command output in your production image is to keep its size to a minimum.</span></span>

<span data-ttu-id="6d89d-137">Certaines images .NET Core partagent des couches entre différentes balises pour que le téléchargement de la dernière balise soit un processus relativement simple.</span><span class="sxs-lookup"><span data-stu-id="6d89d-137">Some .NET Core images share layers between different tags so downloading the latest tag is a relatively lightweight process.</span></span> <span data-ttu-id="6d89d-138">Si vous avez déjà une version antérieure sur votre ordinateur, cette architecture diminue l’espace disque nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6d89d-138">If you already have an older version on your machine, this architecture decreases the needed disk space.</span></span>

<span data-ttu-id="6d89d-139">Quand plusieurs applications utilisent des images communes sur le même ordinateur, la mémoire est partagée entre ces images.</span><span class="sxs-lookup"><span data-stu-id="6d89d-139">When multiple applications use common images on the same machine, memory is shared between the common images.</span></span> <span data-ttu-id="6d89d-140">Les images doivent être identiques pour être partagées.</span><span class="sxs-lookup"><span data-stu-id="6d89d-140">The images must be the same to be shared.</span></span>

## <a name="docker-image-variations"></a><span data-ttu-id="6d89d-141">Variantes des images Docker</span><span class="sxs-lookup"><span data-stu-id="6d89d-141">Docker image variations</span></span>

<span data-ttu-id="6d89d-142">Pour atteindre les objectifs ci-dessus, nous fournissons des variantes d’images sous [`microsoft/dotnet`](https://hub.docker.com/r/microsoft/dotnet/).</span><span class="sxs-lookup"><span data-stu-id="6d89d-142">To achieve the goals above, we provide image variants under [`microsoft/dotnet`](https://hub.docker.com/r/microsoft/dotnet/).</span></span>

* <span data-ttu-id="6d89d-143">`microsoft/dotnet:<version>-sdk`(`microsoft/dotnet:2.1-sdk`) Cette image contient le kit SDK .NET Core, qui inclut .NET Core et les outils en ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="6d89d-143">`microsoft/dotnet:<version>-sdk`(`microsoft/dotnet:2.1-sdk`) This image contains the .NET Core SDK, which includes the .NET Core and Command Line Tools (CLI).</span></span> <span data-ttu-id="6d89d-144">Cette image est adaptée au **scénario de développement**.</span><span class="sxs-lookup"><span data-stu-id="6d89d-144">This image maps to the **development scenario**.</span></span> <span data-ttu-id="6d89d-145">Vous utilisez cette image pour le développement local, le débogage et les tests unitaires.</span><span class="sxs-lookup"><span data-stu-id="6d89d-145">You use this image for local development, debugging, and unit testing.</span></span> <span data-ttu-id="6d89d-146">Cette image peut également être utilisée pour vos scénarios de **génération**.</span><span class="sxs-lookup"><span data-stu-id="6d89d-146">This image can also be used for your **build** scenarios.</span></span> <span data-ttu-id="6d89d-147">L’utilisation de `microsoft/dotnet:sdk` vous donne toujours la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="6d89d-147">Using `microsoft/dotnet:sdk` always gives you the latest version.</span></span>

> [!TIP]
> <span data-ttu-id="6d89d-148">Si vous ne savez pas de quoi vous avez besoin, vous pouvez utiliser l’image `microsoft/dotnet:<version>-sdk`.</span><span class="sxs-lookup"><span data-stu-id="6d89d-148">If you are unsure about your needs, you want to use the `microsoft/dotnet:<version>-sdk` image.</span></span> <span data-ttu-id="6d89d-149">En tant qu’image « de facto », elle est conçue pour être utilisée comme conteneur jetable (montez votre code source et démarrez le conteneur pour démarrer votre application) et comme image de base à partir de laquelle générer d’autres images.</span><span class="sxs-lookup"><span data-stu-id="6d89d-149">As the "de facto" image, it's designed to be used as a throw away container (mount your source code and start the container to start your app), and as the base image to build other images from.</span></span>

* <span data-ttu-id="6d89d-150">`microsoft/dotnet:<version>-runtime`: cette image contient .NET Core (runtime et bibliothèques) et est optimisée pour l’exécution des applications .NET Core en **production**.</span><span class="sxs-lookup"><span data-stu-id="6d89d-150">`microsoft/dotnet:<version>-runtime`: This image contains the .NET Core (runtime and libraries) and is optimized for running .NET Core apps in **production**.</span></span>

## <a name="alternative-images"></a><span data-ttu-id="6d89d-151">Images alternatives</span><span class="sxs-lookup"><span data-stu-id="6d89d-151">Alternative images</span></span>

<span data-ttu-id="6d89d-152">En plus des scénarios de développement, de génération et de production optimisés, nous fournissons des images supplémentaires :</span><span class="sxs-lookup"><span data-stu-id="6d89d-152">In addition to the optimized scenarios of development, build and production, we provide additional images:</span></span>

* <span data-ttu-id="6d89d-153">`microsoft/dotnet:<version>-runtime-deps`: l’image **runtime-deps** contient le système d’exploitation avec toutes les dépendances natives nécessaires à .NET Core.</span><span class="sxs-lookup"><span data-stu-id="6d89d-153">`microsoft/dotnet:<version>-runtime-deps`: The **runtime-deps** image contains the operating system with all of the native dependencies needed by .NET Core.</span></span> <span data-ttu-id="6d89d-154">Cette image est destinée aux [applications autonomes](../deploying/index.md).</span><span class="sxs-lookup"><span data-stu-id="6d89d-154">This image is for [self-contained applications](../deploying/index.md).</span></span>

<span data-ttu-id="6d89d-155">Versions les plus récentes de chaque variante :</span><span class="sxs-lookup"><span data-stu-id="6d89d-155">Latest versions of each variant:</span></span>

* <span data-ttu-id="6d89d-156">`microsoft/dotnet` ou `microsoft/dotnet:latest` (alias pour l’image du kit SDK)</span><span class="sxs-lookup"><span data-stu-id="6d89d-156">`microsoft/dotnet` or `microsoft/dotnet:latest` (alias for the SDK image)</span></span>
* `microsoft/dotnet:sdk`
* `microsoft/dotnet:runtime`
* `microsoft/dotnet:runtime-deps`

## <a name="samples-to-explore"></a><span data-ttu-id="6d89d-157">Exemples à explorer</span><span class="sxs-lookup"><span data-stu-id="6d89d-157">Samples to explore</span></span>

* <span data-ttu-id="6d89d-158">[Cet exemple d’ASP.NET Core Docker](https://github.com/dotnet/dotnet-docker/tree/master/samples/aspnetapp) montre un modèle des meilleures pratiques pour la création d’images Docker pour les applications ASP.NET Core pour la production.</span><span class="sxs-lookup"><span data-stu-id="6d89d-158">[This ASP.NET Core Docker sample](https://github.com/dotnet/dotnet-docker/tree/master/samples/aspnetapp) demonstrates a best practice pattern for building Docker images for ASP.NET Core apps for production.</span></span> <span data-ttu-id="6d89d-159">L’exemple s’applique aux conteneurs Linux et Windows.</span><span class="sxs-lookup"><span data-stu-id="6d89d-159">The sample works with both Linux and Windows containers.</span></span>

* <span data-ttu-id="6d89d-160">Cet exemple de Docker .NET Core montre un modèle des meilleures pratiques pour la [création d’images Docker pour les applications .NET Core pour la production.](https://github.com/dotnet/dotnet-docker/tree/master/samples/dotnetapp)</span><span class="sxs-lookup"><span data-stu-id="6d89d-160">This .NET Core Docker sample demonstrates a best practice pattern for [building Docker images for .NET Core apps for production.](https://github.com/dotnet/dotnet-docker/tree/master/samples/dotnetapp)</span></span>

## <a name="forward-the-request-scheme-and-original-ip-address"></a><span data-ttu-id="6d89d-161">Transférer le schéma de demande et l’adresse IP d’origine</span><span class="sxs-lookup"><span data-stu-id="6d89d-161">Forward the request scheme and original IP address</span></span>

<span data-ttu-id="6d89d-162">Les serveurs proxy, les équilibreurs de charge et autres appliances réseau masquent souvent les informations sur une requête avant qu’elle n’atteigne l’application conteneurisée :</span><span class="sxs-lookup"><span data-stu-id="6d89d-162">Proxy servers, load balancers, and other network appliances often obscure information about a request before it reaches the containerized app:</span></span>

* <span data-ttu-id="6d89d-163">Quand les requêtes HTTPS sont transmises par proxy via HTTP, le schéma d’origine (HTTPS) est perdu et doit être transféré dans un en-tête.</span><span class="sxs-lookup"><span data-stu-id="6d89d-163">When HTTPS requests are proxied over HTTP, the original scheme (HTTPS) is lost and must be forwarded in a header.</span></span>
* <span data-ttu-id="6d89d-164">Étant donné qu’une application reçoit une requête du proxy et non pas de sa source réelle sur Internet ou sur le réseau d’entreprise, l’adresse IP du client d’origine doit également être transférée dans un en-tête.</span><span class="sxs-lookup"><span data-stu-id="6d89d-164">Because an app receives a request from the proxy and not its true source on the Internet or corporate network, the original client IP address must also be forwarded in a header.</span></span>

<span data-ttu-id="6d89d-165">Ces informations peuvent être importantes pour traiter les requêtes, par exemple dans les redirections, l’authentification, la génération de lien, l’évaluation des stratégies et la géolocalisation des clients.</span><span class="sxs-lookup"><span data-stu-id="6d89d-165">This information may be important in request processing, for example in redirects, authentication, link generation, policy evaluation, and client geolocation.</span></span>

<span data-ttu-id="6d89d-166">Pour transférer le schéma et l’adresse IP d’origine à une application ASP.NET Core conteneurisée, utilisez le middleware (intergiciel) d’en-têtes transférés.</span><span class="sxs-lookup"><span data-stu-id="6d89d-166">To forward the scheme and original IP address to a containerized ASP.NET Core app, use Forwarded Headers Middleware.</span></span> <span data-ttu-id="6d89d-167">Pour plus d’informations, consultez [Configurer ASP.NET Core pour l’utilisation de serveurs proxy et d’équilibreurs de charge](/aspnet/core/host-and-deploy/proxy-load-balancer).</span><span class="sxs-lookup"><span data-stu-id="6d89d-167">For more information, see [Configure ASP.NET Core to work with proxy servers and load balancers](/aspnet/core/host-and-deploy/proxy-load-balancer).</span></span>

## <a name="your-first-aspnet-core-docker-app"></a><span data-ttu-id="6d89d-168">Votre première application Docker ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="6d89d-168">Your first ASP.NET Core Docker app</span></span>

<span data-ttu-id="6d89d-169">Pour ce didacticiel, utilisons un exemple d’application Docker ASP.NET Core pour l’application à dockeriser.</span><span class="sxs-lookup"><span data-stu-id="6d89d-169">For this tutorial, lets use an ASP.NET Core Docker sample application for the app we want to dockerize.</span></span> <span data-ttu-id="6d89d-170">Cet exemple d’application Docker ASP.NET Core montre un modèle de bonnes pratiques de création d’images Docker pour les applications ASP.NET Core destinées à la production.</span><span class="sxs-lookup"><span data-stu-id="6d89d-170">This ASP.NET Core Docker sample application demonstrates a best practice pattern for building Docker images for ASP.NET Core apps for production.</span></span> <span data-ttu-id="6d89d-171">L’exemple s’applique aux conteneurs Linux et Windows.</span><span class="sxs-lookup"><span data-stu-id="6d89d-171">The sample works with both Linux and Windows containers.</span></span>

<span data-ttu-id="6d89d-172">L’exemple de fichier Dockerfile crée une image Docker d’application ASP.NET Core basée sur l’image de base Docker de runtime ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="6d89d-172">The sample Dockerfile creates an ASP.NET Core application Docker image based off of the ASP.NET Core Runtime Docker base image.</span></span>

<span data-ttu-id="6d89d-173">Il utilise la [fonctionnalité de build en plusieurs étapes Docker](https://docs.docker.com/engine/userguide/eng-image/multistage-build/) pour :</span><span class="sxs-lookup"><span data-stu-id="6d89d-173">It uses the [Docker multi-stage build feature](https://docs.docker.com/engine/userguide/eng-image/multistage-build/) to:</span></span>

* <span data-ttu-id="6d89d-174">Générer l’exemple dans un conteneur selon l’image de base Docker de build ASP.NET Core **la plus grande**</span><span class="sxs-lookup"><span data-stu-id="6d89d-174">build the sample in a container based on the **larger** ASP.NET Core Build Docker base image</span></span> 
* <span data-ttu-id="6d89d-175">Copier le résultat de la build finale dans une image Docker basée sur l’image de base Docker de runtime ASP.NET Core **la plus petite**</span><span class="sxs-lookup"><span data-stu-id="6d89d-175">copies the final build result into a Docker image based on the **smaller** ASP.NET Core Docker Runtime base image</span></span>

> [!NOTE]
> <span data-ttu-id="6d89d-176">L’image de build contient les outils requis pour créer des applications, contrairement à l’image de runtime.</span><span class="sxs-lookup"><span data-stu-id="6d89d-176">The build image contains required tools to build applications while the runtime image does not.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="6d89d-177">Prérequis</span><span class="sxs-lookup"><span data-stu-id="6d89d-177">Prerequisites</span></span>

<span data-ttu-id="6d89d-178">Pour générer et exécuter, installez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="6d89d-178">To build and run, install the following items:</span></span>

#### <a name="net-core-21-sdk"></a><span data-ttu-id="6d89d-179">SDK .NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="6d89d-179">.NET Core 2.1 SDK</span></span>

* <span data-ttu-id="6d89d-180">Installez le [Kit SDK .NET Core 2.1](https://www.microsoft.com/net/core).</span><span class="sxs-lookup"><span data-stu-id="6d89d-180">Install [.NET Core 2.1 SDK](https://www.microsoft.com/net/core).</span></span>

* <span data-ttu-id="6d89d-181">Installez votre éditeur de code favori, si ce n’est pas déjà fait.</span><span class="sxs-lookup"><span data-stu-id="6d89d-181">Install your favorite code editor, if you haven't already.</span></span>

> [!TIP]
> <span data-ttu-id="6d89d-182">Vous avez besoin d’installer un éditeur de code ?</span><span class="sxs-lookup"><span data-stu-id="6d89d-182">Need to install a code editor?</span></span> <span data-ttu-id="6d89d-183">Essayez [Visual Studio](https://visualstudio.com/downloads) !</span><span class="sxs-lookup"><span data-stu-id="6d89d-183">Try [Visual Studio](https://visualstudio.com/downloads)!</span></span>

#### <a name="installing-docker-client"></a><span data-ttu-id="6d89d-184">Installation du client Docker</span><span class="sxs-lookup"><span data-stu-id="6d89d-184">Installing Docker Client</span></span>

<span data-ttu-id="6d89d-185">Installez la version [Docker 18.03](https://docs.docker.com/release-notes/docker-ce/) ou ultérieure du client Docker.</span><span class="sxs-lookup"><span data-stu-id="6d89d-185">Install [Docker 18.03](https://docs.docker.com/release-notes/docker-ce/) or later of the Docker client.</span></span>

<span data-ttu-id="6d89d-186">Le client Docker peut être installé dans :</span><span class="sxs-lookup"><span data-stu-id="6d89d-186">The Docker client can be installed in:</span></span>

* <span data-ttu-id="6d89d-187">Distributions Linux</span><span class="sxs-lookup"><span data-stu-id="6d89d-187">Linux distributions</span></span>

   * [<span data-ttu-id="6d89d-188">CentOS</span><span class="sxs-lookup"><span data-stu-id="6d89d-188">CentOS</span></span>](https://docs.docker.com/install/linux/docker-ce/centos/)

   * [<span data-ttu-id="6d89d-189">Debian</span><span class="sxs-lookup"><span data-stu-id="6d89d-189">Debian</span></span>](https://docs.docker.com/install/linux/docker-ce/debian/)

   * [<span data-ttu-id="6d89d-190">Fedora</span><span class="sxs-lookup"><span data-stu-id="6d89d-190">Fedora</span></span>](https://docs.docker.com/install/linux/docker-ce/fedora/)

   * [<span data-ttu-id="6d89d-191">Ubuntu</span><span class="sxs-lookup"><span data-stu-id="6d89d-191">Ubuntu</span></span>](https://docs.docker.com/install/linux/docker-ce/ubuntu/)

* [<span data-ttu-id="6d89d-192">macOS</span><span class="sxs-lookup"><span data-stu-id="6d89d-192">macOS</span></span>](https://docs.docker.com/docker-for-mac/install/)

* <span data-ttu-id="6d89d-193">[Windows](https://docs.docker.com/docker-for-windows/install/).</span><span class="sxs-lookup"><span data-stu-id="6d89d-193">[Windows](https://docs.docker.com/docker-for-windows/install/).</span></span>

#### <a name="installing-git-for-sample-repository"></a><span data-ttu-id="6d89d-194">Installation de Git pour un dépôt d’exemples</span><span class="sxs-lookup"><span data-stu-id="6d89d-194">Installing Git for sample repository</span></span>

* <span data-ttu-id="6d89d-195">Installez [git](https://git-scm.com/download) si vous souhaitez cloner le dépôt.</span><span class="sxs-lookup"><span data-stu-id="6d89d-195">Install [git](https://git-scm.com/download) if you wish to clone the repository.</span></span>

### <a name="getting-the-sample-application"></a><span data-ttu-id="6d89d-196">Obtention de l’exemple d’application</span><span class="sxs-lookup"><span data-stu-id="6d89d-196">Getting the sample application</span></span>

<span data-ttu-id="6d89d-197">La façon la plus simple d’obtenir l’exemple consiste à cloner le [référentiel .NET Core Docker](https://github.com/dotnet/dotnet-docker) avec git, en utilisant les instructions suivantes :</span><span class="sxs-lookup"><span data-stu-id="6d89d-197">The easiest way to get the sample is by cloning the [.NET Core Docker repository](https://github.com/dotnet/dotnet-docker) with git, using the following instructions:</span></span> 

```console
git clone https://github.com/dotnet/dotnet-docker
```

<span data-ttu-id="6d89d-198">Vous pouvez également télécharger le dépôt (qui est petit) comme un fichier zip à partir du dépôt Docker .NET Core.</span><span class="sxs-lookup"><span data-stu-id="6d89d-198">You can also download the repository (it is small) as a zip from the .NET Core Docker repository.</span></span>

### <a name="run-the-aspnet-app-locally"></a><span data-ttu-id="6d89d-199">Exécuter l’application ASP.NET localement</span><span class="sxs-lookup"><span data-stu-id="6d89d-199">Run the ASP.NET app locally</span></span>

<span data-ttu-id="6d89d-200">Pour établir un point de référence, avant de mettre l’application dans un conteneur, exécutez l’application localement.</span><span class="sxs-lookup"><span data-stu-id="6d89d-200">For a reference point, before we containerize the application, first run the application locally.</span></span>

<span data-ttu-id="6d89d-201">Vous pouvez générer et exécuter l’application localement avec le kit SDK .NET Core 2.1 à l’aide des commandes suivantes (les instructions supposent la racine du dépôt) :</span><span class="sxs-lookup"><span data-stu-id="6d89d-201">You can build and run the application locally with the .NET Core 2.1 SDK using the following commands (The instructions assume the root of the repository):</span></span>

```console
cd dotnet-docker
cd samples
cd aspnetapp // solution scope where the dockerfile is located
cd aspnetapp // project scope

dotnet run
```

<span data-ttu-id="6d89d-202">Une fois que l’application démarre, accédez à **http://localhost:5000** dans votre navigateur web.</span><span class="sxs-lookup"><span data-stu-id="6d89d-202">After the application starts, visit **http://localhost:5000** in your web browser.</span></span>

### <a name="build-and-run-the-sample-with-docker-for-linux-containers"></a><span data-ttu-id="6d89d-203">Générer et exécuter l’exemple avec Docker pour des conteneurs Linux</span><span class="sxs-lookup"><span data-stu-id="6d89d-203">Build and run the sample with Docker for Linux containers</span></span>

<span data-ttu-id="6d89d-204">Vous pouvez générer et exécuter l’exemple dans Docker avec des conteneurs Linux à l’aide des commandes suivantes (les instructions supposent la racine du dépôt) :</span><span class="sxs-lookup"><span data-stu-id="6d89d-204">You can build and run the sample in Docker using Linux containers using the following commands (The instructions assume the root of the repository):</span></span>

```console
cd dotnet-docker
cd samples
cd aspnetapp // solution scope where the dockerfile is located

docker build -t aspnetapp .
docker run -it --rm -p 5000:80 --name aspnetcore_sample aspnetapp
```

> [!NOTE]
> <span data-ttu-id="6d89d-205">L’argument `docker run` '-p' mappe le port 5000 sur votre ordinateur local au port 80 dans le conteneur (la forme de mappage de port est `host:container`).</span><span class="sxs-lookup"><span data-stu-id="6d89d-205">The `docker run` '-p' argument maps port 5000 on your local machine to port 80 in the container (the port mapping form is `host:container`).</span></span> <span data-ttu-id="6d89d-206">Pour plus d’informations, consultez la référence [docker run](https://docs.docker.com/engine/reference/commandline/exec/) dans les paramètres de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="6d89d-206">For more information, see the [docker run](https://docs.docker.com/engine/reference/commandline/exec/) reference on command-line parameters.</span></span>

<span data-ttu-id="6d89d-207">Une fois que l’application démarre, accédez à **http://localhost:5000** dans votre navigateur web.</span><span class="sxs-lookup"><span data-stu-id="6d89d-207">After the application starts, visit **http://localhost:5000** in your web browser.</span></span>

### <a name="build-and-run-the-sample-with-docker-for-windows-containers"></a><span data-ttu-id="6d89d-208">Générer et exécuter l’exemple avec Docker pour des conteneurs Windows</span><span class="sxs-lookup"><span data-stu-id="6d89d-208">Build and run the sample with Docker for Windows containers</span></span>

<span data-ttu-id="6d89d-209">Vous pouvez générer et exécuter l’exemple dans Docker avec des conteneurs Windows à l’aide des commandes suivantes (les instructions supposent la racine du dépôt) :</span><span class="sxs-lookup"><span data-stu-id="6d89d-209">You can build and run the sample in Docker using Windows containers using the following commands (The instructions assume the root of the repository):</span></span>

```console
cd dotnet-docker
cd samples
cd aspnetapp // solution scope where the dockerfile is located

docker build -t aspnetapp .
docker run -it --rm --name aspnetcore_sample aspnetapp
```

> [!IMPORTANT]
> <span data-ttu-id="6d89d-210">Si vous utilisez des conteneurs Windows, vous devez accéder directement à **l’adresse IP de conteneur** (par opposition à `http://localhost`) dans votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="6d89d-210">You must navigate to the **container IP address** (as opposed to `http://localhost`) in your browser directly when using Windows containers.</span></span> <span data-ttu-id="6d89d-211">Vous pouvez obtenir l’adresse IP de votre conteneur en effectuant les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="6d89d-211">You can get the IP address of your container with the following steps:</span></span>

* <span data-ttu-id="6d89d-212">Ouvrez une autre invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="6d89d-212">Open up another command prompt.</span></span>
* <span data-ttu-id="6d89d-213">Exécutez `docker ps` pour voir vos conteneurs en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="6d89d-213">Run `docker ps` to see your running containers.</span></span> <span data-ttu-id="6d89d-214">Le conteneur « aspnetcore_sample » doit être visible.</span><span class="sxs-lookup"><span data-stu-id="6d89d-214">The "aspnetcore_sample" container should be there.</span></span>
* <span data-ttu-id="6d89d-215">Exécutez `docker exec aspnetcore_sample ipconfig`.</span><span class="sxs-lookup"><span data-stu-id="6d89d-215">Run `docker exec aspnetcore_sample ipconfig`.</span></span>
* <span data-ttu-id="6d89d-216">Copiez l’adresse IP de conteneur et collez-la dans votre navigateur (par exemple, 172.29.245.43).</span><span class="sxs-lookup"><span data-stu-id="6d89d-216">Copy the container IP address and paste into your browser (for example, 172.29.245.43).</span></span>

> [!NOTE]
> <span data-ttu-id="6d89d-217">Docker exec prend en charge l’identification des conteneurs avec le nom ou le hachage.</span><span class="sxs-lookup"><span data-stu-id="6d89d-217">Docker exec supports identifying containers with name or hash.</span></span> <span data-ttu-id="6d89d-218">Dans notre exemple, le nom (aspnetcore_sample) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="6d89d-218">The name (aspnetcore_sample) is used in our example.</span></span>

<span data-ttu-id="6d89d-219">Consultez l’exemple suivant illustrant comment obtenir l’adresse IP d’un conteneur Windows en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="6d89d-219">See the following example of how to get the IP address of a running Windows container.</span></span>

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
> <span data-ttu-id="6d89d-220">Docker exec exécute une nouvelle commande dans un conteneur en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="6d89d-220">Docker exec runs a new command in a running container.</span></span> <span data-ttu-id="6d89d-221">Pour plus d’informations, consultez la [référence docker exec](https://docs.docker.com/engine/reference/commandline/exec/) dans les paramètres de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="6d89d-221">For more information, see the [docker exec reference](https://docs.docker.com/engine/reference/commandline/exec/) on command-line parameters.</span></span>

<span data-ttu-id="6d89d-222">Vous pouvez générer une application qui est prête à être déployée en production localement à l’aide de la commande [dotnet publish](../tools/dotnet-publish.md).</span><span class="sxs-lookup"><span data-stu-id="6d89d-222">You can produce an application that is ready to deploy to production locally using the [dotnet publish](../tools/dotnet-publish.md) command.</span></span>

```console
dotnet publish -c Release -o published
```

> [!NOTE]
> <span data-ttu-id="6d89d-223">L’argument -c Release génère l’application en mode mise en production (la valeur par défaut est le mode débogage).</span><span class="sxs-lookup"><span data-stu-id="6d89d-223">The -c Release argument builds the application in release mode (the default is debug mode).</span></span> <span data-ttu-id="6d89d-224">Pour plus d’informations, consultez la [référence dotnet run](../tools/dotnet-run.md) dans les paramètres de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="6d89d-224">For more information, see the [dotnet run reference](../tools/dotnet-run.md) on command-line parameters.</span></span>

<span data-ttu-id="6d89d-225">Vous pouvez exécuter l’application sur **Windows** à l’aide de la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="6d89d-225">You can run the application on **Windows** using the following command.</span></span>

```console
dotnet published\aspnetapp.dll
```

<span data-ttu-id="6d89d-226">Vous pouvez exécuter l’application sur **Linux** ou **macOS** à l’aide de la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="6d89d-226">You can run the application on **Linux** or **macOS** using the following command.</span></span>

```bash
dotnet published/aspnetapp.dll
```

### <a name="docker-images-used-in-this-sample"></a><span data-ttu-id="6d89d-227">Images Docker utilisées dans cet exemple</span><span class="sxs-lookup"><span data-stu-id="6d89d-227">Docker Images used in this sample</span></span>

<span data-ttu-id="6d89d-228">Les images Docker suivantes sont utilisées dans cet exemple de fichier Dockerfile.</span><span class="sxs-lookup"><span data-stu-id="6d89d-228">The following Docker images are used in this sample's dockerfile.</span></span>

* `microsoft/dotnet:2.1-sdk`
* `microsoft/dotnet:2.1-aspnetcore-runtime`

<span data-ttu-id="6d89d-229">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="6d89d-229">Congratulations!</span></span> <span data-ttu-id="6d89d-230">Vous venez de :</span><span class="sxs-lookup"><span data-stu-id="6d89d-230">you have just:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="6d89d-231">Découvrir les images Docker Microsoft .NET Core</span><span class="sxs-lookup"><span data-stu-id="6d89d-231">Learned about Microsoft .NET Core Docker images</span></span>
> * <span data-ttu-id="6d89d-232">Obtenir un exemple d’application ASP.NET Core à dockeriser</span><span class="sxs-lookup"><span data-stu-id="6d89d-232">Got an ASP.NET Core sample app to Dockerize</span></span>
> * <span data-ttu-id="6d89d-233">Exécuter l’exemple d’application ASP.NET localement</span><span class="sxs-lookup"><span data-stu-id="6d89d-233">Ran the ASP.NET sample app locally</span></span>
> * <span data-ttu-id="6d89d-234">Générer et exécuter l’exemple avec Docker pour des conteneurs Linux</span><span class="sxs-lookup"><span data-stu-id="6d89d-234">Built and ran the sample with Docker for Linux containers</span></span>
> * <span data-ttu-id="6d89d-235">Générer et exécuter l’exemple avec Docker pour des conteneurs Windows</span><span class="sxs-lookup"><span data-stu-id="6d89d-235">Built and ran the sample with Docker for Windows containers</span></span>

<span data-ttu-id="6d89d-236">**Étapes suivantes**</span><span class="sxs-lookup"><span data-stu-id="6d89d-236">**Next Steps**</span></span>

<span data-ttu-id="6d89d-237">Voici quelques étapes suivantes que vous pouvez effectuer :</span><span class="sxs-lookup"><span data-stu-id="6d89d-237">Here are some next steps you can take:</span></span>

* [<span data-ttu-id="6d89d-238">Utilisation des outils Docker dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6d89d-238">Working with Visual Studio Docker Tools</span></span>](https://docs.microsoft.com/aspnet/core/publishing/visual-studio-tools-for-docker)
* [<span data-ttu-id="6d89d-239">Déploiement d’images Docker à partir du Registre de conteneurs Azure dans Azure Container Instances</span><span class="sxs-lookup"><span data-stu-id="6d89d-239">Deploying Docker Images from the Azure Container Registry to Azure Container Instances</span></span>](https://blogs.msdn.microsoft.com/stevelasker/2017/07/28/deploying-docker-images-from-the-azure-container-registry-to-azure-container-instances/)
* [<span data-ttu-id="6d89d-240">Débogage avec Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="6d89d-240">Debugging with Visual Studio Code</span></span>](https://code.visualstudio.com/docs/nodejs/debugging-recipes#_nodejs-typescript-docker-container) 
* [<span data-ttu-id="6d89d-241">Prise en main de Visual Studio pour Mac, les conteneurs et le code serverless dans le cloud</span><span class="sxs-lookup"><span data-stu-id="6d89d-241">Getting hands on with Visual Studio for Mac, containers, and serverless code in the cloud</span></span>](https://blogs.msdn.microsoft.com/visualstudio/2017/08/31/hands-on-with-visual-studio-for-mac-containers-serverless-code-in-the-cloud/#comments)
* [<span data-ttu-id="6d89d-242">Bien démarrer avec Docker et Visual Studio pour Mac Lab</span><span class="sxs-lookup"><span data-stu-id="6d89d-242">Getting Started with Docker and Visual Studio for Mac Lab</span></span>](https://github.com/Microsoft/vs4mac-labs/tree/master/Docker/Getting-Started)

> [!NOTE]
> <span data-ttu-id="6d89d-243">Si vous ne disposez pas d’abonnement Azure, [inscrivez-vous dès aujourd'hui](https://azure.microsoft.com/free/?b=16.48) pour obtenir un compte gratuit pendant 30 jours et 200 dollars US en crédits Azure pour essayer une combinaison quelconque de services Azure.</span><span class="sxs-lookup"><span data-stu-id="6d89d-243">If you do not have an Azure subscription, [sign up today](https://azure.microsoft.com/free/?b=16.48) for a free 30-day account and get $200 in Azure Credits to try out any combination of Azure services.</span></span>
