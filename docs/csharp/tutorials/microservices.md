---
title: Microservices hébergés dans Docker - C#
description: Apprenez à créer des services principaux ASP.NET qui s’exécutent dans des conteneurs Docker
ms.date: 06/08/2017
ms.assetid: 87e93838-a363-4813-b859-7356023d98ed
ms.openlocfilehash: 1f4b38243beb1210b1374bd701fac66b2fa72cc5
ms.sourcegitcommit: 979597cd8055534b63d2c6ee8322938a27d0c87b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2018
ms.locfileid: "37106348"
---
# <a name="microservices-hosted-in-docker"></a><span data-ttu-id="4f9ad-103">Microservices hébergés dans Docker</span><span class="sxs-lookup"><span data-stu-id="4f9ad-103">Microservices hosted in Docker</span></span>

<span data-ttu-id="4f9ad-104">Ce didacticiel détaille les tâches nécessaires pour générer et déployer un microservice ASP.NET Core dans un conteneur Docker.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-104">This tutorial details the tasks necessary to build and deploy an ASP.NET Core microservice in a Docker container.</span></span> <span data-ttu-id="4f9ad-105">Au cours de ce didacticiel, vous apprendrez à :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-105">During the course of this tutorial, you'll learn:</span></span>

* <span data-ttu-id="4f9ad-106">Générer une application ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-106">How to generate an ASP.NET Core application.</span></span>
* <span data-ttu-id="4f9ad-107">Créer un environnement de développement Docker.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-107">How to create a development Docker environment.</span></span>
* <span data-ttu-id="4f9ad-108">Créer une image Docker basée sur une image existante.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-108">How to build a Docker image based on an existing image.</span></span>
* <span data-ttu-id="4f9ad-109">Déployer votre service dans un conteneur Docker.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-109">How to deploy your service into a Docker container.</span></span>

<span data-ttu-id="4f9ad-110">Au passage, vous verrez également certaines fonctionnalités du langage C# :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-110">Along the way, you'll also see some C# language features:</span></span>

* <span data-ttu-id="4f9ad-111">Conversion des objets C# en charges utiles JSON.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-111">How to convert C# objects into JSON payloads.</span></span>
* <span data-ttu-id="4f9ad-112">Création d’objets de transfert de données immuables</span><span class="sxs-lookup"><span data-stu-id="4f9ad-112">How to build immutable Data Transfer Objects.</span></span>
* <span data-ttu-id="4f9ad-113">Traitement des requêtes HTTP entrantes et création de la réponse HTTP</span><span class="sxs-lookup"><span data-stu-id="4f9ad-113">How to process incoming HTTP Requests and generate the HTTP Response.</span></span>
* <span data-ttu-id="4f9ad-114">Utilisation des types valeur Nullable</span><span class="sxs-lookup"><span data-stu-id="4f9ad-114">How to work with nullable value types.</span></span>

<span data-ttu-id="4f9ad-115">Vous pouvez [afficher ou télécharger l’exemple d’application](https://github.com/dotnet/samples/tree/master/csharp/getting-started/WeatherMicroservice) de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-115">You can [view or download the sample app](https://github.com/dotnet/samples/tree/master/csharp/getting-started/WeatherMicroservice) for this topic.</span></span> <span data-ttu-id="4f9ad-116">Pour obtenir des instructions de téléchargement, consultez [Exemples et didacticiels](../../samples-and-tutorials/index.md#viewing-and-downloading-samples).</span><span class="sxs-lookup"><span data-stu-id="4f9ad-116">For download instructions, see [Samples and Tutorials](../../samples-and-tutorials/index.md#viewing-and-downloading-samples).</span></span>

## <a name="why-docker"></a><span data-ttu-id="4f9ad-117">Pourquoi Docker ?</span><span class="sxs-lookup"><span data-stu-id="4f9ad-117">Why Docker?</span></span>

<span data-ttu-id="4f9ad-118">Docker facilite la création d’images de machine standard pour héberger vos services dans un centre de données ou dans le cloud public.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-118">Docker makes it easy to create standard machine images to host your services in a data center, or the public cloud.</span></span> <span data-ttu-id="4f9ad-119">Docker vous permet de configurer l’image et de la répliquer en fonction des besoins pour mettre à l’échelle l’installation de votre application.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-119">Docker enables you to configure the image, and replicate it as needed to scale the installation of your application.</span></span>

<span data-ttu-id="4f9ad-120">Tout le code de ce didacticiel fonctionne dans n’importe quel environnement .NET Core.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-120">All the code in this tutorial will work in any .NET Core environment.</span></span>
<span data-ttu-id="4f9ad-121">Les tâches supplémentaires pour une installation Docker fonctionneront pour une application ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-121">The additional tasks for a Docker installation will work for an ASP.NET Core application.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="4f9ad-122">Prérequis</span><span class="sxs-lookup"><span data-stu-id="4f9ad-122">Prerequisites</span></span>

<span data-ttu-id="4f9ad-123">Vous devez configurer votre ordinateur pour exécuter .NET Core.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-123">You’ll need to setup your machine to run .NET Core.</span></span> <span data-ttu-id="4f9ad-124">Vous trouverez les instructions d’installation sur la page de [.NET Core](https://www.microsoft.com/net/core).</span><span class="sxs-lookup"><span data-stu-id="4f9ad-124">You can find the installation instructions on the [.NET Core](https://www.microsoft.com/net/core) page.</span></span>
<span data-ttu-id="4f9ad-125">Vous pouvez exécuter cette application sur Windows, Linux, Mac OS ou dans un conteneur Docker.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-125">You can run this application on Windows, Linux, macOS or in a Docker container.</span></span>
<span data-ttu-id="4f9ad-126">Vous devez installer l’éditeur de code de votre choix.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-126">You’ll need to install your favorite code editor.</span></span> <span data-ttu-id="4f9ad-127">Les descriptions ci-dessous utilisent [Visual Studio Code](https://code.visualstudio.com/), un éditeur open source et multiplateforme.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-127">The descriptions below use [Visual Studio Code](https://code.visualstudio.com/) which is an open source, cross platform editor.</span></span> <span data-ttu-id="4f9ad-128">Cependant, vous pouvez utiliser les outils avec lesquels vous êtes le plus à l’aise.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-128">However, you can use whatever tools you are comfortable with.</span></span>

<span data-ttu-id="4f9ad-129">Vous devez également installer le moteur Docker.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-129">You'll also need to install the Docker engine.</span></span> <span data-ttu-id="4f9ad-130">Consultez la [page d’installation de Docker](http://www.docker.com/products/docker) pour obtenir des instructions pour votre plateforme.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-130">See the [Docker Installation page](http://www.docker.com/products/docker) for instructions for your platform.</span></span>
<span data-ttu-id="4f9ad-131">Docker peut être installé dans de nombreuses distributions Linux, Mac OS ou Windows.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-131">Docker can be installed in many Linux distributions, macOS, or Windows.</span></span> <span data-ttu-id="4f9ad-132">La page mentionnée ci-dessus contient des sections pour chacune des installations disponibles.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-132">The page referenced above contains sections to each of the available installations.</span></span>

## <a name="create-the-application"></a><span data-ttu-id="4f9ad-133">Création de l’application</span><span class="sxs-lookup"><span data-stu-id="4f9ad-133">Create the Application</span></span>

<span data-ttu-id="4f9ad-134">Maintenant que vous avez installé tous les outils, créez une application ASP.NET Core dans un répertoire appelé « WeatherMicroservice » en exécutant la commande suivante dans votre interpréteur de commandes préféré :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-134">Now that you've installed all the tools, create a new ASP.NET Core application in a directory called "WeatherMicroservice" by executing the following command in your favorite shell:</span></span>

```console
dotnet new web -o WeatherMicroservice
```

<span data-ttu-id="4f9ad-135">La commande `dotnet` exécute les outils nécessaires pour le développement .NET.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-135">The `dotnet` command runs the tools necessary for .NET development.</span></span> <span data-ttu-id="4f9ad-136">Chaque verbe exécute une commande différente.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-136">Each verb executes a different command.</span></span>

<span data-ttu-id="4f9ad-137">La commande `dotnet new` sert à créer des projets .NET Core.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-137">The `dotnet new` command is used to create .Net Core projects.</span></span>

<span data-ttu-id="4f9ad-138">L’option `-o WeatherMicroservice` après la commande `dotnet new` est utilisée pour indiquer l’emplacement où créer l’application ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-138">The `-o WeatherMicroservice` option after the `dotnet new` command is used to give the location to create the ASP.NET Core application.</span></span>

<span data-ttu-id="4f9ad-139">Pour ce microservice, nous souhaitons que l’application web soit la plus simple et la plus légère possible. Nous avons donc utilisé le modèle « ASP.NET Core vide », en spécifiant son nom court, `web`.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-139">For this microservice, we want the simplest, most lightweight web application possible, so we used the "ASP.NET Core Empty" template, by specifying its short name, `web`.</span></span>

<span data-ttu-id="4f9ad-140">Le modèle crée quatre fichiers pour vous :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-140">The template creates four files for you:</span></span>

* <span data-ttu-id="4f9ad-141">Un fichier Startup.cs.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-141">A Startup.cs file.</span></span> <span data-ttu-id="4f9ad-142">Cela contient la base de l’application.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-142">This contains the basis of the application.</span></span>
* <span data-ttu-id="4f9ad-143">Un fichier Program.cs.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-143">A Program.cs file.</span></span> <span data-ttu-id="4f9ad-144">Cela contient le point d’entrée de l’application.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-144">This contains the entry point of the application.</span></span>
* <span data-ttu-id="4f9ad-145">Un fichier WeatherMicroservice.csproj.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-145">A WeatherMicroservice.csproj file.</span></span> <span data-ttu-id="4f9ad-146">Il s’agit du fichier de génération de l’application.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-146">This is the build file for the application.</span></span>
* <span data-ttu-id="4f9ad-147">Un fichier Properties/launchSettings.json.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-147">A Properties/launchSettings.json file.</span></span> <span data-ttu-id="4f9ad-148">Il contient les paramètres de débogage utilisés par l’EDI.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-148">This contains debugging settings used by IDEs.</span></span>

<span data-ttu-id="4f9ad-149">Vous pouvez maintenant exécuter l’application générée par le modèle :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-149">Now you can run the template generated application:</span></span>

```console
dotnet run
```

<span data-ttu-id="4f9ad-150">Cette commande restaure tout d’abord les dépendances requises pour générer l’application, puis elle génère l’application.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-150">This command will first restore dependencies required to build the application and then it will build the application.</span></span>

<span data-ttu-id="4f9ad-151">La configuration par défaut écoute le port `http://localhost:5000`.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-151">The default configuration listens to `http://localhost:5000`.</span></span> <span data-ttu-id="4f9ad-152">Vous pouvez ouvrir un navigateur et accéder à cette page pour voir un « Hello World! »</span><span class="sxs-lookup"><span data-stu-id="4f9ad-152">You can open a browser and navigate to that page and see a "Hello World!"</span></span> <span data-ttu-id="4f9ad-153">« Operation Not Found! ».</span><span class="sxs-lookup"><span data-stu-id="4f9ad-153">message.</span></span>

<span data-ttu-id="4f9ad-154">Quand vous avez terminé, vous pouvez arrêter l’application en appuyant sur <kbd>Ctrl</kbd>+<kbd>C</kbd>.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-154">When you're done, you can shut down the application by pressing <kbd>Ctrl</kbd>+<kbd>C</kbd>.</span></span>

### <a name="anatomy-of-an-aspnet-core-application"></a><span data-ttu-id="4f9ad-155">Anatomie d’une application ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="4f9ad-155">Anatomy of an ASP.NET Core application</span></span>

<span data-ttu-id="4f9ad-156">Maintenant que vous avez créé l’application, nous allons voir comment cette fonctionnalité est implémentée.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-156">Now that you've built the application, let's look at how this functionality is implemented.</span></span> <span data-ttu-id="4f9ad-157">Deux des fichiers générés sont particulièrement intéressants à ce stade : WeatherMicroservice.csproj et Startup.cs.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-157">There are two of the generated files that are particularly interesting at this point: WeatherMicroservice.csproj and Startup.cs.</span></span> 

<span data-ttu-id="4f9ad-158">Le fichier .csproj contient des informations sur le projet.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-158">The .csproj file contains information about the project.</span></span>
<span data-ttu-id="4f9ad-159">Les deux nœuds les plus intéressants sont `<TargetFramework>` et `<PackageReference>`.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-159">The two nodes that are most interesting are `<TargetFramework>` and `<PackageReference>`.</span></span>

<span data-ttu-id="4f9ad-160">Le nœud `<TargetFramework>` spécifie la version de .NET qui exécutera cette application.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-160">The `<TargetFramework>` node specifies the version of .NET that will run this application.</span></span>

<span data-ttu-id="4f9ad-161">Chaque nœud `<PackageReference>` sert à spécifier un package qui est nécessaire pour cette application.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-161">Each `<PackageReference>` node is used to specify a package that is needed for this application.</span></span>

<span data-ttu-id="4f9ad-162">L’application est implémentée dans Startup.cs.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-162">The application is implemented in Startup.cs.</span></span> <span data-ttu-id="4f9ad-163">Ce fichier contient la classe de démarrage.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-163">This file contains the startup class.</span></span>

<span data-ttu-id="4f9ad-164">Les deux méthodes sont appelées par l’infrastructure ASP.NET Core pour configurer et exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-164">The two methods are called by the ASP.NET Core infrastructure to configure and run the application.</span></span> <span data-ttu-id="4f9ad-165">La méthode `ConfigureServices` décrit les services qui sont nécessaires pour cette application.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-165">The `ConfigureServices` method describes the services that are necessary for this application.</span></span> <span data-ttu-id="4f9ad-166">Vous créez un microservice épuré, vous n’avez donc pas besoin de configurer de dépendances.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-166">You're building a lean microservice, so it doesn't need to configure any dependencies.</span></span> <span data-ttu-id="4f9ad-167">La méthode `Configure` configure les gestionnaires pour les requêtes HTTP entrantes.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-167">The `Configure` method configures the handlers for incoming HTTP Requests.</span></span> <span data-ttu-id="4f9ad-168">Le modèle génère un gestionnaire simple qui répond à une demande dont le texte est « Hello World! ».</span><span class="sxs-lookup"><span data-stu-id="4f9ad-168">The template generates a simple handler that responds to any request with the text 'Hello World!'.</span></span>

## <a name="build-a-microservice"></a><span data-ttu-id="4f9ad-169">Créer un microservice</span><span class="sxs-lookup"><span data-stu-id="4f9ad-169">Build a microservice</span></span>

<span data-ttu-id="4f9ad-170">Le service que vous vous apprêtez à générer fournira des rapports météorologiques depuis n’importe où dans le monde.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-170">The service you're going to build will deliver weather reports from anywhere around the globe.</span></span> <span data-ttu-id="4f9ad-171">Dans une application de production, vous appelleriez un service pour récupérer des données météorologiques.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-171">In a production application, you'd call some service to retrieve weather data.</span></span> <span data-ttu-id="4f9ad-172">Pour notre exemple, nous allons générer des prévisions météorologiques aléatoires.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-172">For our sample, we'll generate a random weather forecast.</span></span> 

<span data-ttu-id="4f9ad-173">Il existe un certain nombre de tâches que vous devez effectuer pour implémenter notre service météo aléatoire :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-173">There are a number of tasks you'll need to perform in order to implement our random weather service:</span></span>

* <span data-ttu-id="4f9ad-174">Analyser la requête entrante pour lire la latitude et la longitude.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-174">Parse the incoming request to read the latitude and longitude.</span></span>
* <span data-ttu-id="4f9ad-175">Générer des données de prévision aléatoires.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-175">Generate some random forecast data.</span></span>
* <span data-ttu-id="4f9ad-176">Convertir ces données de prévision aléatoires d’objets C# en paquets JSON.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-176">Convert that random forecast data from C# objects into JSON packets.</span></span>
* <span data-ttu-id="4f9ad-177">Définir l’en-tête de réponse pour indiquer que votre service renvoie JSON.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-177">Set the response header to indicate that your service sends back JSON.</span></span>
* <span data-ttu-id="4f9ad-178">Écrivez la réponse.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-178">Write the response.</span></span>

<span data-ttu-id="4f9ad-179">Les sections suivantes décrivent chacune de ces étapes.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-179">The next sections walk you through each of these steps.</span></span>

### <a name="parsing-the-query-string"></a><span data-ttu-id="4f9ad-180">Analyse de la chaîne de requête</span><span class="sxs-lookup"><span data-stu-id="4f9ad-180">Parsing the Query String</span></span>

<span data-ttu-id="4f9ad-181">Vous commencerez par analyser la chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-181">You'll begin by parsing the query string.</span></span> <span data-ttu-id="4f9ad-182">Le service acceptera les arguments 'lat' et 'longs' sur la chaîne de requête dans ce formulaire :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-182">The service will accept 'lat' and 'long' arguments on the query string in this form:</span></span>

```
http://localhost:5000/?lat=-35.55&long=-12.35
```

<span data-ttu-id="4f9ad-183">Toutes les modifications que vous devez apporter se trouvent dans l’expression lambda définie comme argument de `app.Run` dans votre classe de démarrage.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-183">All the changes you need to make are in the lambda expression defined as the argument to `app.Run` in your startup class.</span></span>

<span data-ttu-id="4f9ad-184">L’argument de l’expression lambda est le `HttpContext` pour la demande.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-184">The argument on the lambda expression is the `HttpContext` for the request.</span></span> <span data-ttu-id="4f9ad-185">Une de ses propriétés est l’objet `Request`.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-185">One of its properties is the `Request` object.</span></span> <span data-ttu-id="4f9ad-186">L’objet `Request` a une propriété `Query` qui contient un dictionnaire de toutes les valeurs dans la chaîne de requête pour la demande.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-186">The `Request` object has a `Query` property that contains a dictionary of all the values on the query string for the request.</span></span> <span data-ttu-id="4f9ad-187">La première addition consiste à rechercher les valeurs de latitude et longitude :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-187">The first addition is to find the latitude and longitude values:</span></span>

[!code-csharp[ReadQueryString](../../../samples/csharp/getting-started/WeatherMicroservice/Startup.cs#ReadQueryString "read variables from the query string")]

<span data-ttu-id="4f9ad-188">Les valeurs du dictionnaire `Query` sont de type `StringValue`.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-188">The `Query` dictionary values are `StringValue` type.</span></span> <span data-ttu-id="4f9ad-189">Ce type peut contenir une collection de chaînes.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-189">That type can contain a collection of strings.</span></span> <span data-ttu-id="4f9ad-190">Pour votre service météo, chaque valeur est une chaîne unique.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-190">For your weather service, each value is a single string.</span></span> <span data-ttu-id="4f9ad-191">C’est pourquoi il y a un appel à `FirstOrDefault()` dans le code ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-191">That's why there's the call to `FirstOrDefault()` in the code above.</span></span> 

<span data-ttu-id="4f9ad-192">Ensuite, vous devez convertir les chaînes en valeurs de type double.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-192">Next, you need to convert the strings to doubles.</span></span> <span data-ttu-id="4f9ad-193">La méthode que vous allez utiliser pour convertir la chaîne en double est `double.TryParse()` :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-193">The method you'll use to convert the string to a double is `double.TryParse()`:</span></span>

```csharp
bool TryParse(string s, out double result);
```

<span data-ttu-id="4f9ad-194">Cette méthode s’appuie sur les paramètres de sortie de C# pour indiquer si la chaîne d’entrée peut être convertie en double.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-194">This method leverages C# out parameters to indicate if the input string can be converted to a double.</span></span> <span data-ttu-id="4f9ad-195">Si la chaîne constitue une représentation valide pour un double, la méthode retourne true et l’argument `result` contient la valeur.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-195">If the string does represent a valid representation for a double, the method returns true, and the `result` argument contains the value.</span></span> <span data-ttu-id="4f9ad-196">Si la chaîne ne représente pas une valeur double valide, la méthode retourne false.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-196">If the string does not represent a valid double, the method returns false.</span></span>

<span data-ttu-id="4f9ad-197">Vous pouvez adapter cette API à l’aide d’une *méthode d’extension* qui renvoie un *double Nullable*.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-197">You can adapt that API with the use of an *extension method* that returns a *nullable double*.</span></span> <span data-ttu-id="4f9ad-198">Un *type de valeur Nullable* est un type qui représente un type de valeur et peut également contenir un une valeur manquante ou Null.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-198">A *nullable value type* is a type that represents some value type, and can also hold a missing, or null value.</span></span> <span data-ttu-id="4f9ad-199">Un type Nullable est représenté en ajoutant le caractère `?` à la déclaration de type.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-199">A nullable type is represented by appending the `?` character to the type declaration.</span></span> 

<span data-ttu-id="4f9ad-200">Les méthodes d’extension sont des méthodes qui sont définies comme des méthodes statiques mais qui, en ajoutant le modificateur `this` sur le premier paramètre, peuvent être appelées comme si elles étaient des membres de cette classe.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-200">Extension methods are methods that are defined as static methods, but by adding the `this` modifier on the first parameter, can be called as though they are members of that class.</span></span> <span data-ttu-id="4f9ad-201">Les méthodes d’extension peuvent être définies uniquement dans les classes statiques.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-201">Extension methods may only be defined in static classes.</span></span> <span data-ttu-id="4f9ad-202">Voici la définition de la classe contenant la méthode d’extension pour l’analyse :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-202">Here's the definition of the class containing the extension method for parse:</span></span>

[!code-csharp[TryParseExtension](../../../samples/csharp/getting-started/WeatherMicroservice/Extensions.cs#TryParseExtension "try parse to a nullable")]

<span data-ttu-id="4f9ad-203">Avant d’appeler la méthode d’extension, changez la culture actuelle pour qu’elle soit invariante :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-203">Before calling the extension method, change the current culture to invariant:</span></span>

[!code-csharp[SetCulture](../../../samples/csharp/getting-started/WeatherMicroservice/Startup.cs#SetCulture "set current culture to invariant")]

<span data-ttu-id="4f9ad-204">Cela permet de s’assurer que votre application analyse les nombres de la même façon sur tous les serveurs, quel que soit sa culture par défaut.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-204">This ensures that your application parses numbers the same on any server, regardless of its default culture.</span></span>

<span data-ttu-id="4f9ad-205">Vous pouvez maintenant utiliser la méthode d’extension pour convertir les arguments de chaîne de requête en type double :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-205">Now you can use the extension method to convert the query string arguments into the double type:</span></span>

[!code-csharp[UseTryParse](../../../samples/csharp/getting-started/WeatherMicroservice/Startup.cs#UseTryParse "Use the try parse extension method")]

<span data-ttu-id="4f9ad-206">Pour tester facilement le code d’analyse, mettez à jour la réponse pour inclure les valeurs des arguments :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-206">To easily test the parsing code, update the response to include the values of the arguments:</span></span>

[!code-csharp[WriteResponse](../../../samples/csharp/getting-started/WeatherMicroservice/Startup.cs#WriteResponse "Write the output response")]

<span data-ttu-id="4f9ad-207">À ce stade, vous pouvez exécuter l’application web et voir si votre code d’analyse fonctionne.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-207">At this point, you can run the web application and see if your parsing code is working.</span></span> <span data-ttu-id="4f9ad-208">Ajoutez des valeurs à la requête web dans un navigateur, et vous devriez voir les résultats de la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-208">Add values to the web request in a browser, and you should see the updated results.</span></span>

### <a name="build-a-random-weather-forecast"></a><span data-ttu-id="4f9ad-209">Générer des prévisions météorologiques aléatoires</span><span class="sxs-lookup"><span data-stu-id="4f9ad-209">Build a random weather forecast</span></span>

<span data-ttu-id="4f9ad-210">La tâche suivante consiste à créer des prévisions météorologiques aléatoires.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-210">Your next task is to build a random weather forecast.</span></span> <span data-ttu-id="4f9ad-211">Commençons avec un conteneur de données qui contient les valeurs que vous souhaiteriez pour les prévisions météorologiques :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-211">Let's start with a data container that holds the values you'd want for a weather forecast:</span></span>

```csharp
public class WeatherReport
{
    private static readonly string[] PossibleConditions =
    {
        "Sunny",
        "Mostly Sunny",
        "Partly Sunny",
        "Partly Cloudy",
        "Mostly Cloudy",
        "Rain"
    };

    public int HighTemperatureFahrenheit { get; }
    public int LowTemperatureFahrenheit { get; }
    public int AverageWindSpeedMph { get; }
    public string Condition { get; }
}
```

<span data-ttu-id="4f9ad-212">Ensuite, générez un constructeur qui définit de façon aléatoire ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-212">Next, build a constructor that randomly sets those values.</span></span> <span data-ttu-id="4f9ad-213">Ce constructeur utilise les valeurs de latitude et de longitude pour amorcer le générateur de nombres `Random`.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-213">This constructor uses the values for the latitude and longitude to seed the `Random` number generator.</span></span> <span data-ttu-id="4f9ad-214">Cela signifie que la prévision pour un même emplacement est la même.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-214">That means the forecast for the same location is the same.</span></span> <span data-ttu-id="4f9ad-215">Si vous changez les arguments de latitude et de longitude, vous obtiendrez une prévision différente (car vous démarrez avec une valeur initiale différente).</span><span class="sxs-lookup"><span data-stu-id="4f9ad-215">If you change the arguments for the latitude and longitude, you'll get a different forecast (because you start with a different seed).</span></span>

[!code-csharp[WeatherReportConstructor](../../../samples/csharp/getting-started/WeatherMicroservice/WeatherReport.cs#WeatherReportConstructor "Weather Report Constructor")]

<span data-ttu-id="4f9ad-216">Vous pouvez maintenant générer des prévisions sur 5 jours dans votre méthode de réponse :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-216">You can now generate the 5-day forecast in your response method:</span></span>

```csharp
if (latitude.HasValue && longitude.HasValue)
{
    var forecast = new List<WeatherReport>();
    for (var days = 1; days <= 5; days++)
    {
        forecast.Add(new WeatherReport(latitude.Value, longitude.Value, days));
    }
}
```

### <a name="build-the-json-response"></a><span data-ttu-id="4f9ad-217">Générer la réponse JSON</span><span class="sxs-lookup"><span data-stu-id="4f9ad-217">Build the JSON response</span></span>

<span data-ttu-id="4f9ad-218">La tâche de code finale sur le serveur consiste à convertir la liste `WeatherReport` en document JSON, et à renvoyer cela au client.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-218">The final code task on the server is to convert the `WeatherReport` list into JSON document, and send that back to the client.</span></span> <span data-ttu-id="4f9ad-219">Commençons par créer le document JSON.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-219">Let's start by creating the JSON document.</span></span> <span data-ttu-id="4f9ad-220">Vous allez ajouter le sérialiseur JSON Newtonsoft à la liste des dépendances.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-220">You'll add the Newtonsoft JSON serializer to the list of dependencies.</span></span> <span data-ttu-id="4f9ad-221">Vous pouvez pour cela utiliser la commande `dotnet` suivante :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-221">You can do that using the following `dotnet` command:</span></span>

```console
dotnet add package Newtonsoft.Json
```

<span data-ttu-id="4f9ad-222">Ensuite, vous pouvez utiliser la classe `JsonConvert` pour écrire l’objet dans une chaîne :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-222">Then, you can use the `JsonConvert` class to write the object to a string:</span></span>

[!code-csharp[ConvertToJson](../../../samples/csharp/getting-started/WeatherMicroservice/Startup.cs#ConvertToJSON "Convert objects to JSON")]

<span data-ttu-id="4f9ad-223">Le code ci-dessus convertit l’objet de prévision (une liste d’objets `WeatherForecast`) en document JSON.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-223">The code above converts the forecast object (a list of `WeatherForecast` objects) into a JSON document.</span></span> <span data-ttu-id="4f9ad-224">Une fois que vous avez construit le document de réponse, vous définissez le type de contenu `application/json` et écrivez la chaîne.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-224">After you've constructed the response document, you set the content type to `application/json`, and write the string.</span></span>

<span data-ttu-id="4f9ad-225">Maintenant, l’application s’exécute et renvoie des prévisions aléatoires.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-225">The application now runs and returns random forecasts.</span></span>

## <a name="build-a-docker-image"></a><span data-ttu-id="4f9ad-226">Créer une image Docker</span><span class="sxs-lookup"><span data-stu-id="4f9ad-226">Build a Docker image</span></span>

<span data-ttu-id="4f9ad-227">La dernière tâche consiste à exécuter l’application dans Docker.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-227">Our final task is to run the application in Docker.</span></span> <span data-ttu-id="4f9ad-228">Nous allons créer un conteneur Docker qui exécute une image Docker qui représente l’application.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-228">We'll create a Docker container that runs a Docker image that represents our application.</span></span>

<span data-ttu-id="4f9ad-229">Une ***image Docker*** est un fichier qui définit l’environnement d’exécution de l’application.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-229">A ***Docker Image*** is a file that defines the environment for running the application.</span></span>

<span data-ttu-id="4f9ad-230">Un ***conteneur Docker*** représente une instance en cours d’exécution d’une image Docker.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-230">A ***Docker Container*** represents a running instance of a Docker Image.</span></span>

<span data-ttu-id="4f9ad-231">Par analogie, vous pouvez considérer *l’Image Docker* comme une *classe* et le *conteneur Docker* comme un objet ou une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-231">By analogy, you can think of the *Docker Image* as a *class*, and the *Docker Container* as an object, or an instance of that class.</span></span>  

<span data-ttu-id="4f9ad-232">Le Dockerfile suivant correspond à nos besoins :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-232">The following Dockerfile will serve for our purposes:</span></span>

```
FROM microsoft/dotnet:2.1-sdk AS build
WORKDIR /app

# Copy csproj and restore as distinct layers
COPY *.csproj ./
RUN dotnet restore

# Copy everything else and build
COPY . ./
RUN dotnet publish -c Release -o out

# Build runtime image
FROM microsoft/dotnet:2.1-aspnetcore-runtime
WORKDIR /app
COPY --from=build /app/out .
ENTRYPOINT ["dotnet", "WeatherMicroservice.dll"]
```

<span data-ttu-id="4f9ad-233">Attardons-nous sur son contenu.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-233">Let's go over its contents.</span></span>

<span data-ttu-id="4f9ad-234">La première ligne spécifie l’image source utilisée pour générer l’application :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-234">The first line specifies the source image used for building the application:</span></span>

```
FROM microsoft/dotnet:2.1-sdk AS build
```

<span data-ttu-id="4f9ad-235">Docker vous permet de configurer une image d’ordinateur basée sur un modèle source.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-235">Docker allows you to configure a machine image based on a source template.</span></span> <span data-ttu-id="4f9ad-236">Cela signifie que vous n’êtes pas obligé de fournir tous les paramètres de la machine lorsque vous démarrez. Il vous suffit de fournir les modifications éventuelles.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-236">That means you don't have to supply all the machine parameters when you start, you only need to supply any changes.</span></span> <span data-ttu-id="4f9ad-237">Les modifications apportées ici serviront à inclure notre application.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-237">The changes here will be to include our application.</span></span>

<span data-ttu-id="4f9ad-238">Dans cet exemple, nous allons utiliser la version `2.1-sdk` de l’image `dotnet`.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-238">In this sample, we'll use the `2.1-sdk` version of the `dotnet` image.</span></span> <span data-ttu-id="4f9ad-239">Il s’agit du moyen le plus simple de créer un environnement Docker.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-239">This is the easiest way to create a working Docker environment.</span></span> <span data-ttu-id="4f9ad-240">Cette image inclut le runtime .NET Core et le kit SDK .NET Core.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-240">This image includes the .NET Core runtime, and the .NET Core SDK.</span></span>
<span data-ttu-id="4f9ad-241">Cela simplifie la prise en main et la génération initiale, mais crée une image plus grande. Nous allons donc utiliser cette image pour générer l’application et une image différente pour l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-241">That makes it easier to get started and build, but does create a larger image, so we'll use this image for building the application and a different image to run it.</span></span>

<span data-ttu-id="4f9ad-242">Les lignes suivantes configurent et génèrent votre application :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-242">The next lines setup and build your application:</span></span>

```
WORKDIR /app

# Copy csproj and restore as distinct layers
COPY *.csproj ./
RUN dotnet restore

# Copy everything else and build
COPY . ./
RUN dotnet publish -c Release -o out
```

<span data-ttu-id="4f9ad-243">Cela copie le fichier projet du répertoire actif sur la machine virtuelle Docker et restaure tous les packages.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-243">This will copy the project file from the  current directory to the Docker VM, and restore all the packages.</span></span> <span data-ttu-id="4f9ad-244">L’utilisation de l’interface de ligne de commande dotnet signifie que l’image Docker doit inclure le kit de développement logiciel .NET Core.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-244">Using the dotnet CLI means that the Docker image must include the .NET Core SDK.</span></span> <span data-ttu-id="4f9ad-245">Après cela, le reste de votre application est copié et la commande `dotnet
publish` génère et crée un package de votre application.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-245">After that, the rest of your application gets copied, and the `dotnet
publish` command builds and packages your application.</span></span>

<span data-ttu-id="4f9ad-246">Pour finir, nous allons créer une deuxième image Docker qui exécute l’application :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-246">Finally, we create a second Docker image that runs the application:</span></span>

```
# Build runtime image
FROM microsoft/dotnet:2.1-aspnetcore-runtime
WORKDIR /app
COPY --from=build /app/out .
ENTRYPOINT ["dotnet", "WeatherMicroservice.dll"]
```

<span data-ttu-id="4f9ad-247">Cette image utilise la version `2.1-aspnetcore-runtime` de l’image `dotnet`, qui contient tous les éléments nécessaires pour exécuter des applications ASP.NET Core, mais n’inclut pas le kit SDK .NET Core.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-247">This image uses the `2.1-aspnetcore-runtime` version of the `dotnet` image, which contains everything necessary to run ASP.NET Core applications, but does not include the .NET Core SDK.</span></span> <span data-ttu-id="4f9ad-248">Cela signifie que nous ne pouvons pas utiliser cette image pour créer des applications .NET Core, mais par contre cela limite la taille de l’image finale.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-248">This means this image can't be used to build .NET Core applications, but it also makes the final image smaller.</span></span>

<span data-ttu-id="4f9ad-249">Nous allons copier l’application générée de la première image vers la deuxième.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-249">To make this work, we copy the built application from the first image to the second one.</span></span>

<span data-ttu-id="4f9ad-250">La commande `ENTRYPOINT` indique à Docker quelle commande démarre le service.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-250">The `ENTRYPOINT` command informs Docker what command starts the service.</span></span>

## <a name="building-and-running-the-image-in-a-container"></a><span data-ttu-id="4f9ad-251">Génération et exécution de l’image dans un conteneur</span><span class="sxs-lookup"><span data-stu-id="4f9ad-251">Building and running the image in a container</span></span>

<span data-ttu-id="4f9ad-252">Nous allons créer une image et exécuter le service à l’intérieur d’un conteneur Docker.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-252">Let's build an image and run the service inside a Docker container.</span></span> <span data-ttu-id="4f9ad-253">Nous ne voulons pas que tous les fichiers de votre répertoire local soient copiés dans l’image.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-253">You don't want all the files from your local directory copied into the image.</span></span> <span data-ttu-id="4f9ad-254">Au lieu de cela, nous allons développer l’application dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-254">Instead, you'll build the application in the container.</span></span> <span data-ttu-id="4f9ad-255">Vous allez créer un fichier `.dockerignore` pour spécifier les répertoires qui ne sont pas copiés dans l’image.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-255">You'll create a `.dockerignore` file to specify the directories that are not copied into the image.</span></span> <span data-ttu-id="4f9ad-256">Nous ne souhaitons copier aucune des ressources build.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-256">You don't want any of the build assets copied.</span></span> <span data-ttu-id="4f9ad-257">Spécifiez les répertoires build et publish dans le fichier `.dockerignore` :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-257">Specify the build and publish directories in the `.dockerignore` file:</span></span>

```
bin/*
obj/*
out/*
```

<span data-ttu-id="4f9ad-258">Vous générez l’image avec la commande `docker build`.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-258">You build the image using the `docker build` command.</span></span> <span data-ttu-id="4f9ad-259">Exécutez la commande suivante à partir du répertoire qui contient votre code.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-259">Run the following command from the directory containing your code.</span></span>

```console
docker build -t weather-microservice .
```

<span data-ttu-id="4f9ad-260">Cette commande génère l’image de conteneur sur la base de toutes les informations de votre fichier Docker.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-260">This command builds the container image based on all the information in your Dockerfile.</span></span> <span data-ttu-id="4f9ad-261">L’argument `-t` fournit une balise ou un nom pour cette image de conteneur.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-261">The `-t` argument provides a tag, or name, for this container image.</span></span> <span data-ttu-id="4f9ad-262">Dans la ligne de commande ci-dessus, la balise utilisée pour le conteneur Docker est `weather-microservice`.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-262">In the command line above, the tag used for the Docker container is `weather-microservice`.</span></span> <span data-ttu-id="4f9ad-263">Lorsque cette commande est terminée, vous disposez d’un conteneur prêt à exécuter votre nouveau service.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-263">When this command completes, you have a container ready to run your new service.</span></span> 

<span data-ttu-id="4f9ad-264">Exécutez la commande suivante pour démarrer le conteneur et lancer votre service :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-264">Run the following command to start the container and launch your service:</span></span>

```console
docker run -d -p 80:80 --name hello-docker weather-microservice
```

<span data-ttu-id="4f9ad-265">L’option `-d` consiste à exécuter le conteneur de façon détachée du terminal actuel.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-265">The `-d` option means to run the container detached from the current terminal.</span></span> <span data-ttu-id="4f9ad-266">Cela signifie que vous ne verrez pas le résultat de la commande dans votre terminal.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-266">That means you won't see the command output in your terminal.</span></span> <span data-ttu-id="4f9ad-267">L’option `-p` indique le mappage de port entre le service et la machine hôte.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-267">The `-p` option indicates the port mapping between the service and the host.</span></span> <span data-ttu-id="4f9ad-268">Ici, elle indique que toute requête entrante sur le port 80 doit être transférée vers le port 80 sur le conteneur.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-268">Here it says that any incoming request on port 80 should be forwarded to port 80 on the container.</span></span> <span data-ttu-id="4f9ad-269">Le fait de spécifier 80 permet d’établir une correspondance avec le port sur lequel votre service écoute, qui est le port par défaut pour les applications de production.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-269">Using 80 matches the port your service is listening on, which is the default port for production applications.</span></span> <span data-ttu-id="4f9ad-270">L’argument `--name` nomme votre conteneur en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-270">The `--name` argument names your running container.</span></span> <span data-ttu-id="4f9ad-271">Il s’agit d’un nom convivial que vous pouvez utiliser pour travailler avec ce conteneur.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-271">It's a convenient name you can use to work with that container.</span></span>

<span data-ttu-id="4f9ad-272">Vous pouvez voir si l’image est en cours d’exécution avec la commande :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-272">You can see if the image is running by checking the command:</span></span>

```console
docker ps
```

<span data-ttu-id="4f9ad-273">Si votre conteneur est en cours d’exécution, vous verrez une ligne qui répertorie les processus en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-273">If your container is running, you'll see a line that lists it in the running processes.</span></span> <span data-ttu-id="4f9ad-274">(Il peut s’agir du seul processus.)</span><span class="sxs-lookup"><span data-stu-id="4f9ad-274">(It may be the only one.)</span></span>

<span data-ttu-id="4f9ad-275">Vous pouvez tester votre service en ouvrant un navigateur et en accédant à localhost et en spécifiant une latitude et une longitude :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-275">You can test your service by opening a browser and navigating to localhost, and specifying a latitude and longitude:</span></span>

```
http://localhost/?lat=35.5&long=40.75
```

## <a name="attaching-to-a-running-container"></a><span data-ttu-id="4f9ad-276">Attachement à un conteneur en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="4f9ad-276">Attaching to a running container</span></span>

<span data-ttu-id="4f9ad-277">Quand vous avez exécuté votre service dans une fenêtre de commande, vous avez pu voir les informations de diagnostic imprimées pour chaque requête.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-277">When you ran your service in a command window, you could see diagnostic information printed for each request.</span></span> <span data-ttu-id="4f9ad-278">Ces informations ne s’affichent pas lorsque votre conteneur s’exécute en mode détaché.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-278">You don't see that information when your container is running in detached mode.</span></span> <span data-ttu-id="4f9ad-279">La commande attach de Docker vous permet de vous attacher à un conteneur en cours d’exécution afin de voir les informations du journal.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-279">The Docker attach command enables you to attach to a running container so that you can see the log information.</span></span>  <span data-ttu-id="4f9ad-280">Exécutez cette commande à partir d’une fenêtre de commande :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-280">Run this command from a command window:</span></span>

```console
docker attach --sig-proxy=false hello-docker
```

<span data-ttu-id="4f9ad-281">L’argument `--sig-proxy=false` signifie que les commandes <kbd>Ctrl</kbd>+<kbd>C</kbd> ne sont pas envoyées au processus de conteneur, mais arrêtent plutôt la commande `docker attach`.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-281">The `--sig-proxy=false` argument means that <kbd>Ctrl</kbd>+<kbd>C</kbd> commands do not get sent to the container process, but rather stop the `docker attach` command.</span></span> <span data-ttu-id="4f9ad-282">Le dernier argument est le nom donné au conteneur dans la commande `docker run`.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-282">The final argument is the name given to the container in the `docker run` command.</span></span> 

> [!NOTE]
> <span data-ttu-id="4f9ad-283">Vous pouvez également utiliser l’ID de conteneur assigné au Docker pour faire référence à un conteneur.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-283">You can also use the Docker assigned container ID to refer to any container.</span></span> <span data-ttu-id="4f9ad-284">Si vous n’avez pas spécifié de nom pour votre conteneur dans `docker run`, vous devez utiliser l’ID de conteneur.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-284">If you didn't specify a name for your container in `docker run` you must use the container ID.</span></span>

<span data-ttu-id="4f9ad-285">Ouvrez un navigateur et accédez à votre service.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-285">Open a browser and navigate to your service.</span></span> <span data-ttu-id="4f9ad-286">Vous verrez les messages de diagnostic dans la fenêtre de commande à partir du conteneur en cours d’exécution attaché.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-286">You'll see the diagnostic messages in the command windows from the attached running container.</span></span>

<span data-ttu-id="4f9ad-287">Appuyez sur <kbd>Ctrl</kbd>+<kbd>C</kbd> pour arrêter le processus d’attachement.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-287">Press <kbd>Ctrl</kbd>+<kbd>C</kbd> to stop the attach process.</span></span>

<span data-ttu-id="4f9ad-288">Lorsque vous avez terminé de manipuler votre conteneur, vous pouvez l’arrêter :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-288">When you are done working with your container, you can stop it:</span></span>

```console
docker stop hello-docker
```

<span data-ttu-id="4f9ad-289">Le conteneur et l’image sont toujours disponibles pour vous permettre de redémarrer.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-289">The container and image is still available for you to restart.</span></span>  <span data-ttu-id="4f9ad-290">Si vous souhaitez supprimer le conteneur de votre machine, utilisez cette commande :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-290">If you want to remove the container from your machine, you use this command:</span></span>

```console
docker rm hello-docker
```

<span data-ttu-id="4f9ad-291">Si vous souhaitez supprimer des images inutilisées dans votre machine, utilisez cette commande :</span><span class="sxs-lookup"><span data-stu-id="4f9ad-291">If you want to remove unused images from your machine, you use this command:</span></span>

```console
docker rmi weather-microservice
```

## <a name="conclusion"></a><span data-ttu-id="4f9ad-292">Conclusion</span><span class="sxs-lookup"><span data-stu-id="4f9ad-292">Conclusion</span></span> 

<span data-ttu-id="4f9ad-293">Dans ce didacticiel, vous avez créé un microservice ASP.NET Core, auquel vous avez ensuite ajouté quelques fonctionnalités simples.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-293">In this tutorial, you built an ASP.NET Core microservice, and added a few simple features.</span></span>

<span data-ttu-id="4f9ad-294">Vous avez créé une image conteneur Docker pour ce service et exécuté ce conteneur sur votre machine.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-294">You built a Docker container image for that service, and ran that container on your machine.</span></span> <span data-ttu-id="4f9ad-295">Vous avez attaché une fenêtre de terminal au service et vu les messages de diagnostic à partir de votre service.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-295">You attached a terminal window to the service, and saw the diagnostic messages from your service.</span></span>

<span data-ttu-id="4f9ad-296">En chemin, vous avez vu plusieurs fonctionnalités du langage C# en action.</span><span class="sxs-lookup"><span data-stu-id="4f9ad-296">Along the way, you saw several features of the C# language in action.</span></span>
