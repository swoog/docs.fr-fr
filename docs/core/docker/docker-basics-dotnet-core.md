---
title: Conteneuriser une application avec Docker - .NET Core
description: Ce tutoriel vous apprend à créer une application .NET Core de base et à la conteneuriser avec Docker.
ms.date: 10/11/2018
ms.topic: tutorial
ms.custom: mvc, seodec18
ms.openlocfilehash: 8f08936142b0cc44baf268f100e228f68920b69d
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53126366"
---
# <a name="how-to-containerize-a-net-core-application"></a><span data-ttu-id="b6578-103">Conteneuriser une application .NET Core</span><span class="sxs-lookup"><span data-stu-id="b6578-103">How to containerize a .NET Core application</span></span>

<span data-ttu-id="b6578-104">Ce didacticiel vous apprend la création de conteneur Docker et les tâches de déploiement pour une application .NET Core.</span><span class="sxs-lookup"><span data-stu-id="b6578-104">This tutorial teaches the Docker container build and deploy tasks for a .NET Core application.</span></span> <span data-ttu-id="b6578-105">La [plateforme Docker](https://docs.docker.com/engine/docker-overview/#the-docker-platform) utilise le [moteur Docker](https://docs.docker.com/engine/docker-overview/#docker-engine) pour générer et empaqueter rapidement des applications comme [images Docker](https://docs.docker.com/glossary/?term=image).</span><span class="sxs-lookup"><span data-stu-id="b6578-105">The [Docker platform](https://docs.docker.com/engine/docker-overview/#the-docker-platform) uses the [Docker Engine](https://docs.docker.com/engine/docker-overview/#docker-engine) to quickly build and package apps as [Docker images](https://docs.docker.com/glossary/?term=image).</span></span> <span data-ttu-id="b6578-106">Ces images sont écrites au format [Dockerfile](https://docs.docker.com/glossary/?term=Dockerfile) pour être déployées et exécutées dans un [conteneur en couches](https://docs.docker.com/engine/userguide/storagedriver/imagesandcontainers/#container-and-layers).</span><span class="sxs-lookup"><span data-stu-id="b6578-106">These images are written in the [Dockerfile](https://docs.docker.com/glossary/?term=Dockerfile) format to be deployed and run in a [layered container](https://docs.docker.com/engine/userguide/storagedriver/imagesandcontainers/#container-and-layers).</span></span>

<span data-ttu-id="b6578-107">Au cours de ce didacticiel, vous apprenez à :</span><span class="sxs-lookup"><span data-stu-id="b6578-107">During the course of this tutorial, you learn:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="b6578-108">Créer un fichier Dockerfile</span><span class="sxs-lookup"><span data-stu-id="b6578-108">How to create a Dockerfile</span></span>
> * <span data-ttu-id="b6578-109">Créer une application .NET Core</span><span class="sxs-lookup"><span data-stu-id="b6578-109">How to create a .NET Core app.</span></span>
> * <span data-ttu-id="b6578-110">Déployer votre application dans un conteneur Docker</span><span class="sxs-lookup"><span data-stu-id="b6578-110">How to deploy your app into a Docker container.</span></span>

## <a name="net-core-easiest-way-to-get-started"></a><span data-ttu-id="b6578-111">.NET Core : la façon la plus simple de bien démarrer</span><span class="sxs-lookup"><span data-stu-id="b6578-111">.NET Core: Easiest way to get started</span></span>

<span data-ttu-id="b6578-112">Avant de créer l’image Docker, vous avez besoin d’une application à mettre en conteneur.</span><span class="sxs-lookup"><span data-stu-id="b6578-112">Before creating the Docker image, you need an application to containerize.</span></span> <span data-ttu-id="b6578-113">Vous pouvez la créer sous Linux, MacOS ou Windows.</span><span class="sxs-lookup"><span data-stu-id="b6578-113">You can create it on Linux, MacOS, or Windows.</span></span> <span data-ttu-id="b6578-114">La façon la plus rapide et la plus simple de procéder consiste à utiliser .NET Core.</span><span class="sxs-lookup"><span data-stu-id="b6578-114">The quickest and easiest way to do that is to use .NET Core.</span></span>

<span data-ttu-id="b6578-115">Si vous n’êtes pas familiarisé avec l’ensemble d’outils CLI .NET Core, consultez [Vue d’ensemble du SDK .NET Core](../tools/index.md).</span><span class="sxs-lookup"><span data-stu-id="b6578-115">If you're unfamiliar with the .NET Core CLI toolset, read the [.NET Core SDK overview](../tools/index.md).</span></span>

<span data-ttu-id="b6578-116">Vous pouvez créer des conteneurs Windows et Linux avec des [balises multi-arch](https://github.com/dotnet/announcements/issues/14).</span><span class="sxs-lookup"><span data-stu-id="b6578-116">You can build both Windows and Linux containers with [multi-arch based tags](https://github.com/dotnet/announcements/issues/14).</span></span>

## <a name="your-first-net-core-docker-app"></a><span data-ttu-id="b6578-117">Votre première application Docker .NET Core</span><span class="sxs-lookup"><span data-stu-id="b6578-117">Your first .NET Core Docker app</span></span>

### <a name="prerequisites"></a><span data-ttu-id="b6578-118">Prérequis</span><span class="sxs-lookup"><span data-stu-id="b6578-118">Prerequisites</span></span>

<span data-ttu-id="b6578-119">Pour suivre ce didacticiel :</span><span class="sxs-lookup"><span data-stu-id="b6578-119">To complete this tutorial:</span></span>

#### <a name="net-core-sdk"></a><span data-ttu-id="b6578-120">SDK .NET Core</span><span class="sxs-lookup"><span data-stu-id="b6578-120">.NET Core SDK</span></span>

* <span data-ttu-id="b6578-121">Installez [SDK .NET Core 2.1](https://www.microsoft.com/net/download) ou versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b6578-121">Install [.NET Core 2.1 SDK](https://www.microsoft.com/net/download) or later.</span></span>

<span data-ttu-id="b6578-122">Consultez [.NET Core 2.1 - Versions des systèmes d’exploitation prises en charge](https://github.com/dotnet/core/blob/master/release-notes/2.1/2.1-supported-os.md) pour obtenir la liste complète des systèmes d’exploitation pris en charge par .NET Core 2.1, les systèmes d’exploitation non pris en charge et des liens sur la politique concernant le cycle de vie.</span><span class="sxs-lookup"><span data-stu-id="b6578-122">See [.NET Core 2.1 Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/2.1/2.1-supported-os.md) for the complete list of .NET Core 2.1 supported operating systems, out of support OS versions, and lifecycle policy links.</span></span>

* <span data-ttu-id="b6578-123">Installez votre éditeur de code favori, si ce n’est pas déjà fait.</span><span class="sxs-lookup"><span data-stu-id="b6578-123">Install your favorite code editor, if you haven't already.</span></span>

> [!TIP]
> <span data-ttu-id="b6578-124">Vous avez besoin d’installer un éditeur de code ?</span><span class="sxs-lookup"><span data-stu-id="b6578-124">Need to install a code editor?</span></span> <span data-ttu-id="b6578-125">Testez [Visual Studio Code](https://code.visualstudio.com/download) !</span><span class="sxs-lookup"><span data-stu-id="b6578-125">Try [Visual Studio Code](https://code.visualstudio.com/download)!</span></span>

#### <a name="installing-docker-client"></a><span data-ttu-id="b6578-126">Installation du client Docker</span><span class="sxs-lookup"><span data-stu-id="b6578-126">Installing Docker Client</span></span>

<span data-ttu-id="b6578-127">Installez la version [Docker 18.06](https://docs.docker.com/release-notes/docker-ce/) ou ultérieure du client Docker.</span><span class="sxs-lookup"><span data-stu-id="b6578-127">Install [Docker 18.06](https://docs.docker.com/release-notes/docker-ce/) or later of the Docker client.</span></span>

<span data-ttu-id="b6578-128">Le client Docker peut être installé dans :</span><span class="sxs-lookup"><span data-stu-id="b6578-128">The Docker client can be installed in:</span></span>

* <span data-ttu-id="b6578-129">Distributions Linux</span><span class="sxs-lookup"><span data-stu-id="b6578-129">Linux distributions</span></span>

   * [<span data-ttu-id="b6578-130">CentOS</span><span class="sxs-lookup"><span data-stu-id="b6578-130">CentOS</span></span>](https://docs.docker.com/install/linux/docker-ce/centos/)

   * [<span data-ttu-id="b6578-131">Debian</span><span class="sxs-lookup"><span data-stu-id="b6578-131">Debian</span></span>](https://docs.docker.com/install/linux/docker-ce/debian/)

   * [<span data-ttu-id="b6578-132">Fedora</span><span class="sxs-lookup"><span data-stu-id="b6578-132">Fedora</span></span>](https://docs.docker.com/install/linux/docker-ce/fedora/)

   * [<span data-ttu-id="b6578-133">Ubuntu</span><span class="sxs-lookup"><span data-stu-id="b6578-133">Ubuntu</span></span>](https://docs.docker.com/install/linux/docker-ce/ubuntu/)

* [<span data-ttu-id="b6578-134">macOS</span><span class="sxs-lookup"><span data-stu-id="b6578-134">macOS</span></span>](https://docs.docker.com/docker-for-mac/install/)

* <span data-ttu-id="b6578-135">[Windows](https://docs.docker.com/docker-for-windows/install/).</span><span class="sxs-lookup"><span data-stu-id="b6578-135">[Windows](https://docs.docker.com/docker-for-windows/install/).</span></span>

### <a name="create-a-net-core-21-console-app-for-dockerization"></a><span data-ttu-id="b6578-136">Créer une application console .NET Core 2.1 pour la dockerisation</span><span class="sxs-lookup"><span data-stu-id="b6578-136">Create a .NET Core 2.1 console app for Dockerization</span></span>

<span data-ttu-id="b6578-137">Ouvrez une invite de commandes et créez un dossier nommé *Hello*.</span><span class="sxs-lookup"><span data-stu-id="b6578-137">Open a command prompt and create a folder named *Hello*.</span></span> <span data-ttu-id="b6578-138">Accédez au dossier créé et tapez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b6578-138">Navigate to the folder you created and type the following commands:</span></span>

```console
dotnet new console
dotnet run
```

<span data-ttu-id="b6578-139">Suivons une procédure pas à pas rapide :</span><span class="sxs-lookup"><span data-stu-id="b6578-139">Let's do a quick walkthrough:</span></span>

1. `$ dotnet new console`

   <span data-ttu-id="b6578-140">[`dotnet new`](../tools/dotnet-new.md) crée un fichier projet `Hello.csproj` à jour avec les dépendances nécessaires pour générer une application console.</span><span class="sxs-lookup"><span data-stu-id="b6578-140">[`dotnet new`](../tools/dotnet-new.md) creates an up-to-date `Hello.csproj` project file with the dependencies necessary to build a console app.</span></span>  <span data-ttu-id="b6578-141">Il crée également `Program.cs`, un fichier de base contenant le point d’entrée pour l’application.</span><span class="sxs-lookup"><span data-stu-id="b6578-141">It also creates a `Program.cs`, a basic file containing the entry point for the application.</span></span>

   <span data-ttu-id="b6578-142">`Hello.csproj`:</span><span class="sxs-lookup"><span data-stu-id="b6578-142">`Hello.csproj`:</span></span>

   <span data-ttu-id="b6578-143">Le fichier projet spécifie tout ce qui est nécessaire pour restaurer les dépendances et générer le programme.</span><span class="sxs-lookup"><span data-stu-id="b6578-143">The project file specifies everything that's needed to restore dependencies and build the program.</span></span>

   * <span data-ttu-id="b6578-144">La balise `OutputType` spécifie que nous générons un fichier exécutable, autrement dit une application console.</span><span class="sxs-lookup"><span data-stu-id="b6578-144">The `OutputType` tag specifies that we're building an executable, in other words a console application.</span></span>
   * <span data-ttu-id="b6578-145">La balise `TargetFramework` spécifie l’implémentation .NET que nous ciblons.</span><span class="sxs-lookup"><span data-stu-id="b6578-145">The `TargetFramework` tag specifies what .NET implementation we're targeting.</span></span> <span data-ttu-id="b6578-146">Dans un scénario avancé, vous pouvez spécifier plusieurs frameworks cibles et y effectuer une génération globale en une seule opération.</span><span class="sxs-lookup"><span data-stu-id="b6578-146">In an advanced scenario, you can specify multiple target frameworks and build to the specified frameworks in a single operation.</span></span> <span data-ttu-id="b6578-147">Dans ce didacticiel, nous effectuons une génération pour .NET Core 2.1.</span><span class="sxs-lookup"><span data-stu-id="b6578-147">In this tutorial, we build for .NET Core 2.1.</span></span>

   <span data-ttu-id="b6578-148">`Program.cs`:</span><span class="sxs-lookup"><span data-stu-id="b6578-148">`Program.cs`:</span></span>

   <span data-ttu-id="b6578-149">Le programme commence par `using System`.</span><span class="sxs-lookup"><span data-stu-id="b6578-149">The program starts by `using System`.</span></span> <span data-ttu-id="b6578-150">Cette instruction signifie « Placer tout ce qui se trouve dans l’espace de noms `System` dans la portée de ce fichier ».</span><span class="sxs-lookup"><span data-stu-id="b6578-150">This statement means, "Bring everything in the `System` namespace into scope for this file."</span></span> <span data-ttu-id="b6578-151">L’espace de noms `System` inclut des constructions de base, telles que `string`, ou des types numériques.</span><span class="sxs-lookup"><span data-stu-id="b6578-151">The `System` namespace includes basic constructs such as `string`, or numeric types.</span></span>

   <span data-ttu-id="b6578-152">Ensuite, nous définissons un espace de noms appelé `Hello`.</span><span class="sxs-lookup"><span data-stu-id="b6578-152">We then define a namespace called `Hello`.</span></span> <span data-ttu-id="b6578-153">Vous pouvez le modifier à votre gré.</span><span class="sxs-lookup"><span data-stu-id="b6578-153">You can change namespace to anything you want.</span></span> <span data-ttu-id="b6578-154">Une classe nommée `Program` est définie dans cet espace de noms avec une méthode `Main` qui accepte un tableau de chaînes comme argument.</span><span class="sxs-lookup"><span data-stu-id="b6578-154">A class named `Program` is defined within that namespace, with a `Main` method that takes an array of strings as its argument.</span></span> <span data-ttu-id="b6578-155">Ce tableau contient la liste des arguments passés quand le programme compilé est appelé.</span><span class="sxs-lookup"><span data-stu-id="b6578-155">This array contains the list of arguments passed in when the compiled program is called.</span></span> <span data-ttu-id="b6578-156">Dans notre exemple, le programme écrit uniquement « Hello World! »</span><span class="sxs-lookup"><span data-stu-id="b6578-156">In our example, the program only writes "Hello World!"</span></span> <span data-ttu-id="b6578-157">dans la console.</span><span class="sxs-lookup"><span data-stu-id="b6578-157">to the console.</span></span>

   <span data-ttu-id="b6578-158">**dotnet new** exécute la commande [`dotnet restore`](../tools/dotnet-restore.md).</span><span class="sxs-lookup"><span data-stu-id="b6578-158">**dotnet new** runs the [`dotnet restore`](../tools/dotnet-restore.md) command.</span></span> <span data-ttu-id="b6578-159">**Dotnet restore** restaure l’arborescence des dépendances avec un appel [NuGet](https://www.nuget.org/) (gestionnaire de package .NET).</span><span class="sxs-lookup"><span data-stu-id="b6578-159">**Dotnet restore** restores the tree of dependencies with a [NuGet](https://www.nuget.org/)(.NET package manager) call.</span></span>
   <span data-ttu-id="b6578-160">NuGet exécute les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="b6578-160">NuGet performs the following tasks:</span></span>
   * <span data-ttu-id="b6578-161">il analyse le fichier *Hello.csproj* ;</span><span class="sxs-lookup"><span data-stu-id="b6578-161">analyzes the *Hello.csproj* file.</span></span>
   * <span data-ttu-id="b6578-162">il télécharge les dépendances de fichiers (ou les extrait du cache de votre ordinateur) ;</span><span class="sxs-lookup"><span data-stu-id="b6578-162">downloads the file dependencies (or grabs from your machine cache).</span></span>
   * <span data-ttu-id="b6578-163">il écrit le fichier *obj/project.assets.json*.</span><span class="sxs-lookup"><span data-stu-id="b6578-163">writes the *obj/project.assets.json* file.</span></span>

   <span data-ttu-id="b6578-164">Le fichier *project.assets.json* réunit le graphique des dépendances NuGet, les résolutions de liaisons et d’autres métadonnées d’application.</span><span class="sxs-lookup"><span data-stu-id="b6578-164">The *project.assets.json* file is a complete set of the NuGet dependencies graph, binding resolutions, and other app metadata.</span></span> <span data-ttu-id="b6578-165">Ce fichier requis est utilisé par d’autres outils, tels que [`dotnet build`](../tools/dotnet-build.md) et [`dotnet run`](../tools/dotnet-run.md), pour traiter correctement le code source.</span><span class="sxs-lookup"><span data-stu-id="b6578-165">This required file is used by other tools, such as [`dotnet build`](../tools/dotnet-build.md) and [`dotnet run`](../tools/dotnet-run.md), to correctly process the source code.</span></span>

2. `$ dotnet run`

   <span data-ttu-id="b6578-166">[`dotnet run`](../tools/dotnet-run.md) appelle [`dotnet build`](../tools/dotnet-build.md) pour confirmer une génération réussie, puis appelle `dotnet <assembly.dll>` pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="b6578-166">[`dotnet run`](../tools/dotnet-run.md) calls [`dotnet build`](../tools/dotnet-build.md) to confirm a successful build, and then calls `dotnet <assembly.dll>` to run the application.</span></span>

    ```console
    $ dotnet run

    Hello World!
    ```

    <span data-ttu-id="b6578-167">Pour les scénarios avancés, consultez [Déploiement d’applications .NET Core](../deploying/index.md) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="b6578-167">For advanced scenarios,  see [.NET Core Application Deployment](../deploying/index.md) for details.</span></span>

## <a name="dockerize-the-net-core-application"></a><span data-ttu-id="b6578-168">Dockeriser l’application .NET Core</span><span class="sxs-lookup"><span data-stu-id="b6578-168">Dockerize the .NET Core application</span></span>

<span data-ttu-id="b6578-169">L’application console .NET Core Hello est exécutée correctement en local.</span><span class="sxs-lookup"><span data-stu-id="b6578-169">The Hello .NET Core console app successfully runs locally.</span></span> <span data-ttu-id="b6578-170">Franchissons maintenant une étape supplémentaire pour générer et exécuter l’application dans Docker.</span><span class="sxs-lookup"><span data-stu-id="b6578-170">Now let's take it a step further and build and run the app in Docker.</span></span>

### <a name="your-first-dockerfile"></a><span data-ttu-id="b6578-171">Votre premier fichier Dockerfile</span><span class="sxs-lookup"><span data-stu-id="b6578-171">Your first Dockerfile</span></span>

<span data-ttu-id="b6578-172">Ouvrez votre éditeur de texte et c’est parti !</span><span class="sxs-lookup"><span data-stu-id="b6578-172">Open your text editor and let's get started!</span></span> <span data-ttu-id="b6578-173">Nous travaillons encore à partir du répertoire Hello dans lequel nous avons créé l’application.</span><span class="sxs-lookup"><span data-stu-id="b6578-173">We're still working from the Hello directory we built the app in.</span></span>

<span data-ttu-id="b6578-174">Ajoutez les instructions Docker suivantes pour les [conteneurs Windows](https://docs.microsoft.com/virtualization/windowscontainers/about/) ou Linux à un nouveau fichier.</span><span class="sxs-lookup"><span data-stu-id="b6578-174">Add the following Docker instructions for either Linux or [Windows Containers](https://docs.microsoft.com/virtualization/windowscontainers/about/) to a new file.</span></span> <span data-ttu-id="b6578-175">Quand vous avez terminé, enregistrez-le à la racine de votre répertoire Hello comme **Dockerfile**, sans extension (vous devrez peut-être définir le type de fichier `All types (*.*)` ou un type similaire).</span><span class="sxs-lookup"><span data-stu-id="b6578-175">When finished, save it in the root of your Hello directory as **Dockerfile**, with no extension (You may need to set your file type to `All types (*.*)` or something similar).</span></span>

```Dockerfile
FROM microsoft/dotnet:2.1-sdk
WORKDIR /app

# copy csproj and restore as distinct layers
COPY *.csproj ./
RUN dotnet restore

# copy and build everything else
COPY . ./
RUN dotnet publish -c Release -o out
ENTRYPOINT ["dotnet", "out/Hello.dll"]
```

<span data-ttu-id="b6578-176">Le fichier Dockerfile contient des instructions de génération Docker qui s’exécutent de manière séquentielle.</span><span class="sxs-lookup"><span data-stu-id="b6578-176">The Dockerfile contains Docker build instructions that run sequentially.</span></span>

<span data-ttu-id="b6578-177">La première instruction doit être [**FROM**](https://docs.docker.com/engine/reference/builder/#from).</span><span class="sxs-lookup"><span data-stu-id="b6578-177">The first instruction must be [**FROM**](https://docs.docker.com/engine/reference/builder/#from).</span></span> <span data-ttu-id="b6578-178">Cette instruction initialise une nouvelle étape de génération et définit l’image de base pour les instructions restantes.</span><span class="sxs-lookup"><span data-stu-id="b6578-178">This instruction initializes a new build stage and sets the Base Image for the remaining instructions.</span></span> <span data-ttu-id="b6578-179">Les balises multi-arch extraient les conteneurs Windows ou Linux selon le [mode conteneur](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers) Docker pour Windows.</span><span class="sxs-lookup"><span data-stu-id="b6578-179">The multi-arch tags pull either Windows or Linux containers depending on the Docker for Windows [container mode](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span> <span data-ttu-id="b6578-180">L’image de base pour notre exemple est l’image 2.1-sdk du dépôt microsoft/dotnet,</span><span class="sxs-lookup"><span data-stu-id="b6578-180">The Base Image for our sample is the 2.1-sdk image from the microsoft/dotnet repository,</span></span>

```Dockerfile
FROM microsoft/dotnet:2.1-sdk
```

<span data-ttu-id="b6578-181">L’instruction [**WORKDIR**](https://docs.docker.com/engine/reference/builder/#workdir) définit le répertoire de travail pour toute instruction Dockerfile RUN, CMD, ENTRYPOINT, COPY et ADD restante.</span><span class="sxs-lookup"><span data-stu-id="b6578-181">The [**WORKDIR**](https://docs.docker.com/engine/reference/builder/#workdir) instruction sets the working directory for any remaining RUN, CMD, ENTRYPOINT, COPY, and ADD Dockerfile instructions.</span></span> <span data-ttu-id="b6578-182">Si le répertoire n’existe pas, il est créé.</span><span class="sxs-lookup"><span data-stu-id="b6578-182">If the directory doesn't exist, it's created.</span></span> <span data-ttu-id="b6578-183">Dans ce cas, WORKDIR est définie sur le répertoire de l’application.</span><span class="sxs-lookup"><span data-stu-id="b6578-183">In this case, WORKDIR is set to the app directory.</span></span>

```Dockerfile
WORKDIR /app
```

<span data-ttu-id="b6578-184">L’instruction [**COPY**](https://docs.docker.com/engine/reference/builder/#copy) copie les nouveaux fichiers ou répertoires du chemin source et les ajoute au système de fichiers du conteneur de destination.</span><span class="sxs-lookup"><span data-stu-id="b6578-184">The [**COPY**](https://docs.docker.com/engine/reference/builder/#copy) instruction copies new files or directories from the source path and adds them to the destination container filesystem.</span></span> <span data-ttu-id="b6578-185">Avec cette instruction, nous copions le fichier projet C# dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="b6578-185">With this instruction, we are copying the C# project file to the container.</span></span>

```Dockerfile
COPY *.csproj ./
```

<span data-ttu-id="b6578-186">L’instruction [**RUN**](https://docs.docker.com/engine/reference/builder/#run) exécute toutes les commandes dans une nouvelle couche sur l’image actuelle et valide les résultats.</span><span class="sxs-lookup"><span data-stu-id="b6578-186">The [**RUN**](https://docs.docker.com/engine/reference/builder/#run) instruction executes any commands in a new layer on top of the current image and commit the results.</span></span> <span data-ttu-id="b6578-187">L’image validée obtenue est utilisée pour l’étape suivante dans le fichier Dockerfile.</span><span class="sxs-lookup"><span data-stu-id="b6578-187">The resulting committed image is used for the next step in the Dockerfile.</span></span> <span data-ttu-id="b6578-188">Nous exécutons **dotnet restore** pour obtenir les dépendances nécessaires du fichier projet C#.</span><span class="sxs-lookup"><span data-stu-id="b6578-188">We are running **dotnet restore** to get the needed dependencies of the C# project file.</span></span> 

```Dockerfile
RUN dotnet restore
```

<span data-ttu-id="b6578-189">Cette instruction **COPY** copie le reste des fichiers dans notre conteneur dans de nouvelles [couches](https://docs.docker.com/engine/userguide/storagedriver/imagesandcontainers/#images-and-layers).</span><span class="sxs-lookup"><span data-stu-id="b6578-189">This **COPY** instruction copies the rest of the files into our container into new [layers](https://docs.docker.com/engine/userguide/storagedriver/imagesandcontainers/#images-and-layers).</span></span>

```Dockerfile
COPY . ./
```

<span data-ttu-id="b6578-190">Nous publions l’application avec cette instruction **RUN**.</span><span class="sxs-lookup"><span data-stu-id="b6578-190">We are publishing the app with this **RUN** instruction.</span></span> <span data-ttu-id="b6578-191">La commande [**dotnet publish**](../tools/dotnet-publish.md) compile l’application, parcourt ses dépendances spécifiées dans le fichier projet et publie l’ensemble de fichiers obtenus dans un répertoire.</span><span class="sxs-lookup"><span data-stu-id="b6578-191">The [**dotnet publish**](../tools/dotnet-publish.md) command compiles the application, reads through its dependencies specified in the project file, and publishes the resulting set of files to a directory.</span></span> <span data-ttu-id="b6578-192">Notre application est publiée avec une configuration **Release** et une sortie vers le répertoire par défaut.</span><span class="sxs-lookup"><span data-stu-id="b6578-192">Our app is published with a **Release** configuration and output to the default directory.</span></span>

```Dockerfile
RUN dotnet publish -c Release -o out
```

<span data-ttu-id="b6578-193">L’instruction [**ENTRYPOINT**](https://docs.docker.com/engine/reference/builder/#entrypoint) permet d’exécuter le conteneur comme un fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="b6578-193">The [**ENTRYPOINT**](https://docs.docker.com/engine/reference/builder/#entrypoint) instruction allows the container to run as an executable.</span></span>

```Dockerfile
ENTRYPOINT ["dotnet", "out/Hello.dll"]
```

<span data-ttu-id="b6578-194">Vous disposez maintenant d’un fichier Dockerfile qui :</span><span class="sxs-lookup"><span data-stu-id="b6578-194">Now you have a Dockerfile that:</span></span>

* <span data-ttu-id="b6578-195">Copie votre application sur l’image</span><span class="sxs-lookup"><span data-stu-id="b6578-195">copies your app to the image</span></span>
* <span data-ttu-id="b6578-196">Ajoute les dépendances de votre application à l’image</span><span class="sxs-lookup"><span data-stu-id="b6578-196">your app's dependencies to the image</span></span>
* <span data-ttu-id="b6578-197">Génère l’application pour l’exécuter comme un fichier exécutable</span><span class="sxs-lookup"><span data-stu-id="b6578-197">builds the app to run as an executable</span></span>

### <a name="build-and-run-the-hello-net-core-app"></a><span data-ttu-id="b6578-198">Générer et exécuter l’application .NET Core Hello</span><span class="sxs-lookup"><span data-stu-id="b6578-198">Build and run the Hello .NET Core app</span></span>

#### <a name="essential-docker-commands"></a><span data-ttu-id="b6578-199">Commandes Docker essentielles</span><span class="sxs-lookup"><span data-stu-id="b6578-199">Essential Docker commands</span></span>

<span data-ttu-id="b6578-200">Ces commandes Docker sont essentielles :</span><span class="sxs-lookup"><span data-stu-id="b6578-200">These Docker commands are essential:</span></span>

* [<span data-ttu-id="b6578-201">docker build</span><span class="sxs-lookup"><span data-stu-id="b6578-201">docker build</span></span>](https://docs.docker.com/engine/reference/commandline/build/)
* [<span data-ttu-id="b6578-202">docker run</span><span class="sxs-lookup"><span data-stu-id="b6578-202">docker run</span></span>](https://docs.docker.com/engine/reference/commandline/run/)
* [<span data-ttu-id="b6578-203">docker ps</span><span class="sxs-lookup"><span data-stu-id="b6578-203">docker ps</span></span>](https://docs.docker.com/engine/reference/commandline/ps/)
* [<span data-ttu-id="b6578-204">docker stop</span><span class="sxs-lookup"><span data-stu-id="b6578-204">docker stop</span></span>](https://docs.docker.com/engine/reference/commandline/stop/)
* [<span data-ttu-id="b6578-205">docker rm</span><span class="sxs-lookup"><span data-stu-id="b6578-205">docker rm</span></span>](https://docs.docker.com/engine/reference/commandline/rm/)
* [<span data-ttu-id="b6578-206">docker rmi</span><span class="sxs-lookup"><span data-stu-id="b6578-206">docker rmi</span></span>](https://docs.docker.com/engine/reference/commandline/rmi/)
* [<span data-ttu-id="b6578-207">docker image</span><span class="sxs-lookup"><span data-stu-id="b6578-207">docker image</span></span>](https://docs.docker.com/engine/reference/commandline/image/)

#### <a name="build-and-run"></a><span data-ttu-id="b6578-208">Générer et exécuter</span><span class="sxs-lookup"><span data-stu-id="b6578-208">Build and run</span></span>

<span data-ttu-id="b6578-209">Vous avez écrit le fichier Dockerfile ; maintenant, Docker génère votre application, puis exécute le conteneur.</span><span class="sxs-lookup"><span data-stu-id="b6578-209">You wrote the dockerfile; now Docker builds your app and then runs the container.</span></span>

```console
docker build -t dotnetapp-dev .
docker run --rm dotnetapp-dev Hello from Docker
```

<span data-ttu-id="b6578-210">La sortie de la commande `docker build` doit être similaire à la sortie de console suivante :</span><span class="sxs-lookup"><span data-stu-id="b6578-210">The output from the `docker build` command should be similar to the following console output:</span></span>

```console
Sending build context to Docker daemon   173.1kB
Step 1/7 : FROM microsoft/dotnet:2.1-sdk
 ---> 288f8c45f7c2
Step 2/7 : WORKDIR /app
 ---> Using cache
 ---> 9af1fbdc7972
Step 3/7 : COPY *.csproj ./
 ---> Using cache
 ---> 86c8c332d4b3
Step 4/7 : RUN dotnet restore
 ---> Using cache
 ---> 86fcd7dd0ea4
Step 5/7 : COPY . ./
 ---> Using cache
 ---> 6faf0a53607f
Step 6/7 : RUN dotnet publish -c Release -o out
 ---> Using cache
 ---> f972328318c8
Step 7/7 : ENTRYPOINT dotnet out/Hello.dll
 ---> Using cache
 ---> 53c337887e18
Successfully built 46db075bd98d
Successfully tagged dotnetapp-dev:latest
```

<span data-ttu-id="b6578-211">Comme vous pouvez le voir dans la sortie, le moteur Docker a utilisé le fichier Dockerfile pour créer notre conteneur.</span><span class="sxs-lookup"><span data-stu-id="b6578-211">As you can see from the output, the Docker Engine used the Dockerfile to build our container.</span></span>

<span data-ttu-id="b6578-212">La sortie de la commande `docker run` doit être similaire à la sortie de console suivante :</span><span class="sxs-lookup"><span data-stu-id="b6578-212">The output from the `docker run` command should be similar to the following console output:</span></span>

```console
Hello World!
```

<span data-ttu-id="b6578-213">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="b6578-213">Congratulations!</span></span> <span data-ttu-id="b6578-214">Vous venez de :</span><span class="sxs-lookup"><span data-stu-id="b6578-214">You have just:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="b6578-215">Créer une application .NET Core locale</span><span class="sxs-lookup"><span data-stu-id="b6578-215">Created a local .NET Core app</span></span>
> * <span data-ttu-id="b6578-216">Créer un fichier Dockerfile pour générer votre premier conteneur</span><span class="sxs-lookup"><span data-stu-id="b6578-216">Created a Dockerfile to build your first container</span></span>
> * <span data-ttu-id="b6578-217">Générer et exécuter votre application dockerisée</span><span class="sxs-lookup"><span data-stu-id="b6578-217">Built and ran your Dockerized app</span></span>

## <a name="next-steps"></a><span data-ttu-id="b6578-218">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="b6578-218">Next steps</span></span>

<span data-ttu-id="b6578-219">Voici quelques étapes suivantes que vous pouvez effectuer :</span><span class="sxs-lookup"><span data-stu-id="b6578-219">Here are some next steps you can take:</span></span>

* [<span data-ttu-id="b6578-220">Introduction to .NET Docker Images Video</span><span class="sxs-lookup"><span data-stu-id="b6578-220">Introduction to .NET Docker Images Video</span></span>](https://channel9.msdn.com/Shows/Code-Conversations/Introduction-to-NET-Docker-Images-with-Kendra-Havens?term=docker)
* [<span data-ttu-id="b6578-221">Visual Studio, Docker & Azure Container Instances better together!</span><span class="sxs-lookup"><span data-stu-id="b6578-221">Visual Studio, Docker & Azure Container Instances better together!</span></span>](https://medium.com/@AliMazaheri/visual-studio-docker-azure-container-instances-better-together-bf8c2f0419ae)
* [<span data-ttu-id="b6578-222">Guides de démarrage rapide Docker pour Azure</span><span class="sxs-lookup"><span data-stu-id="b6578-222">Docker for Azure Quickstarts</span></span>](https://docs.docker.com/docker-for-azure/#docker-community-edition-ce-for-azure)
* [<span data-ttu-id="b6578-223">Déployer votre application sur Docker pour Azure</span><span class="sxs-lookup"><span data-stu-id="b6578-223">Deploy your app on Docker for Azure</span></span>](https://docs.docker.com/docker-for-azure/deploy/)

> [!Note]
> <span data-ttu-id="b6578-224">Si vous ne disposez pas d’abonnement Azure, [inscrivez-vous dès aujourd'hui](https://azure.microsoft.com/free/?b=16.48) pour obtenir un compte gratuit pendant 30 jours et 200 dollars US en crédits Azure pour essayer une combinaison quelconque de services Azure.</span><span class="sxs-lookup"><span data-stu-id="b6578-224">If you do not have an Azure subscription, [sign up today](https://azure.microsoft.com/free/?b=16.48) for a free 30-day account and get $200 in Azure Credits to try out any combination of Azure services.</span></span>

## <a name="docker-images-used-in-this-sample"></a><span data-ttu-id="b6578-225">Images Docker utilisées dans cet exemple</span><span class="sxs-lookup"><span data-stu-id="b6578-225">Docker Images used in this sample</span></span>

<span data-ttu-id="b6578-226">Les images Docker suivantes sont utilisées dans cet exemple</span><span class="sxs-lookup"><span data-stu-id="b6578-226">The following Docker images are used in this sample</span></span>

* [`microsoft/dotnet:2.1-sdk`](https://hub.docker.com/r/microsoft/dotnet)

## <a name="related-resources"></a><span data-ttu-id="b6578-227">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="b6578-227">Related resources</span></span>

* [<span data-ttu-id="b6578-228">Exemples Docker .NET Core</span><span class="sxs-lookup"><span data-stu-id="b6578-228">.NET Core Docker samples</span></span>](https://github.com/dotnet/dotnet-docker/tree/master/samples)
* [<span data-ttu-id="b6578-229">Dockerfile sur les conteneurs Windows</span><span class="sxs-lookup"><span data-stu-id="b6578-229">Dockerfile on Windows Containers</span></span>](https://docs.microsoft.com/virtualization/windowscontainers/manage-docker/manage-windows-dockerfile)
* [<span data-ttu-id="b6578-230">Exemples Docker .NET Framework</span><span class="sxs-lookup"><span data-stu-id="b6578-230">.NET Framework Docker samples</span></span>](https://github.com/Microsoft/dotnet-framework-docker-samples)
* [<span data-ttu-id="b6578-231">ASP.NET Core sur DockerHub</span><span class="sxs-lookup"><span data-stu-id="b6578-231">ASP.NET Core on DockerHub</span></span>](https://hub.docker.com/r/microsoft/aspnetcore/)
* [<span data-ttu-id="b6578-232">Dockeriser une application .NET Core - Didacticiel Docker</span><span class="sxs-lookup"><span data-stu-id="b6578-232">Dockerize a .NET Core application - Docker Tutorial</span></span>](https://docs.docker.com/engine/examples/dotnetcore/)
* [<span data-ttu-id="b6578-233">Utilisation des outils Docker dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b6578-233">Working with Visual Studio Docker Tools</span></span>](https://docs.microsoft.com/aspnet/core/publishing/visual-studio-tools-for-docker)
* [<span data-ttu-id="b6578-234">Déploiement d’images Docker à partir du Registre de conteneurs Azure dans Azure Container Instances</span><span class="sxs-lookup"><span data-stu-id="b6578-234">Deploying Docker Images from the Azure Container Registry to Azure Container Instances</span></span>](https://blogs.msdn.microsoft.com/stevelasker/2017/07/28/deploying-docker-images-from-the-azure-container-registry-to-azure-container-instances/)