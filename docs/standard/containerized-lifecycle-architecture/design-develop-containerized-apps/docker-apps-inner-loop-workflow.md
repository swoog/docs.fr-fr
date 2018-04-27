---
title: Flux de travail de développement de la boucle interne pour les applications de Docker
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
ms.prod: .net
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.topic: article
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 8ee1918091fe72e8606be6e7503ecd850084a4ba
ms.sourcegitcommit: 2e8acae16ae802f2d6d04e3ce0a6dbf04e476513
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2018
---
# <a name="inner-loop-development-workflow-for-docker-apps"></a><span data-ttu-id="c9728-103">Flux de travail de développement de la boucle interne pour les applications de Docker</span><span class="sxs-lookup"><span data-stu-id="c9728-103">Inner-loop development workflow for Docker apps</span></span>

<span data-ttu-id="c9728-104">Avant de déclencher le flux de travail de boucle externe couvrant l’ensemble DevOps cycle, tout commence sur l’ordinateur de chaque développeur, le codage de l’application elle-même, à l’aide de leurs langues par défaut ou les plateformes et de le tester localement la (Figure 4-14).</span><span class="sxs-lookup"><span data-stu-id="c9728-104">Before triggering the outer-loop workflow spanning the entire DevOps cycle, it all begins on each developer's machine, coding the app itself, using their preferred languages or platforms, and testing it locally (Figure 4-14).</span></span> <span data-ttu-id="c9728-105">Mais dans tous les cas, vous aurez un point très important, en commun, quel que soit le langage, framework ou plateformes que vous choisissez.</span><span class="sxs-lookup"><span data-stu-id="c9728-105">But in every case, you will have a very important point in common, no matter what language, framework, or platforms you choose.</span></span> <span data-ttu-id="c9728-106">Dans ce flux de travail spécifique, vous toujours développez et testez les conteneurs Docker, mais localement.</span><span class="sxs-lookup"><span data-stu-id="c9728-106">In this specific workflow, you are always developing and testing Docker containers, but locally.</span></span>

![](./media/image18.png)

<span data-ttu-id="c9728-107">Contexte de développement de la boucle interne de la figure 4-14 :</span><span class="sxs-lookup"><span data-stu-id="c9728-107">Figure 4-14: Inner-loop development context</span></span>

<span data-ttu-id="c9728-108">Le conteneur ou l’instance d’une image Docker contiendra ces composants :</span><span class="sxs-lookup"><span data-stu-id="c9728-108">The container or instance of a Docker image will contain these components:</span></span>

-   <span data-ttu-id="c9728-109">Une sélection de système d’exploitation (par exemple, une distribution Linux ou Windows)</span><span class="sxs-lookup"><span data-stu-id="c9728-109">An operating system selection (for example, a Linux distribution or Windows)</span></span>

-   <span data-ttu-id="c9728-110">Fichiers ajoutés par le développeur (par exemple, les binaires d’application)</span><span class="sxs-lookup"><span data-stu-id="c9728-110">Files added by the developer (for example, app binaries)</span></span>

-   <span data-ttu-id="c9728-111">Configuration (par exemple, les paramètres d’environnement et les dépendances)</span><span class="sxs-lookup"><span data-stu-id="c9728-111">Configuration (for example, environment settings and dependencies)</span></span>

-   <span data-ttu-id="c9728-112">Instructions pour les processus à exécuter par Docker</span><span class="sxs-lookup"><span data-stu-id="c9728-112">Instructions for what processes to run by Docker</span></span>

<span data-ttu-id="c9728-113">Vous pouvez configurer le flux de travail de développement de la boucle interne qui utilise des Docker en tant que le processus (décrit dans la section suivante).</span><span class="sxs-lookup"><span data-stu-id="c9728-113">You can set up the inner-loop development workflow that utilizes Docker as the process (described in the next section).</span></span> <span data-ttu-id="c9728-114">Prendre en compte que les premières étapes pour configurer l’environnement n’est pas inclus, car vous devez le faire une seule fois.</span><span class="sxs-lookup"><span data-stu-id="c9728-114">Take into account that the initial steps to set up the environment is not included, because you need to do that just once.</span></span>

## <a name="building-a-single-app-within-a-docker-container-using-visual-studio-code-and-docker-cli"></a><span data-ttu-id="c9728-115">Création d’une application unique dans un conteneur Docker à l’aide de Code Visual Studio et l’interface CLI de Docker</span><span class="sxs-lookup"><span data-stu-id="c9728-115">Building a single app within a Docker container using Visual Studio Code and Docker CLI</span></span>

<span data-ttu-id="c9728-116">Les applications sont constituées à partir de vos propres services ainsi que des bibliothèques supplémentaires (dépendances).</span><span class="sxs-lookup"><span data-stu-id="c9728-116">Apps are made up from your own services plus additional libraries (dependencies).</span></span>

<span data-ttu-id="c9728-117">Figure 4-15 montre les étapes de base que vous devez généralement exécuter lors de la création d’une application de Docker, suivie d’une description détaillée de chaque étape.</span><span class="sxs-lookup"><span data-stu-id="c9728-117">Figure 4-15 shows the basic steps that you usually need to carry out when building a Docker app, followed by detailed descriptions of each step.</span></span>

![](./media/image19.png)

<span data-ttu-id="c9728-118">Figure 4-15 : les flux de haut niveau pour le cycle de vie des applications de Docker placées dans des conteneurs à l’aide de Docker CLI</span><span class="sxs-lookup"><span data-stu-id="c9728-118">Figure 4-15: High-level workflow for the life cycle for Docker containerized applications using Docker CLI</span></span>

### <a name="step-1-start-coding-in-visual-studio-code-and-create-your-initial-appservice-baseline"></a><span data-ttu-id="c9728-119">Étape 1 : Commencer à coder dans le Code de Visual Studio et créez votre ligne de base initiale du service d’applications /</span><span class="sxs-lookup"><span data-stu-id="c9728-119">Step 1: Start coding in Visual Studio Code and create your initial app/service baseline</span></span>

<span data-ttu-id="c9728-120">La méthode de développement de votre application est très similaire à la façon dont vous le faire sans Docker.</span><span class="sxs-lookup"><span data-stu-id="c9728-120">The way you develop your application is pretty similar to the way you do it without Docker.</span></span> <span data-ttu-id="c9728-121">La différence est que lors du développement, vous déployez et testez votre application ou les services qui s’exécutent dans des conteneurs Docker placés dans votre environnement local (comme une Linux VM ou de Windows).</span><span class="sxs-lookup"><span data-stu-id="c9728-121">The difference is that while developing, you are deploying and testing your application or services running within Docker containers placed in your local environment (like a Linux VM or Windows).</span></span>

<span data-ttu-id="c9728-122">**Configuration de votre environnement local**</span><span class="sxs-lookup"><span data-stu-id="c9728-122">**Setting up your local environment**</span></span>

<span data-ttu-id="c9728-123">Avec les versions plus récentes de Docker pour Mac et Windows, il est plus facile que jamais à développer des applications de Docker, et le programme d’installation est simple.</span><span class="sxs-lookup"><span data-stu-id="c9728-123">With the latest versions of Docker for Mac and Windows, it's easier than ever to develop Docker applications, and the setup is straightforward.</span></span>

<span data-ttu-id="c9728-124">**Plus d’informations** pour obtenir des instructions sur la configuration de Docker pour Windows, accédez à [ https://docs.docker.com/docker-for-windows/ ](https://docs.docker.com/docker-for-windows/).</span><span class="sxs-lookup"><span data-stu-id="c9728-124">**More info** For instructions on setting up Docker for Windows, go to [https://docs.docker.com/docker-for-windows/](https://docs.docker.com/docker-for-windows/).</span></span>

<span data-ttu-id="c9728-125">Pour obtenir des instructions sur la configuration de Docker pour Mac, accédez à <https://docs.docker.com/docker-for-mac/>.</span><span class="sxs-lookup"><span data-stu-id="c9728-125">For instructions on setting up Docker for Mac, go to <https://docs.docker.com/docker-for-mac/>.</span></span>

<span data-ttu-id="c9728-126">Vous devez en outre, un éditeur de code afin que vous pouvez développer effectivement de votre application lors de l’utilisation de Docker CLI.</span><span class="sxs-lookup"><span data-stu-id="c9728-126">In addition, you'll need a code editor so that you can actually develop your application while using Docker CLI.</span></span>

<span data-ttu-id="c9728-127">Microsoft fournit le Code de Visual Studio, qui est un éditeur de code léger qui est pris en charge sur Windows, Mac et Linux et fournit la fonctionnalité IntelliSense avec [prise en charge de nombreux langages](https://code.visualstudio.com/docs/languages/overview) (JavaScript, .NET, Go, Java, Ruby, Python et la plupart les langages modernes), [débogage](https://code.visualstudio.com/Docs/editor/debugging), [integration avec Git](https://code.visualstudio.com/Docs/editor/versioncontrol) et [prise en charge des extensions](https://code.visualstudio.com/docs/extensions/overview).</span><span class="sxs-lookup"><span data-stu-id="c9728-127">Microsoft provides Visual Studio Code, which is a lightweight code editor that is supported on Mac, Windows, and Linux, and provides IntelliSense with [support for many languages](https://code.visualstudio.com/docs/languages/overview) (JavaScript, .NET, Go, Java, Ruby, Python, and most modern languages), [debugging](https://code.visualstudio.com/Docs/editor/debugging), [integration with Git](https://code.visualstudio.com/Docs/editor/versioncontrol) and [extensions support](https://code.visualstudio.com/docs/extensions/overview).</span></span> <span data-ttu-id="c9728-128">Cet éditeur est parfait pour les développeurs Mac et Linux.</span><span class="sxs-lookup"><span data-stu-id="c9728-128">This editor is a great fit for Mac and Linux developers.</span></span> <span data-ttu-id="c9728-129">Dans Windows, vous pouvez également utiliser l’application complète de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c9728-129">In Windows, you also can use the full Visual Studio application.</span></span>

<span data-ttu-id="c9728-130">**Plus d’informations** pour obtenir des instructions sur l’installation de Visual Studio pour Windows, Mac ou Linux, accédez à [ http://code.visualstudio.com/docs/setup/setup-overview/https://docs.docker.com/docker-for-mac/ ](http://code.visualstudio.com/docs/setup/setup-overview/https:/docs.docker.com/docker-for-mac/).</span><span class="sxs-lookup"><span data-stu-id="c9728-130">**More info** For instructions on installing Visual Studio for Windows, Mac, or Linux, go to [http://code.visualstudio.com/docs/setup/setup-overview/https://docs.docker.com/docker-for-mac/](http://code.visualstudio.com/docs/setup/setup-overview/https:/docs.docker.com/docker-for-mac/).</span></span>

<span data-ttu-id="c9728-131">Vous pouvez utiliser avec l’interface CLI de Docker et écrire votre code à l’aide de n’importe quel éditeur de code, mais si vous utilisez Visual Studio Code, il rend faciles à l’auteur du fichier Dockerfile et docker-compose.yml fichiers dans votre espace de travail.</span><span class="sxs-lookup"><span data-stu-id="c9728-131">You can work with Docker CLI and write your code using any code editor, but if you use Visual Studio Code, it makes it easy to author Dockerfile and docker-compose.yml files in your workspace.</span></span> <span data-ttu-id="c9728-132">De plus, vous pouvez exécuter des tâches de Code Visual Studio à partir de l’IDE qui invite les scripts qui peuvent exécuter des opérations élaborées à l’aide de CLI Docker en dessous.</span><span class="sxs-lookup"><span data-stu-id="c9728-132">Plus, you can run Visual Studio Code tasks from the IDE that will prompt scripts that can be running elaborated operations using Docker CLI underneath.</span></span>

<span data-ttu-id="c9728-133">Code Visual Studio est fourni par une extension, vous devez installer.</span><span class="sxs-lookup"><span data-stu-id="c9728-133">Visual Studio Code is provided by an extension, which you'll need to install.</span></span> <span data-ttu-id="c9728-134">Pour ce faire, appuyez sur Ctrl + Maj + P, tapez **ext installer**, puis exécutez les Extensions : commande d’installer l’Extension pour afficher la liste des extensions Marketplace.</span><span class="sxs-lookup"><span data-stu-id="c9728-134">To do so, Press Ctrl+Shift+P, type **ext install**, and then run the Extensions: Install Extension command to bring up the Marketplace extension list.</span></span> <span data-ttu-id="c9728-135">Ensuite, tapez **docker** pour filtrer les résultats, puis sélectionnez le fichier Dockerfile et Docker composer des fichier (yml), extension de la prise en charge, comme illustré dans la Figure 4-16.</span><span class="sxs-lookup"><span data-stu-id="c9728-135">Next, type **docker** to filter the results, and then select the Dockerfile And Docker Compose File (yml) Support extension, as depicted in Figure 4-16.</span></span>

![](./media/image20.png)

<span data-ttu-id="c9728-136">Figure 4-16 : l’installation de l’Extension Docker dans Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="c9728-136">Figure 4-16: Installing the Docker Extension in Visual Studio Code</span></span>

### <a name="step-2-create-a-dockerfile-related-to-an-existing-image-plain-os-or-dev-environments-like-net-core-nodejs-and-ruby"></a><span data-ttu-id="c9728-137">Étape 2 : Créer un fichier DockerFile lié à une image existante (système d’exploitation standard ou les environnements de développement, Ruby, Node.js et .NET Core)</span><span class="sxs-lookup"><span data-stu-id="c9728-137">Step 2: Create a DockerFile related to an existing image (plain OS or dev environments like .NET Core, Node.js, and Ruby)</span></span>

<span data-ttu-id="c9728-138">Vous aurez besoin d’un fichier DockerFile par une image personnalisée doit être créé et par le conteneur à déployer, par conséquent, si votre application est composée d’un simple service personnalisé, vous devez un fichier DockerFile unique.</span><span class="sxs-lookup"><span data-stu-id="c9728-138">You will need a DockerFile per custom image to be built and per container to be deployed, therefore, if your app is made up of a single custom service, you will need a single DockerFile.</span></span> <span data-ttu-id="c9728-139">Toutefois, si votre application est composée de plusieurs services (comme dans une architecture microservices), vous aurez besoin d’un fichier Dockerfile par service.</span><span class="sxs-lookup"><span data-stu-id="c9728-139">But, if your app is composed of multiple services (as in a microservices architecture), you'll need one Dockerfile per service.</span></span>

<span data-ttu-id="c9728-140">Le fichier DockerFile est généralement placé dans le dossier racine de votre application ou le service et contient les commandes requises pour que cette Docker sache comment configurer et exécuter cette application ou un service.</span><span class="sxs-lookup"><span data-stu-id="c9728-140">The DockerFile is usually placed within the root folder of your app or service and contains the required commands so that Docker knows how to set up and run that app or service.</span></span> <span data-ttu-id="c9728-141">Vous pouvez créer votre fichier DockerFile et ajoutez-le à votre projet, ainsi que votre code (node.js, .NET Core, etc.), ou, si vous ne connaissez pas l’environnement, regardez l’info-bulle suivante.</span><span class="sxs-lookup"><span data-stu-id="c9728-141">You can create your DockerFile and add it to your project along with your code (node.js, .NET Core, etc.), or, if you are new to the environment, take a look at the following Tip.</span></span>

> [!TIP]
> <span data-ttu-id="c9728-142">Vous pouvez utiliser un outil de ligne de commande appelé [v docker](https://github.com/Microsoft/generator-docker), lequel micro-capsules des fichiers à partir de votre projet dans la langue que vous choisissez et ajoute les fichiers de configuration de Docker requis.</span><span class="sxs-lookup"><span data-stu-id="c9728-142">You can use a command-line tool called [yo docker](https://github.com/Microsoft/generator-docker), which scaffolds files from your project in the language you choose and adds the required Docker configuration files.</span></span> <span data-ttu-id="c9728-143">En fait, pour aider les développeurs de la mise en route, il crée le fichier DockerFile approprié, docker-compose.yml et autres scripts associés pour générer et exécuter vos conteneurs Docker.</span><span class="sxs-lookup"><span data-stu-id="c9728-143">Basically, to assist developers getting started, it creates the appropriate DockerFile, docker-compose.yml, and other associated scripts to build and run your Docker containers.</span></span> <span data-ttu-id="c9728-144">Ce générateur yeoman vous invitera à quelques questions, vous demandant de votre hôte de conteneur de langue et de destination sélectionné de développement.</span><span class="sxs-lookup"><span data-stu-id="c9728-144">This yeoman generator will prompt you with a few questions, asking your selected development language and destination container host.</span></span>

![v docker](./media/image21.png)

<span data-ttu-id="c9728-146">Par exemple, la Figure 4-17 présente deux captures d’écran les terminaux de dans Windows et sur un Mac, dans les deux cas, en cours d’exécution v docker, ce qui génère les projets de code exemple (actuellement .NET Core, Golang et Node.js que les langues prises en charge) déjà configurés pour fonctionner sur haut de Docker.</span><span class="sxs-lookup"><span data-stu-id="c9728-146">For instance, Figure 4-17 shows two screenshots from the terminals in Windows and on a Mac, in both cases, running yo docker, which will generate the sample code projects (currently .NET Core, Golang, and Node.js as supported languages) already configured to work on top of Docker.</span></span>

![](./media/image22.PNG)  ![](./media/image23.png)

<span data-ttu-id="c9728-147">Figure 4-17 : v docker outil de commande dans Windows (à gauche) et sur un Mac</span><span class="sxs-lookup"><span data-stu-id="c9728-147">Figure 4-17: yo docker command tool in Windows (left) and on a Mac</span></span>

<span data-ttu-id="c9728-148">Figure 4-18 présente un exemple d’utilisation v docker une fois que vous avez un projet .NET Core existant en place pour être structuré.</span><span class="sxs-lookup"><span data-stu-id="c9728-148">Figure 4-18 presents an example using yo docker after you have an existing .NET Core project in place to be scaffolded.</span></span>

![](./media/image24.PNG)

<span data-ttu-id="c9728-149">Figure 4-18 : v docker avec un .NET Core existants du projet en place</span><span class="sxs-lookup"><span data-stu-id="c9728-149">Figure 4-18: yo docker with an existing .NET Core project in place</span></span>

<span data-ttu-id="c9728-150">À partir du fichier DockerFile, vous spécifiez quelle image Docker base, vous allez utiliser (par exemple, à l’aide de « de microsoft/dotnet:1.0.0-core »).</span><span class="sxs-lookup"><span data-stu-id="c9728-150">From the DockerFile, you specify what base Docker image you'll be using (like using "FROM microsoft/dotnet:1.0.0-core").</span></span> <span data-ttu-id="c9728-151">Vous allez généralement créer votre image personnalisée sur une image de base que vous pouvez obtenir à partir de n’importe quel référentiel officiel à partir de la [Registre du Hub Docker](https://hub.docker.com/) (comme un [image pour .NET Core](https://hub.docker.com/r/microsoft/dotnet/) ou un [pour Node.js](https://hub.docker.com/_/node/)).</span><span class="sxs-lookup"><span data-stu-id="c9728-151">You usually will build your custom image on top of a base image that you can get from any official repository at the [Docker Hub registry](https://hub.docker.com/) (like an [image for .NET Core](https://hub.docker.com/r/microsoft/dotnet/) or one [for Node.js](https://hub.docker.com/_/node/)).</span></span>

<span data-ttu-id="c9728-152">***Option a : utiliser une image Docker officielle existante***</span><span class="sxs-lookup"><span data-stu-id="c9728-152">***Option A: Use an existing official Docker image***</span></span>

<span data-ttu-id="c9728-153">À l’aide d’un dépôt officiel d’une pile de langage avec un numéro de version garantit que les mêmes fonctionnalités de langage sont disponibles sur tous les ordinateurs (y compris le développement, test et production).</span><span class="sxs-lookup"><span data-stu-id="c9728-153">Using an official repository of a language stack with a version number ensures that the same language features are available on all machines (including development, testing, and production).</span></span>

<span data-ttu-id="c9728-154">Voici un exemple de fichier DockerFile pour un conteneur de .NET Core :</span><span class="sxs-lookup"><span data-stu-id="c9728-154">Following is a sample DockerFile for a .NET Core container:</span></span>

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

<span data-ttu-id="c9728-155">Dans ce cas, il est à l’aide de la version 1.0.1 de l’image de ASP.NET Core Docker officiel pour Linux nommé microsoft/aspnetcore:1.0.1.</span><span class="sxs-lookup"><span data-stu-id="c9728-155">In this case, it is using the version 1.0.1 of the official ASP.NET Core Docker image for Linux named microsoft/aspnetcore:1.0.1.</span></span> <span data-ttu-id="c9728-156">Pour plus d’informations, consultez la [page ASP.NET Core Docker images](https://hub.docker.com/r/microsoft/aspnetcore/) et [page de l’Image de Docker .NET Core](https://hub.docker.com/r/microsoft/dotnet/).</span><span class="sxs-lookup"><span data-stu-id="c9728-156">For further details, consult the [ASP.NET Core Docker Image page](https://hub.docker.com/r/microsoft/aspnetcore/) and the [.NET Core Docker Image page](https://hub.docker.com/r/microsoft/dotnet/).</span></span> <span data-ttu-id="c9728-157">Vous également susceptibles d’utiliser une autre image comparable comme nœud : 4-onbuild pour Node.js ou de nombreux autres images préconfigurées pour les langages de développement, qui sont disponibles à [Hub Docker](https://hub.docker.com/explore/).</span><span class="sxs-lookup"><span data-stu-id="c9728-157">You also could be using another comparable image like node:4-onbuild for Node.js, or many other preconfigured images for development languages, which are available at [Docker Hub](https://hub.docker.com/explore/).</span></span>

<span data-ttu-id="c9728-158">Dans le fichier DockerFile, vous devez également indiquent à Docker pour écouter le port TCP que vous utiliserez lors de l’exécution (par exemple le port 80).</span><span class="sxs-lookup"><span data-stu-id="c9728-158">In the DockerFile, you also need to instruct Docker to listen to the TCP port that you will use at runtime (such as port 80).</span></span>

<span data-ttu-id="c9728-159">Il existe des autres lignes de configuration que vous pouvez ajouter dans le fichier DockerFile en fonction de la langue/framework que vous utilisez, pour que Docker sache comment exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="c9728-159">There are other lines of configuration that you can add in the DockerFile depending on the language/framework you are using, so Docker knows how to run the app.</span></span> <span data-ttu-id="c9728-160">Par exemple, vous devez la ligne de point d’entrée \[« dotnet », « MyCustomMicroservice.dll »\] pour exécuter une application .NET Core, bien que vous pouvez avoir plusieurs variantes selon l’approche pour générer et exécuter votre service.</span><span class="sxs-lookup"><span data-stu-id="c9728-160">For instance, you need the ENTRYPOINT line with \["dotnet", "MyCustomMicroservice.dll"\] to run a .NET Core app, although you can have multiple variants depending on the approach to build and run your service.</span></span> <span data-ttu-id="c9728-161">Si vous utilisez le Kit de développement logiciel et dotnet CLI pour générer et exécuter l’application .NET, il est légèrement différent.</span><span class="sxs-lookup"><span data-stu-id="c9728-161">If you're using the SDK and dotnet CLI to build and run the .NET app, it would be slightly different.</span></span> <span data-ttu-id="c9728-162">L’essentiel est que la ligne de point d’entrée ainsi que des lignes supplémentaires sera différentes selon la langue/plateforme que vous choisissez pour votre application.</span><span class="sxs-lookup"><span data-stu-id="c9728-162">The bottom line is that the ENTRYPOINT line plus additional lines will be different depending on the language/platform you choose for your application.</span></span>

<span data-ttu-id="c9728-163">**Plus d’informations** pour plus d’informations sur la création d’images Docker pour les applications .NET Core, accédez à <https://docs.microsoft.com/dotnet/core/docker/building-net-docker-images>.</span><span class="sxs-lookup"><span data-stu-id="c9728-163">**More info** For information about building Docker images for .NET Core applications, go to <https://docs.microsoft.com/dotnet/core/docker/building-net-docker-images>.</span></span>

<span data-ttu-id="c9728-164">Pour en savoir plus sur la création de vos propres images, accédez à [ https://docs.docker.com/engine/\didacticiels/dockerimages/](https://docs.docker.com/engine/tutorials/dockerimages/).</span><span class="sxs-lookup"><span data-stu-id="c9728-164">To learn more about building your own images, go to [https://docs.docker.com/engine/\ tutorials/dockerimages/](https://docs.docker.com/engine/tutorials/dockerimages/).</span></span>

<span data-ttu-id="c9728-165">**Référentiels d’images multiplateforme**</span><span class="sxs-lookup"><span data-stu-id="c9728-165">**Multiplatform image repositories**</span></span>

<span data-ttu-id="c9728-166">Comme les conteneurs Windows répandu, un référentiel unique peut contenir des variantes de plateforme, par exemple une image Linux et Windows.</span><span class="sxs-lookup"><span data-stu-id="c9728-166">As Windows containers become more prevalent, a single repository can contain platform variants, such as a Linux and Windows image.</span></span> <span data-ttu-id="c9728-167">Il s’agit d’une nouvelle fonctionnalité disponible dans Docker qui rend possible pour les fournisseurs d’utiliser un référentiel unique pour couvrir plusieurs plateformes, telles que [microsoft/aspdotnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) référentiel, qui est disponible sur le Registre de docker Hub.</span><span class="sxs-lookup"><span data-stu-id="c9728-167">This is a new feature coming in Docker that makes it possible for vendors to use a single repository to cover multiple platforms, such as [microsoft/aspdotnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) repository, which is available at DockerHub registry.</span></span> <span data-ttu-id="c9728-168">Lorsque la fonctionnalité revient active, extraction de cette image à partir d’un hôte Windows extraira la variante de Windows, alors que l’extraction du même nom de l’image à partir d’un hôte Linux extraira la variante de Linux.</span><span class="sxs-lookup"><span data-stu-id="c9728-168">As the feature comes alive, pulling this image from a Windows host will pull the Windows variant, whereas pulling the same image name from a Linux host will pull the Linux variant.</span></span>

<span data-ttu-id="c9728-169">***Option b : créer votre image de base à partir de zéro***</span><span class="sxs-lookup"><span data-stu-id="c9728-169">***Option B: Create your base image from scratch***</span></span>

<span data-ttu-id="c9728-170">Vous pouvez créer votre propre image de base de Docker à partir de zéro, comme expliqué dans cet [article](https://docs.docker.com/engine/userguide/eng-image/baseimages/) à partir de Docker.</span><span class="sxs-lookup"><span data-stu-id="c9728-170">You can create your own Docker base image from scratch as explained in this [article](https://docs.docker.com/engine/userguide/eng-image/baseimages/) from Docker.</span></span> <span data-ttu-id="c9728-171">Il s’agit d’un scénario qui n’est probablement pas adapté si vous débutez avec Docker, mais si vous souhaitez définir les bits spécifiques de votre propre image de base, vous pouvez le faire.</span><span class="sxs-lookup"><span data-stu-id="c9728-171">This is a scenario that is probably not best for you if you are just starting with Docker, but if you want to set the specific bits of your own base image, you can do it.</span></span>

### <a name="step-3-create-your-custom-docker-images-embedding-your-service-in-it"></a><span data-ttu-id="c9728-172">Étape 3 : Créer vos images Docker personnalisées, incorporation de votre service qu’il contient</span><span class="sxs-lookup"><span data-stu-id="c9728-172">Step 3: Create your custom Docker images embedding your service in it</span></span>

<span data-ttu-id="c9728-173">Pour chaque service personnalisée qui compose votre application, vous devez créer une image associée.</span><span class="sxs-lookup"><span data-stu-id="c9728-173">For each custom service that comprises your app, you'll need to create a related image.</span></span> <span data-ttu-id="c9728-174">Si votre application est composée d’un seul service ou une application web, vous aurez besoin d’une seule image.</span><span class="sxs-lookup"><span data-stu-id="c9728-174">If your app is made up of a single service or web app, you'll need just a single image.</span></span>

> [!NOTE]
> <span data-ttu-id="c9728-175">Lors de la prise en compte le « boucle externe DevOps flux de travail », les images sont créées par un processus de génération automatisé chaque fois que vous effectuez un push votre code source vers un référentiel Git (intégration continue) pour les images seront créés dans cet environnement global à partir de votre code source.</span><span class="sxs-lookup"><span data-stu-id="c9728-175">When taking into account the "outer-loop DevOps workflow," the images will be created by an automated build process whenever you push your source code to a Git repository (Continuous Integration) so the images will be created in that global environment from your source code.</span></span>

<span data-ttu-id="c9728-176">Toutefois, nous considérons atteindre cet itinéraire de la boucle externe, nous devons vérifier que l’application Docker réellement fonctionne correctement afin qu’ils ne poussent le code qui peut ne pas fonctionne correctement dans le système de contrôle de source (Git, etc.).</span><span class="sxs-lookup"><span data-stu-id="c9728-176">But, before we consider going to that outer-loop route, we need to ensure that the Docker application is actually working properly so that they don't push code that might not work properly to the source control system (Git, etc.).</span></span>

<span data-ttu-id="c9728-177">Par conséquent, chaque développeur doit tout d’abord effectuer tout le processus de la boucle interne pour tester localement et continuer à développer jusqu'à ce qu’ils souhaitent push d’une fonctionnalité complète ou de modifier le système de contrôle source.</span><span class="sxs-lookup"><span data-stu-id="c9728-177">Therefore, each developer first needs to do the entire inner-loop process to test locally and continue developing until they want to push a complete feature or change to the source control system.</span></span>

<span data-ttu-id="c9728-178">Pour créer une image dans votre environnement local et à l’aide du fichier DockerFile, vous pouvez utiliser la commande de génération docker, comme illustré dans la Figure 4-19 (vous pouvez également exécuter docker-composer des--créer pour les applications composées par plusieurs conteneurs/services).</span><span class="sxs-lookup"><span data-stu-id="c9728-178">To create an image in your local environment and using the DockerFile, you can use the docker build command, as demonstrated in Figure 4-19 (you also can run docker-compose up --build for applications composed by several containers/services).</span></span>

![](./media/image25.png)

<span data-ttu-id="c9728-179">Figure 4-19 : génération docker en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="c9728-179">Figure 4-19: Running docker build</span></span>

<span data-ttu-id="c9728-180">Si vous le souhaitez, au lieu d’exécuter directement des docker build à partir du dossier du projet, vous pouvez tout d’abord générer un dossier peut être déployé avec les bibliothèques .NET nécessaires à l’aide de l’exécution dotnet publication de commande et exécutez génération docker.</span><span class="sxs-lookup"><span data-stu-id="c9728-180">Optionally, instead of directly running docker build from the project's folder, you first can generate a deployable folder with the .NET libraries needed by using the run dotnet publish command, and then run docker build.</span></span>

<span data-ttu-id="c9728-181">Dans cet exemple, cela crée une image Docker avec le nom cesardl/netcore-webapi-microservice-docker : premier ( : tout d’abord est une balise, comme une version spécifique).</span><span class="sxs-lookup"><span data-stu-id="c9728-181">In this example, this creates a Docker image with the name cesardl/netcore-webapi-microservice-docker:first (:first is a tag, like a specific version).</span></span> <span data-ttu-id="c9728-182">Vous pouvez effectuer cette étape pour chaque image personnalisée, que vous devez créer pour votre application Docker composée avec plusieurs conteneurs.</span><span class="sxs-lookup"><span data-stu-id="c9728-182">You can take this step for each custom image you need to create for your composed Docker application with several containers.</span></span>

<span data-ttu-id="c9728-183">Vous trouverez les images existantes dans votre référentiel local (votre ordinateur de développement) à l’aide de la docker commande d’images, comme illustré dans la Figure 4-20.</span><span class="sxs-lookup"><span data-stu-id="c9728-183">You can find the existing images in your local repository (your development machine) by using the docker images command, as illustrated in Figure 4-20.</span></span>

![](./media/image26.png)

<span data-ttu-id="c9728-184">Figure 4-20 : affichage des images existantes à l’aide d’images docker</span><span class="sxs-lookup"><span data-stu-id="c9728-184">Figure 4-20: Viewing existing images using docker images</span></span>

### <a name="step-4-optional-define-your-services-in-docker-composeyml-when-building-a-composed-docker-app-with-multiple-services"></a><span data-ttu-id="c9728-185">Étape 4 : (Facultatif) définir vos services dans docker-compose.yml lors de la création d’une application composée de Docker avec plusieurs services</span><span class="sxs-lookup"><span data-stu-id="c9728-185">Step 4: (Optional) Define your services in docker-compose.yml when building a composed Docker app with multiple services</span></span>

<span data-ttu-id="c9728-186">Avec le fichier compose.yml de docker, vous pouvez définir un ensemble de services liés à être déployée comme une application composée avec les commandes de déploiement expliqués dans la section étape suivante.</span><span class="sxs-lookup"><span data-stu-id="c9728-186">With the docker-compose.yml file you can define a set of related services to be deployed as a composed application with the deployment commands explained in the next step section.</span></span>

<span data-ttu-id="c9728-187">Vous devez créer ce fichier dans votre main ou un dossier de solution racine ; Il doit avoir un contenu similaire dans le fichier docker-compose.yml suivant :</span><span class="sxs-lookup"><span data-stu-id="c9728-187">You need to create that file in your main or root solution folder; it should have a similar content to the following docker-compose.yml file:</span></span>

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

<span data-ttu-id="c9728-188">Dans ce cas particulier, ce fichier définit deux services : le service web (votre service personnalisé) et le service de redis (un service de cache populaires).</span><span class="sxs-lookup"><span data-stu-id="c9728-188">In this particular case, this file defines two services: the web service (your custom service) and the redis service (a popular cache service).</span></span> <span data-ttu-id="c9728-189">Chaque service sera déployé en tant que conteneur, afin que nous devons utiliser une image Docker concrète pour chacun.</span><span class="sxs-lookup"><span data-stu-id="c9728-189">Each service will be deployed as a container, so we need to use a concrete Docker image for each.</span></span> <span data-ttu-id="c9728-190">Pour ce service web spécifique, l’image devez effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c9728-190">For this particular web service, the image will need to do the following:</span></span>

-   <span data-ttu-id="c9728-191">Génération du fichier dockerfile dans le répertoire actif</span><span class="sxs-lookup"><span data-stu-id="c9728-191">Build from the DockerFile in the current directory</span></span>

-   <span data-ttu-id="c9728-192">Transférer l’exposé port 80 sur le conteneur sur le port 81 sur l’ordinateur hôte</span><span class="sxs-lookup"><span data-stu-id="c9728-192">Forward the exposed port 80 on the container to port 81 on the host machine</span></span>

-   <span data-ttu-id="c9728-193">Monter le répertoire du projet sur l’ordinateur hôte à /code au sein du conteneur, ce qui vous permet de modifier le code sans avoir à recréer l’image</span><span class="sxs-lookup"><span data-stu-id="c9728-193">Mount the project directory on the host to /code within the container, making it possible for you to modify the code without having to rebuild the image</span></span>

-   <span data-ttu-id="c9728-194">Lier le service web pour le service de redis</span><span class="sxs-lookup"><span data-stu-id="c9728-194">Link the web service to the redis service</span></span>

<span data-ttu-id="c9728-195">Le service redis utilise le [dernière image redis public](https://hub.docker.com/_/redis/) extraite à partir du Registre du Hub d’ancrage.</span><span class="sxs-lookup"><span data-stu-id="c9728-195">The redis service uses the [latest public redis image](https://hub.docker.com/_/redis/) pulled from the Docker Hub registry.</span></span> <span data-ttu-id="c9728-196">[redis](https://redis.io/) est un système de cache très populaire pour les applications côté serveur.</span><span class="sxs-lookup"><span data-stu-id="c9728-196">[redis](https://redis.io/) is a very popular cache system for server-side applications.</span></span>

### <a name="step-5-build-and-run-your-docker-app"></a><span data-ttu-id="c9728-197">Étape 5 : Générer et exécuter votre application de Docker</span><span class="sxs-lookup"><span data-stu-id="c9728-197">Step 5: Build and run your Docker app</span></span>

<span data-ttu-id="c9728-198">Si votre application a uniquement un seul conteneur, vous devez l’exécuter en la déployant sur l’hôte Docker (machine virtuelle ou serveur physique).</span><span class="sxs-lookup"><span data-stu-id="c9728-198">If your app has only a single container, you just need to run it by deploying it to your Docker Host (VM or physical server).</span></span> <span data-ttu-id="c9728-199">Toutefois, si votre application est composée de plusieurs services, vous devez *composer*, trop.</span><span class="sxs-lookup"><span data-stu-id="c9728-199">However, if your app is made up of multiple services, you need to *compose it*, too.</span></span> <span data-ttu-id="c9728-200">Nous allons voir les différentes options.</span><span class="sxs-lookup"><span data-stu-id="c9728-200">Let's see the different options.</span></span>

<span data-ttu-id="c9728-201">***Option a : exécuter un seul conteneur ou service***</span><span class="sxs-lookup"><span data-stu-id="c9728-201">***Option A: Run a single container or service***</span></span>

<span data-ttu-id="c9728-202">Vous pouvez exécuter l’image Docker à l’aide de la commande docker run, comme illustré ici :</span><span class="sxs-lookup"><span data-stu-id="c9728-202">You can run the Docker image by using the docker run command, as shown here:</span></span>

```
docker run -t -d -p 80:5000
cesardl/netcore-webapi-microservice-docker:first
```

<span data-ttu-id="c9728-203">Notez que pour ce déploiement particulier, nous allons rediriger les demandes envoyées au port 80 pour le port interne 5000.</span><span class="sxs-lookup"><span data-stu-id="c9728-203">Note that for this particular deployment, we'll be redirecting requests sent to port 80 to the internal port 5000.</span></span> <span data-ttu-id="c9728-204">À présent, l’application est à l’écoute sur le port externe 80 au niveau de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="c9728-204">Now, the application is listening on the external port 80 at the host level.</span></span>

<span data-ttu-id="c9728-205">***Option b : composer et exécuter une application de plusieurs conteneurs***</span><span class="sxs-lookup"><span data-stu-id="c9728-205">***Option B: Compose and run a multiple-container application***</span></span>

<span data-ttu-id="c9728-206">Dans la plupart des scénarios d’entreprise, une application de Docker sera composée de plusieurs services.</span><span class="sxs-lookup"><span data-stu-id="c9728-206">In most enterprise scenarios, a Docker application will be composed of multiple services.</span></span> <span data-ttu-id="c9728-207">Dans ce cas, vous pouvez exécuter la commande docker-composer des (Figure 4-21), qui utilise le fichier docker-compose.yml que vous avez peut-être créé précédemment.</span><span class="sxs-lookup"><span data-stu-id="c9728-207">For these cases, you can run the command docker-compose up (Figure 4-21), which will use the docker-compose.yml file that you might have created previously.</span></span> <span data-ttu-id="c9728-208">Exécution de cette commande déploie une application composée avec tous ses conteneurs connexes.</span><span class="sxs-lookup"><span data-stu-id="c9728-208">Running this command deploys a composed application with all of its related containers.</span></span>

![](./media/image27.png)

<span data-ttu-id="c9728-209">Figure 4-21 : les résultats de l’exécution de la commande « docker-composer des »</span><span class="sxs-lookup"><span data-stu-id="c9728-209">Figure 4-21: Results of running the "docker-compose up" command</span></span>

<span data-ttu-id="c9728-210">Après avoir exécuté docker-composer des, vous déployez votre application et ses conteneurs connexes dans l’hôte Docker, comme illustré dans la Figure 4-22, dans la représentation sous forme de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="c9728-210">After you run docker-compose up, you deploy your application and its related container(s) into your Docker Host, as illustrated in Figure 4-22, in the VM representation.</span></span>

![](./media/image28.png)

<span data-ttu-id="c9728-211">Machine virtuelle de la figure 4-22 : avec des conteneurs Docker déployé</span><span class="sxs-lookup"><span data-stu-id="c9728-211">Figure 4-22: VM with Docker containers deployed</span></span>

<span data-ttu-id="c9728-212">Docker Remarque-composer des et docker exécuter peut être assez vos conteneurs de test dans votre environnement de développement, mais vous ne pouvez pas à les utiliser si vous prévoyez de travailler avec des clusters de Docker et orchestrators comme Docker Swarm, mésosphère contrôleur de domaine/système d’exploitation ou Kubernetes Pour pouvoir évoluer.</span><span class="sxs-lookup"><span data-stu-id="c9728-212">Note docker-compose up and docker run might be enough for testing your containers in your development environment, but you might not use them at all if you are expecting to work with Docker clusters and orchestrators like Docker Swarm, Mesosphere DC/OS, or Kubernetes in order to be able to scale up.</span></span> <span data-ttu-id="c9728-213">Si vous utilisez un cluster comme [Docker Swarm le mode](https://docs.docker.com/engine/swarm/) (disponible dans Docker pour Windows et Mac depuis la version 1.12), vous devez déployer et tester avec des commandes supplémentaires, telles que la création du service de docker pour les services uniques, ou lorsque vous êtes déploiement d’une application composée de plusieurs conteneurs, à l’aide de docker Composer offre groupée et docker déployer myBundleFile, en déployant l’application composée comme une pile, comme expliqué dans l’article [groupes d’applications distribuées](https://blog.docker.com/2016/06/docker-app-bundle/) à partir de Docker.</span><span class="sxs-lookup"><span data-stu-id="c9728-213">If you're using a cluster like [Docker Swarm mode](https://docs.docker.com/engine/swarm/) (available in Docker for Windows and Mac since version 1.12), you need to deploy and test with additional commands such as docker service create for single services, or when you're deploying an app composed of several containers, using docker compose bundle and docker deploy myBundleFile, by deploying the composed app as a stack, as explained in the article [Distributed Application Bundles](https://blog.docker.com/2016/06/docker-app-bundle/) from Docker.</span></span>

<span data-ttu-id="c9728-214">Pour [DC/OS](https://mesosphere.com/blog/2015/09/02/dcos-cli-command-line-tool-datacenter/) et [Kubernetes](http://kubernetes.io/docs/user-guide/deployments/#creating-a-deployment) vous utiliseriez les commandes de déploiement différentes et des scripts, ainsi.</span><span class="sxs-lookup"><span data-stu-id="c9728-214">For [DC/OS](https://mesosphere.com/blog/2015/09/02/dcos-cli-command-line-tool-datacenter/) and [Kubernetes](http://kubernetes.io/docs/user-guide/deployments/#creating-a-deployment) you would use different deployment commands and scripts, as well.</span></span>

### <a name="step-6-test-your-docker-application-locally-in-your-local-cd-vm"></a><span data-ttu-id="c9728-215">Étape 6 : Tester votre application Docker (localement, dans votre machine virtuelle d’un local CD)</span><span class="sxs-lookup"><span data-stu-id="c9728-215">Step 6: Test your Docker application (locally, in your local CD VM)</span></span>

<span data-ttu-id="c9728-216">Cette étape varie en fonction de ce que fait votre application.</span><span class="sxs-lookup"><span data-stu-id="c9728-216">This step will vary depending on what your app is doing.</span></span>

<span data-ttu-id="c9728-217">Dans une très .NET Core API Web simple « Hello World » déployé comme un seul conteneur ou un service, vous devez simplement accéder au service en fournissant le port TCP spécifié dans le fichier DockerFile.</span><span class="sxs-lookup"><span data-stu-id="c9728-217">In a very simple .NET Core Web API "Hello World" deployed as a single container or service, you'd just need to access the service by providing the TCP port specified in the DockerFile.</span></span>

<span data-ttu-id="c9728-218">Si localhost n’est pas activé, pour accéder à votre service, vous pouvez rechercher l’adresse IP de l’ordinateur à l’aide de cette commande :</span><span class="sxs-lookup"><span data-stu-id="c9728-218">If localhost is not turned on, to navigate to your service, find the IP address for the machine by using this command:</span></span>

<span data-ttu-id="c9728-219">machine de docker ip *votre nom de conteneur*</span><span class="sxs-lookup"><span data-stu-id="c9728-219">docker-machine ip *your-container-name*</span></span>

<span data-ttu-id="c9728-220">Sur l’hôte Docker, ouvrez un navigateur et accédez à ce site. Vous devez voir votre service / d’application en cours d’exécution, comme illustré dans la Figure 4-23.</span><span class="sxs-lookup"><span data-stu-id="c9728-220">On the Docker host, open a browser and navigate to that site; you should see your app/service running, as demonstrated in Figure 4-23.</span></span>

![](./media/image29.png)

<span data-ttu-id="c9728-221">Figure 4-23 : test de votre application de Docker localement en utilisant localhost</span><span class="sxs-lookup"><span data-stu-id="c9728-221">Figure 4-23: Testing your Docker application locally using localhost</span></span>

<span data-ttu-id="c9728-222">Notez qu’il utilise le port 80, mais en interne qu’il a été redirigé vers le port 5000, car c’est la façon dont elle a été déployée avec docker, exécuter, comme expliqué plus haut.</span><span class="sxs-lookup"><span data-stu-id="c9728-222">Note that it is using port 80, but internally it was being redirected to port 5000, because that's how it was deployed with docker run, as explained earlier.</span></span>

<span data-ttu-id="c9728-223">Vous pouvez le tester à l’aide de CURL à partir du terminal.</span><span class="sxs-lookup"><span data-stu-id="c9728-223">You can test this by using CURL from the terminal.</span></span> <span data-ttu-id="c9728-224">Dans une installation Docker sur Windows, l’adresse IP par défaut est 10.0.75.1, comme illustré dans la Figure 4-24.</span><span class="sxs-lookup"><span data-stu-id="c9728-224">In a Docker installation on Windows, the default IP is 10.0.75.1, as depicted in Figure 4-24.</span></span>

![](./media/image30.png)

<span data-ttu-id="c9728-225">Figure 4-24 : test d’une application de Docker localement à l’aide de CURL</span><span class="sxs-lookup"><span data-stu-id="c9728-225">Figure 4-24: Testing a Docker application locally by using CURL</span></span>

<span data-ttu-id="c9728-226">**Débogage d’un conteneur en cours d’exécution sur Docker**</span><span class="sxs-lookup"><span data-stu-id="c9728-226">**Debugging a container running on Docker**</span></span>

<span data-ttu-id="c9728-227">Code Visual Studio prend en charge le débogage Docker si vous utilisez Node.js et autres plateformes comme des conteneurs de .NET Core.</span><span class="sxs-lookup"><span data-stu-id="c9728-227">Visual Studio Code supports debugging Docker if you're using Node.js and other platforms like .NET Core containers.</span></span>

<span data-ttu-id="c9728-228">Vous également pourrez déboguer les conteneurs .NET Core dans Docker lors de l’utilisation de Visual Studio, comme décrit dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="c9728-228">You also can debug .NET Core containers in Docker when using Visual Studio, as described in the next section.</span></span>

<span data-ttu-id="c9728-229">**Plus d’informations :** pour en savoir plus sur le débogage des conteneurs Docker de Node.js, accédez à <https://blog.docker.com/2016/07/live-debugging-docker/> et [ https://blogs.msdn.microsoft.com/\ utilisateur\_ed/2016/02/27 / Visual-Studio-code-New-Features-13-Big-Debugging-Updates-Rich-Object-Hover-Conditional-Breakpoints-Node-js-mono-more/](https://blogs.msdn.microsoft.com/user_ed/2016/02/27/visual-studio-code-new-features-13-big-debugging-updates-rich-object-hover-conditional-breakpoints-node-js-mono-more/).</span><span class="sxs-lookup"><span data-stu-id="c9728-229">**More info:** To learn more about debugging Node.js Docker containers, go to <https://blog.docker.com/2016/07/live-debugging-docker/> and [https://blogs.msdn.microsoft.com/\ user\_ed/2016/02/27/visual-studio-code-new-features-13-big-debugging-updates-rich-object-hover-conditional-breakpoints-node-js-mono-more/](https://blogs.msdn.microsoft.com/user_ed/2016/02/27/visual-studio-code-new-features-13-big-debugging-updates-rich-object-hover-conditional-breakpoints-node-js-mono-more/).</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="c9728-230">[Précédente] (docker-applications-développement-environment.md) [suivant] (visual-studio-outils-de-docker.md)</span><span class="sxs-lookup"><span data-stu-id="c9728-230">[Previous] (docker-apps-development-environment.md) [Next] (visual-studio-tools-for-docker.md)</span></span>
