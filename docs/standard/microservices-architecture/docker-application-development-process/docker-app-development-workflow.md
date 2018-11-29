---
title: Workflow de développement des applications Docker
description: Architecture des microservices .NET pour les applications .NET conteneurisées | Workflow de développement des applications Docker
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/05/2018
ms.openlocfilehash: 00cffde7e7eb548f755b60f64aa596210b570d07
ms.sourcegitcommit: 35316b768394e56087483cde93f854ba607b63bc
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2018
ms.locfileid: "52297515"
---
# <a name="development-workflow-for-docker-apps"></a><span data-ttu-id="e8bab-103">Workflow de développement des applications Docker</span><span class="sxs-lookup"><span data-stu-id="e8bab-103">Development workflow for Docker apps</span></span>

<span data-ttu-id="e8bab-104">Le cycle de vie du développement d’une application débute sur une machine de développeur, là où le développeur code l’application dans le langage de son choix et où il teste localement sa nouvelle application.</span><span class="sxs-lookup"><span data-stu-id="e8bab-104">The application development life cycle starts at each developer’s machine, where the developer codes the application using their preferred language and tests it locally.</span></span> <span data-ttu-id="e8bab-105">Quels que soient le langage, le framework et la plateforme choisis par le développeur, avec ce workflow, le développeur crée et teste toujours des conteneurs Docker, mais il le fait en local.</span><span class="sxs-lookup"><span data-stu-id="e8bab-105">No matter which language, framework, and platform the developer chooses, with this workflow, the developer is always developing and testing Docker containers, but doing so locally.</span></span>

<span data-ttu-id="e8bab-106">Chaque conteneur (instance d’une image Docker) inclut les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e8bab-106">Each container (an instance of a Docker image) includes the following components:</span></span>

- <span data-ttu-id="e8bab-107">Un système d’exploitation sélectionné (par exemple, une distribution Linux, Windows Nano Server ou Windows Server Core)</span><span class="sxs-lookup"><span data-stu-id="e8bab-107">An operating system selection (for example, a Linux distribution, Windows Nano Server, or Windows Server Core).</span></span>

- <span data-ttu-id="e8bab-108">Des fichiers ajoutés par le développeur (binaires de l’application, etc.)</span><span class="sxs-lookup"><span data-stu-id="e8bab-108">Files added by the developer (application binaries, etc.).</span></span>

- <span data-ttu-id="e8bab-109">Des informations de configuration (paramètres d’environnement et dépendances)</span><span class="sxs-lookup"><span data-stu-id="e8bab-109">Configuration information (environment settings and dependencies).</span></span>

## <a name="workflow-for-developing-docker-container-based-applications"></a><span data-ttu-id="e8bab-110">Workflow pour développer des applications basées sur des conteneurs Docker</span><span class="sxs-lookup"><span data-stu-id="e8bab-110">Workflow for developing Docker container-based applications</span></span>

<span data-ttu-id="e8bab-111">Cette section décrit le workflow de développement de la *boucle interne* pour les applications basées sur des conteneurs Docker.</span><span class="sxs-lookup"><span data-stu-id="e8bab-111">This section describes the *inner-loop* development workflow for Docker container-based applications.</span></span> <span data-ttu-id="e8bab-112">Dans ce workflow de la boucle interne, le workflow DevOps plus global n’est pas pris en compte et seules les étapes de développement effectuées sur l’ordinateur du développeur sont couvertes.</span><span class="sxs-lookup"><span data-stu-id="e8bab-112">The inner-loop workflow means it is not taking into account the broader DevOps workflow and just focuses on the development work done on the developer’s computer.</span></span> <span data-ttu-id="e8bab-113">Les étapes initiales de configuration de l’environnement ne sont pas incluses non plus, car elles sont effectuées une seule fois.</span><span class="sxs-lookup"><span data-stu-id="e8bab-113">The initial steps to set up the environment are not included, since those are done only once.</span></span>

<span data-ttu-id="e8bab-114">Une application est composée de vos propres services et de bibliothèques supplémentaires (dépendances).</span><span class="sxs-lookup"><span data-stu-id="e8bab-114">An application is composed of your own services plus additional libraries (dependencies).</span></span> <span data-ttu-id="e8bab-115">La figure 5-1 illustre les principales étapes qu’un développeur doit généralement effectuer pour créer une application Docker.</span><span class="sxs-lookup"><span data-stu-id="e8bab-115">The following are the basic steps you usually take when building a Docker application, as illustrated in Figure 5-1.</span></span>

![Diagramme du workflow pas à pas pour développer des applications Docker conteneurisées](./media/image1.png)

<span data-ttu-id="e8bab-117">**Figure 5-1.**</span><span class="sxs-lookup"><span data-stu-id="e8bab-117">**Figure 5-1.**</span></span> <span data-ttu-id="e8bab-118">Workflow pas à pas pour développer des applications Docker conteneurisées</span><span class="sxs-lookup"><span data-stu-id="e8bab-118">Step-by-step workflow for developing Docker containerized apps</span></span>

<span data-ttu-id="e8bab-119">Ce guide décrit tout ce processus en détail, en expliquant chacune des étapes majeures dans l’optique d’un environnement Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e8bab-119">In this guide, this whole process is detailed and every major step is explained by focusing on a Visual Studio environment.</span></span>

<span data-ttu-id="e8bab-120">Si vous optez pour une approche de développement avec un éditeur ou une interface CLI (par exemple, Visual Studio Code plus la CLI Docker sur macOS ou Windows), vous aurez besoin de connaître toutes les étapes, sans doute de manière plus détaillée que pour Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e8bab-120">When you are using an editor/CLI development approach (for example, Visual Studio Code plus Docker CLI on macOS or Windows), you need to know every step, generally in more detail than if you are using Visual Studio.</span></span> <span data-ttu-id="e8bab-121">Pour plus d’informations sur le développement dans un environnement CLI, consultez le livre électronique [Containerized Docker Application lifecycle with Microsoft Platforms and Tools](https://aka.ms/dockerlifecycleebook/).</span><span class="sxs-lookup"><span data-stu-id="e8bab-121">For more information about working in a CLI environment, see the e-book [Containerized Docker Application lifecycle with Microsoft Platforms and Tools](https://aka.ms/dockerlifecycleebook/).</span></span>

<span data-ttu-id="e8bab-122">Si vous utilisez Visual Studio, bon nombre de ces étapes sont faites à votre place, ce qui vous fait gagner énormément de temps dans votre travail.</span><span class="sxs-lookup"><span data-stu-id="e8bab-122">When you're using Visual Studio, many of those steps are handled for you, which dramatically improves your productivity.</span></span> <span data-ttu-id="e8bab-123">Cela est encore plus vrai si vous utilisez Visual Studio 2017 et ciblez des applications multiconteneurs.</span><span class="sxs-lookup"><span data-stu-id="e8bab-123">This is especially true when you are using Visual Studio 2017 and targeting multi-container applications.</span></span> <span data-ttu-id="e8bab-124">Par exemple, avec un seul clic de souris, Visual Studio ajoute les fichiers *Dockerfile* et *docker-compose.yml* à vos projets, avec la configuration de votre application.</span><span class="sxs-lookup"><span data-stu-id="e8bab-124">For instance, with just one mouse click, Visual Studio adds the *Dockerfile* and *docker-compose.yml* files to your projects with the configuration for your application.</span></span> <span data-ttu-id="e8bab-125">Quand vous exécutez l’application dans Visual Studio, le programme crée l’image Docker et exécute l’application multiconteneur directement dans Docker.</span><span class="sxs-lookup"><span data-stu-id="e8bab-125">When you run the application in Visual Studio, it builds the Docker image and runs the multi-container application directly in Docker.</span></span> <span data-ttu-id="e8bab-126">Il vous permet même de déboguer plusieurs conteneurs à la fois.</span><span class="sxs-lookup"><span data-stu-id="e8bab-126">It even allows you to debug several containers at once.</span></span> <span data-ttu-id="e8bab-127">Grâce à ces fonctionnalités, vous développez nettement plus vite.</span><span class="sxs-lookup"><span data-stu-id="e8bab-127">These features boost your development speed.</span></span>

<span data-ttu-id="e8bab-128">Dans les instructions qui suivent, nous expliquons les dessous de chaque étape avec Docker.</span><span class="sxs-lookup"><span data-stu-id="e8bab-128">In the guidance that follows, we explain what's happening "under the covers" with Docker.</span></span>

![Image de l’étape 1, « Code your app »](./media/image2.png)

## <a name="step-1-start-coding-and-create-your-initial-application-or-service-baseline"></a><span data-ttu-id="e8bab-130">Étape 1.</span><span class="sxs-lookup"><span data-stu-id="e8bab-130">Step 1.</span></span> <span data-ttu-id="e8bab-131">Commencer le codage et créer votre base de référence initiale pour l’application ou le service</span><span class="sxs-lookup"><span data-stu-id="e8bab-131">Start coding and create your initial application or service baseline</span></span>

<span data-ttu-id="e8bab-132">Le développement d’une application se déroule de façon similaire avec ou sans Docker.</span><span class="sxs-lookup"><span data-stu-id="e8bab-132">Developing a Docker application is similar to the way you develop an application without Docker.</span></span> <span data-ttu-id="e8bab-133">La différence est que, lors du développement avec Docker, vous déployez et testez l’application ou les services exécutés dans des conteneurs Docker dans votre environnement local.</span><span class="sxs-lookup"><span data-stu-id="e8bab-133">The difference is that while developing for Docker, you are deploying and testing your application or services running within Docker containers in your local environment.</span></span> <span data-ttu-id="e8bab-134">Le conteneur peut être un conteneur Linux ou Windows.</span><span class="sxs-lookup"><span data-stu-id="e8bab-134">The container can be either a Linux container or a Windows container.</span></span>

### <a name="set-up-your-local-environment-with-visual-studio"></a><span data-ttu-id="e8bab-135">Configurer votre environnement local avec Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e8bab-135">Set up your local environment with Visual Studio</span></span>

<span data-ttu-id="e8bab-136">Pour commencer, assurez-vous que [Docker Community Edition (CE)](https://www.docker.com/community-edition) pour Windows est installé, comme cela est expliqué dans les instructions suivantes :</span><span class="sxs-lookup"><span data-stu-id="e8bab-136">To begin, make sure you have [Docker Community Edition (CE)](https://www.docker.com/community-edition) for Windows installed, as explained in the following instructions:</span></span>

[<span data-ttu-id="e8bab-137">Get started with Docker CE for Windows</span><span class="sxs-lookup"><span data-stu-id="e8bab-137">Get started with Docker CE for Windows</span></span>](https://docs.docker.com/docker-for-windows/)

<span data-ttu-id="e8bab-138">Vous avez également besoin de **Visual Studio 2017**, avec la charge de travail « Développement multiplateforme .NET Core » installée (voir la figure 5-2).</span><span class="sxs-lookup"><span data-stu-id="e8bab-138">In addition, you need Visual Studio 2017 with the **.NET Core cross-platform development** workload installed, as shown in Figure 5-2.</span></span>

![](./media/image3.png)

<span data-ttu-id="e8bab-139">**Figure 5-2**.</span><span class="sxs-lookup"><span data-stu-id="e8bab-139">**Figure 5-2**.</span></span> <span data-ttu-id="e8bab-140">Sélection de la charge de travail **.NET Core et Docker** durant l’installation de Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="e8bab-140">Selecting the **.NET Core and Docker** workload during Visual Studio 2017 setup</span></span>

<span data-ttu-id="e8bab-141">Vous pouvez commencer le codage de votre application en.NET brut (généralement dans .NET Core si vous envisagez d’utiliser des conteneurs) même si vous n’avez pas encore activé Docker dans votre application, ni effectuer de déploiement et de test dans Docker.</span><span class="sxs-lookup"><span data-stu-id="e8bab-141">You can start coding your application in plain .NET (usually in .NET Core if you are planning to use containers) even before enabling Docker in your application and deploying and testing in Docker.</span></span> <span data-ttu-id="e8bab-142">Toutefois, nous vous recommandons de commencer à travailler dans Docker le plus tôt possible, car Docker sera le véritable environnement de développement, et vous pourrez détecter les problèmes éventuels dès le début.</span><span class="sxs-lookup"><span data-stu-id="e8bab-142">However, it is recommended that you start working on Docker as soon as possible, because that will be the real environment and any issues can be discovered as soon as possible.</span></span> <span data-ttu-id="e8bab-143">Nous le conseillons d’autant plus que Visual Studio rend l’utilisation de Docker extrêmement simple et intuitive. L’exemple le plus significatif est le débogage des applications multiconteneurs à partir de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e8bab-143">This is encouraged because Visual Studio makes it so easy to work with Docker that it almost feels transparent — the best example when debugging multi-container applications from Visual Studio.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="e8bab-144">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e8bab-144">Additional resources</span></span>

- <span data-ttu-id="e8bab-145">**Get started with Docker CE for Windows**</span><span class="sxs-lookup"><span data-stu-id="e8bab-145">**Get started with Docker CE for Windows**</span></span>

   [*https://docs.docker.com/docker-for-windows/*](https://docs.docker.com/docker-for-windows/)

- <span data-ttu-id="e8bab-146">**Visual Studio 2017**</span><span class="sxs-lookup"><span data-stu-id="e8bab-146">**Visual Studio 2017**</span></span>

   [*https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs*](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs)

![Image de l’étape 2, « Write Dockerfiles »](./media/image4.png)

## <a name="step-2-create-a-dockerfile-related-to-an-existing-net-base-image"></a><span data-ttu-id="e8bab-148">Étape 2.</span><span class="sxs-lookup"><span data-stu-id="e8bab-148">Step 2.</span></span> <span data-ttu-id="e8bab-149">Créer un fichier Dockerfile associé à une image de base .NET existante</span><span class="sxs-lookup"><span data-stu-id="e8bab-149">Create a Dockerfile related to an existing .NET base image</span></span>

<span data-ttu-id="e8bab-150">Vous avez besoin d’un fichier Dockerfile pour chaque image personnalisée que vous souhaitez créer. Vous avez également besoin d’un fichier Dockerfile pour chaque conteneur à déployer, que vous choisissiez de le déployer automatiquement à partir de Visual Studio ou manuellement à l’aide de la CLI Docker (commandes docker run et docker-compose).</span><span class="sxs-lookup"><span data-stu-id="e8bab-150">You need a Dockerfile for each custom image you want to build; you also need a Dockerfile for each container to be deployed, whether you deploy automatically from Visual Studio or manually using the Docker CLI (docker run and docker-compose commands).</span></span> <span data-ttu-id="e8bab-151">Si votre application contient un seul service personnalisé, créez un seul fichier Dockerfile.</span><span class="sxs-lookup"><span data-stu-id="e8bab-151">If your application contains a single custom service, you need a single Dockerfile.</span></span> <span data-ttu-id="e8bab-152">Si votre application contient plusieurs services (comme dans une architecture de microservices), vous devez créer un fichier Dockerfile pour chaque service.</span><span class="sxs-lookup"><span data-stu-id="e8bab-152">If your application contains multiple services (as in a microservices architecture), you need one Dockerfile for each service.</span></span>

<span data-ttu-id="e8bab-153">Le fichier Dockerfile est créé dans le dossier racine de votre application ou service.</span><span class="sxs-lookup"><span data-stu-id="e8bab-153">The Dockerfile is placed in the root folder of your application or service.</span></span> <span data-ttu-id="e8bab-154">Il contient les commandes qui indiquent à Docker comment configurer et exécuter votre application ou service dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="e8bab-154">It contains the commands that tell Docker how to set up and run your application or service in a container.</span></span> <span data-ttu-id="e8bab-155">Vous pouvez créer manuellement un fichier Dockerfile dans le code et l’ajouter à votre projet, avec vos dépendances .NET.</span><span class="sxs-lookup"><span data-stu-id="e8bab-155">You can manually create a Dockerfile in code and add it to your project along with your .NET dependencies.</span></span>

<span data-ttu-id="e8bab-156">Avec Visual Studio Tools pour Docker, cette tâche se fait en quelques clics de souris seulement.</span><span class="sxs-lookup"><span data-stu-id="e8bab-156">With Visual Studio Tools for Docker, this task requires only a few mouse clicks.</span></span> <span data-ttu-id="e8bab-157">Quand vous créez un projet dans Visual Studio 2017, vous voyez une option nommée **Activer la prise en charge de Docker** (voir la figure 5-3).</span><span class="sxs-lookup"><span data-stu-id="e8bab-157">When you create a new project in Visual Studio 2017, there's an option named **Enable Docker Support**, as shown in Figure 5-3.</span></span>

![Option Activer la prise en charge de Docker affichée lors de la création d’un projet dans Visual Studio 2017](./media/image5.png)

<span data-ttu-id="e8bab-159">**Figure 5-3**.</span><span class="sxs-lookup"><span data-stu-id="e8bab-159">**Figure 5-3**.</span></span> <span data-ttu-id="e8bab-160">Option Activer la prise en charge de Docker affichée lors de la création d’un projet dans Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="e8bab-160">Enabling Docker Support when creating a new project in Visual Studio 2017</span></span>

<span data-ttu-id="e8bab-161">Vous pouvez aussi activer la prise en charge de Docker dans un projet d’application web .NET Core existant en cliquant avec le bouton droit sur le projet dans l’**Explorateur de solutions** et en sélectionnant **Ajouter** > **Prise en charge de Docker** (voir la figure 5-4).</span><span class="sxs-lookup"><span data-stu-id="e8bab-161">You can also enable Docker support on an existing .NET Core web app project by right-clicking the project in **Solution Explorer** and selecting **Add** > **Docker Support**, as shown in Figure 5-4.</span></span>

![Option de menu Ajouter la prise en charge de Docker dans Visual Studio](./media/add-docker-support.png)

<span data-ttu-id="e8bab-163">**Figure 5-4**.</span><span class="sxs-lookup"><span data-stu-id="e8bab-163">**Figure 5-4**.</span></span> <span data-ttu-id="e8bab-164">Activation de la prise en charge de Docker dans un projet Visual Studio 2017 existant</span><span class="sxs-lookup"><span data-stu-id="e8bab-164">Enabling Docker support in an existing Visual Studio 2017 project</span></span>

<span data-ttu-id="e8bab-165">Cette action ajoute un fichier *Dockerfile* au projet avec la configuration requise. Elle est disponible uniquement dans les projets d’application web .NET Core.</span><span class="sxs-lookup"><span data-stu-id="e8bab-165">This action adds a *Dockerfile* to the project with the required configuration, and is only available on .NET Core web app projects.</span></span>

<span data-ttu-id="e8bab-166">Pour ajouter un fichier *docker-compose.yml* pour la solution entière, cliquez avec le bouton droit sur le projet dans l’**Explorateur de solutions** et sélectionnez **Ajouter** > **Prise en charge de l’orchestrateur de conteneurs** (voir la figure 5-5).</span><span class="sxs-lookup"><span data-stu-id="e8bab-166">To add a *docker-compose.yml* file for the whole solution, right-click on the project in **Solution Explorer** and select **Add** > **Container Orchestrator Support**, as shown in Figure 5-5.</span></span>

![Option de menu Ajouter la prise en charge de l’orchestrateur de conteneurs dans Visual Studio](./media/add-container-orchestrator-support.png)

<span data-ttu-id="e8bab-168">**Figure 5-5**.</span><span class="sxs-lookup"><span data-stu-id="e8bab-168">**Figure 5-5**.</span></span> <span data-ttu-id="e8bab-169">Ajout de la prise en charge de l’orchestrateur de conteneurs à un projet existant dans Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="e8bab-169">Adding container orchestrator support to an existing project in Visual Studio 2017.</span></span>

<span data-ttu-id="e8bab-170">Dans les sections suivantes, nous décrivons les informations à ajouter dans chacun de ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="e8bab-170">In the following sections, we describe the information that goes into each of those files.</span></span> <span data-ttu-id="e8bab-171">Visual Studio peut effectuer cette tâche à votre place, mais il est utile de savoir ce que contient un fichier Dockerfile.</span><span class="sxs-lookup"><span data-stu-id="e8bab-171">Visual Studio can do this work for you, but it is useful to understand what goes into a Dockerfile.</span></span>

### <a name="option-a-creating-a-project-using-an-existing-official-net-docker-image"></a><span data-ttu-id="e8bab-172">Option A : Création d’un projet à l’aide d’une image Docker .NET officielle existante</span><span class="sxs-lookup"><span data-stu-id="e8bab-172">Option A: Creating a project using an existing official .NET Docker image</span></span>

<span data-ttu-id="e8bab-173">Le plus souvent, vous créez une image personnalisée pour votre conteneur à partir d’une image de base que vous obtenez d’un dépôt officiel dans le registre [Docker Hub](https://hub.docker.com/).</span><span class="sxs-lookup"><span data-stu-id="e8bab-173">You usually build a custom image for your container on top of a base image you can get from an official repository at the [Docker Hub](https://hub.docker.com/) registry.</span></span> <span data-ttu-id="e8bab-174">C’est précisément ce qui se passe en arrière-plan quand vous activez la prise en charge de Docker dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e8bab-174">That is precisely what happens under the covers when you enable Docker support in Visual Studio.</span></span> <span data-ttu-id="e8bab-175">Le fichier Dockerfile utilise une image aspnetcore existante.</span><span class="sxs-lookup"><span data-stu-id="e8bab-175">The Dockerfile uses an existing aspnetcore image.</span></span>

<span data-ttu-id="e8bab-176">Précédemment, nous avons expliqué quels images et dépôts Docker vous pouvez utiliser selon le framework et le système d’exploitation que vous avez choisis.</span><span class="sxs-lookup"><span data-stu-id="e8bab-176">Earlier we explained which Docker images and repos you can use, depending on the framework and OS you have chosen.</span></span> <span data-ttu-id="e8bab-177">Par exemple, si vous souhaitez utiliser ASP.NET Core (Windows ou Linux), vous devez utiliser l’image microsoft/aspnetcore:2.0.</span><span class="sxs-lookup"><span data-stu-id="e8bab-177">For instance, if you want to use ASP.NET Core (Linux or Windows), the image to use is microsoft/aspnetcore:2.0.</span></span> <span data-ttu-id="e8bab-178">La seule chose à faire est donc de spécifier l’image Docker de base à utiliser pour votre conteneur.</span><span class="sxs-lookup"><span data-stu-id="e8bab-178">Therefore, you just need to specify what base Docker image you will use for your container.</span></span> <span data-ttu-id="e8bab-179">Pour cela, vous ajoutez FROM microsoft/aspnetcore:2.0 dans votre fichier Dockerfile.</span><span class="sxs-lookup"><span data-stu-id="e8bab-179">You do that by adding FROM microsoft/aspnetcore:2.0 to your Dockerfile.</span></span> <span data-ttu-id="e8bab-180">Cette opération est effectuée automatiquement par Visual Studio, mais si vous avez à mettre à jour la version, vous devez modifier cette valeur.</span><span class="sxs-lookup"><span data-stu-id="e8bab-180">This is automatically performed by Visual Studio, but if you were to update the version, you update this value.</span></span>

<span data-ttu-id="e8bab-181">L’utilisation d’un dépôt d’images .NET officiel fourni dans le Docker Hub avec un numéro de version garantit que les mêmes fonctionnalités de langage sont disponibles sur toutes les machines (y compris celles de développement, test et production).</span><span class="sxs-lookup"><span data-stu-id="e8bab-181">Using an official .NET image repository from Docker Hub with a version number ensures that the same language features are available on all machines (including development, testing, and production).</span></span>

<span data-ttu-id="e8bab-182">L’extrait de code suivant est un exemple de fichier Dockerfile pour un conteneur ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="e8bab-182">The following example shows a sample Dockerfile for an ASP.NET Core container.</span></span>

```Dockerfile
FROM microsoft/aspnetcore:2.0

ARG source

WORKDIR /app

EXPOSE 80

COPY ${source:-obj/Docker/publish} .

ENTRYPOINT ["dotnet", " MySingleContainerWebApp.dll "]
```

<span data-ttu-id="e8bab-183">Dans ce cas, le conteneur est basé sur la version 2.0 de l’image Docker ASP.NET Core officielle (multi-arch pour Linux et Windows).</span><span class="sxs-lookup"><span data-stu-id="e8bab-183">In this case, the container is based on version 2.0 of the official ASP.NET Core Docker image (multi-arch for Linux and Windows).</span></span> <span data-ttu-id="e8bab-184">Il s’agit du paramètre `FROM microsoft/aspnetcore:2.0`.</span><span class="sxs-lookup"><span data-stu-id="e8bab-184">This is the setting `FROM microsoft/aspnetcore:2.0`.</span></span> <span data-ttu-id="e8bab-185">(Pour plus d’informations sur cette image de base, consultez la page [Image Docker ASP.NET Core](https://hub.docker.com/r/microsoft/aspnetcore/) et la page [Image Docker .NET Core](https://hub.docker.com/r/microsoft/dotnet/).) Dans le fichier Dockerfile, vous devez également indiquer à Docker d’écouter le port TCP qui sera utilisé au moment de l’exécution (dans cet exemple, le port 80 est configuré avec le paramètre EXPOSE).</span><span class="sxs-lookup"><span data-stu-id="e8bab-185">(For more information about this base image, see the [ASP.NET Core Docker Image](https://hub.docker.com/r/microsoft/aspnetcore/) page and the [.NET Core Docker Image](https://hub.docker.com/r/microsoft/dotnet/) page.) In the Dockerfile, you also need to instruct Docker to listen on the TCP port you will use at runtime (in this case, port 80, as configured with the EXPOSE setting).</span></span>

<span data-ttu-id="e8bab-186">Vous pouvez spécifier des paramètres de configuration supplémentaires dans le fichier Dockerfile, en fonction du langage et du framework que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="e8bab-186">You can specify additional configuration settings in the Dockerfile, depending on the language and framework you are using.</span></span> <span data-ttu-id="e8bab-187">Par exemple, la ligne ENTRYPOINT avec \["dotnet", "MySingleContainerWebApp.dll"\] indique à Docker d’exécuter une application .NET Core.</span><span class="sxs-lookup"><span data-stu-id="e8bab-187">For instance, the ENTRYPOINT line with \["dotnet", "MySingleContainerWebApp.dll"\] tells Docker to run a .NET Core application.</span></span> <span data-ttu-id="e8bab-188">Si vous utilisez le SDK et l’interface CLI (dotnet) de .NET Core pour créer et exécuter l’application .NET, ce paramètre est différent.</span><span class="sxs-lookup"><span data-stu-id="e8bab-188">If you are using the SDK and the .NET Core CLI (dotnet CLI) to build and run the .NET application, this setting would be different.</span></span> <span data-ttu-id="e8bab-189">L’essentiel à retenir est que la ligne ENTRYPOINT et certains autres paramètres varient selon le langage et la plateforme choisis pour votre application.</span><span class="sxs-lookup"><span data-stu-id="e8bab-189">The bottom line is that the ENTRYPOINT line and other settings will be different depending on the language and platform you choose for your application.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="e8bab-190">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e8bab-190">Additional resources</span></span>

- <span data-ttu-id="e8bab-191">**Création d’images Docker pour les applications .NET Core**</span><span class="sxs-lookup"><span data-stu-id="e8bab-191">**Building Docker Images for .NET Core Applications**</span></span>

   [*https://docs.microsoft.com/dotnet/core/docker/building-net-docker-images*](../../../core/docker/building-net-docker-images.md)

- <span data-ttu-id="e8bab-192">**Créer votre propre image**.</span><span class="sxs-lookup"><span data-stu-id="e8bab-192">**Build your own image**.</span></span> <span data-ttu-id="e8bab-193">Documentation officielle de Docker.</span><span class="sxs-lookup"><span data-stu-id="e8bab-193">In the official Docker documentation.</span></span>

   [*https://docs.docker.com/engine/tutorials/dockerimages/*](https://docs.docker.com/engine/tutorials/dockerimages/)

### <a name="using-multi-arch-image-repositories"></a><span data-ttu-id="e8bab-194">Utilisation de dépôts d’images multi-arch</span><span class="sxs-lookup"><span data-stu-id="e8bab-194">Using multi-arch image repositories</span></span>

<span data-ttu-id="e8bab-195">Un dépôt peut contenir des variantes de plateforme, comme une image Linux et une image Windows.</span><span class="sxs-lookup"><span data-stu-id="e8bab-195">A single repo can contain platform variants, such as a Linux image and a Windows image.</span></span> <span data-ttu-id="e8bab-196">Cette fonctionnalité permet aux fournisseurs comme Microsoft (créateurs d’images de base) de créer un dépôt commun pour plusieurs plateformes (Linux et Windows).</span><span class="sxs-lookup"><span data-stu-id="e8bab-196">This feature allows vendors like Microsoft (base image creators) to create a single repo to cover multiple platforms (that is Linux and Windows).</span></span> <span data-ttu-id="e8bab-197">Par exemple, le dépôt [microsoft/dotnet](https://hub.docker.com/r/microsoft/aspnetcore/) disponible dans le registre Docker Hub fournit une prise en charge de Linux et Windows Nano Server en utilisant le même nom de dépôt.</span><span class="sxs-lookup"><span data-stu-id="e8bab-197">For example, the [microsoft/dotnet](https://hub.docker.com/r/microsoft/aspnetcore/) repository available in the Docker Hub registry provides support for Linux and Windows Nano Server by using the same repo name.</span></span>

<span data-ttu-id="e8bab-198">Si vous spécifiez une balise, le ciblage d’une plateforme est explicite, comme dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="e8bab-198">If you specify a tag, targeting a platform that is explicit like in the following cases:</span></span>

- <span data-ttu-id="e8bab-199">**microsoft/aspnetcore:2.0.0-jessie**</span><span class="sxs-lookup"><span data-stu-id="e8bab-199">**microsoft/aspnetcore:2.0.0-jessie**</span></span>

        .NET Core 2.0 runtime-only on Linux

- <span data-ttu-id="e8bab-200">**microsoft/aspnetcore:2.0.0-nanoserver**</span><span class="sxs-lookup"><span data-stu-id="e8bab-200">**microsoft/aspnetcore:2.0.0-nanoserver**</span></span>

        .NET Core 2.0 runtime-only on Windows Nano Server

<span data-ttu-id="e8bab-201">Cependant, et cela est nouveau depuis le milieu de l’année 2017, si vous spécifiez le même nom d’image avec la même balise, les nouvelles images multi-arch (comme l’image aspnetcore, qui prend en charge multi-arch) utiliseront la version Windows ou Linux selon le système d’exploitation de l’hôte Docker que vous déployez, comme cela est montré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="e8bab-201">But, and this is new since mid-2017, if you specify the same image name, even with the same tag, the new multi-arch images (like the aspnetcore image, which supports multi-arch) will use the Linux or Windows version depending on the Docker host OS you are deploying, as shown in the following example:</span></span>

- <span data-ttu-id="e8bab-202">**microsoft/aspnetcore:2.0**</span><span class="sxs-lookup"><span data-stu-id="e8bab-202">**microsoft/aspnetcore:2.0**</span></span>

        Multi-arch: .NET Core 2.0 runtime-only on Linux or Windows Nano Server depending on the Docker host OS

<span data-ttu-id="e8bab-203">Ainsi, quand vous tirez (pull) une image d’un hôte Windows, la variante Windows est tirée et quand vous tirez le même nom d’image d’un hôte Linux, la variante Linux est tirée.</span><span class="sxs-lookup"><span data-stu-id="e8bab-203">This way, when you pull an image from a Windows host, it will pull the Windows variant, and pulling the same image name from a Linux host will pull the Linux variant.</span></span>

### <a name="option-b-creating-your-base-image-from-scratch"></a><span data-ttu-id="e8bab-204">Option B : Créer votre image de base à partir de zéro</span><span class="sxs-lookup"><span data-stu-id="e8bab-204">Option B: Creating your base image from scratch</span></span>

<span data-ttu-id="e8bab-205">Vous pouvez créer votre propre image de base Docker à partir de zéro.</span><span class="sxs-lookup"><span data-stu-id="e8bab-205">You can create your own Docker base image from scratch.</span></span> <span data-ttu-id="e8bab-206">Ce scénario n’est pas recommandé si vous n’êtes pas encore familiarisé avec Docker, mais si vous souhaitez définir les bits spécifiques de votre propre image de base, vous pouvez le faire.</span><span class="sxs-lookup"><span data-stu-id="e8bab-206">This scenario is not recommended for someone who is starting with Docker, but if you want to set the specific bits of your own base image, you can do so.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="e8bab-207">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e8bab-207">Additional resources</span></span>

- <span data-ttu-id="e8bab-208">**Images .NET Core multi-arch**.</span><span class="sxs-lookup"><span data-stu-id="e8bab-208">**Multi-arch .NET Core images**.</span></span>

   https://github.com/dotnet/announcements/issues/14

- <span data-ttu-id="e8bab-209">**Créer une image de base**.</span><span class="sxs-lookup"><span data-stu-id="e8bab-209">**Create a base image**.</span></span> <span data-ttu-id="e8bab-210">Documentation officielle de Docker.</span><span class="sxs-lookup"><span data-stu-id="e8bab-210">Official Docker documentation.</span></span>

   [*https://docs.docker.com/engine/userguide/eng-image/baseimages/*](https://docs.docker.com/engine/userguide/eng-image/baseimages/)

![Image de l’étape 3, « Create images »](./media/image7.png)

## <a name="step-3-create-your-custom-docker-images-and-embed-your-application-or-service-in-them"></a><span data-ttu-id="e8bab-212">Étape 3.</span><span class="sxs-lookup"><span data-stu-id="e8bab-212">Step 3.</span></span> <span data-ttu-id="e8bab-213">Créer vos images Docker personnalisées et incorporer votre application ou service dans ces images</span><span class="sxs-lookup"><span data-stu-id="e8bab-213">Create your custom Docker images and embed your application or service in them</span></span>

<span data-ttu-id="e8bab-214">Pour chaque service inclus dans votre application, vous devez créer une image associée.</span><span class="sxs-lookup"><span data-stu-id="e8bab-214">For each service in your application, you need to create a related image.</span></span> <span data-ttu-id="e8bab-215">Si votre application est composée uniquement d’un service ou d’une application web, vous avez besoin d’une seule image.</span><span class="sxs-lookup"><span data-stu-id="e8bab-215">If your application is made up of a single service or web application, you just need a single image.</span></span>

<span data-ttu-id="e8bab-216">Les images Docker sont créées automatiquement dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e8bab-216">The Docker images are built automatically for you in Visual Studio.</span></span> <span data-ttu-id="e8bab-217">Les étapes suivantes s’appliquent uniquement dans le cadre du workflow avec un éditeur ou une CLI. Elles sont expliquées pour vous permettre de bien en comprendre tous les dessous.</span><span class="sxs-lookup"><span data-stu-id="e8bab-217">The following steps are only needed for the editor/CLI workflow and explained for clarity about what happens underneath.</span></span>

<span data-ttu-id="e8bab-218">En tant que développeur, vous avez besoin d’écrire du code et de le tester localement avant de pousser (push) une fonctionnalité ou un changement terminé à votre système de contrôle de code source (par exemple, à GitHub).</span><span class="sxs-lookup"><span data-stu-id="e8bab-218">You, as developer, need to develop and test locally until you push a completed feature or change to your source control system (for example, to GitHub).</span></span> <span data-ttu-id="e8bab-219">Cela signifie que vous devez créer les images Docker et déployer des conteneurs sur un hôte Docker local (machine virtuelle Windows ou Linux), et exécuter, tester et déboguer dans ces conteneurs locaux.</span><span class="sxs-lookup"><span data-stu-id="e8bab-219">This means that you need to create the Docker images and deploy containers to a local Docker host (Windows or Linux VM) and run, test, and debug against those local containers.</span></span>

<span data-ttu-id="e8bab-220">Pour créer une image personnalisée dans votre environnement local avec la CLI Docker et votre fichier Dockerfile, vous pouvez utiliser la commande docker build (voir la figure 5-5).</span><span class="sxs-lookup"><span data-stu-id="e8bab-220">To create a custom image in your local environment by using Docker CLI and your Dockerfile, you can use the docker build command, as in Figure 5-5.</span></span>

![Création d’une image Docker personnalisée](./media/image8.png)

<span data-ttu-id="e8bab-222">**Figure 5-5**.</span><span class="sxs-lookup"><span data-stu-id="e8bab-222">**Figure 5-5**.</span></span> <span data-ttu-id="e8bab-223">Création d’une image Docker personnalisée</span><span class="sxs-lookup"><span data-stu-id="e8bab-223">Creating a custom Docker image</span></span>

<span data-ttu-id="e8bab-224">Si vous le souhaitez, au lieu d’exécuter la commande docker build directement à partir du dossier de projet, vous pouvez d’abord exécuter la commande dotnet publish pour créer un dossier déployable contenant les binaires et bibliothèques .NET nécessaires, puis utiliser la commande docker build.</span><span class="sxs-lookup"><span data-stu-id="e8bab-224">Optionally, instead of directly running docker build from the project folder, you can first generate a deployable folder with the required .NET libraries and binaries by running dotnet publish, and then use the docker build command.</span></span>

<span data-ttu-id="e8bab-225">Cela crée une image Docker nommée **cesardl/netcore-webapi-microservice-docker:first**.</span><span class="sxs-lookup"><span data-stu-id="e8bab-225">This will create a Docker image with the name **cesardl/netcore-webapi-microservice-docker:first**.</span></span> <span data-ttu-id="e8bab-226">Dans ce cas, :first est une balise qui représente une version spécifique.</span><span class="sxs-lookup"><span data-stu-id="e8bab-226">In this case, :first is a tag representing a specific version.</span></span> <span data-ttu-id="e8bab-227">Vous pouvez répéter cette étape pour chaque image personnalisée à créer pour votre application Docker composée.</span><span class="sxs-lookup"><span data-stu-id="e8bab-227">You can repeat this step for each custom image you need to create for your composed Docker application.</span></span>

<span data-ttu-id="e8bab-228">Quand une application est constituée de plusieurs conteneurs (c’est donc une application multiconteneur), vous pouvez également utiliser la commande docker-compose up --build pour créer toutes les images associées avec une seule commande à l’aide des métadonnées exposées dans les fichiers docker-compose.yml associés.</span><span class="sxs-lookup"><span data-stu-id="e8bab-228">When an application is made of multiple containers (that is, it is a multi-container application), you can also use the docker-compose up --build command to build all the related images with a single command by using the metadata exposed in the related docker-compose.yml files.</span></span>

<span data-ttu-id="e8bab-229">Vous pouvez rechercher les images existantes dans votre dépôt local avec la commande docker images (voir la figure 5-6).</span><span class="sxs-lookup"><span data-stu-id="e8bab-229">You can find the existing images in your local repository by using the docker images command, as shown in Figure 5-6.</span></span>

![Affichage des images existantes à l’aide de la commande docker images](./media/image9.png)

<span data-ttu-id="e8bab-231">**Figure 5-6.**</span><span class="sxs-lookup"><span data-stu-id="e8bab-231">**Figure 5-6.**</span></span> <span data-ttu-id="e8bab-232">Affichage des images existantes à l’aide de la commande docker images</span><span class="sxs-lookup"><span data-stu-id="e8bab-232">Viewing existing images using the docker images command</span></span>

### <a name="creating-docker-images-with-visual-studio"></a><span data-ttu-id="e8bab-233">Création d’images Docker avec Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e8bab-233">Creating Docker images with Visual Studio</span></span>

<span data-ttu-id="e8bab-234">Quand vous utilisez Visual Studio pour créer un projet avec la prise en charge de Docker, vous ne créez pas une image explicitement.</span><span class="sxs-lookup"><span data-stu-id="e8bab-234">When you use Visual Studio to create a project with Docker support, you don't explicitly create an image.</span></span> <span data-ttu-id="e8bab-235">En fait, l’image est créée quand vous appuyez sur **F5** pour exécuter l’application ou le service Docker.</span><span class="sxs-lookup"><span data-stu-id="e8bab-235">Instead, the image is created for you when you press **F5** to run the dockerized application or service.</span></span> <span data-ttu-id="e8bab-236">Cette étape est automatique dans Visual Studio. Vous ne la verrez donc pas à l’écran, mais il est important d’en comprendre le mécanisme.</span><span class="sxs-lookup"><span data-stu-id="e8bab-236">This step is automatic in Visual Studio and you won't see it happen, but it's important that you know what's going on underneath.</span></span>

![Image de l’étape 4, « Define services »](./media/image10.png)

## <a name="step-4-define-your-services-in-docker-composeyml-when-building-a-multi-container-docker-application"></a><span data-ttu-id="e8bab-238">Étape 4.</span><span class="sxs-lookup"><span data-stu-id="e8bab-238">Step 4.</span></span> <span data-ttu-id="e8bab-239">Définir vos services dans docker-compose.yml lors de la création d’une application Docker multiconteneur</span><span class="sxs-lookup"><span data-stu-id="e8bab-239">Define your services in docker-compose.yml when building a multi-container Docker application</span></span>

<span data-ttu-id="e8bab-240">Le fichier [docker-compose.yml](https://docs.docker.com/compose/compose-file/) vous permet de définir un ensemble de services à déployer ensemble comme application composée avec les commandes de déploiement.</span><span class="sxs-lookup"><span data-stu-id="e8bab-240">The [docker-compose.yml](https://docs.docker.com/compose/compose-file/) file lets you define a set of related services to be deployed as a composed application with deployment commands.</span></span>

<span data-ttu-id="e8bab-241">Pour utiliser un fichier docker-compose.yml, vous devez d’abord le créer dans votre dossier solution principal ou racine. Le contenu du fichier doit être semblable à l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="e8bab-241">To use a docker-compose.yml file, you need to create the file in your main or root solution folder, with content similar to that in the following example:</span></span>

```yml
version: '3'

services:

  webmvc:
    image: eshop/web
    environment:
      - CatalogUrl=http://catalog.api
      - OrderingUrl=http://ordering.api
    ports:
      - "80:80"
    depends_on:
      - catalog.api
      - ordering.api

  catalog.api:
    image: eshop/catalog.api
    environment:
      - ConnectionString=Server=sql.data;Database=CatalogDB;…
    ports:
      - "81:80"
    depends_on:
      - sql.data

  ordering.api:
    image: eshop/ordering.api
    environment:
      - ConnectionString=Server=sql.data;Database=OrderingDb;…
    ports:
      - "82:80"
    extra_hosts:
      - "CESARDLBOOKVHD:10.0.75.1"
    depends_on:
      - sql.data

  sql.data:
    image: mssql-server-linux:latest
    environment:
      - SA_PASSWORD=Pass@word
      - ACCEPT_EULA=Y
    ports:
      - "5433:1433"
```

<span data-ttu-id="e8bab-242">Ce fichier docker-compose.yml est une version simplifiée et fusionnée.</span><span class="sxs-lookup"><span data-stu-id="e8bab-242">This docker-compose.yml file is a simplified and merged version.</span></span> <span data-ttu-id="e8bab-243">Il contient des données de configuration statiques pour chaque conteneur (comme le nom de l’image personnalisée), qui s’appliquent toujours, ainsi que des informations de configuration variables selon l’environnement de déploiement, comme la chaîne de connexion.</span><span class="sxs-lookup"><span data-stu-id="e8bab-243">It contains static configuration data for each container (like the name of the custom image), which always applies, plus configuration information that might depend on the deployment environment, like the connection string.</span></span> <span data-ttu-id="e8bab-244">Dans des sections ultérieures, vous découvrirez comment vous pouvez fractionner le fichier de configuration docker-compose.yml en plusieurs fichiers docker-compose et substituer les valeurs en fonction de l’environnement et du type d’exécution (debug ou release).</span><span class="sxs-lookup"><span data-stu-id="e8bab-244">In later sections, you will learn how you can split the docker-compose.yml configuration into multiple docker-compose files and override values depending on the environment and execution type (debug or release).</span></span>

<span data-ttu-id="e8bab-245">L’exemple de fichier docker-compose.yml définit quatre services : le service webmvc (une application web), deux microservices (catalog.api et ordering.api), et un conteneur source de données (sql.data), basé sur SQL Server pour Linux exécuté en tant que conteneur.</span><span class="sxs-lookup"><span data-stu-id="e8bab-245">The docker-compose.yml file example defines four services: the webmvc service (a web application), two microservices (catalog.api and ordering.api), and one data source container, sql.data, based on SQL Server for Linux running as a container.</span></span> <span data-ttu-id="e8bab-246">Chaque service étant déployé en tant que conteneur, une image Docker est nécessaire pour chacun.</span><span class="sxs-lookup"><span data-stu-id="e8bab-246">Each service is deployed as a container, so a Docker image is required for each.</span></span>

<span data-ttu-id="e8bab-247">Le fichier docker-compose.yml spécifie les conteneurs utilisés, mais aussi la configuration de chaque conteneur.</span><span class="sxs-lookup"><span data-stu-id="e8bab-247">The docker-compose.yml file specifies not only what containers are being used, but how they are individually configured.</span></span> <span data-ttu-id="e8bab-248">Par exemple, la définition du conteneur webmvc dans le fichier .yml :</span><span class="sxs-lookup"><span data-stu-id="e8bab-248">For instance, the webmvc container definition in the .yml file:</span></span>

- <span data-ttu-id="e8bab-249">Utilise une image eshop/web:latest précréée.</span><span class="sxs-lookup"><span data-stu-id="e8bab-249">Uses a pre-built eshop/web:latest image.</span></span> <span data-ttu-id="e8bab-250">Toutefois, vous pouvez également configurer l’image à créer à l’exécution de docker-compose avec une configuration supplémentaire basée sur une section :build dans le fichier docker-compose.</span><span class="sxs-lookup"><span data-stu-id="e8bab-250">However, you could also configure the image to be built as part of the docker-compose execution with an additional configuration based on a build: section in the docker-compose file.</span></span>

- <span data-ttu-id="e8bab-251">Initialise deux variables d’environnement (CatalogUrl et OrderingUrl).</span><span class="sxs-lookup"><span data-stu-id="e8bab-251">Initializes two environment variables (CatalogUrl and OrderingUrl).</span></span>

- <span data-ttu-id="e8bab-252">Transfère le port exposé 80 sur le conteneur vers le port externe 80 sur la machine hôte.</span><span class="sxs-lookup"><span data-stu-id="e8bab-252">Forwards the exposed port 80 on the container to the external port 80 on the host machine.</span></span>

- <span data-ttu-id="e8bab-253">Lie l’application web aux services catalog et ordering avec le paramètre depends\_on.</span><span class="sxs-lookup"><span data-stu-id="e8bab-253">Links the web app to the catalog and ordering service with the depends\_on setting.</span></span> <span data-ttu-id="e8bab-254">Cela force le service à attendre le démarrage de ces services.</span><span class="sxs-lookup"><span data-stu-id="e8bab-254">This causes the service to wait until those services are started.</span></span>

<span data-ttu-id="e8bab-255">Nous reparlerons du fichier docker-compose.yml dans une section ultérieure, quand nous expliquerons comment implémenter des microservices et des applications multiconteneurs.</span><span class="sxs-lookup"><span data-stu-id="e8bab-255">We will revisit the docker-compose.yml file in a later section when we cover how to implement microservices and multi-container apps.</span></span>

### <a name="working-with-docker-composeyml-in-visual-studio-2017"></a><span data-ttu-id="e8bab-256">Utilisation de docker-compose.yml dans Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="e8bab-256">Working with docker-compose.yml in Visual Studio 2017</span></span>

<span data-ttu-id="e8bab-257">Quand vous ajoutez la prise en charge de l’orchestrateur de conteneurs à un projet d’application web, comme illustré à la figure 5-7, Visual Studio ajoute une section service (projet) à la solution qui contient un fichier docker-compose.yml.</span><span class="sxs-lookup"><span data-stu-id="e8bab-257">When you add container orchestrator support to a web app project, as shown in Figure 5-7, Visual Studio adds a service section (project) to the solution that contains a docker-compose.yml file.</span></span> <span data-ttu-id="e8bab-258">C’est une méthode simple pour commencer à composer une solution multiconteneur.</span><span class="sxs-lookup"><span data-stu-id="e8bab-258">This is an easy way to start composing a multiple-container solution.</span></span>

![Élément de menu Ajouter la prise en charge de l’orchestrateur de conteneurs dans Visual Studio](./media/add-container-orchestrator-support.png)

<span data-ttu-id="e8bab-260">**Figure 5-7**.</span><span class="sxs-lookup"><span data-stu-id="e8bab-260">**Figure 5-7**.</span></span> <span data-ttu-id="e8bab-261">Ajout de la prise en charge de Docker dans Visual Studio 2017 en cliquant avec le bouton droit sur un projet ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="e8bab-261">Adding Docker support in Visual Studio 2017 by right-clicking an ASP.NET Core project</span></span>

<span data-ttu-id="e8bab-262">L’ajout de la prise en charge de l’orchestrateur de conteneurs ajoute le fichier Dockerfile à votre projet (s’il n’existe pas déjà).</span><span class="sxs-lookup"><span data-stu-id="e8bab-262">Adding container orchestrator support adds the Dockerfile to your project (if it doesn't already exist).</span></span> <span data-ttu-id="e8bab-263">Cette opération ajoute également des informations de configuration dans un fichier docker-compose.yml global au niveau de la solution.</span><span class="sxs-lookup"><span data-stu-id="e8bab-263">It also adds configuration information to a global docker-compose.yml file at the solution level.</span></span> <span data-ttu-id="e8bab-264">Vous voyez un nouveau nœud de projet (le fichier projet *docker-compose.dcproj*) dans l’**Explorateur de solutions** qui contient le fichier docker-compose.yml (voir la figure 5-8).</span><span class="sxs-lookup"><span data-stu-id="e8bab-264">You'll see a new project node (the *docker-compose.dcproj* project file) in **Solution Explorer** that contains the docker-compose.yml file, as shown in Figure 5-8.</span></span>

![Nœud docker-compose dans l’Explorateur de solutions](./media/docker-compose-files.png)

<span data-ttu-id="e8bab-266">**Figure 5-8**.</span><span class="sxs-lookup"><span data-stu-id="e8bab-266">**Figure 5-8**.</span></span> <span data-ttu-id="e8bab-267">Nœud d’arborescence **docker-compose** ajouté dans l’Explorateur de solutions de Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="e8bab-267">The **docker-compose** tree node added in Visual Studio 2017 Solution Explorer</span></span>

<span data-ttu-id="e8bab-268">Vous pouvez ensuite ouvrir le fichier docker-compose.yml et le mettre à jour avec des fonctionnalités supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e8bab-268">You can then open the docker-compose.yml file and update it with additional features.</span></span>

<span data-ttu-id="e8bab-269">Vous pouvez aussi déployer une application multiconteneur avec un seul fichier docker-compose.yml en utilisant la commande `docker-compose up`.</span><span class="sxs-lookup"><span data-stu-id="e8bab-269">You can deploy a multi-container application with a single docker-compose.yml file by using the `docker-compose up` command.</span></span>

![Image de l’étape 5, « Run app »](./media/image12.png)

## <a name="step-5-build-and-run-your-docker-application"></a><span data-ttu-id="e8bab-271">Étape 5.</span><span class="sxs-lookup"><span data-stu-id="e8bab-271">Step 5.</span></span> <span data-ttu-id="e8bab-272">Générer et exécuter votre application Docker</span><span class="sxs-lookup"><span data-stu-id="e8bab-272">Build and run your Docker application</span></span>

<span data-ttu-id="e8bab-273">Si votre application n’a qu’un seul conteneur, vous pouvez l’exécuter en la déployant sur l’hôte Docker (machine virtuelle ou serveur physique).</span><span class="sxs-lookup"><span data-stu-id="e8bab-273">If your application only has a single container, you can run it by deploying it to your Docker host (VM or physical server).</span></span> <span data-ttu-id="e8bab-274">Si votre application contient plusieurs services, vous pouvez la déployer comme une application composée, soit à l’aide d’une seule commande CLI (docker-compose up), soit avec Visual Studio, qui utilise cette commande en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="e8bab-274">However, if your application contains multiple services, you can deploy it as a composed application, either using a single CLI command (docker-compose up), or with Visual Studio, which will use that command under the covers.</span></span> <span data-ttu-id="e8bab-275">Examinons les différentes options.</span><span class="sxs-lookup"><span data-stu-id="e8bab-275">Let’s look at the different options.</span></span>

### <a name="option-a-run-a-single-container-app"></a><span data-ttu-id="e8bab-276">Option A : Exécuter une application monoconteneur</span><span class="sxs-lookup"><span data-stu-id="e8bab-276">Option A: Run a single-container app</span></span>

#### <a name="docker-cli"></a><span data-ttu-id="e8bab-277">CLI Docker</span><span class="sxs-lookup"><span data-stu-id="e8bab-277">Docker CLI</span></span>

<span data-ttu-id="e8bab-278">Vous pouvez exécuter un conteneur Docker à l’aide de la commande docker run, comme dans la figure 5-9 ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="e8bab-278">You can run a Docker container using the docker run command, as in Figure 5-9:</span></span>

```console
  docker run -t -d -p 80:5000 cesardl/netcore-webapi-microservice-docker:first
```

![Exécution d’un conteneur Docker à l’aide de la commande docker run](./media/image13.png)

<span data-ttu-id="e8bab-280">**Figure 5-9**.</span><span class="sxs-lookup"><span data-stu-id="e8bab-280">**Figure 5-9**.</span></span> <span data-ttu-id="e8bab-281">Exécution d’un conteneur Docker à l’aide de la commande docker run</span><span class="sxs-lookup"><span data-stu-id="e8bab-281">Running a Docker container using the docker run command</span></span>

<span data-ttu-id="e8bab-282">Dans ce cas, la commande lie le port interne 5000 du conteneur au port 80 de la machine hôte.</span><span class="sxs-lookup"><span data-stu-id="e8bab-282">In this case, the command binds the internal port 5000 of the container to port 80 of the host machine.</span></span> <span data-ttu-id="e8bab-283">Cela signifie que l’hôte écoute le port 80 et transfère le port sur le port 5000 sur le conteneur.</span><span class="sxs-lookup"><span data-stu-id="e8bab-283">This means that the host is listening on port 80 and forwarding to port 5000 on the container.</span></span>

#### <a name="visual-studio"></a><span data-ttu-id="e8bab-284">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e8bab-284">Visual Studio</span></span>

<span data-ttu-id="e8bab-285">Si vous n’avez pas ajouté la prise en charge de l’orchestrateur de conteneurs, vous pouvez également exécuter une application monoconteneur dans Visual Studio, en appuyant sur **F5**.</span><span class="sxs-lookup"><span data-stu-id="e8bab-285">If you haven't added container orchestrator support, you can also run a single container app in Visual Studio by pressing **F5**.</span></span> <span data-ttu-id="e8bab-286">Avec docker run, le conteneur s’exécute localement.</span><span class="sxs-lookup"><span data-stu-id="e8bab-286">The container runs locally using docker run.</span></span>

### <a name="option-b-run-a-multi-container-app"></a><span data-ttu-id="e8bab-287">Option B : Exécuter une application multiconteneur</span><span class="sxs-lookup"><span data-stu-id="e8bab-287">Option B: Run a multi-container app</span></span>

<span data-ttu-id="e8bab-288">Dans la plupart des scénarios d’entreprise, une application Docker est composée de plusieurs services, ce qui signifie que vous devez exécuter une application multiconteneur, comme illustré à la figure 5-10.</span><span class="sxs-lookup"><span data-stu-id="e8bab-288">In most enterprise scenarios, a Docker application will be composed of multiple services, which means you need to run a multi-container application, as shown in Figure 5-10.</span></span>

![Image illustrant une machine virtuelle avec des conteneurs Docker déployés](./media/image14.png)

<span data-ttu-id="e8bab-290">**Figure 5-10**.</span><span class="sxs-lookup"><span data-stu-id="e8bab-290">**Figure 5-10**.</span></span> <span data-ttu-id="e8bab-291">Machine virtuelle avec des conteneurs Docker déployés</span><span class="sxs-lookup"><span data-stu-id="e8bab-291">VM with Docker containers deployed</span></span>

#### <a name="docker-cli"></a><span data-ttu-id="e8bab-292">CLI Docker</span><span class="sxs-lookup"><span data-stu-id="e8bab-292">Docker CLI</span></span>

<span data-ttu-id="e8bab-293">Pour exécuter une application multiconteneur avec la CLI Docker, exécutez la commande docker-compose up.</span><span class="sxs-lookup"><span data-stu-id="e8bab-293">To run a multi-container application with the Docker CLI, you can run the docker-compose up command.</span></span> <span data-ttu-id="e8bab-294">Cette commande utilise le fichier docker-compose.yml défini au niveau de la solution pour déployer une application multiconteneur.</span><span class="sxs-lookup"><span data-stu-id="e8bab-294">This command uses the docker-compose.yml file that you have at the solution level to deploy a multi-container application.</span></span> <span data-ttu-id="e8bab-295">La figure 5-11 montre les résultats de l’exécution de la commande à partir de votre répertoire de projet principal, qui contient le fichier docker-compose.yml.</span><span class="sxs-lookup"><span data-stu-id="e8bab-295">Figure 5-11 shows the results when running the command from your main project directory, which contains the docker-compose.yml file.</span></span>

![Exemple de résultats de l’exécution de la commande docker-compose up](./media/image15.png)

<span data-ttu-id="e8bab-297">**Figure 5-11**.</span><span class="sxs-lookup"><span data-stu-id="e8bab-297">**Figure 5-11**.</span></span> <span data-ttu-id="e8bab-298">Exemple de résultats de l’exécution de la commande docker-compose up</span><span class="sxs-lookup"><span data-stu-id="e8bab-298">Example results when running the docker-compose up command</span></span>

<span data-ttu-id="e8bab-299">Après l’exécution de la commande docker-compose up, l’application et ses conteneurs associés sont déployés sur votre hôte Docker.</span><span class="sxs-lookup"><span data-stu-id="e8bab-299">After the docker-compose up command runs, the application and its related containers are deployed into your Docker host.</span></span>

#### <a name="visual-studio"></a><span data-ttu-id="e8bab-300">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e8bab-300">Visual Studio</span></span>

<span data-ttu-id="e8bab-301">L’exécution d’une application multiconteneur à l’aide de Visual Studio 2017 est simple.</span><span class="sxs-lookup"><span data-stu-id="e8bab-301">Running a multi-container application using Visual Studio 2017 is simple.</span></span> <span data-ttu-id="e8bab-302">En plus d’exécuter l’application multiconteneur, vous pouvez déboguer tous ses conteneurs directement dans Visual Studio en définissant des points d’arrêt réguliers.</span><span class="sxs-lookup"><span data-stu-id="e8bab-302">Not only can you run the multi-container application, but you're able to debug all its containers directly from Visual Studio by setting regular breakpoints.</span></span>

<span data-ttu-id="e8bab-303">Comme nous l’avons mentionné plus haut, chaque fois que vous ajoutez la prise en charge de l’orchestrateur de conteneurs à un projet dans une solution, ce projet est configuré dans le fichier docker-compose.yml global (au niveau de la solution), ce qui vous permet d’exécuter ou de déboguer la solution dans son intégralité.</span><span class="sxs-lookup"><span data-stu-id="e8bab-303">As mentioned before, each time you add container orchestrator support to a project within a solution, that project is configured in the global (solution-level) docker-compose.yml file, which lets you run or debug the whole solution at once.</span></span> <span data-ttu-id="e8bab-304">Visual Studio démarre un conteneur pour chaque projet pour lequel la prise en charge de la solution Docker est activée, puis il effectue automatiquement toutes les étapes internes (dotnet publish, docker build, etc.).</span><span class="sxs-lookup"><span data-stu-id="e8bab-304">Visual Studio will start one container for each project that has Docker solution support enabled and perform all the internal steps for you (dotnet publish, docker build, etc.).</span></span>

<span data-ttu-id="e8bab-305">Le point important ici est que, comme indiqué dans la figure 5-12, Visual Studio 2017 fournit une commande **Docker** supplémentaire associée à l’action de la touche **F5**.</span><span class="sxs-lookup"><span data-stu-id="e8bab-305">The important point here is that, as shown in Figure 5-12, in Visual Studio 2017 there's an additional **Docker** command for the **F5** key action.</span></span> <span data-ttu-id="e8bab-306">Cette option vous permet d’exécuter ou de déboguer une application multiconteneur en exécutant tous les conteneurs qui sont définis dans les fichiers docker-compose.yml au niveau de la solution.</span><span class="sxs-lookup"><span data-stu-id="e8bab-306">This option lets you run or debug a multi-container application by running all the containers that are defined in the docker-compose.yml files at the solution level.</span></span> <span data-ttu-id="e8bab-307">Pour déboguer des solutions multiconteneurs, vous pouvez définir plusieurs points d’arrêt, chaque point d’arrêt dans un projet (conteneur) distinct, et, pendant le débogage à partir de Visual Studio, vous vous arrêtez aux points d’arrêt définis dans les différents projets et exécutés sur des conteneurs différents.</span><span class="sxs-lookup"><span data-stu-id="e8bab-307">The ability to debug multiple-container solutions means that you can set several breakpoints, each breakpoint in a different project (container), and while debugging from Visual Studio you will stop at breakpoints defined in different projects and running on different containers.</span></span>

![Exécution d’applications multiconteneurs dans Visual Studio 2017](./media/image16.png)

<span data-ttu-id="e8bab-309">**Figure 5-12**.</span><span class="sxs-lookup"><span data-stu-id="e8bab-309">**Figure 5-12**.</span></span> <span data-ttu-id="e8bab-310">Exécution d’applications multiconteneurs dans Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="e8bab-310">Running multi-container apps in Visual Studio 2017</span></span>

### <a name="additional-resources"></a><span data-ttu-id="e8bab-311">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e8bab-311">Additional resources</span></span>

-  <span data-ttu-id="e8bab-312">**Déployer un conteneur ASP.NET sur un hôte Docker distant**</span><span class="sxs-lookup"><span data-stu-id="e8bab-312">**Deploy an ASP.NET container to a remote Docker host**</span></span>

   [*https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker*](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)

### <a name="a-note-about-testing-and-deploying-with-orchestrators"></a><span data-ttu-id="e8bab-313">Note sur le test et le déploiement avec des orchestrateurs</span><span class="sxs-lookup"><span data-stu-id="e8bab-313">A note about testing and deploying with orchestrators</span></span>

<span data-ttu-id="e8bab-314">Les commandes docker-compose up et docker run (ou l’exécution et le débogage des conteneurs dans Visual Studio) sont une approche appropriée pour tester les conteneurs dans votre environnement de développement.</span><span class="sxs-lookup"><span data-stu-id="e8bab-314">The docker-compose up and docker run commands (or running and debugging the containers in Visual Studio) are adequate for testing containers in your development environment.</span></span> <span data-ttu-id="e8bab-315">Mais n’utilisez pas cette approche si vous ciblez des clusters Docker et des orchestrateurs tels que Docker Swarm, Mesosphere DC/OS ou Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="e8bab-315">But you should not use this approach if you are targeting Docker clusters and orchestrators like Docker Swarm, Mesosphere DC/OS, or Kubernetes.</span></span> <span data-ttu-id="e8bab-316">Si vous utilisez un cluster comme le [mode Docker Swarm](https://docs.docker.com/engine/swarm/) (disponible dans Docker CE pour Windows et Mac depuis la version 1.12), vous devez déployer et tester avec des commandes supplémentaires comme [docker service create](https://docs.docker.com/engine/reference/commandline/service_create/) pour des services uniques.</span><span class="sxs-lookup"><span data-stu-id="e8bab-316">If you are using a cluster like [Docker Swarm mode](https://docs.docker.com/engine/swarm/) (available in Docker CE for Windows and Mac since version 1.12), you need to deploy and test with additional commands like [docker service create](https://docs.docker.com/engine/reference/commandline/service_create/) for single services.</span></span> <span data-ttu-id="e8bab-317">Si vous déployez une application composée de plusieurs conteneurs, utilisez [docker compose bundle](https://docs.docker.com/compose/reference/bundle/) et [docker deploy myBundleFile](https://docs.docker.com/engine/reference/commandline/deploy/) pour déployer cette application en tant que *pile*.</span><span class="sxs-lookup"><span data-stu-id="e8bab-317">If you are deploying an application composed of several containers, you use [docker compose bundle](https://docs.docker.com/compose/reference/bundle/) and [docker deploy myBundleFile](https://docs.docker.com/engine/reference/commandline/deploy/) to deploy the composed application as a *stack*.</span></span> <span data-ttu-id="e8bab-318">Pour plus d’informations, consultez le billet de blog [Introducing Experimental Distributed Application Bundles](https://blog.docker.com/2016/06/docker-app-bundle/) dans la documentation Docker</span><span class="sxs-lookup"><span data-stu-id="e8bab-318">For more information, see the blog post [Introducing Experimental Distributed Application Bundles](https://blog.docker.com/2016/06/docker-app-bundle/) in the Docker documentation.</span></span> <span data-ttu-id="e8bab-319">disponible sur le site Docker.</span><span class="sxs-lookup"><span data-stu-id="e8bab-319">on the Docker site.</span></span>

<span data-ttu-id="e8bab-320">Avec [DC/OS](https://mesosphere.com/blog/2015/09/02/dcos-cli-command-line-tool-datacenter/) et [Kubernetes](https://kubernetes.io/docs/user-guide/deployments/), vous devez également utiliser des commandes et scripts de déploiement différents.</span><span class="sxs-lookup"><span data-stu-id="e8bab-320">For [DC/OS](https://mesosphere.com/blog/2015/09/02/dcos-cli-command-line-tool-datacenter/) and [Kubernetes](https://kubernetes.io/docs/user-guide/deployments/) you would use different deployment commands and scripts as well.</span></span>

![Image de l’étape 6](./media/image17.png)

## <a name="step-6-test-your-docker-application-using-your-local-docker-host"></a><span data-ttu-id="e8bab-322">Étape 6.</span><span class="sxs-lookup"><span data-stu-id="e8bab-322">Step 6.</span></span> <span data-ttu-id="e8bab-323">Tester votre application Docker à l’aide de l’hôte Docker local</span><span class="sxs-lookup"><span data-stu-id="e8bab-323">Test your Docker application using your local Docker host</span></span>

<span data-ttu-id="e8bab-324">Cette étape varie en fonction de ce que fait votre application.</span><span class="sxs-lookup"><span data-stu-id="e8bab-324">This step will vary depending on what your application is doing.</span></span> <span data-ttu-id="e8bab-325">Dans une application web .NET Core simple qui est déployée comme service ou conteneur unique, vous pouvez accéder au service en ouvrant un navigateur sur l’hôte Docker et en accédant à ce site (voir la figure 5-13).</span><span class="sxs-lookup"><span data-stu-id="e8bab-325">In a simple .NET Core Web application that is deployed as a single container or service, you can access the service by opening a browser on the Docker host and navigating to that site, as shown in Figure 5-13.</span></span> <span data-ttu-id="e8bab-326">(Si la configuration dans le fichier Dockerfile mappe le conteneur à un autre port sur l’hôte que le port 80, incluez le port de l’hôte dans l’URL.)</span><span class="sxs-lookup"><span data-stu-id="e8bab-326">(If the configuration in the Dockerfile maps the container to a port on the host that is anything other than 80, include the host port in the URL.)</span></span>

![Exemple de test de l’application Docker en local avec localhost](./media/image18.png)

<span data-ttu-id="e8bab-328">**Figure 5-13**.</span><span class="sxs-lookup"><span data-stu-id="e8bab-328">**Figure 5-13**.</span></span> <span data-ttu-id="e8bab-329">Exemple de test de l’application Docker en local avec localhost</span><span class="sxs-lookup"><span data-stu-id="e8bab-329">Example of testing your Docker application locally using localhost</span></span>

<span data-ttu-id="e8bab-330">Si localhost ne pointe pas vers l’IP de l’hôte Docker (contrairement à la configuration par défaut quand vous utilisez Docker CE), spécifiez l’adresse IP de la carte réseau de votre machine pour pouvoir accéder à votre service.</span><span class="sxs-lookup"><span data-stu-id="e8bab-330">If localhost is not pointing to the Docker host IP (by default, when using Docker CE, it should), to navigate to your service, use the IP address of your machine’s network card.</span></span>

<span data-ttu-id="e8bab-331">Cette URL dans le navigateur utilise le port 80 pour l’exemple de conteneur particulier présenté ici.</span><span class="sxs-lookup"><span data-stu-id="e8bab-331">This URL in the browser uses port 80 for the particular container example being discussed.</span></span> <span data-ttu-id="e8bab-332">Toutefois, en interne, les requêtes sont redirigées vers le port 5000, car le déploiement a été fait de cette façon avec la commande docker run, comme nous l’avons expliqué dans une étape précédente.</span><span class="sxs-lookup"><span data-stu-id="e8bab-332">However, internally the requests are being redirected to port 5000, because that was how it was deployed with the docker run command, as explained in a previous step.</span></span>

<span data-ttu-id="e8bab-333">Vous pouvez également tester l’application en exécutant curl à partir du terminal, comme indiqué à la figure 5-14.</span><span class="sxs-lookup"><span data-stu-id="e8bab-333">You can also test the application using curl from the terminal, as shown in Figure 5-14.</span></span> <span data-ttu-id="e8bab-334">Dans une installation Docker sur Windows, l’IP par défaut de l’hôte Docker est toujours 10.0.75.1 en plus de l’adresse IP réelle de votre machine.</span><span class="sxs-lookup"><span data-stu-id="e8bab-334">In a Docker installation on Windows, the default Docker Host IP is always 10.0.75.1 in addition to your machine’s actual IP address.</span></span>

![Exemple de test de l’application Docker en local avec curl](./media/image19.png)

<span data-ttu-id="e8bab-336">**Figure 5-14**.</span><span class="sxs-lookup"><span data-stu-id="e8bab-336">**Figure 5-14**.</span></span> <span data-ttu-id="e8bab-337">Exemple de test de l’application Docker en local avec curl</span><span class="sxs-lookup"><span data-stu-id="e8bab-337">Example of testing your Docker application locally using curl</span></span>

### <a name="testing-and-debugging-containers-with-visual-studio-2017"></a><span data-ttu-id="e8bab-338">Test et débogage des conteneurs avec Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="e8bab-338">Testing and debugging containers with Visual Studio 2017</span></span>

<span data-ttu-id="e8bab-339">Quand vous exécutez et déboguez les conteneurs avec Visual Studio 2017, vous pouvez déboguer l’application .NET pratiquement de la même façon que pour une exécution sans conteneurs.</span><span class="sxs-lookup"><span data-stu-id="e8bab-339">When running and debugging the containers with Visual Studio 2017, you can debug the .NET application in much the same way as you would when running without containers.</span></span>

### <a name="testing-and-debugging-without-visual-studio"></a><span data-ttu-id="e8bab-340">Test et débogage sans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e8bab-340">Testing and debugging without Visual Studio</span></span>

<span data-ttu-id="e8bab-341">Si vous avez choisi l’approche de développement avec un éditeur ou une CLI, le débogage des conteneurs est plus difficile. Vous pouvez alors déboguer les conteneurs en générant des traces.</span><span class="sxs-lookup"><span data-stu-id="e8bab-341">If you are developing using the editor/CLI approach, debugging containers is more difficult and you will want to debug by generating traces.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="e8bab-342">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e8bab-342">Additional resources</span></span>

- <span data-ttu-id="e8bab-343">**Débogage d’applications dans un conteneur Docker local**</span><span class="sxs-lookup"><span data-stu-id="e8bab-343">**Debugging apps in a local Docker container**</span></span>

   [*https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh*](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)

- <span data-ttu-id="e8bab-344">**Steve Lasker. Build, Debug, Deploy ASP.NET Core Apps with Docker.**</span><span class="sxs-lookup"><span data-stu-id="e8bab-344">**Steve Lasker. Build, Debug, Deploy ASP.NET Core Apps with Docker.**</span></span> <span data-ttu-id="e8bab-345">Vidéo.</span><span class="sxs-lookup"><span data-stu-id="e8bab-345">Video.</span></span>

   [*https://channel9.msdn.com/Events/Visual-Studio/Visual-Studio-2017-Launch/T115*](https://channel9.msdn.com/Events/Visual-Studio/Visual-Studio-2017-Launch/T115)

## <a name="simplified-workflow-when-developing-containers-with-visual-studio"></a><span data-ttu-id="e8bab-346">Workflow simplifié du développement de conteneurs avec Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e8bab-346">Simplified workflow when developing containers with Visual Studio</span></span>

<span data-ttu-id="e8bab-347">En effet, le workflow avec Visual Studio est beaucoup plus simple que si vous utilisez un éditeur ou une CLI.</span><span class="sxs-lookup"><span data-stu-id="e8bab-347">Effectively, the workflow when using Visual Studio is a lot simpler than if you use the editor/CLI approach.</span></span> <span data-ttu-id="e8bab-348">La plupart des étapes requises par Docker liées aux fichiers Dockerfile et docker-compose.yml sont masquées ou simplifiées par Visual Studio, comme illustré à la figure 5-15.</span><span class="sxs-lookup"><span data-stu-id="e8bab-348">Most of the steps required by Docker related to the Dockerfile and docker-compose.yml files are hidden or simplified by Visual Studio, as shown in Figure 5-15.</span></span>

![Workflow simplifié du développement avec Visual Studio](./media/image20.png)

<span data-ttu-id="e8bab-350">**Figure 5-15**.</span><span class="sxs-lookup"><span data-stu-id="e8bab-350">**Figure 5-15**.</span></span> <span data-ttu-id="e8bab-351">Workflow simplifié du développement avec Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e8bab-351">Simplified workflow when developing with Visual Studio</span></span>

<span data-ttu-id="e8bab-352">De plus, notez que vous devez effectuer l’étape 2 (ajout de la prise en charge de Docker à vos projets) une seule fois.</span><span class="sxs-lookup"><span data-stu-id="e8bab-352">In addition, you need to perform step 2 (adding Docker support to your projects) just once.</span></span> <span data-ttu-id="e8bab-353">Le workflow est donc similaire aux tâches de développement que vous avez l’habitude de faire dans le cadre d’un développement avec .NET.</span><span class="sxs-lookup"><span data-stu-id="e8bab-353">Therefore, the workflow is similar to your usual development tasks when using .NET for any other development.</span></span> <span data-ttu-id="e8bab-354">Vous devez comprendre ce qui se passe en arrière-plan (le processus de création d’image, les images de base utilisées, le déploiement des conteneurs, etc.). Par ailleurs, vous aurez parfois besoin de modifier le fichier Dockerfile ou docker-compose.yml pour personnaliser les comportements.</span><span class="sxs-lookup"><span data-stu-id="e8bab-354">You need to know what is going on under the covers (the image build process, what base images you are using, deployment of containers, etc.) and sometimes you will also need to edit the Dockerfile or docker-compose.yml file to customize behaviors.</span></span> <span data-ttu-id="e8bab-355">Au final, Visual Studio simplifie considérablement la plupart des tâches et vous permet de développer beaucoup plus rapidement.</span><span class="sxs-lookup"><span data-stu-id="e8bab-355">But most of the work is greatly simplified by using Visual Studio, making you a lot more productive.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="e8bab-356">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e8bab-356">Additional resources</span></span>

- <span data-ttu-id="e8bab-357">**Steve Lasker. Vidéo .NET Docker Development with Visual Studio 2017**</span><span class="sxs-lookup"><span data-stu-id="e8bab-357">**Steve Lasker. .NET Docker Development with Visual Studio 2017**</span></span>

   [*https://channel9.msdn.com/Events/Visual-Studio/Visual-Studio-2017-Launch/T111*](https://channel9.msdn.com/Events/Visual-Studio/Visual-Studio-2017-Launch/T111)

- <span data-ttu-id="e8bab-358">**Jeffrey T. Fritz. Put a .NET Core App in a Container with the new Docker Tools for Visual Studio**</span><span class="sxs-lookup"><span data-stu-id="e8bab-358">**Jeffrey T. Fritz. Put a .NET Core App in a Container with the new Docker Tools for Visual Studio**</span></span>

   [*https://blogs.msdn.microsoft.com/webdev/2016/11/16/new-docker-tools-for-visual-studio/*](https://blogs.msdn.microsoft.com/webdev/2016/11/16/new-docker-tools-for-visual-studio/)

## <a name="using-powershell-commands-in-a-dockerfile-to-set-up-windows-containers"></a><span data-ttu-id="e8bab-359">Utilisation de commandes PowerShell dans un fichier Dockerfile pour configurer des conteneurs Windows</span><span class="sxs-lookup"><span data-stu-id="e8bab-359">Using PowerShell commands in a Dockerfile to set up Windows Containers</span></span>

<span data-ttu-id="e8bab-360">Les [conteneurs Windows](/virtualization/windowscontainers/about/) vous permettent de convertir vos applications Windows existantes en images Docker, puis de les déployer avec les mêmes outils que le reste de l’écosystème Docker.</span><span class="sxs-lookup"><span data-stu-id="e8bab-360">[Windows Containers](/virtualization/windowscontainers/about/) allow you to convert your existing Windows applications into Docker images and deploy them with the same tools as the rest of the Docker ecosystem.</span></span> <span data-ttu-id="e8bab-361">Pour utiliser les conteneurs Windows, vous exécutez des commandes PowerShell dans le fichier Dockerfile, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="e8bab-361">To use Windows Containers, you run PowerShell commands in the Dockerfile, as shown in the following example:</span></span>

```Dockerfile
FROM microsoft/windowsservercore

LABEL Description="IIS" Vendor="Microsoft" Version="10"

RUN powershell -Command Add-WindowsFeature Web-Server

CMD [ "ping", "localhost", "-t" ]
```

<span data-ttu-id="e8bab-362">Dans ce cas, nous utilisons une image de base Windows Server Core (le paramètre FROM) et nous installons IIS à l’aide d’une commande PowerShell (le paramètre RUN).</span><span class="sxs-lookup"><span data-stu-id="e8bab-362">In this case, we are using a Windows Server Core base image (the FROM setting) and installing IIS with a PowerShell command (the RUN setting).</span></span> <span data-ttu-id="e8bab-363">De la même façon, vous pouvez également utiliser des commandes PowerShell pour configurer des composants supplémentaires comme ASP.NET 4.x, .NET 4.6 ou tout autre logiciel Windows.</span><span class="sxs-lookup"><span data-stu-id="e8bab-363">In a similar way, you could also use PowerShell commands to set up additional components like ASP.NET 4.x, .NET 4.6, or any other Windows software.</span></span> <span data-ttu-id="e8bab-364">Par exemple, la commande suivante dans un fichier Dockerfile configure ASP.NET 4.5 :</span><span class="sxs-lookup"><span data-stu-id="e8bab-364">For example, the following command in a Dockerfile sets up ASP.NET 4.5:</span></span>

```Dockerfile
RUN powershell add-windowsfeature web-asp-net45
```

### <a name="additional-resources"></a><span data-ttu-id="e8bab-365">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e8bab-365">Additional resources</span></span>

- <span data-ttu-id="e8bab-366">**aspnet-docker/Dockerfile.**</span><span class="sxs-lookup"><span data-stu-id="e8bab-366">**aspnet-docker/Dockerfile.**</span></span> <span data-ttu-id="e8bab-367">Exemples de commandes PowerShell à exécuter à partir de fichiers Dockerfile pour ajouter des fonctionnalités Windows.</span><span class="sxs-lookup"><span data-stu-id="e8bab-367">Example Powershell commands to run from dockerfiles to include Windows features.</span></span>

   [*https://github.com/Microsoft/aspnet-docker/blob/master/4.6.2/Dockerfile*](https://github.com/Microsoft/aspnet-docker/blob/master/4.6.2/Dockerfile)

>[!div class="step-by-step"]
<span data-ttu-id="e8bab-368">[Précédent](index.md)
[Suivant](../net-core-single-containers-linux-windows-server-hosts/index.md)</span><span class="sxs-lookup"><span data-stu-id="e8bab-368">[Previous](index.md)
[Next](../net-core-single-containers-linux-windows-server-hosts/index.md)</span></span>