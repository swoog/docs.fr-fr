---
title: Flux de travail de développement de la boucle interne pour les applications Docker
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: f7acb60e6136c0250d18bdce23ac21fb6aa80b34
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53148858"
---
# <a name="inner-loop-development-workflow-for-docker-apps"></a><span data-ttu-id="927e5-103">Flux de travail de développement de la boucle interne pour les applications Docker</span><span class="sxs-lookup"><span data-stu-id="927e5-103">Inner-loop development workflow for Docker apps</span></span>

<span data-ttu-id="927e5-104">Avant de déclencher le flux de travail de boucle externe couvrant l’ensemble DevOps cycle, tout cela commence sur chaque machine de développeur, codage de l’application elle-même, à l’aide de leurs plateformes ou langages préférés et de le tester localement (Figure 4-14).</span><span class="sxs-lookup"><span data-stu-id="927e5-104">Before triggering the outer-loop workflow spanning the entire DevOps cycle, it all begins on each developer's machine, coding the app itself, using their preferred languages or platforms, and testing it locally (Figure 4-14).</span></span> <span data-ttu-id="927e5-105">Mais dans tous les cas, vous aurez un point très important en commun, peu importe quel langage, infrastructure ou plateformes que vous choisissez.</span><span class="sxs-lookup"><span data-stu-id="927e5-105">But in every case, you will have a very important point in common, no matter what language, framework, or platforms you choose.</span></span> <span data-ttu-id="927e5-106">Dans ce flux de travail spécifique, vous toujours développez et testez des conteneurs Docker, mais localement.</span><span class="sxs-lookup"><span data-stu-id="927e5-106">In this specific workflow, you are always developing and testing Docker containers, but locally.</span></span>

![](./media/image18.png)

<span data-ttu-id="927e5-107">Figure 4-14 : Contexte de développement de la boucle interne</span><span class="sxs-lookup"><span data-stu-id="927e5-107">Figure 4-14: Inner-loop development context</span></span>

<span data-ttu-id="927e5-108">Le conteneur ou une instance d’une image Docker contiendra ces composants :</span><span class="sxs-lookup"><span data-stu-id="927e5-108">The container or instance of a Docker image will contain these components:</span></span>

-   <span data-ttu-id="927e5-109">Une sélection de système d’exploitation (par exemple, une distribution Linux ou Windows)</span><span class="sxs-lookup"><span data-stu-id="927e5-109">An operating system selection (for example, a Linux distribution or Windows)</span></span>

-   <span data-ttu-id="927e5-110">Fichiers ajoutés par le développeur (par exemple, les binaires d’application)</span><span class="sxs-lookup"><span data-stu-id="927e5-110">Files added by the developer (for example, app binaries)</span></span>

-   <span data-ttu-id="927e5-111">Configuration (par exemple, les paramètres d’environnement et les dépendances)</span><span class="sxs-lookup"><span data-stu-id="927e5-111">Configuration (for example, environment settings and dependencies)</span></span>

-   <span data-ttu-id="927e5-112">Instructions pour les processus pour exécuter par Docker</span><span class="sxs-lookup"><span data-stu-id="927e5-112">Instructions for what processes to run by Docker</span></span>

<span data-ttu-id="927e5-113">Vous pouvez configurer le flux de travail de développement de la boucle interne qui utilise Docker en tant que le processus (décrit dans la section suivante).</span><span class="sxs-lookup"><span data-stu-id="927e5-113">You can set up the inner-loop development workflow that utilizes Docker as the process (described in the next section).</span></span> <span data-ttu-id="927e5-114">Prenez en compte que les premières étapes pour configurer l’environnement n’est pas inclus, car vous devez le faire qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="927e5-114">Take into account that the initial steps to set up the environment is not included, because you need to do that just once.</span></span>

## <a name="building-a-single-app-within-a-docker-container-using-visual-studio-code-and-docker-cli"></a><span data-ttu-id="927e5-115">Création d’une application unique dans un conteneur Docker à l’aide de Visual Studio Code et interface CLI Docker</span><span class="sxs-lookup"><span data-stu-id="927e5-115">Building a single app within a Docker container using Visual Studio Code and Docker CLI</span></span>

<span data-ttu-id="927e5-116">Les applications sont constituées à partir de vos propres services ainsi que des bibliothèques supplémentaires (dépendances).</span><span class="sxs-lookup"><span data-stu-id="927e5-116">Apps are made up from your own services plus additional libraries (dependencies).</span></span>

<span data-ttu-id="927e5-117">Figure 4-15 montre les étapes de base que vous devez généralement exécuter lors de la création d’une application Docker, suivie d’une description détaillée de chaque étape.</span><span class="sxs-lookup"><span data-stu-id="927e5-117">Figure 4-15 shows the basic steps that you usually need to carry out when building a Docker app, followed by detailed descriptions of each step.</span></span>

![](./media/image19.png)

<span data-ttu-id="927e5-118">Figure 4-15 : Flux de travail général pour le cycle de vie pour les applications Docker en conteneur à l’aide de la CLI Docker</span><span class="sxs-lookup"><span data-stu-id="927e5-118">Figure 4-15: High-level workflow for the life cycle for Docker containerized applications using Docker CLI</span></span>

### <a name="step-1-start-coding-in-visual-studio-code-and-create-your-initial-appservice-baseline"></a><span data-ttu-id="927e5-119">Étape 1 : Commencer le codage dans Visual Studio Code et créer votre base de référence de l’application ou du service initial</span><span class="sxs-lookup"><span data-stu-id="927e5-119">Step 1: Start coding in Visual Studio Code and create your initial app/service baseline</span></span>

<span data-ttu-id="927e5-120">Manière de développer votre application est assez similaire à la façon de que procéder sans Docker.</span><span class="sxs-lookup"><span data-stu-id="927e5-120">The way you develop your application is pretty similar to the way you do it without Docker.</span></span> <span data-ttu-id="927e5-121">La différence est que lors du développement, vous déployez et testez l’application ou les services qui s’exécutent dans des conteneurs Docker placés dans votre environnement local (comme un Linux VM ou de Windows).</span><span class="sxs-lookup"><span data-stu-id="927e5-121">The difference is that while developing, you are deploying and testing your application or services running within Docker containers placed in your local environment (like a Linux VM or Windows).</span></span>

<span data-ttu-id="927e5-122">**Configuration de votre environnement local**</span><span class="sxs-lookup"><span data-stu-id="927e5-122">**Setting up your local environment**</span></span>

<span data-ttu-id="927e5-123">Avec les dernières versions de Docker pour Mac et Windows, il est plus facile que jamais pour développer des applications de Docker, et le programme d’installation est simple.</span><span class="sxs-lookup"><span data-stu-id="927e5-123">With the latest versions of Docker for Mac and Windows, it's easier than ever to develop Docker applications, and the setup is straightforward.</span></span>

<span data-ttu-id="927e5-124">**Plus d’informations** pour obtenir des instructions sur la configuration de Docker pour Windows, accédez à [ https://docs.docker.com/docker-for-windows/ ](https://docs.docker.com/docker-for-windows/).</span><span class="sxs-lookup"><span data-stu-id="927e5-124">**More info** For instructions on setting up Docker for Windows, go to [https://docs.docker.com/docker-for-windows/](https://docs.docker.com/docker-for-windows/).</span></span>

<span data-ttu-id="927e5-125">Pour obtenir des instructions sur la configuration Docker pour Mac, accédez à <https://docs.docker.com/docker-for-mac/>.</span><span class="sxs-lookup"><span data-stu-id="927e5-125">For instructions on setting up Docker for Mac, go to <https://docs.docker.com/docker-for-mac/>.</span></span>

<span data-ttu-id="927e5-126">Vous devez en outre, un éditeur de code afin que vous pouvez développer en fait votre application tout en utilisant l’interface CLI Docker.</span><span class="sxs-lookup"><span data-stu-id="927e5-126">In addition, you'll need a code editor so that you can actually develop your application while using Docker CLI.</span></span>

<span data-ttu-id="927e5-127">Microsoft fournit Visual Studio Code, qui est un éditeur de code léger qui est pris en charge sur Mac, Windows et Linux et fournit des fonctionnalités IntelliSense avec [prise en charge de nombreux langages](https://code.visualstudio.com/docs/languages/overview) (JavaScript, .NET, Go, Java, Ruby, Python et la plupart les langages modernes), [débogage](https://code.visualstudio.com/Docs/editor/debugging), [une intégration avec Git](https://code.visualstudio.com/Docs/editor/versioncontrol) et [prise en charge des extensions](https://code.visualstudio.com/docs/extensions/overview).</span><span class="sxs-lookup"><span data-stu-id="927e5-127">Microsoft provides Visual Studio Code, which is a lightweight code editor that is supported on Mac, Windows, and Linux, and provides IntelliSense with [support for many languages](https://code.visualstudio.com/docs/languages/overview) (JavaScript, .NET, Go, Java, Ruby, Python, and most modern languages), [debugging](https://code.visualstudio.com/Docs/editor/debugging), [integration with Git](https://code.visualstudio.com/Docs/editor/versioncontrol) and [extensions support](https://code.visualstudio.com/docs/extensions/overview).</span></span> <span data-ttu-id="927e5-128">Cet éditeur est parfait pour les développeurs Mac et Linux.</span><span class="sxs-lookup"><span data-stu-id="927e5-128">This editor is a great fit for Mac and Linux developers.</span></span> <span data-ttu-id="927e5-129">Dans Windows, vous pouvez également utiliser l’application complète de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="927e5-129">In Windows, you also can use the full Visual Studio application.</span></span>

<span data-ttu-id="927e5-130">**Plus d’informations** pour obtenir des instructions sur l’installation de Visual Studio pour Windows, Mac ou Linux, accédez à <https://code.visualstudio.com/docs/setup/setup-overview/>.</span><span class="sxs-lookup"><span data-stu-id="927e5-130">**More info** For instructions on installing Visual Studio for Windows, Mac, or Linux, go to <https://code.visualstudio.com/docs/setup/setup-overview/>.</span></span>

<span data-ttu-id="927e5-131">Vous pouvez utiliser avec l’interface CLI Docker et écrivez votre code à l’aide de n’importe quel éditeur de code, mais si vous utilisez Visual Studio Code, il est facilement auteur Dockerfile et les fichiers docker-compose.yml dans votre espace de travail.</span><span class="sxs-lookup"><span data-stu-id="927e5-131">You can work with Docker CLI and write your code using any code editor, but if you use Visual Studio Code, it makes it easy to author Dockerfile and docker-compose.yml files in your workspace.</span></span> <span data-ttu-id="927e5-132">En outre, vous pouvez exécuter des tâches de Visual Studio Code à partir de l’IDE qui invite les scripts qui peuvent être en cours d’exécution des opérations élaborées à l’aide de la CLI Docker sous.</span><span class="sxs-lookup"><span data-stu-id="927e5-132">Plus, you can run Visual Studio Code tasks from the IDE that will prompt scripts that can be running elaborated operations using Docker CLI underneath.</span></span>

<span data-ttu-id="927e5-133">Visual Studio Code est fourni par une extension, vous devez installer.</span><span class="sxs-lookup"><span data-stu-id="927e5-133">Visual Studio Code is provided by an extension, which you'll need to install.</span></span> <span data-ttu-id="927e5-134">Pour ce faire, appuyez sur Ctrl + Maj + P, tapez **ext installer**, puis exécutez les Extensions : Installer la commande d’Extension pour afficher la liste des extensions Marketplace.</span><span class="sxs-lookup"><span data-stu-id="927e5-134">To do so, Press Ctrl+Shift+P, type **ext install**, and then run the Extensions: Install Extension command to bring up the Marketplace extension list.</span></span> <span data-ttu-id="927e5-135">Ensuite, tapez **docker** pour filtrer les résultats, puis sélectionnez le fichier Dockerfile et le fichier Docker Compose (yml) extension de prise en charge, comme illustré dans la Figure 4-16.</span><span class="sxs-lookup"><span data-stu-id="927e5-135">Next, type **docker** to filter the results, and then select the Dockerfile And Docker Compose File (yml) Support extension, as depicted in Figure 4-16.</span></span>

![](./media/image20.png)

<span data-ttu-id="927e5-136">Figure 4-16 : L’installation de l’Extension Docker dans Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="927e5-136">Figure 4-16: Installing the Docker Extension in Visual Studio Code</span></span>

### <a name="step-2-create-a-dockerfile-related-to-an-existing-image-plain-os-or-dev-environments-like-net-core-nodejs-and-ruby"></a><span data-ttu-id="927e5-137">Étape 2 : Créer un fichier DockerFile associé à une image existante (système d’exploitation brut ou des environnements de développement tels que .NET Core, Node.js et Ruby)</span><span class="sxs-lookup"><span data-stu-id="927e5-137">Step 2: Create a DockerFile related to an existing image (plain OS or dev environments like .NET Core, Node.js, and Ruby)</span></span>

<span data-ttu-id="927e5-138">Vous devez un fichier DockerFile par une image personnalisée à générer et par conteneur à déployer, par conséquent, si votre application se compose d’un seul service personnalisé, vous devez un fichier DockerFile unique.</span><span class="sxs-lookup"><span data-stu-id="927e5-138">You will need a DockerFile per custom image to be built and per container to be deployed, therefore, if your app is made up of a single custom service, you will need a single DockerFile.</span></span> <span data-ttu-id="927e5-139">Toutefois, si votre application est composée de plusieurs services (comme dans une architecture de microservices), vous devez créer un fichier Dockerfile par service.</span><span class="sxs-lookup"><span data-stu-id="927e5-139">But, if your app is composed of multiple services (as in a microservices architecture), you'll need one Dockerfile per service.</span></span>

<span data-ttu-id="927e5-140">Le fichier DockerFile est généralement placé dans le dossier racine de votre application ou service et contient les commandes requises pour que cette Docker sache comment configurer et exécuter l’application ou le service.</span><span class="sxs-lookup"><span data-stu-id="927e5-140">The DockerFile is usually placed within the root folder of your app or service and contains the required commands so that Docker knows how to set up and run that app or service.</span></span> <span data-ttu-id="927e5-141">Vous pouvez créer votre fichier DockerFile et ajoutez-le à votre projet, ainsi que votre code (node.js, .NET Core, etc.), ou, si vous ne connaissez pas l’environnement, examinons l’info-bulle suivante.</span><span class="sxs-lookup"><span data-stu-id="927e5-141">You can create your DockerFile and add it to your project along with your code (node.js, .NET Core, etc.), or, if you are new to the environment, take a look at the following Tip.</span></span>

> [!TIP]
> <span data-ttu-id="927e5-142">Vous pouvez utiliser un outil de ligne de commande appelé [yo docker](https://github.com/Microsoft/generator-docker), qui structure des fichiers à partir de votre projet dans le langage que vous choisissez et ajoute les fichiers de configuration Docker requis.</span><span class="sxs-lookup"><span data-stu-id="927e5-142">You can use a command-line tool called [yo docker](https://github.com/Microsoft/generator-docker), which scaffolds files from your project in the language you choose and adds the required Docker configuration files.</span></span> <span data-ttu-id="927e5-143">En fait, pour aider les développeurs qui débutent, il crée le fichier DockerFile approprié, docker-compose.yml et autres scripts associés pour générer et exécuter vos conteneurs Docker.</span><span class="sxs-lookup"><span data-stu-id="927e5-143">Basically, to assist developers getting started, it creates the appropriate DockerFile, docker-compose.yml, and other associated scripts to build and run your Docker containers.</span></span> <span data-ttu-id="927e5-144">Ce générateur yeoman vous invitera à quelques questions, vous demandant votre hôte de conteneur de langage et de destination sélectionné de développement.</span><span class="sxs-lookup"><span data-stu-id="927e5-144">This yeoman generator will prompt you with a few questions, asking your selected development language and destination container host.</span></span>

![yo docker](./media/image21.png)

<span data-ttu-id="927e5-146">Par exemple, la Figure 4-17 montre les deux captures d’écran à partir de terminaux dans Windows et sur un Mac, dans les deux cas, en cours d’exécution yo docker, ce qui génère les projets de code échantillon (actuellement .NET Core, Golang et Node.js en tant que langues prises en charge) déjà configurés pour fonctionner sur haut de Docker.</span><span class="sxs-lookup"><span data-stu-id="927e5-146">For instance, Figure 4-17 shows two screenshots from the terminals in Windows and on a Mac, in both cases, running yo docker, which will generate the sample code projects (currently .NET Core, Golang, and Node.js as supported languages) already configured to work on top of Docker.</span></span>

![](./media/image22.PNG)  ![](./media/image23.png)

<span data-ttu-id="927e5-147">Figure 4-17 : yo docker outil de commande dans Windows (à gauche) et sur un Mac</span><span class="sxs-lookup"><span data-stu-id="927e5-147">Figure 4-17: yo docker command tool in Windows (left) and on a Mac</span></span>

<span data-ttu-id="927e5-148">Figure 4-18 présente un exemple à l’aide d’yo docker une fois que vous avez un projet .NET Core existant en place pour être généré automatiquement.</span><span class="sxs-lookup"><span data-stu-id="927e5-148">Figure 4-18 presents an example using yo docker after you have an existing .NET Core project in place to be scaffolded.</span></span>

![](./media/image24.PNG)

<span data-ttu-id="927e5-149">Figure 4-18 : yo docker avec un .NET Core existants du projet en place</span><span class="sxs-lookup"><span data-stu-id="927e5-149">Figure 4-18: yo docker with an existing .NET Core project in place</span></span>

<span data-ttu-id="927e5-150">À partir du fichier DockerFile, vous spécifiez quelle image Docker de base à utiliser (par exemple, à l’aide de « FROM microsoft/dotnet:1.0.0-core »).</span><span class="sxs-lookup"><span data-stu-id="927e5-150">From the DockerFile, you specify what base Docker image you'll be using (like using "FROM microsoft/dotnet:1.0.0-core").</span></span> <span data-ttu-id="927e5-151">Vous allez généralement générer votre image personnalisée sur une image de base que vous pouvez obtenir à partir de n’importe quel dépôt officiel dans le [Registre Docker Hub](https://hub.docker.com/) (comme un [image pour .NET Core](https://hub.docker.com/r/microsoft/dotnet/) ou un [pour Node.js](https://hub.docker.com/_/node/)).</span><span class="sxs-lookup"><span data-stu-id="927e5-151">You usually will build your custom image on top of a base image that you can get from any official repository at the [Docker Hub registry](https://hub.docker.com/) (like an [image for .NET Core](https://hub.docker.com/r/microsoft/dotnet/) or one [for Node.js](https://hub.docker.com/_/node/)).</span></span>

<span data-ttu-id="927e5-152">***Option a : Utilisez une image Docker officielle existante***</span><span class="sxs-lookup"><span data-stu-id="927e5-152">***Option A: Use an existing official Docker image***</span></span>

<span data-ttu-id="927e5-153">À l’aide d’un dépôt officiel de la pile de langage avec un numéro de version garantit que les mêmes fonctionnalités de langage sont disponibles sur toutes les machines (y compris le développement, test et production).</span><span class="sxs-lookup"><span data-stu-id="927e5-153">Using an official repository of a language stack with a version number ensures that the same language features are available on all machines (including development, testing, and production).</span></span>

<span data-ttu-id="927e5-154">Voici un exemple de fichier DockerFile pour un conteneur .NET Core :</span><span class="sxs-lookup"><span data-stu-id="927e5-154">Following is a sample DockerFile for a .NET Core container:</span></span>

```
# Base Docker image to use
FROM microsoft/aspnetcore:1.0.1\

# Set the Working Directory and files to be copied to the image
ARG source
WORKDIR /app
COPY ${source:-bin/Release/PublishOutput} .

# Configure the listening port to 80 (Internal/Secured port within Docker host)
EXPOSE 80

# Application entry point
ENTRYPOINT ["dotnet", "MyCustomMicroservice.dll"]
```

<span data-ttu-id="927e5-155">Dans ce cas, il est à l’aide de la version 1.0.1 de l’image Docker ASP.NET Core officielle pour Linux nommé microsoft/aspnetcore:1.0.1.</span><span class="sxs-lookup"><span data-stu-id="927e5-155">In this case, it is using the version 1.0.1 of the official ASP.NET Core Docker image for Linux named microsoft/aspnetcore:1.0.1.</span></span> <span data-ttu-id="927e5-156">Pour plus d’informations, consultez le [page de l’Image Docker ASP.NET Core](https://hub.docker.com/r/microsoft/aspnetcore/) et [page de l’Image Docker .NET Core](https://hub.docker.com/r/microsoft/dotnet/).</span><span class="sxs-lookup"><span data-stu-id="927e5-156">For further details, consult the [ASP.NET Core Docker Image page](https://hub.docker.com/r/microsoft/aspnetcore/) and the [.NET Core Docker Image page](https://hub.docker.com/r/microsoft/dotnet/).</span></span> <span data-ttu-id="927e5-157">Vous également pouvez utiliser une autre image comparable à nœud : 4-onbuild pour Node.js ou de nombreux autres images préconfigurées pour les langages de développement, qui sont disponibles dans [Docker Hub](https://hub.docker.com/explore/).</span><span class="sxs-lookup"><span data-stu-id="927e5-157">You also could be using another comparable image like node:4-onbuild for Node.js, or many other preconfigured images for development languages, which are available at [Docker Hub](https://hub.docker.com/explore/).</span></span>

<span data-ttu-id="927e5-158">Dans le fichier DockerFile, vous devez également indiquer à Docker d’écouter sur le port TCP que vous utiliserez lors de l’exécution (par exemple, le port 80).</span><span class="sxs-lookup"><span data-stu-id="927e5-158">In the DockerFile, you also need to instruct Docker to listen to the TCP port that you will use at runtime (such as port 80).</span></span>

<span data-ttu-id="927e5-159">Il existe des autres lignes de configuration que vous pouvez ajouter dans le fichier DockerFile en fonction de la langue/infrastructure que vous utilisez, pour que Docker sache comment exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="927e5-159">There are other lines of configuration that you can add in the DockerFile depending on the language/framework you are using, so Docker knows how to run the app.</span></span> <span data-ttu-id="927e5-160">Par exemple, vous devez la ligne ENTRYPOINT avec \[« dotnet », « MyCustomMicroservice.dll »\] pour exécuter une application .NET Core, bien que vous pouvez avoir plusieurs variantes selon l’approche pour générer et exécuter votre service.</span><span class="sxs-lookup"><span data-stu-id="927e5-160">For instance, you need the ENTRYPOINT line with \["dotnet", "MyCustomMicroservice.dll"\] to run a .NET Core app, although you can have multiple variants depending on the approach to build and run your service.</span></span> <span data-ttu-id="927e5-161">Si vous utilisez le Kit de développement logiciel et l’interface CLI dotnet pour générer et exécuter l’application .NET, il serait légèrement différente.</span><span class="sxs-lookup"><span data-stu-id="927e5-161">If you're using the SDK and dotnet CLI to build and run the .NET app, it would be slightly different.</span></span> <span data-ttu-id="927e5-162">L’essentiel est que la ligne ENTRYPOINT ainsi que des lignes supplémentaires sera différents selon la langue/plateforme que vous choisissez pour votre application.</span><span class="sxs-lookup"><span data-stu-id="927e5-162">The bottom line is that the ENTRYPOINT line plus additional lines will be different depending on the language/platform you choose for your application.</span></span>

<span data-ttu-id="927e5-163">**Plus d’informations** pour plus d’informations sur la création d’images Docker pour les applications .NET Core, accédez à <https://docs.microsoft.com/dotnet/core/docker/building-net-docker-images>.</span><span class="sxs-lookup"><span data-stu-id="927e5-163">**More info** For information about building Docker images for .NET Core applications, go to <https://docs.microsoft.com/dotnet/core/docker/building-net-docker-images>.</span></span>

<span data-ttu-id="927e5-164">Pour en savoir plus sur la création de vos propres images, accédez à [ https://docs.docker.com/engine/\ didacticiels/dockerimages/](https://docs.docker.com/engine/tutorials/dockerimages/).</span><span class="sxs-lookup"><span data-stu-id="927e5-164">To learn more about building your own images, go to [https://docs.docker.com/engine/\ tutorials/dockerimages/](https://docs.docker.com/engine/tutorials/dockerimages/).</span></span>

<span data-ttu-id="927e5-165">**Référentiels d’images multi-plateformes**</span><span class="sxs-lookup"><span data-stu-id="927e5-165">**Multiplatform image repositories**</span></span>

<span data-ttu-id="927e5-166">Comme les conteneurs Windows deviennent de plus en plus répandus, un référentiel unique peut contenir des variantes de plateforme, comme une image Linux et Windows.</span><span class="sxs-lookup"><span data-stu-id="927e5-166">As Windows containers become more prevalent, a single repository can contain platform variants, such as a Linux and Windows image.</span></span> <span data-ttu-id="927e5-167">Il s’agit d’une nouvelle fonctionnalité proposée dans Docker qui rend possible pour les fournisseurs d’utiliser un référentiel unique pour couvrir plusieurs plateformes, telles que [microsoft/aspdotnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) référentiel, ce qui est disponible sur le Registre DockerHub.</span><span class="sxs-lookup"><span data-stu-id="927e5-167">This is a new feature coming in Docker that makes it possible for vendors to use a single repository to cover multiple platforms, such as [microsoft/aspdotnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) repository, which is available at DockerHub registry.</span></span> <span data-ttu-id="927e5-168">Comme la fonctionnalité entre Active, extraction de cette image à partir d’un ordinateur hôte Windows extraira la variante de Windows, tandis que l’extraction du même nom d’image à partir d’un hôte Linux extraira la variante Linux.</span><span class="sxs-lookup"><span data-stu-id="927e5-168">As the feature comes alive, pulling this image from a Windows host will pull the Windows variant, whereas pulling the same image name from a Linux host will pull the Linux variant.</span></span>

<span data-ttu-id="927e5-169">***Option b : Créer votre image de base à partir de zéro***</span><span class="sxs-lookup"><span data-stu-id="927e5-169">***Option B: Create your base image from scratch***</span></span>

<span data-ttu-id="927e5-170">Vous pouvez créer votre propre image de base de Docker à partir de zéro, comme expliqué dans cet [article](https://docs.docker.com/engine/userguide/eng-image/baseimages/) à partir de Docker.</span><span class="sxs-lookup"><span data-stu-id="927e5-170">You can create your own Docker base image from scratch as explained in this [article](https://docs.docker.com/engine/userguide/eng-image/baseimages/) from Docker.</span></span> <span data-ttu-id="927e5-171">Il s’agit d’un scénario qui n’est probablement pas vous convient le mieux si vous débutez avec Docker, mais si vous souhaitez définir les bits spécifiques de votre propre image de base, vous pouvez le faire.</span><span class="sxs-lookup"><span data-stu-id="927e5-171">This is a scenario that is probably not best for you if you are just starting with Docker, but if you want to set the specific bits of your own base image, you can do it.</span></span>

### <a name="step-3-create-your-custom-docker-images-embedding-your-service-in-it"></a><span data-ttu-id="927e5-172">Étape 3 : Créer votre l’incorporation de votre service qu’il contient des images Docker personnalisées</span><span class="sxs-lookup"><span data-stu-id="927e5-172">Step 3: Create your custom Docker images embedding your service in it</span></span>

<span data-ttu-id="927e5-173">Pour chaque service personnalisé qui compose votre application, vous devez créer une image associée.</span><span class="sxs-lookup"><span data-stu-id="927e5-173">For each custom service that comprises your app, you'll need to create a related image.</span></span> <span data-ttu-id="927e5-174">Si votre application est composée d’un service unique ou d’application web, vous aurez besoin en une seule image.</span><span class="sxs-lookup"><span data-stu-id="927e5-174">If your app is made up of a single service or web app, you'll need just a single image.</span></span>

> [!NOTE]
> <span data-ttu-id="927e5-175">Lorsque prenant en compte la « boucle externe flux de travail DevOps », les images seront créés par un processus de génération automatisé dès que vous ajoutez votre code source à un référentiel Git (intégration continue) pour les images sont créées dans cet environnement global à partir de votre code source.</span><span class="sxs-lookup"><span data-stu-id="927e5-175">When taking into account the "outer-loop DevOps workflow," the images will be created by an automated build process whenever you push your source code to a Git repository (Continuous Integration) so the images will be created in that global environment from your source code.</span></span>

<span data-ttu-id="927e5-176">Toutefois, avant de nous estimons qu’accédant à cet itinéraire de la boucle externe, nous devons vérifier que l’application Docker réellement fonctionne correctement afin qu’ils n’est pas envoyé de code qui peut ne pas fonctionne correctement pour le système de contrôle de code source (Git, etc.).</span><span class="sxs-lookup"><span data-stu-id="927e5-176">But, before we consider going to that outer-loop route, we need to ensure that the Docker application is actually working properly so that they don't push code that might not work properly to the source control system (Git, etc.).</span></span>

<span data-ttu-id="927e5-177">Par conséquent, chaque développeur doit d’abord faire tout le processus de boucle interne pour tester localement et continuer à développer jusqu'à ce qu’ils souhaitent push d’une fonctionnalité complète ou de modifier le système de contrôle source.</span><span class="sxs-lookup"><span data-stu-id="927e5-177">Therefore, each developer first needs to do the entire inner-loop process to test locally and continue developing until they want to push a complete feature or change to the source control system.</span></span>

<span data-ttu-id="927e5-178">Pour créer une image dans votre environnement local et à l’aide du fichier DockerFile, vous pouvez utiliser la commande docker build, comme illustré dans la Figure 4-19 (vous pouvez également exécuter docker-compose up--build pour les applications composées de plusieurs conteneurs/Services).</span><span class="sxs-lookup"><span data-stu-id="927e5-178">To create an image in your local environment and using the DockerFile, you can use the docker build command, as demonstrated in Figure 4-19 (you also can run docker-compose up --build for applications composed by several containers/services).</span></span>

![](./media/image25.png)

<span data-ttu-id="927e5-179">Figure 4-19 : Build de docker en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="927e5-179">Figure 4-19: Running docker build</span></span>

<span data-ttu-id="927e5-180">Si vous le souhaitez, au lieu d’exécuter directement docker build à partir du dossier du projet, vous pouvez tout d’abord créer un dossier déployable avec les bibliothèques .NET nécessaires à l’aide de l’exécution dotnet commande publish, et puis exécutez build de docker.</span><span class="sxs-lookup"><span data-stu-id="927e5-180">Optionally, instead of directly running docker build from the project's folder, you first can generate a deployable folder with the .NET libraries needed by using the run dotnet publish command, and then run docker build.</span></span>

<span data-ttu-id="927e5-181">Dans cet exemple, cela crée une image Docker avec le nom cesardl/netcore-webapi-microservice-docker : first ( : tout d’abord est une balise, comme une version spécifique).</span><span class="sxs-lookup"><span data-stu-id="927e5-181">In this example, this creates a Docker image with the name cesardl/netcore-webapi-microservice-docker:first (:first is a tag, like a specific version).</span></span> <span data-ttu-id="927e5-182">Vous pouvez effectuer cette étape pour chaque image personnalisée que vous créez pour votre application Docker composée avec plusieurs conteneurs.</span><span class="sxs-lookup"><span data-stu-id="927e5-182">You can take this step for each custom image you need to create for your composed Docker application with several containers.</span></span>

<span data-ttu-id="927e5-183">Vous trouverez les images existantes dans votre référentiel local (votre ordinateur de développement) à l’aide de docker commande images, comme illustré dans la Figure 4-20.</span><span class="sxs-lookup"><span data-stu-id="927e5-183">You can find the existing images in your local repository (your development machine) by using the docker images command, as illustrated in Figure 4-20.</span></span>

![](./media/image26.png)

<span data-ttu-id="927e5-184">Figure 4-20 : Affichage des images existantes à l’aide d’images docker</span><span class="sxs-lookup"><span data-stu-id="927e5-184">Figure 4-20: Viewing existing images using docker images</span></span>

### <a name="step-4-optional-define-your-services-in-docker-composeyml-when-building-a-composed-docker-app-with-multiple-services"></a><span data-ttu-id="927e5-185">Étape 4 : (Facultatif) Définir vos services dans docker-compose.yml lors de la création d’une application Docker composée avec plusieurs services</span><span class="sxs-lookup"><span data-stu-id="927e5-185">Step 4: (Optional) Define your services in docker-compose.yml when building a composed Docker app with multiple services</span></span>

<span data-ttu-id="927e5-186">Avec le fichier docker-compose.yml, vous pouvez définir un ensemble de services à être déployé comme une application composée avec les commandes de déploiement expliqués dans la section étape suivante.</span><span class="sxs-lookup"><span data-stu-id="927e5-186">With the docker-compose.yml file you can define a set of related services to be deployed as a composed application with the deployment commands explained in the next step section.</span></span>

<span data-ttu-id="927e5-187">Vous devez créer ce fichier dans votre main ou un dossier de solution racine ; Il doit avoir un contenu similaire dans le fichier docker-compose.yml suivant :</span><span class="sxs-lookup"><span data-stu-id="927e5-187">You need to create that file in your main or root solution folder; it should have a similar content to the following docker-compose.yml file:</span></span>

```yml
version: '2'
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

<span data-ttu-id="927e5-188">Dans ce cas particulier, ce fichier définit deux services : le service web (votre service personnalisé) et le service redis (un service de cache bien connu).</span><span class="sxs-lookup"><span data-stu-id="927e5-188">In this particular case, this file defines two services: the web service (your custom service) and the redis service (a popular cache service).</span></span> <span data-ttu-id="927e5-189">Chaque service sera déployé en tant que conteneur, nous devons utiliser une image Docker concrete pour chacun.</span><span class="sxs-lookup"><span data-stu-id="927e5-189">Each service will be deployed as a container, so we need to use a concrete Docker image for each.</span></span> <span data-ttu-id="927e5-190">Pour ce service web particulier, l’image doit effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="927e5-190">For this particular web service, the image will need to do the following:</span></span>

-   <span data-ttu-id="927e5-191">Construire à partir du fichier DockerFile dans le répertoire actif</span><span class="sxs-lookup"><span data-stu-id="927e5-191">Build from the DockerFile in the current directory</span></span>

-   <span data-ttu-id="927e5-192">Transférer le port exposé 80 sur le conteneur sur le port 81 sur l’ordinateur hôte</span><span class="sxs-lookup"><span data-stu-id="927e5-192">Forward the exposed port 80 on the container to port 81 on the host machine</span></span>

-   <span data-ttu-id="927e5-193">Monter le répertoire du projet sur l’ordinateur hôte/code au sein du conteneur, ce qui permet de modifier le code sans avoir à recréer l’image</span><span class="sxs-lookup"><span data-stu-id="927e5-193">Mount the project directory on the host to /code within the container, making it possible for you to modify the code without having to rebuild the image</span></span>

-   <span data-ttu-id="927e5-194">Lier le service web au service redis</span><span class="sxs-lookup"><span data-stu-id="927e5-194">Link the web service to the redis service</span></span>

<span data-ttu-id="927e5-195">Le service redis utilise le [dernière image publique redis](https://hub.docker.com/_/redis/) extraite du Registre Docker Hub.</span><span class="sxs-lookup"><span data-stu-id="927e5-195">The redis service uses the [latest public redis image](https://hub.docker.com/_/redis/) pulled from the Docker Hub registry.</span></span> <span data-ttu-id="927e5-196">[redis](https://redis.io/) est un système de cache très populaire pour les applications côté serveur.</span><span class="sxs-lookup"><span data-stu-id="927e5-196">[redis](https://redis.io/) is a very popular cache system for server-side applications.</span></span>

### <a name="step-5-build-and-run-your-docker-app"></a><span data-ttu-id="927e5-197">Étape 5 : Générer et exécuter votre application Docker</span><span class="sxs-lookup"><span data-stu-id="927e5-197">Step 5: Build and run your Docker app</span></span>

<span data-ttu-id="927e5-198">Si votre application a uniquement un seul conteneur, vous devez l’exécuter en la déployant sur votre hôte Docker (machine virtuelle ou serveur physique).</span><span class="sxs-lookup"><span data-stu-id="927e5-198">If your app has only a single container, you just need to run it by deploying it to your Docker Host (VM or physical server).</span></span> <span data-ttu-id="927e5-199">Toutefois, si votre application est composée de plusieurs services, vous devez *composer*, trop.</span><span class="sxs-lookup"><span data-stu-id="927e5-199">However, if your app is made up of multiple services, you need to *compose it*, too.</span></span> <span data-ttu-id="927e5-200">Nous allons voir les différentes options.</span><span class="sxs-lookup"><span data-stu-id="927e5-200">Let's see the different options.</span></span>

<span data-ttu-id="927e5-201">***Option a : Exécuter un conteneur unique ou un service***</span><span class="sxs-lookup"><span data-stu-id="927e5-201">***Option A: Run a single container or service***</span></span>

<span data-ttu-id="927e5-202">Vous pouvez exécuter l’image Docker à l’aide de la commande docker run, comme illustré ici :</span><span class="sxs-lookup"><span data-stu-id="927e5-202">You can run the Docker image by using the docker run command, as shown here:</span></span>

```
docker run -t -d -p 80:5000
cesardl/netcore-webapi-microservice-docker:first
```

<span data-ttu-id="927e5-203">Notez que pour ce déploiement, nous allons être redirection des demandes envoyées vers le port 80 vers le port interne 5000.</span><span class="sxs-lookup"><span data-stu-id="927e5-203">Note that for this particular deployment, we'll be redirecting requests sent to port 80 to the internal port 5000.</span></span> <span data-ttu-id="927e5-204">À présent, l’application est à l’écoute sur le port externe 80 au niveau de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="927e5-204">Now, the application is listening on the external port 80 at the host level.</span></span>

<span data-ttu-id="927e5-205">***Option b : Composer et exécuter une application de plusieurs conteneurs***</span><span class="sxs-lookup"><span data-stu-id="927e5-205">***Option B: Compose and run a multiple-container application***</span></span>

<span data-ttu-id="927e5-206">Dans la plupart des scénarios d’entreprise, une application Docker est composée de plusieurs services.</span><span class="sxs-lookup"><span data-stu-id="927e5-206">In most enterprise scenarios, a Docker application will be composed of multiple services.</span></span> <span data-ttu-id="927e5-207">Dans ce cas, vous pouvez exécuter la commande docker-compose haut (Figure 4-21), qui utilisera le fichier docker-compose.yml que vous avez peut-être créé précédemment.</span><span class="sxs-lookup"><span data-stu-id="927e5-207">For these cases, you can run the command docker-compose up (Figure 4-21), which will use the docker-compose.yml file that you might have created previously.</span></span> <span data-ttu-id="927e5-208">Exécution de cette commande déploie une application composée avec toutes ses conteneurs associés.</span><span class="sxs-lookup"><span data-stu-id="927e5-208">Running this command deploys a composed application with all of its related containers.</span></span>

![](./media/image27.png)

<span data-ttu-id="927e5-209">Figure 4-21 : Résultats de l’exécution de la commande « docker-compose up »</span><span class="sxs-lookup"><span data-stu-id="927e5-209">Figure 4-21: Results of running the "docker-compose up" command</span></span>

<span data-ttu-id="927e5-210">Après avoir exécuté docker-compose haut, vous déployez votre application et ses conteneurs associés sur votre hôte Docker, comme illustré dans la Figure 4-22, dans la représentation sous forme de machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="927e5-210">After you run docker-compose up, you deploy your application and its related container(s) into your Docker Host, as illustrated in Figure 4-22, in the VM representation.</span></span>

![](./media/image28.png)

<span data-ttu-id="927e5-211">Figure 4-22 : Machine virtuelle avec des conteneurs Docker déployés</span><span class="sxs-lookup"><span data-stu-id="927e5-211">Figure 4-22: VM with Docker containers deployed</span></span>

<span data-ttu-id="927e5-212">Remarque docker compose haut et docker exécuter peut être suffisant pour le test de vos conteneurs dans votre environnement de développement, mais vous ne pouvez pas les utiliser du tout si vous prévoyez d’utiliser des clusters Docker et orchestrateurs tels que Docker Swarm, Mesosphere DC/OS ou Kubernetes pour être en mesure de monter en puissance.</span><span class="sxs-lookup"><span data-stu-id="927e5-212">Note docker-compose up and docker run might be enough for testing your containers in your development environment, but you might not use them at all if you are expecting to work with Docker clusters and orchestrators like Docker Swarm, Mesosphere DC/OS, or Kubernetes in order to be able to scale up.</span></span> <span data-ttu-id="927e5-213">Si vous utilisez un cluster comme [mode Docker Swarm](https://docs.docker.com/engine/swarm/) (disponible dans Docker pour Windows et Mac depuis la version 1.12), vous devez déployer et tester avec des commandes supplémentaires telles que la création du service de docker pour des services uniques, ou lorsque vous êtes déploiement d’une application composée de plusieurs conteneurs, à l’aide de docker compose bundle et docker déployer myBundleFile, en déployant l’application composée comme une pile, comme expliqué dans l’article [Distributed Application Bundles](https://blog.docker.com/2016/06/docker-app-bundle/) à partir de Docker.</span><span class="sxs-lookup"><span data-stu-id="927e5-213">If you're using a cluster like [Docker Swarm mode](https://docs.docker.com/engine/swarm/) (available in Docker for Windows and Mac since version 1.12), you need to deploy and test with additional commands such as docker service create for single services, or when you're deploying an app composed of several containers, using docker compose bundle and docker deploy myBundleFile, by deploying the composed app as a stack, as explained in the article [Distributed Application Bundles](https://blog.docker.com/2016/06/docker-app-bundle/) from Docker.</span></span>

<span data-ttu-id="927e5-214">Pour [DC/OS](https://mesosphere.com/blog/2015/09/02/dcos-cli-command-line-tool-datacenter/) et [Kubernetes](https://kubernetes.io/docs/user-guide/deployments/#creating-a-deployment) vous utiliseriez les commandes de déploiement différents et des scripts, également.</span><span class="sxs-lookup"><span data-stu-id="927e5-214">For [DC/OS](https://mesosphere.com/blog/2015/09/02/dcos-cli-command-line-tool-datacenter/) and [Kubernetes](https://kubernetes.io/docs/user-guide/deployments/#creating-a-deployment) you would use different deployment commands and scripts, as well.</span></span>

### <a name="step-6-test-your-docker-application-locally-in-your-local-cd-vm"></a><span data-ttu-id="927e5-215">Étape 6 : Tester votre application Docker (local, dans votre machine virtuelle de CD locale)</span><span class="sxs-lookup"><span data-stu-id="927e5-215">Step 6: Test your Docker application (locally, in your local CD VM)</span></span>

<span data-ttu-id="927e5-216">Cette étape varie en fonction de ce que fait votre application.</span><span class="sxs-lookup"><span data-stu-id="927e5-216">This step will vary depending on what your app is doing.</span></span>

<span data-ttu-id="927e5-217">Dans une très simple .NET Core API Web « Hello World » déployé comme un seul conteneur ou un service, vous devez simplement accéder au service en fournissant le port TCP spécifié dans le fichier DockerFile.</span><span class="sxs-lookup"><span data-stu-id="927e5-217">In a very simple .NET Core Web API "Hello World" deployed as a single container or service, you'd just need to access the service by providing the TCP port specified in the DockerFile.</span></span>

<span data-ttu-id="927e5-218">Si localhost est désactivée, pour accéder à votre service, vous pouvez trouver l’adresse IP de l’ordinateur à l’aide de cette commande :</span><span class="sxs-lookup"><span data-stu-id="927e5-218">If localhost is not turned on, to navigate to your service, find the IP address for the machine by using this command:</span></span>

<span data-ttu-id="927e5-219">docker-machine ip *votre nom de conteneur*</span><span class="sxs-lookup"><span data-stu-id="927e5-219">docker-machine ip *your-container-name*</span></span>

<span data-ttu-id="927e5-220">Sur l’hôte Docker, ouvrez un navigateur et accédez à ce site ; Vous devez voir votre application ou du service en cours d’exécution, comme illustré dans la Figure 4-23.</span><span class="sxs-lookup"><span data-stu-id="927e5-220">On the Docker host, open a browser and navigate to that site; you should see your app/service running, as demonstrated in Figure 4-23.</span></span>

![](./media/image29.png)

<span data-ttu-id="927e5-221">Figure 4-23 : Test de votre application Docker localement en utilisant localhost</span><span class="sxs-lookup"><span data-stu-id="927e5-221">Figure 4-23: Testing your Docker application locally using localhost</span></span>

<span data-ttu-id="927e5-222">Notez qu’il utilise le port 80, mais en interne qu’il a été redirigée vers le port 5000, parce que c’est la façon dont elle a été déployée avec docker run, comme expliqué précédemment.</span><span class="sxs-lookup"><span data-stu-id="927e5-222">Note that it is using port 80, but internally it was being redirected to port 5000, because that's how it was deployed with docker run, as explained earlier.</span></span>

<span data-ttu-id="927e5-223">Vous pouvez tester cela à l’aide de CURL à partir du terminal.</span><span class="sxs-lookup"><span data-stu-id="927e5-223">You can test this by using CURL from the terminal.</span></span> <span data-ttu-id="927e5-224">Dans une installation de Docker sur Windows, l’adresse IP par défaut est 10.0.75.1, comme illustré dans la Figure 4-24.</span><span class="sxs-lookup"><span data-stu-id="927e5-224">In a Docker installation on Windows, the default IP is 10.0.75.1, as depicted in Figure 4-24.</span></span>

![](./media/image30.png)

<span data-ttu-id="927e5-225">Figure 4-24 : Test d’une application de Docker localement à l’aide de CURL</span><span class="sxs-lookup"><span data-stu-id="927e5-225">Figure 4-24: Testing a Docker application locally by using CURL</span></span>

<span data-ttu-id="927e5-226">**Débogage d’un conteneur en cours d’exécution sur Docker**</span><span class="sxs-lookup"><span data-stu-id="927e5-226">**Debugging a container running on Docker**</span></span>

<span data-ttu-id="927e5-227">Visual Studio Code prend en charge le débogage Docker si vous utilisez Node.js et autres plateformes telles que les conteneurs .NET Core.</span><span class="sxs-lookup"><span data-stu-id="927e5-227">Visual Studio Code supports debugging Docker if you're using Node.js and other platforms like .NET Core containers.</span></span>

<span data-ttu-id="927e5-228">Vous également pouvez déboguer les conteneurs .NET Core dans Docker lors de l’utilisation de Visual Studio, comme décrit dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="927e5-228">You also can debug .NET Core containers in Docker when using Visual Studio, as described in the next section.</span></span>

<span data-ttu-id="927e5-229">**Plus d’informations :** pour en savoir plus sur le débogage des conteneurs Docker de Node.js, accédez à <https://blog.docker.com/2016/07/live-debugging-docker/> et [ https://blogs.msdn.microsoft.com/\ utilisateur\_ed/2016/02/27 / Visual-Studio-code-New-Features-13-Big-Debugging-Updates-Rich-Object-Hover-Conditional-Breakpoints-Node-js-mono-more/](https://blogs.msdn.microsoft.com/user_ed/2016/02/27/visual-studio-code-new-features-13-big-debugging-updates-rich-object-hover-conditional-breakpoints-node-js-mono-more/).</span><span class="sxs-lookup"><span data-stu-id="927e5-229">**More info:** To learn more about debugging Node.js Docker containers, go to <https://blog.docker.com/2016/07/live-debugging-docker/> and [https://blogs.msdn.microsoft.com/\ user\_ed/2016/02/27/visual-studio-code-new-features-13-big-debugging-updates-rich-object-hover-conditional-breakpoints-node-js-mono-more/](https://blogs.msdn.microsoft.com/user_ed/2016/02/27/visual-studio-code-new-features-13-big-debugging-updates-rich-object-hover-conditional-breakpoints-node-js-mono-more/).</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="927e5-230">[Précédent](docker-apps-development-environment.md)
>[Suivant](visual-studio-tools-for-docker.md)</span><span class="sxs-lookup"><span data-stu-id="927e5-230">[Previous](docker-apps-development-environment.md)
[Next](visual-studio-tools-for-docker.md)</span></span>