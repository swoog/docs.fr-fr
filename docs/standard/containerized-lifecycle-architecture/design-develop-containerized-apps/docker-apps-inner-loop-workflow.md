---
title: Workflow de développement de la boucle interne pour les applications Docker
description: Découvrez le flux de travail « boucle intérieure » pour le développement d’applications Docker.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 02/15/2019
ms.openlocfilehash: 36fcf5769376375854c2a2631e26e8b136df0de6
ms.sourcegitcommit: a3db1a9eafca89f95ccf361bc1833b47fbb2bb30
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/04/2019
ms.locfileid: "58920907"
---
# <a name="inner-loop-development-workflow-for-docker-apps"></a><span data-ttu-id="fa653-103">Workflow de développement de la boucle interne pour les applications Docker</span><span class="sxs-lookup"><span data-stu-id="fa653-103">Inner-loop development workflow for Docker apps</span></span>

<span data-ttu-id="fa653-104">Avant de déclencher le flux de travail de boucle externe couvrant l’ensemble DevOps cycle, tout cela commence sur chaque machine de développeur, codage de l’application elle-même, à l’aide de leurs plateformes ou langages préférés et de le tester localement (Figure 4-21).</span><span class="sxs-lookup"><span data-stu-id="fa653-104">Before triggering the outer-loop workflow spanning the entire DevOps cycle, it all begins on each developer's machine, coding the app itself, using their preferred languages or platforms, and testing it locally (Figure 4-21).</span></span> <span data-ttu-id="fa653-105">Mais dans tous les cas, vous aurez un point important en commun, peu importe quel langage, infrastructure ou plateformes que vous choisissez.</span><span class="sxs-lookup"><span data-stu-id="fa653-105">But in every case, you'll have an important point in common, no matter what language, framework, or platforms you choose.</span></span> <span data-ttu-id="fa653-106">Dans ce flux de travail spécifique, vous toujours développez et testez des conteneurs Docker, mais localement.</span><span class="sxs-lookup"><span data-stu-id="fa653-106">In this specific workflow, you're always developing and testing Docker containers, but locally.</span></span>

![Étape 1 : Code/Run/Debug](./media/image18.png)

<span data-ttu-id="fa653-108">**Figure 4-21**.</span><span class="sxs-lookup"><span data-stu-id="fa653-108">**Figure 4-21**.</span></span> <span data-ttu-id="fa653-109">Contexte de développement de la boucle interne</span><span class="sxs-lookup"><span data-stu-id="fa653-109">Inner-loop development context</span></span>

<span data-ttu-id="fa653-110">Le conteneur ou une instance d’une image Docker contiendra ces composants :</span><span class="sxs-lookup"><span data-stu-id="fa653-110">The container or instance of a Docker image will contain these components:</span></span>

-   <span data-ttu-id="fa653-111">Une sélection de système d’exploitation (par exemple, une distribution Linux ou Windows)</span><span class="sxs-lookup"><span data-stu-id="fa653-111">An operating system selection (for example, a Linux distribution or Windows)</span></span>

- <span data-ttu-id="fa653-112">Fichiers ajoutés par le développeur (par exemple, les binaires d’application)</span><span class="sxs-lookup"><span data-stu-id="fa653-112">Files added by the developer (for example, app binaries)</span></span>

-   <span data-ttu-id="fa653-113">Configuration (par exemple, les paramètres d’environnement et les dépendances)</span><span class="sxs-lookup"><span data-stu-id="fa653-113">Configuration (for example, environment settings and dependencies)</span></span>

- <span data-ttu-id="fa653-114">Instructions pour les processus pour exécuter par Docker</span><span class="sxs-lookup"><span data-stu-id="fa653-114">Instructions for what processes to run by Docker</span></span>

<span data-ttu-id="fa653-115">Vous pouvez configurer le flux de travail de développement de la boucle interne qui utilise Docker en tant que le processus (décrit dans la section suivante).</span><span class="sxs-lookup"><span data-stu-id="fa653-115">You can set up the inner-loop development workflow that utilizes Docker as the process (described in the next section).</span></span> <span data-ttu-id="fa653-116">Prendre en compte que les premières étapes pour configurer l’environnement ne sont pas inclus, car vous devez uniquement une seule fois.</span><span class="sxs-lookup"><span data-stu-id="fa653-116">Consider that the initial steps to set up the environment are not included, because you only need to do it once.</span></span>

## <a name="building-a-single-app-within-a-docker-container-using-visual-studio-code-and-docker-cli"></a><span data-ttu-id="fa653-117">Création d’une application unique dans un conteneur Docker à l’aide de Visual Studio Code et interface CLI Docker</span><span class="sxs-lookup"><span data-stu-id="fa653-117">Building a single app within a Docker container using Visual Studio Code and Docker CLI</span></span>

<span data-ttu-id="fa653-118">Les applications sont constituées à partir de vos propres services ainsi que des bibliothèques supplémentaires (dépendances).</span><span class="sxs-lookup"><span data-stu-id="fa653-118">Apps are made up from your own services plus additional libraries (dependencies).</span></span>

<span data-ttu-id="fa653-119">Figure 4-22 montre les étapes de base que vous devez généralement exécuter lors de la création d’une application Docker, suivie d’une description détaillée de chaque étape.</span><span class="sxs-lookup"><span data-stu-id="fa653-119">Figure 4-22 shows the basic steps that you usually need to carry out when building a Docker app, followed by detailed descriptions of each step.</span></span>

![Vue d’ensemble du flux de travail : Étape 1 : Code, étape 2 : écrire des fichiers Dockerfile, étape 3 : créer des images définies avec les fichiers Dockerfile, étape 4 : définir des services avec le fichier docker-compose, étape 5 : exécution conteneurs ou applications composées, étape 6 - tester des applications, étape 7 - Push pour lancer la boucle externe (pipelines CI/CD) ou de continuer de veloping.](./media/image19.png)

<span data-ttu-id="fa653-121">**Figure 4-22**.</span><span class="sxs-lookup"><span data-stu-id="fa653-121">**Figure 4-22**.</span></span> <span data-ttu-id="fa653-122">Flux de travail général pour le cycle de vie pour les applications Docker en conteneur à l’aide de la CLI Docker</span><span class="sxs-lookup"><span data-stu-id="fa653-122">High-level workflow for the life cycle for Docker containerized applications using Docker CLI</span></span>

### <a name="step-1-start-coding-in-visual-studio-code-and-create-your-initial-appservice-baseline"></a><span data-ttu-id="fa653-123">Étape 1 : Commencer le codage dans Visual Studio Code et créer votre base de référence de l’application ou du service initial</span><span class="sxs-lookup"><span data-stu-id="fa653-123">Step 1: Start coding in Visual Studio Code and create your initial app/service baseline</span></span>

<span data-ttu-id="fa653-124">Manière de développer votre application est similaire à la façon de que procéder sans Docker.</span><span class="sxs-lookup"><span data-stu-id="fa653-124">The way you develop your application is similar to the way you do it without Docker.</span></span> <span data-ttu-id="fa653-125">La différence est que lors du développement, vous déployez et testez votre application ou les services qui s’exécutent dans des conteneurs Docker placés dans votre environnement local (comme un Linux VM ou de Windows).</span><span class="sxs-lookup"><span data-stu-id="fa653-125">The difference is that while developing, you're deploying and testing your application or services running within Docker containers placed in your local environment (like a Linux VM or Windows).</span></span>

**<span data-ttu-id="fa653-126">Configuration de votre environnement local</span><span class="sxs-lookup"><span data-stu-id="fa653-126">Setting up your local environment</span></span>**

<span data-ttu-id="fa653-127">Avec les dernières versions de Docker pour Mac et Windows, il est plus facile que jamais pour développer des applications de Docker, et le programme d’installation est simple.</span><span class="sxs-lookup"><span data-stu-id="fa653-127">With the latest versions of Docker for Mac and Windows, it's easier than ever to develop Docker applications, and the setup is straightforward.</span></span>

> [!INFORMATION]
>
> <span data-ttu-id="fa653-129">Pour obtenir des instructions sur la configuration de Docker pour Windows, accédez à <https://docs.docker.com/docker-for-windows/>.</span><span class="sxs-lookup"><span data-stu-id="fa653-129">For instructions on setting up Docker for Windows, go to <https://docs.docker.com/docker-for-windows/>.</span></span>
>
><span data-ttu-id="fa653-130">Pour obtenir des instructions sur la configuration Docker pour Mac, accédez à <https://docs.docker.com/docker-for-mac/>.</span><span class="sxs-lookup"><span data-stu-id="fa653-130">For instructions on setting up Docker for Mac, go to <https://docs.docker.com/docker-for-mac/>.</span></span>

<span data-ttu-id="fa653-131">Vous devez en outre, un éditeur de code afin que vous pouvez développer en fait votre application tout en utilisant l’interface CLI Docker.</span><span class="sxs-lookup"><span data-stu-id="fa653-131">In addition, you'll need a code editor so that you can actually develop your application while using Docker CLI.</span></span>

<span data-ttu-id="fa653-132">Microsoft fournit Visual Studio Code, qui est un éditeur de code léger qui est pris en charge sur Mac, Windows et Linux et fournit des fonctionnalités IntelliSense avec [prise en charge de nombreux langages](https://code.visualstudio.com/docs/languages/overview) (JavaScript, .NET, Go, Java, Ruby, Python et la plupart les langages modernes), [débogage](https://code.visualstudio.com/Docs/editor/debugging), [une intégration avec Git](https://code.visualstudio.com/Docs/editor/versioncontrol) et [prise en charge des extensions](https://code.visualstudio.com/docs/extensions/overview).</span><span class="sxs-lookup"><span data-stu-id="fa653-132">Microsoft provides Visual Studio Code, which is a lightweight code editor that's supported on Mac, Windows, and Linux, and provides IntelliSense with [support for many languages](https://code.visualstudio.com/docs/languages/overview) (JavaScript, .NET, Go, Java, Ruby, Python, and most modern languages), [debugging](https://code.visualstudio.com/Docs/editor/debugging), [integration with Git](https://code.visualstudio.com/Docs/editor/versioncontrol) and [extensions support](https://code.visualstudio.com/docs/extensions/overview).</span></span> <span data-ttu-id="fa653-133">Cet éditeur est parfait pour les développeurs Mac et Linux.</span><span class="sxs-lookup"><span data-stu-id="fa653-133">This editor is a great fit for Mac and Linux developers.</span></span> <span data-ttu-id="fa653-134">Dans Windows, vous pouvez également utiliser l’application complète de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="fa653-134">In Windows, you also can use the full Visual Studio application.</span></span>

> [!INFORMATION]
>
> <span data-ttu-id="fa653-136">Pour obtenir des instructions sur l’installation de Visual Studio Code pour Windows, Mac ou Linux, accédez à <https://code.visualstudio.com/docs/setup/setup-overview/>.</span><span class="sxs-lookup"><span data-stu-id="fa653-136">For instructions on installing Visual Studio Code for Windows, Mac, or Linux, go to <https://code.visualstudio.com/docs/setup/setup-overview/>.</span></span>
>
> <span data-ttu-id="fa653-137">Pour obtenir des instructions sur la configuration Docker pour Mac, accédez à <https://docs.docker.com/docker-for-mac/>.</span><span class="sxs-lookup"><span data-stu-id="fa653-137">For instructions on setting up Docker for Mac, go to <https://docs.docker.com/docker-for-mac/>.</span></span>

<span data-ttu-id="fa653-138">Vous pouvez utiliser avec l’interface CLI Docker et écrivez votre code à l’aide de n’importe quel éditeur de code, mais à l’aide de Visual Studio Code avec l’extension Docker facilite auteur `Dockerfile` et `docker-compose.yml` fichiers dans votre espace de travail.</span><span class="sxs-lookup"><span data-stu-id="fa653-138">You can work with Docker CLI and write your code using any code editor, but using Visual Studio Code with the Docker extension makes it easy to author `Dockerfile` and `docker-compose.yml` files in your workspace.</span></span> <span data-ttu-id="fa653-139">Vous pouvez également exécuter des tâches et des scripts à partir de l’IDE de Visual Studio Code pour exécuter des commandes Docker à l’aide de l’interface CLI Docker en dessous.</span><span class="sxs-lookup"><span data-stu-id="fa653-139">You can also run tasks and scripts from the Visual Studio Code IDE to execute Docker commands using the Docker CLI underneath.</span></span>

<span data-ttu-id="fa653-140">L’extension Docker pour VS Code fournit les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="fa653-140">The Docker extension for VS Code provides the following features:</span></span>

- <span data-ttu-id="fa653-141">Automatique `Dockerfile` et `docker-compose.yml` génération de fichiers</span><span class="sxs-lookup"><span data-stu-id="fa653-141">Automatic `Dockerfile` and `docker-compose.yml` file generation</span></span>

- <span data-ttu-id="fa653-142">Conseils de mise en surbrillance et le pointage de syntaxe pour `docker-compose.yml` et `Dockerfile` fichiers</span><span class="sxs-lookup"><span data-stu-id="fa653-142">Syntax highlighting and hover tips for `docker-compose.yml` and `Dockerfile` files</span></span>

- <span data-ttu-id="fa653-143">IntelliSense (saisie semi-automatique) pour `Dockerfile` et `docker-compose.yml` fichiers</span><span class="sxs-lookup"><span data-stu-id="fa653-143">IntelliSense (completions) for `Dockerfile` and `docker-compose.yml` files</span></span>

- <span data-ttu-id="fa653-144">Linting (erreurs et avertissements) pour `Dockerfile` fichiers</span><span class="sxs-lookup"><span data-stu-id="fa653-144">Linting (errors and warnings) for `Dockerfile` files</span></span>

- <span data-ttu-id="fa653-145">Intégration de Palette (F1) pour les commandes Docker les plus courantes de commande</span><span class="sxs-lookup"><span data-stu-id="fa653-145">Command Palette (F1) integration for the most common Docker commands</span></span>

- <span data-ttu-id="fa653-146">Intégration de l’Explorateur pour la gestion des Images et des conteneurs</span><span class="sxs-lookup"><span data-stu-id="fa653-146">Explorer integration for managing Images and Containers</span></span>

- <span data-ttu-id="fa653-147">Déployer des images à partir de DockerHub et des registres de conteneurs Azure sur Azure App Service</span><span class="sxs-lookup"><span data-stu-id="fa653-147">Deploy images from DockerHub and Azure Container Registries to Azure App Service</span></span>

<span data-ttu-id="fa653-148">Pour installer l’extension Docker, appuyez sur Ctrl + Maj + P, tapez `ext install`, puis exécutez la commande d’installer l’Extension pour afficher la liste des extensions Marketplace.</span><span class="sxs-lookup"><span data-stu-id="fa653-148">To install the Docker extension, press Ctrl+Shift+P, type `ext install`, and then run the Install Extension command to bring up the Marketplace extension list.</span></span> <span data-ttu-id="fa653-149">Ensuite, tapez **docker** pour filtrer les résultats, puis sélectionnez l’extension de la prise en charge Docker, comme illustré dans la Figure 4-23.</span><span class="sxs-lookup"><span data-stu-id="fa653-149">Next, type **docker** to filter the results, and then select the Docker Support extension, as depicted in Figure 4-23.</span></span>

![Affichage de l’extension Docker pour VS Code.](./media/image20.png)

<span data-ttu-id="fa653-151">**Figure 4-23**.</span><span class="sxs-lookup"><span data-stu-id="fa653-151">**Figure 4-23**.</span></span> <span data-ttu-id="fa653-152">L’installation de l’Extension Docker dans Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="fa653-152">Installing the Docker Extension in Visual Studio Code</span></span>

### <a name="step-2-create-a-dockerfile-related-to-an-existing-image-plain-os-or-dev-environments-like-net-core-nodejs-and-ruby"></a><span data-ttu-id="fa653-153">Étape 2 : Créer un fichier DockerFile associé à une image existante (système d’exploitation brut ou des environnements de développement tels que .NET Core, Node.js et Ruby)</span><span class="sxs-lookup"><span data-stu-id="fa653-153">Step 2: Create a DockerFile related to an existing image (plain OS or dev environments like .NET Core, Node.js, and Ruby)</span></span>

<span data-ttu-id="fa653-154">Vous aurez besoin d’un `DockerFile` par une image personnalisée à générer et par conteneur à déployer.</span><span class="sxs-lookup"><span data-stu-id="fa653-154">You'll need a `DockerFile` per custom image to be built and per container to be deployed.</span></span> <span data-ttu-id="fa653-155">Si votre application est composée d’un seul service personnalisé, vous aurez besoin d’un seul `DockerFile`.</span><span class="sxs-lookup"><span data-stu-id="fa653-155">If your app is made up of a single custom service, you'll need a single `DockerFile`.</span></span> <span data-ttu-id="fa653-156">Mais si votre application est composée de plusieurs services (comme dans une architecture de microservices), vous avez besoin d’un `Dockerfile` par service.</span><span class="sxs-lookup"><span data-stu-id="fa653-156">But if your app is composed of multiple services (as in a microservices architecture), you'll need one `Dockerfile` per service.</span></span>

<span data-ttu-id="fa653-157">Le `DockerFile` est généralement placé dans le dossier racine de votre application ou service et contient les commandes requises pour que cette Docker sache comment configurer et exécuter l’application ou le service.</span><span class="sxs-lookup"><span data-stu-id="fa653-157">The `DockerFile` is commonly placed in the root folder of your app or service and contains the required commands so that Docker knows how to set up and run that app or service.</span></span> <span data-ttu-id="fa653-158">Vous pouvez créer votre `DockerFile` et ajoutez-le à votre projet, ainsi que votre code (node.js, .NET Core, etc.), ou, si vous débutez avec l’environnement, examinons l’info-bulle suivante.</span><span class="sxs-lookup"><span data-stu-id="fa653-158">You can create your `DockerFile` and add it to your project along with your code (node.js, .NET Core, etc.), or, if you're new to the environment, take a look at the following Tip.</span></span>

> [!TIP]
>
> <span data-ttu-id="fa653-159">Vous pouvez utiliser l’extension Docker pour vous guider lors de l’utilisation du `Dockerfile` et `docker-compose.yml` les fichiers liés à vos conteneurs Docker.</span><span class="sxs-lookup"><span data-stu-id="fa653-159">You can use the Docker extension to guide you when using the `Dockerfile` and `docker-compose.yml` files related to your Docker containers.</span></span> <span data-ttu-id="fa653-160">Finalement, vous allez probablement écrire ces types de fichiers sans cet outil, mais à l’aide de l’extension Docker est un bon point de départ qui permettra d’accélérer votre courbe d’apprentissage.</span><span class="sxs-lookup"><span data-stu-id="fa653-160">Eventually, you'll probably write these kinds of files without this tool, but using the Docker extension is a good starting point that will accelerate your learning curve.</span></span>

<span data-ttu-id="fa653-161">Dans la Figure 4-24, vous pouvez voir comment une commande docker-compose fichier est ajouté à l’aide de l’Extension Docker pour VS Code.</span><span class="sxs-lookup"><span data-stu-id="fa653-161">In Figure 4-24, you can see how a docker-compose file is added by using the Docker Extension for VS Code.</span></span>

![Affichage de la console de l’extension Docker pour VS Code.](./media/image24.png)

<span data-ttu-id="fa653-163">**Figure 4-24**.</span><span class="sxs-lookup"><span data-stu-id="fa653-163">**Figure 4-24**.</span></span> <span data-ttu-id="fa653-164">Fichiers docker ajoutés à l’aide de la **fichiers Docker ajouter à la commande de l’espace de travail**</span><span class="sxs-lookup"><span data-stu-id="fa653-164">Docker files added using the **Add Docker files to Workspace command**</span></span>

<span data-ttu-id="fa653-165">Lorsque vous ajoutez un fichier DockerFile, vous spécifiez quelle image Docker de base vous allez utiliser (comme à l’aide de `FROM mcr.microsoft.com/dotnet/core/aspnet`).</span><span class="sxs-lookup"><span data-stu-id="fa653-165">When you add a DockerFile, you specify what base Docker image you’ll be using (like using `FROM mcr.microsoft.com/dotnet/core/aspnet`).</span></span> <span data-ttu-id="fa653-166">Vous allez générer généralement votre image personnalisée sur une image de base que vous obtenez à partir de n’importe quel dépôt officiel dans le [Registre Docker Hub](https://hub.docker.com/) (comme un [image pour .NET Core](https://hub.docker.com/_/microsoft-dotnet-core/) ou celui [pour Node.js](https://hub.docker.com/_/node/)).</span><span class="sxs-lookup"><span data-stu-id="fa653-166">You'll usually build your custom image on top of a base image that you get from any official repository at the [Docker Hub registry](https://hub.docker.com/) (like an [image for .NET Core](https://hub.docker.com/_/microsoft-dotnet-core/) or the one [for Node.js](https://hub.docker.com/_/node/)).</span></span>

***<span data-ttu-id="fa653-167">Utilisez une image Docker officielle existante</span><span class="sxs-lookup"><span data-stu-id="fa653-167">Use an existing official Docker image</span></span>***

<span data-ttu-id="fa653-168">À l’aide d’un dépôt officiel de la pile de langage avec un numéro de version garantit que les mêmes fonctionnalités de langage sont disponibles sur toutes les machines (y compris le développement, test et production).</span><span class="sxs-lookup"><span data-stu-id="fa653-168">Using an official repository of a language stack with a version number ensures that the same language features are available on all machines (including development, testing, and production).</span></span>

<span data-ttu-id="fa653-169">Voici un exemple de fichier DockerFile pour un conteneur .NET Core :</span><span class="sxs-lookup"><span data-stu-id="fa653-169">The following is a sample DockerFile for a .NET Core container:</span></span>

```Dockerfile
# Base Docker image to use  
FROM mcr.microsoft.com/dotnet/core/aspnet:2.1
  
# Set the Working Directory and files to be copied to the image  
ARG source  
WORKDIR /app  
COPY ${source:-bin/Release/PublishOutput} .  
  
# Configure the listening port to 80 (Internal/Secured port within Docker host)  
EXPOSE 80  
  
# Application entry point  
ENTRYPOINT ["dotnet", "MyCustomMicroservice.dll"]
```

<span data-ttu-id="fa653-170">Dans ce cas, l’image est basée sur la version 2.1 de l’image Docker ASP.NET Core officielle (multi-arch pour Linux et Windows), conformément à la ligne `FROM mcr.microsoft.com/dotnet/core/aspnet:2.1`.</span><span class="sxs-lookup"><span data-stu-id="fa653-170">In this case, the image is based on version 2.1 of the official ASP.NET Core Docker image (multi-arch for Linux and Windows), as per the line `FROM mcr.microsoft.com/dotnet/core/aspnet:2.1`.</span></span> <span data-ttu-id="fa653-171">(Pour plus d’informations sur cette rubrique, consultez le [Image Docker ASP.NET Core](https://hub.docker.com/_/microsoft-dotnet-core-aspnet/) page et le [Image Docker .NET Core](https://hub.docker.com/_/microsoft-dotnet-core/) page).</span><span class="sxs-lookup"><span data-stu-id="fa653-171">(For more information about this topic, see the [ASP.NET Core Docker Image](https://hub.docker.com/_/microsoft-dotnet-core-aspnet/) page and the [.NET Core Docker Image](https://hub.docker.com/_/microsoft-dotnet-core/) page).</span></span>

<span data-ttu-id="fa653-172">Dans le fichier DockerFile, vous pouvez également demander à Docker d’écouter sur le port TCP que vous utiliserez lors de l’exécution (par exemple, le port 80).</span><span class="sxs-lookup"><span data-stu-id="fa653-172">In the DockerFile, you can also instruct Docker to listen to the TCP port that you'll use at runtime (such as port 80).</span></span>

<span data-ttu-id="fa653-173">Vous pouvez spécifier des paramètres de configuration supplémentaires dans le fichier Dockerfile, en fonction du langage et du framework que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="fa653-173">You can specify additional configuration settings in the Dockerfile, depending on the language and framework you're using.</span></span> <span data-ttu-id="fa653-174">Par exemple, le `ENTRYPOINT` ligne avec `["dotnet", "MySingleContainerWebApp.dll"]` indique à Docker pour exécuter une application .NET Core.</span><span class="sxs-lookup"><span data-stu-id="fa653-174">For instance, the `ENTRYPOINT` line with `["dotnet", "MySingleContainerWebApp.dll"]` tells Docker to run a .NET Core application.</span></span> <span data-ttu-id="fa653-175">Si vous utilisez le Kit de développement et de l’interface CLI .NET Core (`dotnet CLI`) pour générer et exécuter l’application .NET, ce paramètre est différent.</span><span class="sxs-lookup"><span data-stu-id="fa653-175">If you're using the SDK and the .NET Core CLI (`dotnet CLI`) to build and run the .NET application, this setting would be different.</span></span> <span data-ttu-id="fa653-176">Le point clé ici est que la ligne ENTRYPOINT et autres paramètres dépendent de la langue et la plateforme que vous choisissez pour votre application.</span><span class="sxs-lookup"><span data-stu-id="fa653-176">The key point here is that the ENTRYPOINT line and other settings depend on the language and platform you choose for your application.</span></span>

> [!INFORMATION]
>
> <span data-ttu-id="fa653-178">Pour plus d’informations sur la création d’images Docker pour les applications .NET Core, accédez à <https://docs.microsoft.com/dotnet/core/docker/building-net-docker-images>.</span><span class="sxs-lookup"><span data-stu-id="fa653-178">For more information about building Docker images for .NET Core applications, go to <https://docs.microsoft.com/dotnet/core/docker/building-net-docker-images>.</span></span>
>
> <span data-ttu-id="fa653-179">Pour en savoir plus sur la création de vos propres images, accédez à <https://docs.docker.com/engine/tutorials/dockerimages/>.</span><span class="sxs-lookup"><span data-stu-id="fa653-179">To learn more about building your own images, go to <https://docs.docker.com/engine/tutorials/dockerimages/>.</span></span>

**<span data-ttu-id="fa653-180">Utiliser les référentiels d’images multi-arch</span><span class="sxs-lookup"><span data-stu-id="fa653-180">Use multi-arch image repositories</span></span>**

<span data-ttu-id="fa653-181">Un nom d’image unique dans un référentiel peut contenir des variantes de plateforme, par exemple une image Linux et une image de Windows.</span><span class="sxs-lookup"><span data-stu-id="fa653-181">A single image name in a repo can contain platform variants, such as a Linux image and a Windows image.</span></span> <span data-ttu-id="fa653-182">Cette fonctionnalité permet aux fournisseurs comme Microsoft (créateurs d’images de base) créer un référentiel unique pour plusieurs plateformes (autrement dit, Linux et Windows).</span><span class="sxs-lookup"><span data-stu-id="fa653-182">This feature allows vendors like Microsoft (base image creators) to create a single repo to cover multiple platforms (that is, Linux and Windows).</span></span> <span data-ttu-id="fa653-183">Par exemple, le [dotnet/core/aspnet](https://hub.docker.com/_/microsoft-dotnet-core-aspnet/) référentiel disponible dans le Registre Docker Hub fournit la prise en charge de Linux et Windows Nano Server en utilisant le même nom d’image.</span><span class="sxs-lookup"><span data-stu-id="fa653-183">For example, the [dotnet/core/aspnet](https://hub.docker.com/_/microsoft-dotnet-core-aspnet/) repository available in the Docker Hub registry provides support for Linux and Windows Nano Server by using the same image name.</span></span>

<span data-ttu-id="fa653-184">Extraction de la [dotnet/core/aspnet](https://hub.docker.com/_/microsoft-dotnet-core-aspnet/) image à partir d’un ordinateur hôte Windows extrait la variante de Windows, tandis que l’extraction du même nom d’image à partir d’un hôte Linux extrait la variante Linux.</span><span class="sxs-lookup"><span data-stu-id="fa653-184">Pulling the [dotnet/core/aspnet](https://hub.docker.com/_/microsoft-dotnet-core-aspnet/) image from a Windows host pulls the Windows variant, whereas pulling the same image name from a Linux host pulls the Linux variant.</span></span>

***<span data-ttu-id="fa653-185">Créer votre image de base à partir de zéro</span><span class="sxs-lookup"><span data-stu-id="fa653-185">Create your base image from scratch</span></span>***

<span data-ttu-id="fa653-186">Vous pouvez créer votre propre image de base de Docker à partir de zéro, comme expliqué dans cet [article](https://docs.docker.com/engine/userguide/eng-image/baseimages/) à partir de Docker.</span><span class="sxs-lookup"><span data-stu-id="fa653-186">You can create your own Docker base image from scratch as explained in this [article](https://docs.docker.com/engine/userguide/eng-image/baseimages/) from Docker.</span></span> <span data-ttu-id="fa653-187">Ce scénario n’est probablement pas vous convient le mieux si vous venez de démarrer avec Docker, mais si vous souhaitez définir les bits spécifiques de votre propre image de base, vous pouvez le faire.</span><span class="sxs-lookup"><span data-stu-id="fa653-187">This scenario is probably not the best for you if you're just starting with Docker, but if you want to set the specific bits of your own base image, you can do it.</span></span>

### <a name="step-3-create-your-custom-docker-images-embedding-your-service-in-it"></a><span data-ttu-id="fa653-188">Étape 3 : Créer votre l’incorporation de votre service qu’il contient des images Docker personnalisées</span><span class="sxs-lookup"><span data-stu-id="fa653-188">Step 3: Create your custom Docker images embedding your service in it</span></span>

<span data-ttu-id="fa653-189">Pour chaque service personnalisé qui compose votre application, vous devez créer une image associée.</span><span class="sxs-lookup"><span data-stu-id="fa653-189">For each custom service that comprises your app, you'll need to create a related image.</span></span> <span data-ttu-id="fa653-190">Si votre application est composée d’un service unique ou d’application web, vous aurez besoin en une seule image.</span><span class="sxs-lookup"><span data-stu-id="fa653-190">If your app is made up of a single service or web app, you'll need just a single image.</span></span>

> [!NOTE]
>
> <span data-ttu-id="fa653-191">Lorsque prenant en compte la « boucle externe flux de travail DevOps », les images seront créées par un processus de génération automatisé dès que vous ajoutez votre code source à un référentiel Git (intégration continue), donc les images sont créées dans cet environnement global à partir de votre code source.</span><span class="sxs-lookup"><span data-stu-id="fa653-191">When taking into account the "outer-loop DevOps workflow", the images will be created by an automated build process whenever you push your source code to a Git repository (Continuous Integration), so the images will be created in that global environment from your source code.</span></span>
>
> <span data-ttu-id="fa653-192">Mais nous estimons qu’accédant à cet itinéraire de la boucle externe, nous devons vérifier que l’application Docker réellement fonctionne correctement afin qu’ils n’est pas envoyé de code qui peut ne pas fonctionne correctement pour le système de contrôle de code source (Git, etc.).</span><span class="sxs-lookup"><span data-stu-id="fa653-192">But before we consider going to that outer-loop route, we need to ensure that the Docker application is actually working properly so that they don't push code that might not work properly to the source control system (Git, etc.).</span></span>
>
> <span data-ttu-id="fa653-193">Par conséquent, chaque développeur doit d’abord faire tout le processus de boucle interne pour tester localement et continuer à développer jusqu'à ce qu’ils souhaitent push d’une fonctionnalité complète ou de modifier le système de contrôle source.</span><span class="sxs-lookup"><span data-stu-id="fa653-193">Therefore, each developer first needs to do the entire inner-loop process to test locally and continue developing until they want to push a complete feature or change to the source control system.</span></span>

<span data-ttu-id="fa653-194">Pour créer une image dans votre environnement local et à l’aide du fichier DockerFile, vous pouvez utiliser la commande docker build, comme illustré dans la Figure 4-25 (vous pouvez également exécuter `docker-compose up --build` pour des applications composées de plusieurs conteneurs/Services).</span><span class="sxs-lookup"><span data-stu-id="fa653-194">To create an image in your local environment and using the DockerFile, you can use the docker build command, as demonstrated in Figure 4-25 (you also can run `docker-compose up --build` for applications composed by several containers/services).</span></span>

![Sortie de la console de la build de docker-compose, affichant les images de la progression du téléchargement.](./media/image25.png)

<span data-ttu-id="fa653-196">**Figure 4-25**.</span><span class="sxs-lookup"><span data-stu-id="fa653-196">**Figure 4-25**.</span></span> <span data-ttu-id="fa653-197">Build de docker en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="fa653-197">Running docker build</span></span>

<span data-ttu-id="fa653-198">Si vous le souhaitez, au lieu d’exécuter directement `docker build` à partir du dossier de projet, vous pouvez tout d’abord générer un dossier déployable avec les bibliothèques .NET nécessaires à l’aide de l’exécution `dotnet publish` commande, puis exécutez `docker build`.</span><span class="sxs-lookup"><span data-stu-id="fa653-198">Optionally, instead of directly running `docker build` from the project folder, you first can generate a deployable folder with the .NET libraries needed by using the run `dotnet publish` command, and then run `docker build`.</span></span>

<span data-ttu-id="fa653-199">Cet exemple crée une image Docker avec le nom `cesardl/netcore-webapi-microservice-docker:first` (`:first` est une balise, comme une version spécifique).</span><span class="sxs-lookup"><span data-stu-id="fa653-199">This example creates a Docker image with the name `cesardl/netcore-webapi-microservice-docker:first` (`:first` is a tag, like a specific version).</span></span> <span data-ttu-id="fa653-200">Vous pouvez effectuer cette étape pour chaque image personnalisée que vous créez pour votre application Docker composée avec plusieurs conteneurs.</span><span class="sxs-lookup"><span data-stu-id="fa653-200">You can take this step for each custom image you need to create for your composed Docker application with several containers.</span></span>

<span data-ttu-id="fa653-201">Vous trouverez les images existantes dans votre référentiel local (votre ordinateur de développement) à l’aide de docker commande images, comme illustré dans la Figure 4-26.</span><span class="sxs-lookup"><span data-stu-id="fa653-201">You can find the existing images in your local repository (your development machine) by using the docker images command, as illustrated in Figure 4-26.</span></span>

![Sortie à partir d’images docker de commande, affichant les images existantes de la console.](./media/image26.png)

<span data-ttu-id="fa653-203">**Figure 4-26**.</span><span class="sxs-lookup"><span data-stu-id="fa653-203">**Figure 4-26**.</span></span> <span data-ttu-id="fa653-204">Affichage des images existantes à l’aide d’images docker</span><span class="sxs-lookup"><span data-stu-id="fa653-204">Viewing existing images using docker images</span></span>

### <a name="step-4-define-your-services-in-docker-composeyml-when-building-a-composed-docker-app-with-multiple-services"></a><span data-ttu-id="fa653-205">Étape 4 : Définir vos services dans docker-compose.yml lors de la création d’une application Docker composée avec plusieurs services</span><span class="sxs-lookup"><span data-stu-id="fa653-205">Step 4: Define your services in docker-compose.yml when building a composed Docker app with multiple services</span></span>

<span data-ttu-id="fa653-206">Avec le `docker-compose.yml` fichier, vous pouvez définir un ensemble de services à être déployé comme une application composée avec les commandes de déploiement expliqués dans la section étape suivante.</span><span class="sxs-lookup"><span data-stu-id="fa653-206">With the `docker-compose.yml` file, you can define a set of related services to be deployed as a composed application with the deployment commands explained in the next step section.</span></span>

<span data-ttu-id="fa653-207">Créez ce fichier dans votre main ou un dossier de solution racine ; Il doit avoir contenu similaire à celle illustrée dans ce `docker-compose.yml` fichier :</span><span class="sxs-lookup"><span data-stu-id="fa653-207">Create that file in your main or root solution folder; it should have content similar to that shown in this `docker-compose.yml` file:</span></span>

```yml
version: '3.4'
services:
  web:
    build: .
    ports:
     - "81:80"
    volumes:
     - .:/code
    depends_on:
     - redis
  redis:
    image: redis
```

<span data-ttu-id="fa653-208">Dans ce cas particulier, ce fichier définit deux services : le service web (votre service personnalisé) et le service redis (un service de cache bien connu).</span><span class="sxs-lookup"><span data-stu-id="fa653-208">In this particular case, this file defines two services: the web service (your custom service) and the redis service (a popular cache service).</span></span> <span data-ttu-id="fa653-209">Chaque service sera déployé en tant que conteneur, nous devons utiliser une image Docker concrete pour chacun.</span><span class="sxs-lookup"><span data-stu-id="fa653-209">Each service will be deployed as a container, so we need to use a concrete Docker image for each.</span></span> <span data-ttu-id="fa653-210">Pour ce service web particulier, l’image doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="fa653-210">For this particular web service, the image will need to do the following:</span></span>

- <span data-ttu-id="fa653-211">Construire à partir du fichier DockerFile dans le répertoire actif</span><span class="sxs-lookup"><span data-stu-id="fa653-211">Build from the DockerFile in the current directory</span></span>

- <span data-ttu-id="fa653-212">Transférer le port exposé 80 sur le conteneur sur le port 81 sur l’ordinateur hôte</span><span class="sxs-lookup"><span data-stu-id="fa653-212">Forward the exposed port 80 on the container to port 81 on the host machine</span></span>

- <span data-ttu-id="fa653-213">Monter le répertoire du projet sur l’ordinateur hôte/code au sein du conteneur, ce qui permet de modifier le code sans avoir à recréer l’image</span><span class="sxs-lookup"><span data-stu-id="fa653-213">Mount the project directory on the host to /code within the container, making it possible for you to modify the code without having to rebuild the image</span></span>

- <span data-ttu-id="fa653-214">Lier le service web au service redis</span><span class="sxs-lookup"><span data-stu-id="fa653-214">Link the web service to the redis service</span></span>

<span data-ttu-id="fa653-215">Le service redis utilise le [dernière image publique redis](https://hub.docker.com/_/redis/) extraite du Registre Docker Hub.</span><span class="sxs-lookup"><span data-stu-id="fa653-215">The redis service uses the [latest public redis image](https://hub.docker.com/_/redis/) pulled from the Docker Hub registry.</span></span> <span data-ttu-id="fa653-216">[redis](https://redis.io/) est un système de cache bien connu pour les applications côté serveur.</span><span class="sxs-lookup"><span data-stu-id="fa653-216">[redis](https://redis.io/) is a popular cache system for server-side applications.</span></span>

### <a name="step-5-build-and-run-your-docker-app"></a><span data-ttu-id="fa653-217">Étape 5 : Générer et exécuter votre application Docker</span><span class="sxs-lookup"><span data-stu-id="fa653-217">Step 5: Build and run your Docker app</span></span>

<span data-ttu-id="fa653-218">Si votre application a uniquement un seul conteneur, vous devez l’exécuter en la déployant sur votre hôte Docker (machine virtuelle ou serveur physique).</span><span class="sxs-lookup"><span data-stu-id="fa653-218">If your app has only a single container, you just need to run it by deploying it to your Docker Host (VM or physical server).</span></span> <span data-ttu-id="fa653-219">Toutefois, si votre application est composée de plusieurs services, vous devez *composer*, trop.</span><span class="sxs-lookup"><span data-stu-id="fa653-219">However, if your app is made up of multiple services, you need to *compose it*, too.</span></span> <span data-ttu-id="fa653-220">Nous allons voir les différentes options.</span><span class="sxs-lookup"><span data-stu-id="fa653-220">Let's see the different options.</span></span>

***<span data-ttu-id="fa653-221">Option A : Exécuter un conteneur unique ou un service</span><span class="sxs-lookup"><span data-stu-id="fa653-221">Option A: Run a single container or service</span></span>***

<span data-ttu-id="fa653-222">Vous pouvez exécuter l’image Docker à l’aide de la commande docker run, comme illustré ici :</span><span class="sxs-lookup"><span data-stu-id="fa653-222">You can run the Docker image by using the docker run command, as shown here:</span></span>

```console
docker run -t -d -p 80:5000 cesardl/netcore-webapi-microservice-docker:first
```

<span data-ttu-id="fa653-223">Pour ce déploiement, nous allons redirection des demandes envoyées vers le port 80 vers le port interne 5000.</span><span class="sxs-lookup"><span data-stu-id="fa653-223">For this particular deployment, we'll be redirecting requests sent to port 80 to the internal port 5000.</span></span> <span data-ttu-id="fa653-224">Maintenant l’application est à l’écoute sur le port externe 80 au niveau de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="fa653-224">Now the application is listening on the external port 80 at the host level.</span></span>

***<span data-ttu-id="fa653-225">Option B : Composer et exécuter une application de plusieurs conteneurs</span><span class="sxs-lookup"><span data-stu-id="fa653-225">Option B: Compose and run a multiple-container application</span></span>***

<span data-ttu-id="fa653-226">Dans la plupart des scénarios d’entreprise, une application Docker est composée de plusieurs services.</span><span class="sxs-lookup"><span data-stu-id="fa653-226">In most enterprise scenarios, a Docker application will be composed of multiple services.</span></span> <span data-ttu-id="fa653-227">Dans ce cas, vous pouvez exécuter la `docker-compose up` commande (Figure 4-27), qui utilise le fichier docker-compose.yml que vous avez peut-être créé précédemment.</span><span class="sxs-lookup"><span data-stu-id="fa653-227">For these cases, you can run the `docker-compose up` command (Figure 4-27), which will use the docker-compose.yml file that you might have created previously.</span></span> <span data-ttu-id="fa653-228">Exécution de cette commande déploie une application composée avec toutes ses conteneurs associés.</span><span class="sxs-lookup"><span data-stu-id="fa653-228">Running this command deploys a composed application with all of its related containers.</span></span>

![Sortie à partir de la console le-commande docker compose up.](./media/image27.png)

<span data-ttu-id="fa653-230">**Figure 4-27**.</span><span class="sxs-lookup"><span data-stu-id="fa653-230">**Figure 4-27**.</span></span> <span data-ttu-id="fa653-231">Résultats de l’exécution de la commande « docker-compose up »</span><span class="sxs-lookup"><span data-stu-id="fa653-231">Results of running the "docker-compose up" command</span></span>

<span data-ttu-id="fa653-232">Après avoir exécuté `docker-compose up`, vous déployez votre application et ses conteneurs associés sur votre hôte Docker, comme illustré dans la Figure 4-28, dans la représentation sous forme de machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="fa653-232">After you run `docker-compose up`, you deploy your application and its related container(s) into your Docker Host, as illustrated in Figure 4-28, in the VM representation.</span></span>

![Machine virtuelle exécutant des applications à plusieurs conteneurs.](./media/image28.png)

<span data-ttu-id="fa653-234">**Figure 4-28**.</span><span class="sxs-lookup"><span data-stu-id="fa653-234">**Figure 4-28**.</span></span> <span data-ttu-id="fa653-235">Machine virtuelle avec des conteneurs Docker déployés</span><span class="sxs-lookup"><span data-stu-id="fa653-235">VM with Docker containers deployed</span></span>

### <a name="step-6-test-your-docker-application-locally-in-your-local-cd-vm"></a><span data-ttu-id="fa653-236">Étape 6 : Tester votre application Docker (local, dans votre machine virtuelle de CD locale)</span><span class="sxs-lookup"><span data-stu-id="fa653-236">Step 6: Test your Docker application (locally, in your local CD VM)</span></span>

<span data-ttu-id="fa653-237">Cette étape varie en fonction de ce que fait votre application.</span><span class="sxs-lookup"><span data-stu-id="fa653-237">This step will vary depending on what your app is doing.</span></span>

<span data-ttu-id="fa653-238">Dans une simple API .NET Core Web « Hello World » déployé comme un seul conteneur ou un service, vous devez simplement accéder au service en fournissant le port TCP spécifié dans le fichier DockerFile.</span><span class="sxs-lookup"><span data-stu-id="fa653-238">In a simple .NET Core Web API "Hello World" deployed as a single container or service, you'd just need to access the service by providing the TCP port specified in the DockerFile.</span></span>

<span data-ttu-id="fa653-239">Si localhost est désactivée, pour accéder à votre service, vous pouvez trouver l’adresse IP de l’ordinateur à l’aide de cette commande :</span><span class="sxs-lookup"><span data-stu-id="fa653-239">If localhost is not turned on, to navigate to your service, find the IP address for the machine by using this command:</span></span>

```console
docker-machine {IP} {YOUR-CONTAINER-NAME}
```

<span data-ttu-id="fa653-240">Sur l’hôte Docker, ouvrez un navigateur et accédez à ce site ; Vous devez voir votre application ou du service en cours d’exécution, comme illustré dans la Figure 4-29.</span><span class="sxs-lookup"><span data-stu-id="fa653-240">On the Docker host, open a browser and navigate to that site; you should see your app/service running, as demonstrated in Figure 4-29.</span></span>

![Affichage du navigateur de la réponse à partir de localhost/API/values.](./media/image29.png)

<span data-ttu-id="fa653-242">**Figure 4-29**.</span><span class="sxs-lookup"><span data-stu-id="fa653-242">**Figure 4-29**.</span></span> <span data-ttu-id="fa653-243">Test de votre application Docker localement en utilisant localhost</span><span class="sxs-lookup"><span data-stu-id="fa653-243">Testing your Docker application locally using localhost</span></span>

<span data-ttu-id="fa653-244">Notez qu’il utilise le port 80, mais en interne qu’il est redirigé vers le port 5000, parce que c’est la façon dont elle a été déployée avec `docker run`, comme expliqué précédemment.</span><span class="sxs-lookup"><span data-stu-id="fa653-244">Note that it's using port 80, but internally it's being redirected to port 5000, because that's how it was deployed with `docker run`, as explained earlier.</span></span>

<span data-ttu-id="fa653-245">Vous pouvez tester cela à l’aide de CURL à partir du terminal.</span><span class="sxs-lookup"><span data-stu-id="fa653-245">You can test this by using CURL from the terminal.</span></span> <span data-ttu-id="fa653-246">Dans une installation de Docker sur Windows, l’adresse IP par défaut est 10.0.75.1, comme illustré dans la Figure 4-30.</span><span class="sxs-lookup"><span data-stu-id="fa653-246">In a Docker installation on Windows, the default IP is 10.0.75.1, as depicted in Figure 4-30.</span></span>

![Sortie à partir de l’obtention de la console le http://10.0.75.1/API/values avec curl](./media/image30.png)

<span data-ttu-id="fa653-248">**Figure 4-30**.</span><span class="sxs-lookup"><span data-stu-id="fa653-248">**Figure 4-30**.</span></span> <span data-ttu-id="fa653-249">Test d’une application de Docker localement à l’aide de CURL</span><span class="sxs-lookup"><span data-stu-id="fa653-249">Testing a Docker application locally by using CURL</span></span>

**<span data-ttu-id="fa653-250">Débogage d’un conteneur en cours d’exécution sur Docker</span><span class="sxs-lookup"><span data-stu-id="fa653-250">Debugging a container running on Docker</span></span>**

<span data-ttu-id="fa653-251">Visual Studio Code prend en charge le débogage Docker si vous utilisez Node.js et autres plateformes telles que les conteneurs .NET Core.</span><span class="sxs-lookup"><span data-stu-id="fa653-251">Visual Studio Code supports debugging Docker if you're using Node.js and other platforms like .NET Core containers.</span></span>

<span data-ttu-id="fa653-252">Vous également pouvez déboguer les conteneurs .NET Core ou .NET Framework dans Docker lorsque vous utilisez Visual Studio pour Windows ou Mac, comme décrit dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="fa653-252">You also can debug .NET Core or .NET Framework containers in Docker when using Visual Studio for Windows or Mac, as described in the next section.</span></span>

> [!INFORMATION]
>
> <span data-ttu-id="fa653-254">Pour en savoir plus sur le débogage des conteneurs Docker de Node.js, accédez à <https://blog.docker.com/2016/07/live-debugging-docker/> et <https://blogs.msdn.microsoft.com/user_ed/2016/02/27/visual-studio-code-new-features-13-big-debugging-updates-rich-object-hover-conditional-breakpoints-node-js-mono-more/>.</span><span class="sxs-lookup"><span data-stu-id="fa653-254">To learn more about debugging Node.js Docker containers, go to <https://blog.docker.com/2016/07/live-debugging-docker/> and <https://blogs.msdn.microsoft.com/user_ed/2016/02/27/visual-studio-code-new-features-13-big-debugging-updates-rich-object-hover-conditional-breakpoints-node-js-mono-more/>.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="fa653-255">[Précédent](docker-apps-development-environment.md)
>[Suivant](visual-studio-tools-for-docker.md)</span><span class="sxs-lookup"><span data-stu-id="fa653-255">[Previous](docker-apps-development-environment.md)
[Next](visual-studio-tools-for-docker.md)</span></span>
