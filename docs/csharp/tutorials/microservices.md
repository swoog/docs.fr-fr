---
title: Microservices hébergés dans Docker - C#
description: Apprenez à créer des services principaux ASP.NET qui s’exécutent dans des conteneurs Docker
ms.date: 02/03/2017
ms.assetid: 87e93838-a363-4813-b859-7356023d98ed
ms.openlocfilehash: 7428051c1d9a29ba98ca1f28288b3c50ea36ae1a
ms.sourcegitcommit: 54231aa56fca059e9297888a96fbca1d4cf3746c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2018
---
# <a name="microservices-hosted-in-docker"></a><span data-ttu-id="e0a33-103">Microservices hébergés dans Docker</span><span class="sxs-lookup"><span data-stu-id="e0a33-103">Microservices hosted in Docker</span></span>

<span data-ttu-id="e0a33-104">Ce didacticiel détaille les tâches nécessaires pour générer et déployer un microservice ASP.NET Core dans un conteneur Docker.</span><span class="sxs-lookup"><span data-stu-id="e0a33-104">This tutorial details the tasks necessary to build and deploy an ASP.NET Core microservice in a Docker container.</span></span> <span data-ttu-id="e0a33-105">Au cours de ce didacticiel, vous apprendrez à :</span><span class="sxs-lookup"><span data-stu-id="e0a33-105">During the course of this tutorial, you'll learn:</span></span>

* <span data-ttu-id="e0a33-106">Générer une application ASP.NET Core à l’aide de Yeoman</span><span class="sxs-lookup"><span data-stu-id="e0a33-106">How to generate an ASP.NET Core application using Yeoman</span></span>
* <span data-ttu-id="e0a33-107">Guide de création d’un environnement de développement Docker</span><span class="sxs-lookup"><span data-stu-id="e0a33-107">How to create a development Docker environment</span></span>
* <span data-ttu-id="e0a33-108">Créer une image Docker basée sur une image existante.</span><span class="sxs-lookup"><span data-stu-id="e0a33-108">How to build a Docker image based on an existing image.</span></span>
* <span data-ttu-id="e0a33-109">Déployer votre service dans un conteneur Docker.</span><span class="sxs-lookup"><span data-stu-id="e0a33-109">How to deploy your service into a Docker container.</span></span>

<span data-ttu-id="e0a33-110">Au passage, vous verrez également certaines fonctionnalités du langage C# :</span><span class="sxs-lookup"><span data-stu-id="e0a33-110">Along the way, you'll also see some C# language features:</span></span>

* <span data-ttu-id="e0a33-111">Conversion des objets C# en charges utiles JSON.</span><span class="sxs-lookup"><span data-stu-id="e0a33-111">How to convert C# objects into JSON payloads.</span></span>
* <span data-ttu-id="e0a33-112">Création d’objets de transfert de données immuables</span><span class="sxs-lookup"><span data-stu-id="e0a33-112">How to build immutable Data Transfer Objects</span></span>
* <span data-ttu-id="e0a33-113">Traitement des demandes HTTP entrantes et création de la réponse HTTP</span><span class="sxs-lookup"><span data-stu-id="e0a33-113">How to process incoming HTTP Requests and generate the HTTP Response</span></span>
* <span data-ttu-id="e0a33-114">Guide pratique de travail avec les types valeur Nuallable</span><span class="sxs-lookup"><span data-stu-id="e0a33-114">How to work with nullable value types</span></span>

<span data-ttu-id="e0a33-115">Vous pouvez [afficher ou télécharger l’exemple d’application](https://github.com/dotnet/samples/tree/master/csharp/getting-started/WeatherMicroservice) de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="e0a33-115">You can [view or download the sample app](https://github.com/dotnet/samples/tree/master/csharp/getting-started/WeatherMicroservice) for this topic.</span></span> <span data-ttu-id="e0a33-116">Pour obtenir des instructions de téléchargement, consultez [Exemples et didacticiels](../../samples-and-tutorials/index.md#viewing-and-downloading-samples).</span><span class="sxs-lookup"><span data-stu-id="e0a33-116">For download instructions, see [Samples and Tutorials](../../samples-and-tutorials/index.md#viewing-and-downloading-samples).</span></span>

### <a name="why-docker"></a><span data-ttu-id="e0a33-117">Pourquoi Docker ?</span><span class="sxs-lookup"><span data-stu-id="e0a33-117">Why Docker?</span></span>

<span data-ttu-id="e0a33-118">Docker facilite la création d’images de machine standard pour héberger vos services dans un centre de données ou dans le cloud public.</span><span class="sxs-lookup"><span data-stu-id="e0a33-118">Docker makes it easy to create standard machine images to host your services in a data center, or the public cloud.</span></span> <span data-ttu-id="e0a33-119">Docker vous permet de configurer l’image et de la répliquer en fonction des besoins pour mettre à l’échelle l’installation de votre application.</span><span class="sxs-lookup"><span data-stu-id="e0a33-119">Docker enables you to configure the image, and replicate it as needed to scale the installation of your application.</span></span>

<span data-ttu-id="e0a33-120">Tout le code de ce didacticiel fonctionne dans n’importe quel environnement .NET Core.</span><span class="sxs-lookup"><span data-stu-id="e0a33-120">All the code in this tutorial will work in any .NET Core environment.</span></span>
<span data-ttu-id="e0a33-121">Les tâches supplémentaires pour une installation Docker fonctionneront pour une application ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="e0a33-121">The additional tasks for a Docker installation will work for an ASP.NET Core application.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="e0a33-122">Prérequis</span><span class="sxs-lookup"><span data-stu-id="e0a33-122">Prerequisites</span></span>
<span data-ttu-id="e0a33-123">Vous devez configurer votre ordinateur pour exécuter .NET Core.</span><span class="sxs-lookup"><span data-stu-id="e0a33-123">You’ll need to setup your machine to run .NET core.</span></span> <span data-ttu-id="e0a33-124">Vous trouverez les instructions d’installation sur la page de [.NET Core](https://www.microsoft.com/net/core).</span><span class="sxs-lookup"><span data-stu-id="e0a33-124">You can find the installation instructions on the [.NET Core](https://www.microsoft.com/net/core) page.</span></span>
<span data-ttu-id="e0a33-125">Vous pouvez exécuter cette application sur Windows, Ubuntu Linux, Mac OS ou dans un conteneur Docker.</span><span class="sxs-lookup"><span data-stu-id="e0a33-125">You can run this application on Windows, Ubuntu Linux, macOS or in a Docker container.</span></span> <span data-ttu-id="e0a33-126">Vous devez installer l’éditeur de code de votre choix.</span><span class="sxs-lookup"><span data-stu-id="e0a33-126">You’ll need to install your favorite code editor.</span></span> <span data-ttu-id="e0a33-127">Les descriptions ci-dessous utilisent [Visual Studio Code](https://code.visualstudio.com/), un éditeur open source et multiplateforme.</span><span class="sxs-lookup"><span data-stu-id="e0a33-127">The descriptions below use [Visual Studio Code](https://code.visualstudio.com/) which is an open source, cross platform editor.</span></span> <span data-ttu-id="e0a33-128">Cependant, vous pouvez utiliser les outils avec lesquels vous êtes le plus à l’aise.</span><span class="sxs-lookup"><span data-stu-id="e0a33-128">However, you can use whatever tools you are comfortable with.</span></span>

<span data-ttu-id="e0a33-129">Vous devez également installer le moteur Docker.</span><span class="sxs-lookup"><span data-stu-id="e0a33-129">You'll also need to install the Docker engine.</span></span> <span data-ttu-id="e0a33-130">Consultez la [page d’installation de Docker](http://www.docker.com/products/docker) pour obtenir des instructions pour votre plateforme.</span><span class="sxs-lookup"><span data-stu-id="e0a33-130">See the [Docker Installation page](http://www.docker.com/products/docker) for instructions for your platform.</span></span>
<span data-ttu-id="e0a33-131">Docker peut être installé dans de nombreuses distributions Linux, Mac OS ou Windows.</span><span class="sxs-lookup"><span data-stu-id="e0a33-131">Docker can be installed in many Linux distributions, macOS, or Windows.</span></span> <span data-ttu-id="e0a33-132">La page mentionnée ci-dessus contient des sections pour chacune des installations disponibles.</span><span class="sxs-lookup"><span data-stu-id="e0a33-132">The page referenced above contains sections to each of the available installations.</span></span>

<span data-ttu-id="e0a33-133">La plupart des composants à installer le sont par un gestionnaire de package.</span><span class="sxs-lookup"><span data-stu-id="e0a33-133">Most components to be installed are done by a package manager.</span></span> <span data-ttu-id="e0a33-134">Si vous disposez du gestionnaire de packages de node.js `npm` installé, vous pouvez ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="e0a33-134">If you have node.js's package manager `npm` installed you can skip this step.</span></span> <span data-ttu-id="e0a33-135">Sinon, installez la dernière version de NodeJs à partir de [nodejs.org](https://nodejs.org), ce qui installe le gestionnaire de packages npm.</span><span class="sxs-lookup"><span data-stu-id="e0a33-135">Otherwise install the latest NodeJs from [nodejs.org](https://nodejs.org) which will install the npm package manager.</span></span> 

<span data-ttu-id="e0a33-136">À ce stade, vous devrez installer un certain nombre d’outils de ligne de commande qui prennent en charge le développement avec ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="e0a33-136">At this point you will need to install a number of command line tools that support ASP.NET core development.</span></span> <span data-ttu-id="e0a33-137">Les modèles de ligne de commande utilisent Yeoman, Bower, Grunt et Gulp.</span><span class="sxs-lookup"><span data-stu-id="e0a33-137">The command line templates use Yeoman, Bower, Grunt, and Gulp.</span></span> <span data-ttu-id="e0a33-138">Si vous les avez déjà installés, c’est parfait, sinon saisissez ce qui suit dans votre interpréteur de commandes préféré :</span><span class="sxs-lookup"><span data-stu-id="e0a33-138">If you have them installed that is good, otherwise type the following into your favorite shell:</span></span>

`npm install -g yo bower grunt-cli gulp`

<span data-ttu-id="e0a33-139">L’option `-g` indique qu’il s’agit d’une installation globale, et que ces outils sont disponibles à l’échelle du système.</span><span class="sxs-lookup"><span data-stu-id="e0a33-139">The `-g` option indicates that it is a global install, and those tools are available system wide.</span></span> <span data-ttu-id="e0a33-140">(Une installation locale définit la portée du package sur un projet unique).</span><span class="sxs-lookup"><span data-stu-id="e0a33-140">(A local install scopes the package to a single project).</span></span> <span data-ttu-id="e0a33-141">Une fois que vous avez installé les outils de base, vous devez installer les générateurs de modèle yeoman ASP.NET :</span><span class="sxs-lookup"><span data-stu-id="e0a33-141">Once you've installed those core tools, you need to install the yeoman ASP.NET template generators:</span></span>

`npm install -g generator-aspnet`

## <a name="create-the-application"></a><span data-ttu-id="e0a33-142">Création de l’application</span><span class="sxs-lookup"><span data-stu-id="e0a33-142">Create the Application</span></span>

<span data-ttu-id="e0a33-143">Maintenant que vous avez installé tous les outils, créez une application ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="e0a33-143">Now that you've installed all the tools, create a new ASP.NET Core application.</span></span> <span data-ttu-id="e0a33-144">Pour utiliser le générateur de ligne de commande, exécutez la commande yeoman suivante dans votre interpréteur de commandes préféré :</span><span class="sxs-lookup"><span data-stu-id="e0a33-144">To use the command line generator, execute the following yeoman command in your favorite shell:</span></span>

`yo aspnet`

<span data-ttu-id="e0a33-145">Cette commande vous invite à sélectionner le type d’application que vous souhaitez créer.</span><span class="sxs-lookup"><span data-stu-id="e0a33-145">This command prompts you to select what Type of application you want to create.</span></span> <span data-ttu-id="e0a33-146">Pour ce microservice, vous souhaitez obtenir l’application web la plus simple et légère possible, sélectionnez donc « Application Web vide ».</span><span class="sxs-lookup"><span data-stu-id="e0a33-146">For this microservice, you want the simplest, most lightweight web application possible, so select 'Empty Web Application'.</span></span> <span data-ttu-id="e0a33-147">Le modèle vous demandera un nom.</span><span class="sxs-lookup"><span data-stu-id="e0a33-147">The template will prompt you for a name.</span></span> <span data-ttu-id="e0a33-148">Sélectionnez « WeatherMicroservice ».</span><span class="sxs-lookup"><span data-stu-id="e0a33-148">Select 'WeatherMicroservice'.</span></span> 

<span data-ttu-id="e0a33-149">Le modèle crée huit fichiers pour vous :</span><span class="sxs-lookup"><span data-stu-id="e0a33-149">The template creates eight files for you:</span></span>

* <span data-ttu-id="e0a33-150">Un fichier .gitignore personnalisé pour les applications ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="e0a33-150">A .gitignore, customized for ASP.NET Core applications.</span></span>
* <span data-ttu-id="e0a33-151">Un fichier Startup.cs.</span><span class="sxs-lookup"><span data-stu-id="e0a33-151">A Startup.cs file.</span></span> <span data-ttu-id="e0a33-152">Cela contient la base de l’application.</span><span class="sxs-lookup"><span data-stu-id="e0a33-152">This contains the basis of the application.</span></span>
* <span data-ttu-id="e0a33-153">Un fichier Program.cs.</span><span class="sxs-lookup"><span data-stu-id="e0a33-153">A Program.cs file.</span></span> <span data-ttu-id="e0a33-154">Cela contient le point d’entrée de l’application.</span><span class="sxs-lookup"><span data-stu-id="e0a33-154">This contains the entry point of the application.</span></span>
* <span data-ttu-id="e0a33-155">Un fichier WeatherMicroservice.csproj.</span><span class="sxs-lookup"><span data-stu-id="e0a33-155">A WeatherMicroservice.csproj file.</span></span> <span data-ttu-id="e0a33-156">Il s’agit du fichier de génération de l’application.</span><span class="sxs-lookup"><span data-stu-id="e0a33-156">This is the build file for the application.</span></span>
* <span data-ttu-id="e0a33-157">Un Dockerfile.</span><span class="sxs-lookup"><span data-stu-id="e0a33-157">A Dockerfile.</span></span> <span data-ttu-id="e0a33-158">Ce script crée une image Docker pour l’application.</span><span class="sxs-lookup"><span data-stu-id="e0a33-158">This script creates a Docker image for the application.</span></span>
* <span data-ttu-id="e0a33-159">Un README.md.</span><span class="sxs-lookup"><span data-stu-id="e0a33-159">A README.md.</span></span> <span data-ttu-id="e0a33-160">Il contient des liens vers d’autres ressources ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="e0a33-160">This contains links to other ASP.NET Core resources.</span></span>
* <span data-ttu-id="e0a33-161">Un fichier web.config.</span><span class="sxs-lookup"><span data-stu-id="e0a33-161">A web.config file.</span></span> <span data-ttu-id="e0a33-162">Les informations de configuration de base s’y trouvent.</span><span class="sxs-lookup"><span data-stu-id="e0a33-162">This contains basic configuration information.</span></span>
* <span data-ttu-id="e0a33-163">Un fichier runtimeconfig.template.json.</span><span class="sxs-lookup"><span data-stu-id="e0a33-163">A runtimeconfig.template.json file.</span></span> <span data-ttu-id="e0a33-164">Il contient les paramètres de débogage utilisés par l’EDI.</span><span class="sxs-lookup"><span data-stu-id="e0a33-164">This contains debugging settings used by IDEs.</span></span>

<span data-ttu-id="e0a33-165">Vous pouvez maintenant exécuter l’application générée par le modèle.</span><span class="sxs-lookup"><span data-stu-id="e0a33-165">Now you can run the template generated application.</span></span> <span data-ttu-id="e0a33-166">Vous pouvez le faire à l’aide d’une série d’outils en ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="e0a33-166">That's done using a series of tools from the command line.</span></span> <span data-ttu-id="e0a33-167">La commande `dotnet` exécute les outils nécessaires pour le développement .NET.</span><span class="sxs-lookup"><span data-stu-id="e0a33-167">The `dotnet` command runs the tools necessary for .NET development.</span></span> <span data-ttu-id="e0a33-168">Chaque verbe exécute une commande différente</span><span class="sxs-lookup"><span data-stu-id="e0a33-168">Each verb executes a different command</span></span>

<span data-ttu-id="e0a33-169">La première étape consiste à restaurer toutes les dépendances :</span><span class="sxs-lookup"><span data-stu-id="e0a33-169">The first step is to restore all the dependencies:</span></span>

```console
dotnet restore
```

<span data-ttu-id="e0a33-170">La restauration Dotnet utilise le gestionnaire de packages NuGet pour installer tous les packages dans le répertoire de l’application.</span><span class="sxs-lookup"><span data-stu-id="e0a33-170">Dotnet restore uses the NuGet package manager to install all the necessary packages into the application directory.</span></span> <span data-ttu-id="e0a33-171">Il génère également un fichier project.json.lock.</span><span class="sxs-lookup"><span data-stu-id="e0a33-171">It also generates a project.json.lock file.</span></span> <span data-ttu-id="e0a33-172">Ce fichier contient des informations sur chaque package référencé.</span><span class="sxs-lookup"><span data-stu-id="e0a33-172">This file contains information about each package that is referenced.</span></span> <span data-ttu-id="e0a33-173">Après la restauration de toutes les dépendances, vous générez l’application :</span><span class="sxs-lookup"><span data-stu-id="e0a33-173">After restoring all the dependencies, you build the application:</span></span>

```console
dotnet build
```
[!INCLUDE[DotNet Restore Note](~/includes/dotnet-restore-note.md)]

<span data-ttu-id="e0a33-174">Et une fois que vous générez l’application, vous l’exécutez à partir de la ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="e0a33-174">And once you build the application, you run it from the command line:</span></span>

```console
dotnet run
```

<span data-ttu-id="e0a33-175">La configuration par défaut écoute le port `http://localhost:5000`.</span><span class="sxs-lookup"><span data-stu-id="e0a33-175">The default configuration listens to `http://localhost:5000`.</span></span> <span data-ttu-id="e0a33-176">Vous pouvez ouvrir un navigateur et accéder à cette page pour voir un « Hello World! »</span><span class="sxs-lookup"><span data-stu-id="e0a33-176">You can open a browser and navigate to that page and see a "Hello World!"</span></span> <span data-ttu-id="e0a33-177">« Operation Not Found! ».</span><span class="sxs-lookup"><span data-stu-id="e0a33-177">message.</span></span>

### <a name="anatomy-of-an-aspnet-core-application"></a><span data-ttu-id="e0a33-178">Anatomie d’une application ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="e0a33-178">Anatomy of an ASP.NET Core application</span></span>

<span data-ttu-id="e0a33-179">Maintenant que vous avez créé l’application, nous allons voir comment cette fonctionnalité est implémentée.</span><span class="sxs-lookup"><span data-stu-id="e0a33-179">Now that you've built the application, let's look at how this functionality is implemented.</span></span> <span data-ttu-id="e0a33-180">Deux des fichiers générés sont particulièrement intéressants à ce stade : project.json et Startup.cs.</span><span class="sxs-lookup"><span data-stu-id="e0a33-180">There are two of the generated files that are particularly interesting at this point: project.json and Startup.cs.</span></span> 

<span data-ttu-id="e0a33-181">Project.json qui contient des informations sur le projet.</span><span class="sxs-lookup"><span data-stu-id="e0a33-181">Project.json contains information about the project.</span></span> <span data-ttu-id="e0a33-182">Ces deux nœuds, que vous utiliserez souvent, sont des « dépendances » et des « frameworks ».</span><span class="sxs-lookup"><span data-stu-id="e0a33-182">The two nodes you'll often work with are 'dependencies' and 'frameworks'.</span></span> <span data-ttu-id="e0a33-183">Le nœud de dépendances répertorie tous les packages qui sont nécessaires pour cette application.</span><span class="sxs-lookup"><span data-stu-id="e0a33-183">The dependencies node lists all the packages that are needed for this application.</span></span>
<span data-ttu-id="e0a33-184">À ce stade, il s’agit d’un petit nœud, qui ne nécessite que les packages qui exécutent le serveur Web.</span><span class="sxs-lookup"><span data-stu-id="e0a33-184">At the moment, this is a small node, needing only the packages that run the web server.</span></span>

<span data-ttu-id="e0a33-185">Le nœud « frameworks » spécifie les versions et les configurations du .NET Framework qui va exécuter cette application.</span><span class="sxs-lookup"><span data-stu-id="e0a33-185">The 'frameworks' node specifies the versions and configurations of the .NET framework that will run this application.</span></span>

<span data-ttu-id="e0a33-186">L’application est implémentée dans Startup.cs.</span><span class="sxs-lookup"><span data-stu-id="e0a33-186">The application is implemented in Startup.cs.</span></span> <span data-ttu-id="e0a33-187">Ce fichier contient la classe de démarrage.</span><span class="sxs-lookup"><span data-stu-id="e0a33-187">This file contains the startup class.</span></span>

<span data-ttu-id="e0a33-188">Les deux méthodes sont appelées par l’infrastructure ASP.NET Core pour configurer et exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="e0a33-188">The two methods are called by the ASP.NET Core infrastructure to configure and run the application.</span></span> <span data-ttu-id="e0a33-189">La méthode `ConfigureServices` décrit les services qui sont nécessaires pour cette application.</span><span class="sxs-lookup"><span data-stu-id="e0a33-189">The `ConfigureServices` method describes the services that are necessary for this application.</span></span> <span data-ttu-id="e0a33-190">Vous créez un microservice épuré, vous n’avez donc pas besoin de configurer de dépendances.</span><span class="sxs-lookup"><span data-stu-id="e0a33-190">You're building a lean microservice, so it doesn't need to configure any dependencies.</span></span> <span data-ttu-id="e0a33-191">La méthode `Configure` configure les gestionnaires pour les requêtes HTTP entrantes.</span><span class="sxs-lookup"><span data-stu-id="e0a33-191">The `Configure` method configures the handlers for incoming HTTP Requests.</span></span> <span data-ttu-id="e0a33-192">Le modèle génère un gestionnaire simple qui répond à une demande dont le texte est « Hello World! ».</span><span class="sxs-lookup"><span data-stu-id="e0a33-192">The template generates a simple handler that responds to any request with the text 'Hello World!'.</span></span>

## <a name="build-a-microservice"></a><span data-ttu-id="e0a33-193">Créer un microservice</span><span class="sxs-lookup"><span data-stu-id="e0a33-193">Build a microservice</span></span>

<span data-ttu-id="e0a33-194">Le service que vous vous apprêtez à générer fournira des rapports météorologiques depuis n’importe où dans le monde.</span><span class="sxs-lookup"><span data-stu-id="e0a33-194">The service you're going to build will deliver weather reports from anywhere around the globe.</span></span> <span data-ttu-id="e0a33-195">Dans une application de production, vous appelleriez un service pour récupérer des données météorologiques.</span><span class="sxs-lookup"><span data-stu-id="e0a33-195">In a production application, you'd call some service to retrieve weather data.</span></span> <span data-ttu-id="e0a33-196">Pour notre exemple, nous allons générer des prévisions météorologiques aléatoires.</span><span class="sxs-lookup"><span data-stu-id="e0a33-196">For our sample, we'll generate a random weather forecast.</span></span> 

<span data-ttu-id="e0a33-197">Il existe un certain nombre de tâches que vous devez effectuer pour implémenter notre service météo aléatoire :</span><span class="sxs-lookup"><span data-stu-id="e0a33-197">There are a number of tasks you'll need to perform in order to implement our random weather service:</span></span>

* <span data-ttu-id="e0a33-198">Analyser la requête entrante pour lire la latitude et la longitude.</span><span class="sxs-lookup"><span data-stu-id="e0a33-198">Parse the incoming request to read the latitude and longitude.</span></span>
* <span data-ttu-id="e0a33-199">Générer des données de prévision aléatoires.</span><span class="sxs-lookup"><span data-stu-id="e0a33-199">Generate some random forecast data.</span></span>
* <span data-ttu-id="e0a33-200">Convertir ces données de prévision aléatoires d’objets C# en paquets JSON.</span><span class="sxs-lookup"><span data-stu-id="e0a33-200">Convert that random forecast data from C# objects into JSON packets.</span></span>
* <span data-ttu-id="e0a33-201">Définir l’en-tête de réponse pour indiquer que votre service renvoie JSON.</span><span class="sxs-lookup"><span data-stu-id="e0a33-201">Set the response header to indicate that your service sends back JSON.</span></span>
* <span data-ttu-id="e0a33-202">Écrivez la réponse.</span><span class="sxs-lookup"><span data-stu-id="e0a33-202">Write the response.</span></span>

<span data-ttu-id="e0a33-203">Les sections suivantes décrivent chacune de ces étapes.</span><span class="sxs-lookup"><span data-stu-id="e0a33-203">The next sections walk you through each of these steps.</span></span>

### <a name="parsing-the-query-string"></a><span data-ttu-id="e0a33-204">Analyse de la chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="e0a33-204">Parsing the Query String.</span></span>

<span data-ttu-id="e0a33-205">Vous commencerez par analyser la chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="e0a33-205">You'll begin by parsing the query string.</span></span> <span data-ttu-id="e0a33-206">Le service acceptera les arguments 'lat' et 'longs' sur la chaîne de requête dans ce formulaire :</span><span class="sxs-lookup"><span data-stu-id="e0a33-206">The service will accept 'lat' and 'long' arguments on the query string in this form:</span></span>

`http://localhost:5000/?lat=-35.55&long=-12.35`  

<span data-ttu-id="e0a33-207">Toutes les modifications que vous devez apporter se trouvent dans l’expression lambda définie comme argument de `app.Run` dans votre classe de démarrage.</span><span class="sxs-lookup"><span data-stu-id="e0a33-207">All the changes you need to make are in the lambda expression defined as the argument to `app.Run` in your startup class.</span></span>

<span data-ttu-id="e0a33-208">L’argument de l’expression lambda est le `HttpContext` pour la demande.</span><span class="sxs-lookup"><span data-stu-id="e0a33-208">The argument on the lambda expression is the `HttpContext` for the request.</span></span> <span data-ttu-id="e0a33-209">Une de ses propriétés est l’objet `Request`.</span><span class="sxs-lookup"><span data-stu-id="e0a33-209">One of its properties is the `Request` object.</span></span> <span data-ttu-id="e0a33-210">L’objet `Request` a une propriété `Query` qui contient un dictionnaire de toutes les valeurs dans la chaîne de requête pour la demande.</span><span class="sxs-lookup"><span data-stu-id="e0a33-210">The `Request` object has a `Query` property that contains a dictionary of all the values on the query string for the request.</span></span> <span data-ttu-id="e0a33-211">La première addition consiste à rechercher les valeurs de latitude et longitude :</span><span class="sxs-lookup"><span data-stu-id="e0a33-211">The first addition is to find the latitude and longitude values:</span></span>

[!code-csharp[ReadQueryString](../../../samples/csharp/getting-started/WeatherMicroservice/Startup.cs#ReadQueryString "read variables from the query string")]

<span data-ttu-id="e0a33-212">Les valeurs du dictionnaire de requêtes sont de type `StringValue`.</span><span class="sxs-lookup"><span data-stu-id="e0a33-212">The Query dictionary values are `StringValue` type.</span></span> <span data-ttu-id="e0a33-213">Ce type peut contenir une collection de chaînes.</span><span class="sxs-lookup"><span data-stu-id="e0a33-213">That type can contain a collection of strings.</span></span> <span data-ttu-id="e0a33-214">Pour votre service météo, chaque valeur est une chaîne unique.</span><span class="sxs-lookup"><span data-stu-id="e0a33-214">For your weather service, each value is a single string.</span></span> <span data-ttu-id="e0a33-215">C’est pourquoi il y a un appel à `FirstOrDefault()` dans le code ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="e0a33-215">That's why there's the call to `FirstOrDefault()` in the code above.</span></span> 

<span data-ttu-id="e0a33-216">Ensuite, vous devez convertir les chaînes en valeurs de type double.</span><span class="sxs-lookup"><span data-stu-id="e0a33-216">Next, you need to convert the strings to doubles.</span></span> <span data-ttu-id="e0a33-217">La méthode que vous allez utiliser pour convertir la chaîne en double est `double.TryParse()` :</span><span class="sxs-lookup"><span data-stu-id="e0a33-217">The method you'll use to convert the string to a double is `double.TryParse()`:</span></span>

```csharp
bool TryParse(string s, out double result);
```

<span data-ttu-id="e0a33-218">Cette méthode s’appuie sur les paramètres de sortie de C# pour indiquer si la chaîne d’entrée peut être convertie en double.</span><span class="sxs-lookup"><span data-stu-id="e0a33-218">This method leverages C# out parameters to indicate if the input string can be converted to a double.</span></span> <span data-ttu-id="e0a33-219">Si la chaîne constitue une représentation valide pour un double, la méthode retourne true et l’argument `result` contient la valeur.</span><span class="sxs-lookup"><span data-stu-id="e0a33-219">If the string does represent a valid representation for a double, the method returns true, and the `result` argument contains the value.</span></span> <span data-ttu-id="e0a33-220">Si la chaîne ne représente pas une valeur double valide, la méthode retourne false.</span><span class="sxs-lookup"><span data-stu-id="e0a33-220">If the string does not represent a valid double, the method returns false.</span></span>

<span data-ttu-id="e0a33-221">Vous pouvez adapter cette API à l’aide d’une *méthode d’extension* qui renvoie un *double Nullable*.</span><span class="sxs-lookup"><span data-stu-id="e0a33-221">You can adapt that API with the use of an *extension method* that returns a *nullable double*.</span></span> <span data-ttu-id="e0a33-222">Un *type de valeur Nullable* est un type qui représente un type de valeur et peut également contenir un une valeur manquante ou Null.</span><span class="sxs-lookup"><span data-stu-id="e0a33-222">A *nullable value type* is a type that represents some value type, and can also hold a missing, or null value.</span></span> <span data-ttu-id="e0a33-223">Un type Nullable est représenté en ajoutant le caractère `?` à la déclaration de type.</span><span class="sxs-lookup"><span data-stu-id="e0a33-223">A nullable type is represented by appending the `?` character to the type declaration.</span></span> 

<span data-ttu-id="e0a33-224">Les méthodes d’extension sont des méthodes qui sont définies comme des méthodes statiques mais qui, en ajoutant le modificateur `this` sur le premier paramètre, peuvent être appelées comme si elles étaient des membres de cette classe.</span><span class="sxs-lookup"><span data-stu-id="e0a33-224">Extension methods are methods that are defined as static methods, but by adding the `this` modifier on the first parameter, can be called as though they are members of that class.</span></span> <span data-ttu-id="e0a33-225">Les méthodes d’extension peuvent être définies uniquement dans les classes statiques.</span><span class="sxs-lookup"><span data-stu-id="e0a33-225">Extension methods may only be defined in static classes.</span></span> <span data-ttu-id="e0a33-226">Voici la définition de la classe contenant la méthode d’extension pour l’analyse :</span><span class="sxs-lookup"><span data-stu-id="e0a33-226">Here's the definition of the class containing the extension method for parse:</span></span>

[!code-csharp[TryParseExtension](../../../samples/csharp/getting-started/WeatherMicroservice/Extensions.cs#TryParseExtension "try parse to a nullable")]

<span data-ttu-id="e0a33-227">L’expression `default(double?)` retourne la valeur par défaut pour le type `double?`.</span><span class="sxs-lookup"><span data-stu-id="e0a33-227">The `default(double?)` expression returns the default value for the `double?` type.</span></span> <span data-ttu-id="e0a33-228">Cette valeur par défaut est la valeur null (ou manquante).</span><span class="sxs-lookup"><span data-stu-id="e0a33-228">That default value is the null (or missing) value.</span></span>

<span data-ttu-id="e0a33-229">Vous pouvez utiliser cette méthode d’extension pour convertir les arguments de chaîne de requête en type double :</span><span class="sxs-lookup"><span data-stu-id="e0a33-229">You can use this extension method to convert the query string arguments into the double type:</span></span>

[!code-csharp[UseTryParse](../../../samples/csharp/getting-started/WeatherMicroservice/Startup.cs#UseTryParse "Use the try parse extension method")]

<span data-ttu-id="e0a33-230">Pour tester facilement le code d’analyse, mettez à jour la réponse pour inclure les valeurs des arguments :</span><span class="sxs-lookup"><span data-stu-id="e0a33-230">To easily test the parsing code, update the response to include the values of the arguments:</span></span>

[!code-csharp[WriteResponse](../../../samples/csharp/getting-started/WeatherMicroservice/Startup.cs#WriteResponse "Write the output response")]

<span data-ttu-id="e0a33-231">À ce stade, vous pouvez exécuter l’application web et voir si votre code d’analyse fonctionne.</span><span class="sxs-lookup"><span data-stu-id="e0a33-231">At this point, you can run the web application and see if your parsing code is working.</span></span> <span data-ttu-id="e0a33-232">Ajoutez des valeurs à la requête web dans un navigateur, et vous devriez voir les résultats de la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="e0a33-232">Add values to the web request in a browser, and you should see the updated results.</span></span>

### <a name="build-a-random-weather-forecast"></a><span data-ttu-id="e0a33-233">Générer des prévisions météorologiques aléatoires</span><span class="sxs-lookup"><span data-stu-id="e0a33-233">Build a random weather forecast</span></span>

<span data-ttu-id="e0a33-234">La tâche suivante consiste à créer des prévisions météorologiques aléatoires.</span><span class="sxs-lookup"><span data-stu-id="e0a33-234">Your next task is to build a random weather forecast.</span></span> <span data-ttu-id="e0a33-235">Commençons avec un conteneur de données qui contient les valeurs que vous souhaiteriez pour les prévisions météorologiques :</span><span class="sxs-lookup"><span data-stu-id="e0a33-235">Let's start with a data container that holds the values you'd want for a weather forecast:</span></span>

```csharp
public class WeatherReport
{
    private static readonly string[] PossibleConditions = new string[]
    {
        "Sunny",
        "Mostly Sunny",
        "Partly Sunny",
        "Partly Cloudy",
        "Mostly Cloudy",
        "Rain"
    };

    public int HiTemperature { get; }
    public int LoTemperature { get; }
    public int AverageWindSpeed { get; }
    public string Conditions { get; }
}
```

<span data-ttu-id="e0a33-236">Ensuite, générez un constructeur qui définit de façon aléatoire ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="e0a33-236">Next, build a constructor that randomly sets those values.</span></span> <span data-ttu-id="e0a33-237">Ce constructeur utilise les valeurs de latitude et de longitude pour amorcer le générateur de nombres aléatoires.</span><span class="sxs-lookup"><span data-stu-id="e0a33-237">This constructor uses the values for the latitude and longitude to seed the Random number generator.</span></span> <span data-ttu-id="e0a33-238">Cela signifie que la prévision pour un même emplacement est la même.</span><span class="sxs-lookup"><span data-stu-id="e0a33-238">That means the forecast for the same location is the same.</span></span> <span data-ttu-id="e0a33-239">Si vous modifiez les arguments pour la latitude et la longitude, vous obtiendrez une prévision différente (parce que vous démarrez avec une valeur initiale différente.)</span><span class="sxs-lookup"><span data-stu-id="e0a33-239">If you change the arguments for the latitude and longitude, you'll get a different forecast (because you start with a different seed.)</span></span>

[!code-csharp[WeatherReportConstructor](../../../samples/csharp/getting-started/WeatherMicroservice/WeatherReport.cs#WeatherReportConstructor "Weather Report Constructor")]

<span data-ttu-id="e0a33-240">Vous pouvez maintenant générer des prévisions sur 5 jours dans votre méthode de réponse :</span><span class="sxs-lookup"><span data-stu-id="e0a33-240">You can now generate the 5-day forecast in your response method:</span></span>

[!code-csharp[GenerateRandomReport](../../../samples/csharp/getting-started/WeatherMicroservice/Startup.cs#GenerateRandomReport "Generate a random weather report")]

### <a name="build-the-json-response"></a><span data-ttu-id="e0a33-241">Générez la réponse JSON.</span><span class="sxs-lookup"><span data-stu-id="e0a33-241">Build the JSON response.</span></span>

<span data-ttu-id="e0a33-242">La tâche de code final sur le serveur consiste à convertir le tableau WeatherReport en un paquet JSON, et de renvoyer cela au client.</span><span class="sxs-lookup"><span data-stu-id="e0a33-242">The final code task on the server is to convert the WeatherReport array into a JSON packet, and send that back to the client.</span></span> <span data-ttu-id="e0a33-243">Commençons par créer le paquet JSON.</span><span class="sxs-lookup"><span data-stu-id="e0a33-243">Let's start by creating the JSON packet.</span></span> <span data-ttu-id="e0a33-244">Vous allez ajouter le sérialiseur JSON NewtonSoft à la liste des dépendances.</span><span class="sxs-lookup"><span data-stu-id="e0a33-244">You'll add the NewtonSoft JSON Serializer to the list of dependencies.</span></span> <span data-ttu-id="e0a33-245">Pour ce faire, utilisez l’interface CLI `dotnet` :</span><span class="sxs-lookup"><span data-stu-id="e0a33-245">You can do that using the `dotnet` CLI:</span></span>

```
dotnet add package Newtonsoft.Json
```

<span data-ttu-id="e0a33-246">Ensuite, vous pouvez utiliser la classe `JsonConvert` pour écrire l’objet dans une chaîne :</span><span class="sxs-lookup"><span data-stu-id="e0a33-246">Then, you can use the `JsonConvert` class to write the object to a string:</span></span>

[!code-csharp[ConvertToJson](../../../samples/csharp/getting-started/WeatherMicroservice/Startup.cs#ConvertToJSON "Convert objects to JSON")]

<span data-ttu-id="e0a33-247">Le code ci-dessus convertit l’objet de prévision (une liste d’objets `WeatherForecast`) en un paquet JSON.</span><span class="sxs-lookup"><span data-stu-id="e0a33-247">The code above converts the forecast object (a list of `WeatherForecast` objects) into a JSON packet.</span></span> <span data-ttu-id="e0a33-248">Une fois que vous avez construit le paquet de réponse, vous définissez le type de contenu `application/json` et écrivez la chaîne.</span><span class="sxs-lookup"><span data-stu-id="e0a33-248">After you've constructed the response packet, you set the content type to `application/json`, and write the string.</span></span>

<span data-ttu-id="e0a33-249">Maintenant, l’application s’exécute et renvoie des prévisions aléatoires.</span><span class="sxs-lookup"><span data-stu-id="e0a33-249">The application now runs and returns random forecasts.</span></span>

## <a name="build-a-docker-image"></a><span data-ttu-id="e0a33-250">Créer une image Docker</span><span class="sxs-lookup"><span data-stu-id="e0a33-250">Build a Docker image</span></span>

<span data-ttu-id="e0a33-251">La dernière tâche consiste à exécuter l’application dans Docker.</span><span class="sxs-lookup"><span data-stu-id="e0a33-251">Our final task is to run the application in Docker.</span></span> <span data-ttu-id="e0a33-252">Nous allons créer un conteneur Docker qui exécute une image Docker qui représente l’application.</span><span class="sxs-lookup"><span data-stu-id="e0a33-252">We'll create a Docker container that runs a Docker image that represents our application.</span></span>

<span data-ttu-id="e0a33-253">Une ***image Docker*** est un fichier qui définit l’environnement d’exécution de l’application.</span><span class="sxs-lookup"><span data-stu-id="e0a33-253">A ***Docker Image*** is a file that defines the environment for running the application.</span></span>

<span data-ttu-id="e0a33-254">Un ***conteneur Docker*** représente une instance en cours d’exécution d’une image Docker.</span><span class="sxs-lookup"><span data-stu-id="e0a33-254">A ***Docker Container*** represents a running instance of a Docker image.</span></span>

<span data-ttu-id="e0a33-255">Par analogie, vous pouvez considérer *l’Image Docker* comme une *classe* et le *conteneur Docker* comme un objet ou une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="e0a33-255">By analogy, you can think of the *Docker Image* as a *class*, and the *Docker Container* as an object, or an instance of that class.</span></span>  

<span data-ttu-id="e0a33-256">Le fichier Dockerfile créé par le modèle ASP.NET prend en charge nos besoins.</span><span class="sxs-lookup"><span data-stu-id="e0a33-256">The Dockerfile created by the ASP.NET template will serve for our purposes.</span></span> <span data-ttu-id="e0a33-257">Attardons-nous sur son contenu.</span><span class="sxs-lookup"><span data-stu-id="e0a33-257">Let's go over its contents.</span></span>

<span data-ttu-id="e0a33-258">La première ligne indique l’image source :</span><span class="sxs-lookup"><span data-stu-id="e0a33-258">The first line specifies the source image:</span></span>

```
FROM microsoft/dotnet:1.1-sdk-msbuild
```

<span data-ttu-id="e0a33-259">Docker vous permet de configurer une image d’ordinateur basée sur un modèle source.</span><span class="sxs-lookup"><span data-stu-id="e0a33-259">Docker allows you to configure a machine image based on a source template.</span></span> <span data-ttu-id="e0a33-260">Cela signifie que vous n’êtes pas obligé de fournir tous les paramètres de la machine lorsque vous démarrez. Il vous suffit de fournir les modifications éventuelles.</span><span class="sxs-lookup"><span data-stu-id="e0a33-260">That means you don't have to supply all the machine parameters when you start, you only need to supply any changes.</span></span> <span data-ttu-id="e0a33-261">Les modifications apportées ici serviront à inclure notre application.</span><span class="sxs-lookup"><span data-stu-id="e0a33-261">The changes here will be to include our application.</span></span>

<span data-ttu-id="e0a33-262">Dans ce premier exemple, nous allons utiliser la version `1.1-sdk-msbuild` de l’image dotnet.</span><span class="sxs-lookup"><span data-stu-id="e0a33-262">In this first sample, we'll use the `1.1-sdk-msbuild` version of the dotnet image.</span></span> <span data-ttu-id="e0a33-263">Il s’agit du moyen le plus simple de créer un environnement Docker.</span><span class="sxs-lookup"><span data-stu-id="e0a33-263">This is the easiest way to create a working Docker environment.</span></span> <span data-ttu-id="e0a33-264">Cette image inclut le composant d’exécution principal dotnet et le kit de développement logiciel dotnet.</span><span class="sxs-lookup"><span data-stu-id="e0a33-264">This image include the dotnet core runtime, and the dotnet SDK.</span></span> <span data-ttu-id="e0a33-265">Cela facilite la mise en route et la création, mais génère aussi une image plus grande.</span><span class="sxs-lookup"><span data-stu-id="e0a33-265">That makes it easier to get started and build, but does create a larger image.</span></span>

<span data-ttu-id="e0a33-266">Les cinq lignes suivantes configurent et génèrent votre application :</span><span class="sxs-lookup"><span data-stu-id="e0a33-266">The next five lines setup and build your application:</span></span>

```
WORKDIR /app

# copy csproj and restore as distinct layers

COPY WeatherMicroService.csproj .
RUN dotnet restore 

# copy and build everything else

COPY . .

# RUN dotnet restore
RUN dotnet publish -c Release -o out
```

[!INCLUDE[DotNet Restore Note](~/includes/dotnet-restore-note.md)]

<span data-ttu-id="e0a33-267">Cela copie le fichier projet du répertoire actif sur la machine virtuelle Docker et restaure tous les packages.</span><span class="sxs-lookup"><span data-stu-id="e0a33-267">This will copy the project file from the  current directory to the Docker VM, and restore all the packages.</span></span> <span data-ttu-id="e0a33-268">L’utilisation de l’interface de ligne de commande dotnet signifie que l’image Docker doit inclure le kit de développement logiciel .NET Core.</span><span class="sxs-lookup"><span data-stu-id="e0a33-268">Using the dotnet CLI means that the Docker image must include the .NET Core SDK.</span></span> <span data-ttu-id="e0a33-269">Après cela, le reste de votre application est copié et le la commande dotnet publish génère et crée un package de votre application.</span><span class="sxs-lookup"><span data-stu-id="e0a33-269">After that, the rest of your application gets copied, and the dotnet publish command builds and packages your application.</span></span>

<span data-ttu-id="e0a33-270">La dernière ligne du fichier exécute l’application :</span><span class="sxs-lookup"><span data-stu-id="e0a33-270">The final line of the file runs the application:</span></span>

```
ENTRYPOINT ["dotnet", "out/WeatherMicroService.dll", "--server.urls", "http://0.0.0.0:5000"]
```

<span data-ttu-id="e0a33-271">Ce port configuré est référencé dans l’argument `--server.urls` sur `dotnet` sur la dernière ligne du fichier Docker.</span><span class="sxs-lookup"><span data-stu-id="e0a33-271">This configured port is referenced in the `--server.urls` argument to `dotnet` on the last  line of the Dockerfile.</span></span> <span data-ttu-id="e0a33-272">La commande `ENTRYPOINT` informe Docker des options de commande et de ligne de commande qui démarrent le service.</span><span class="sxs-lookup"><span data-stu-id="e0a33-272">The `ENTRYPOINT` command informs Docker what command and command-line options start the service.</span></span> 

## <a name="building-and-running-the-image-in-a-container"></a><span data-ttu-id="e0a33-273">Génération et exécution de l’image dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="e0a33-273">Building and running the image in a container.</span></span>

<span data-ttu-id="e0a33-274">Nous allons créer une image et exécuter le service à l’intérieur d’un conteneur Docker.</span><span class="sxs-lookup"><span data-stu-id="e0a33-274">Let's build an image and run the service inside a Docker container.</span></span> <span data-ttu-id="e0a33-275">Nous ne voulons pas que tous les fichiers de votre répertoire local soient copiés dans l’image.</span><span class="sxs-lookup"><span data-stu-id="e0a33-275">You don't want all the files from your local directory copied into the image.</span></span> <span data-ttu-id="e0a33-276">Au lieu de cela, nous allons développer l’application dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="e0a33-276">Instead, you'll build the application in the container.</span></span> <span data-ttu-id="e0a33-277">Vous allez créer un fichier `.dockerignore` pour spécifier les répertoires qui ne sont pas copiés dans l’image.</span><span class="sxs-lookup"><span data-stu-id="e0a33-277">You'll create a `.dockerignore` file to specify the directories that are not copied into the image.</span></span> <span data-ttu-id="e0a33-278">Nous ne souhaitons copier aucune des ressources build.</span><span class="sxs-lookup"><span data-stu-id="e0a33-278">You don't want any of the build assets copied.</span></span> <span data-ttu-id="e0a33-279">Spécifiez les répertoires build et publish dans le fichier `.dockerignore` :</span><span class="sxs-lookup"><span data-stu-id="e0a33-279">Specify the build and publish directories in the `.dockerignore` file:</span></span>

```
bin/*
obj/*
out/*
```

<span data-ttu-id="e0a33-280">Vous générez l’image avec la commande `docker build`.</span><span class="sxs-lookup"><span data-stu-id="e0a33-280">You build the image using the `docker build` command.</span></span> <span data-ttu-id="e0a33-281">Exécutez la commande suivante à partir du répertoire qui contient votre code.</span><span class="sxs-lookup"><span data-stu-id="e0a33-281">Run the following command from the directory containing your code.</span></span>

```console
docker build -t weather-microservice .
```

<span data-ttu-id="e0a33-282">Cette commande génère l’image de conteneur sur la base de toutes les informations de votre fichier Docker.</span><span class="sxs-lookup"><span data-stu-id="e0a33-282">This command builds the container image based on all the information in your Dockerfile.</span></span> <span data-ttu-id="e0a33-283">L’argument `-t` fournit une balise ou un nom pour cette image de conteneur.</span><span class="sxs-lookup"><span data-stu-id="e0a33-283">The `-t` argument provides a tag, or name, for this container image.</span></span> <span data-ttu-id="e0a33-284">Dans la ligne de commande ci-dessus, la balise utilisée pour le conteneur Docker est `weather-microservice`.</span><span class="sxs-lookup"><span data-stu-id="e0a33-284">In the command line above, the tag used for the Docker container is `weather-microservice`.</span></span> <span data-ttu-id="e0a33-285">Lorsque cette commande est terminée, vous disposez d’un conteneur prêt à exécuter votre nouveau service.</span><span class="sxs-lookup"><span data-stu-id="e0a33-285">When this command completes, you have a container ready to run your new service.</span></span> 

<span data-ttu-id="e0a33-286">Exécutez la commande suivante pour démarrer le conteneur et lancer votre service :</span><span class="sxs-lookup"><span data-stu-id="e0a33-286">Run the following command to start the container and launch your service:</span></span>

```console
docker run -d -p 80:5000 --name hello-docker weather-microservice
```

<span data-ttu-id="e0a33-287">L’option `-d` consiste à exécuter le conteneur de façon détachée du terminal actuel.</span><span class="sxs-lookup"><span data-stu-id="e0a33-287">The `-d` option means to run the container detached from the current terminal.</span></span> <span data-ttu-id="e0a33-288">Cela signifie que vous ne verrez pas le résultat de la commande dans votre terminal.</span><span class="sxs-lookup"><span data-stu-id="e0a33-288">That means you won't see the command output in your terminal.</span></span> <span data-ttu-id="e0a33-289">L’option `-p` indique le mappage de port entre le service et la machine hôte.</span><span class="sxs-lookup"><span data-stu-id="e0a33-289">The `-p` option indicates the port mapping between the service and the host.</span></span> <span data-ttu-id="e0a33-290">Ici, elle indique que toute requête entrante sur le port 80 doit être transférée vers le port 5000 sur le conteneur.</span><span class="sxs-lookup"><span data-stu-id="e0a33-290">Here it says that any incoming request on port 80 should be forwarded to port 5000 on the container.</span></span> <span data-ttu-id="e0a33-291">5000 correspond au port sur lequel votre service écoute venant des arguments de ligne de commande spécifiés dans le fichier Docker ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="e0a33-291">Using 5000 matches the port your service is listening on from the command line arguments specified in the Dockerfile above.</span></span> <span data-ttu-id="e0a33-292">L’argument `--name` nomme votre conteneur en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e0a33-292">The `--name` argument names your running container.</span></span> <span data-ttu-id="e0a33-293">Il s’agit d’un nom convivial que vous pouvez utiliser pour travailler avec ce conteneur.</span><span class="sxs-lookup"><span data-stu-id="e0a33-293">It's a convenient name you can use to work with that container.</span></span> 

<span data-ttu-id="e0a33-294">Vous pouvez voir si l’image est en cours d’exécution avec la commande :</span><span class="sxs-lookup"><span data-stu-id="e0a33-294">You can see if the image is running by checking the command:</span></span>

```console
docker ps
```

<span data-ttu-id="e0a33-295">Si votre conteneur est en cours d’exécution, vous verrez une ligne qui répertorie les processus en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e0a33-295">If your container is running, you'll see a line that lists it in the running processes.</span></span> <span data-ttu-id="e0a33-296">(Il peut s’agir de la seule).</span><span class="sxs-lookup"><span data-stu-id="e0a33-296">(It may be the only one).</span></span>

<span data-ttu-id="e0a33-297">Vous pouvez tester votre service en ouvrant un navigateur et en accédant à localhost et en spécifiant une latitude et une longitude :</span><span class="sxs-lookup"><span data-stu-id="e0a33-297">You can test your service by opening a browser and navigating to localhost, and specifying a latitude and longitude:</span></span>

```
http://localhost/?lat=35.5&long=40.75
```

## <a name="attaching-to-a-running-container"></a><span data-ttu-id="e0a33-298">Attachement à un conteneur en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="e0a33-298">Attaching to a running container</span></span>

<span data-ttu-id="e0a33-299">Lorsque vous avez exécuté votre service dans une fenêtre de commande, vous pouvez voir les informations de diagnostic imprimées pour chaque demande.</span><span class="sxs-lookup"><span data-stu-id="e0a33-299">When you ran your sevice in a command window, you could see diagnostic information printed for each request.</span></span> <span data-ttu-id="e0a33-300">Ces informations ne s’affichent pas lorsque votre conteneur s’exécute en mode détaché.</span><span class="sxs-lookup"><span data-stu-id="e0a33-300">You don't see that information when your container is running in detached mode.</span></span> <span data-ttu-id="e0a33-301">La commande attach de Docker vous permet de vous attacher à un conteneur en cours d’exécution afin de voir les informations du journal.</span><span class="sxs-lookup"><span data-stu-id="e0a33-301">The Docker attach command enables you to attach to a running container so that you can see the log information.</span></span>  <span data-ttu-id="e0a33-302">Exécutez cette commande à partir d’une fenêtre de commande :</span><span class="sxs-lookup"><span data-stu-id="e0a33-302">Run this command from a command window:</span></span>

```console
docker attach --sig-proxy=false hello-docker
```

<span data-ttu-id="e0a33-303">L’argument `--sig-proxy=false` signifie que les commandes `Ctrl-C` ne sont pas envoyées au processus de conteneur, mais arrêtent plutôt la commande `docker attach`.</span><span class="sxs-lookup"><span data-stu-id="e0a33-303">The `--sig-proxy=false` argument means that `Ctrl-C` commands do not get sent to the container process, but rather stop the `docker attach` command.</span></span> <span data-ttu-id="e0a33-304">Le dernier argument est le nom donné au conteneur dans la commande `docker run`.</span><span class="sxs-lookup"><span data-stu-id="e0a33-304">The final argument is the name given to the container in the `docker run` command.</span></span> 

> [!NOTE]
> <span data-ttu-id="e0a33-305">Vous pouvez également utiliser l’ID de conteneur assigné au Docker pour faire référence à un conteneur.</span><span class="sxs-lookup"><span data-stu-id="e0a33-305">You can also use the Docker assigned container ID to refer to any container.</span></span> <span data-ttu-id="e0a33-306">Si vous n’avez pas spécifié de nom pour votre conteneur dans `docker run`, vous devez utiliser l’ID de conteneur.</span><span class="sxs-lookup"><span data-stu-id="e0a33-306">If you didn't specify a name for your container in `docker run` you must use the container id.</span></span>

<span data-ttu-id="e0a33-307">Ouvrez un navigateur et accédez à votre service.</span><span class="sxs-lookup"><span data-stu-id="e0a33-307">Open a browser and navigate to your service.</span></span> <span data-ttu-id="e0a33-308">Vous verrez les messages de diagnostic dans la fenêtre de commande à partir du conteneur en cours d’exécution attaché.</span><span class="sxs-lookup"><span data-stu-id="e0a33-308">You'll see the diagnostic messages in the command windows from the attached running container.</span></span>

<span data-ttu-id="e0a33-309">Appuyez sur `Ctrl-C` pour arrêter le processus d’attachement.</span><span class="sxs-lookup"><span data-stu-id="e0a33-309">Press `Ctrl-C` to stop the attach process.</span></span>

<span data-ttu-id="e0a33-310">Lorsque vous avez terminé de manipuler votre conteneur, vous pouvez l’arrêter :</span><span class="sxs-lookup"><span data-stu-id="e0a33-310">When you are done working with your container, you can stop it:</span></span>

```console
docker stop hello-docker
```

<span data-ttu-id="e0a33-311">Le conteneur et l’image sont toujours disponibles pour vous permettre de redémarrer.</span><span class="sxs-lookup"><span data-stu-id="e0a33-311">The container and image is still available for you to restart.</span></span>  <span data-ttu-id="e0a33-312">Si vous souhaitez supprimer le conteneur de votre machine, utilisez cette commande :</span><span class="sxs-lookup"><span data-stu-id="e0a33-312">If you want to remove the container from your machine, you use this command:</span></span>

```console
docker rm hello-docker
```

<span data-ttu-id="e0a33-313">Si vous souhaitez supprimer des images inutilisées dans votre machine, utilisez cette commande :</span><span class="sxs-lookup"><span data-stu-id="e0a33-313">If you want to remove unused images from your machine, you use this command:</span></span>

```console
docker rmi weather-microservice
```

## <a name="conclusion"></a><span data-ttu-id="e0a33-314">Conclusion</span><span class="sxs-lookup"><span data-stu-id="e0a33-314">Conclusion</span></span> 

<span data-ttu-id="e0a33-315">Dans ce didacticiel, vous avez créé un microservice ASP.NET Core, auquel vous avez ensuite ajouté quelques fonctionnalités simples.</span><span class="sxs-lookup"><span data-stu-id="e0a33-315">In this tutorial, you built an ASP.NET Core microservice, and added a few simple features.</span></span>

<span data-ttu-id="e0a33-316">Vous avez créé une image conteneur Docker pour ce service et exécuté ce conteneur sur votre machine.</span><span class="sxs-lookup"><span data-stu-id="e0a33-316">You built a Docker container image for that service, and ran that container on your machine.</span></span> <span data-ttu-id="e0a33-317">Vous avez attaché une fenêtre de terminal au service et vu les messages de diagnostic à partir de votre service.</span><span class="sxs-lookup"><span data-stu-id="e0a33-317">You attached a terminal window to the service, and saw the diagnostic messages from your service.</span></span>

<span data-ttu-id="e0a33-318">En chemin, vous avez vu plusieurs fonctionnalités du langage C# en action.</span><span class="sxs-lookup"><span data-stu-id="e0a33-318">Along the way, you saw several features of the C# language in action.</span></span>
