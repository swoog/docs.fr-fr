---
title: Bien démarrer avec .NET Core à l’aide de l’interface CLI
description: Didacticiel pas à pas montrant comment démarrer avec .NET Core sur Windows, Linux ou Mac OS à l’aide de l’interface de ligne de commande (CLI) .NET Core.
author: cartermp
ms.author: mairaw
ms.date: 09/10/2018
ms.technology: dotnet-cli
ms.openlocfilehash: 89839596509e1ffabd28b8903600a431b5a0ed9c
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53143218"
---
# <a name="getting-started-with-net-core-on-windowslinuxmacos-using-the-command-line"></a><span data-ttu-id="bd2c5-103">Bien démarrer avec .NET Core sur Windows/Linux/macOS à l’aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="bd2c5-103">Getting started with .NET Core on Windows/Linux/macOS using the command line</span></span>

<span data-ttu-id="bd2c5-104">Cette rubrique décrit comment commencer à développer des applications multiplateformes sur votre ordinateur à l’aide des outils CLI .NET Core.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-104">This topic will show you how to start developing cross-platforms apps in your machine using the .NET Core CLI tools.</span></span>

<span data-ttu-id="bd2c5-105">Si vous n’êtes pas familiarisé avec l’ensemble d’outils CLI .NET Core, consultez [Vue d’ensemble du SDK .NET Core](../tools/index.md).</span><span class="sxs-lookup"><span data-stu-id="bd2c5-105">If you're unfamiliar with the .NET Core CLI toolset, read the [.NET Core SDK overview](../tools/index.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bd2c5-106">Prérequis</span><span class="sxs-lookup"><span data-stu-id="bd2c5-106">Prerequisites</span></span>

- <span data-ttu-id="bd2c5-107">[.NET Core SDK 2.1](https://www.microsoft.com/net/download/core).</span><span class="sxs-lookup"><span data-stu-id="bd2c5-107">[.NET Core SDK 2.1](https://www.microsoft.com/net/download/core).</span></span>
- <span data-ttu-id="bd2c5-108">Un éditeur de texte ou un éditeur de code de votre choix.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-108">A text editor or code editor of your choice.</span></span>

## <a name="hello-console-app"></a><span data-ttu-id="bd2c5-109">Application console Hello</span><span class="sxs-lookup"><span data-stu-id="bd2c5-109">Hello, Console App!</span></span>

<span data-ttu-id="bd2c5-110">Vous pouvez [afficher ou télécharger l’exemple de code](https://github.com/dotnet/samples/tree/master/core/console-apps/HelloMsBuild) à partir du dépôt GitHub dotnet/samples.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-110">You can [view or download the sample code](https://github.com/dotnet/samples/tree/master/core/console-apps/HelloMsBuild) from the dotnet/samples GitHub repository.</span></span> <span data-ttu-id="bd2c5-111">Pour obtenir des instructions de téléchargement, consultez [Exemples et didacticiels](../../samples-and-tutorials/index.md#viewing-and-downloading-samples).</span><span class="sxs-lookup"><span data-stu-id="bd2c5-111">For download instructions, see [Samples and Tutorials](../../samples-and-tutorials/index.md#viewing-and-downloading-samples).</span></span>

<span data-ttu-id="bd2c5-112">Ouvrez une invite de commandes et créez un dossier nommé *Hello*.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-112">Open a command prompt and create a folder named *Hello*.</span></span> <span data-ttu-id="bd2c5-113">Accédez au dossier créé et tapez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="bd2c5-113">Navigate to the folder you created and type the following:</span></span>

```console
$ dotnet new console
$ dotnet run
```

<span data-ttu-id="bd2c5-114">Suivons une procédure pas à pas rapide :</span><span class="sxs-lookup"><span data-stu-id="bd2c5-114">Let's do a quick walkthrough:</span></span>

1. `$ dotnet new console`

   <span data-ttu-id="bd2c5-115">[`dotnet new`](../tools/dotnet-new.md) crée un fichier projet `Hello.csproj` à jour avec les dépendances nécessaires pour générer une application console.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-115">[`dotnet new`](../tools/dotnet-new.md) creates an up-to-date `Hello.csproj` project file with the dependencies necessary to build a console app.</span></span>  <span data-ttu-id="bd2c5-116">Il crée également `Program.cs`, un fichier de base contenant le point d’entrée pour l’application.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-116">It also creates a `Program.cs`, a basic file containing the entry point for the application.</span></span>

   <span data-ttu-id="bd2c5-117">`Hello.csproj`:</span><span class="sxs-lookup"><span data-stu-id="bd2c5-117">`Hello.csproj`:</span></span>

   [!code[Hello.csproj](../../../samples/core/console-apps/HelloMsBuild/Hello.csproj)]

   <span data-ttu-id="bd2c5-118">Le fichier projet spécifie tout ce qui est nécessaire pour restaurer les dépendances et générer le programme.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-118">The project file specifies everything that's needed to restore dependencies and build the program.</span></span>

   * <span data-ttu-id="bd2c5-119">La balise `OutputType` spécifie que nous générons un fichier exécutable, autrement dit une application console.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-119">The `OutputType` tag specifies that we're building an executable, in other words a console application.</span></span>
   * <span data-ttu-id="bd2c5-120">La balise `TargetFramework` spécifie l’implémentation .NET que nous ciblons.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-120">The `TargetFramework` tag specifies what .NET implementation we're targeting.</span></span> <span data-ttu-id="bd2c5-121">Dans un scénario avancé, vous pouvez spécifier plusieurs frameworks cibles et y effectuer une génération globale en une seule opération.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-121">In an advanced scenario, you can specify multiple target frameworks and build to all those in a single operation.</span></span> <span data-ttu-id="bd2c5-122">Dans ce tutoriel, nous nous en tiendrons à une génération limitée à .NET Core 2.1.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-122">In this tutorial, we'll stick to building only for .NET Core 2.1.</span></span>

   <span data-ttu-id="bd2c5-123">`Program.cs`:</span><span class="sxs-lookup"><span data-stu-id="bd2c5-123">`Program.cs`:</span></span>

   [!code-csharp[Program.cs](../../../samples/core/console-apps/HelloMsBuild/Program.cs)]

   <span data-ttu-id="bd2c5-124">Le programme commence par `using System`, ce qui signifie « placer tout ce qui se trouve dans l’espace de noms `System` dans la portée de ce fichier ».</span><span class="sxs-lookup"><span data-stu-id="bd2c5-124">The program starts by `using System`, which means "bring everything in the `System` namespace into scope for this file".</span></span> <span data-ttu-id="bd2c5-125">L’espace de noms `System` inclut des constructions de base, telles que `string`, ou des types numériques.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-125">The `System` namespace includes basic constructs such as `string`, or numeric types.</span></span>

   <span data-ttu-id="bd2c5-126">Ensuite, nous définissons un espace de noms appelé `Hello`.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-126">We then define a namespace called `Hello`.</span></span> <span data-ttu-id="bd2c5-127">Vous pouvez le modifier à votre gré.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-127">You can change this to anything you want.</span></span> <span data-ttu-id="bd2c5-128">Une classe nommée `Program` est définie dans cet espace de noms avec une méthode `Main` qui accepte un tableau de chaînes comme argument.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-128">A class named `Program` is defined within that namespace, with a `Main` method that takes an array of strings as its argument.</span></span> <span data-ttu-id="bd2c5-129">Ce tableau contient la liste des arguments passés quand le programme compilé est appelé.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-129">This array contains the list of arguments passed in when the compiled program is called.</span></span> <span data-ttu-id="bd2c5-130">Tel quel, ce tableau n’est pas utilisé : le programme se limite à écrire « Hello World! »</span><span class="sxs-lookup"><span data-stu-id="bd2c5-130">As it is, this array is not used: all the program is doing is to write "Hello World!"</span></span> <span data-ttu-id="bd2c5-131">dans la console.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-131">to the console.</span></span> <span data-ttu-id="bd2c5-132">Plus tard, nous apporterons des modifications au code qui utilisent cet argument.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-132">Later, we'll make changes to the code that will make use of this argument.</span></span>

   [!INCLUDE[DotNet Restore Note](~/includes/dotnet-restore-note.md)]

   <span data-ttu-id="bd2c5-133">`dotnet new` appelle [`dotnet restore`](../tools/dotnet-restore.md) implicitement.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-133">`dotnet new` calls [`dotnet restore`](../tools/dotnet-restore.md) implicitly.</span></span> <span data-ttu-id="bd2c5-134">`dotnet restore` appelle [NuGet](https://www.nuget.org/) (gestionnaire de package .NET) pour restaurer l’arborescence de dépendances.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-134">`dotnet restore` calls into [NuGet](https://www.nuget.org/) (.NET package manager) to restore the tree of dependencies.</span></span> <span data-ttu-id="bd2c5-135">NuGet analyse le fichier *Hello.csproj*, télécharge les dépendances définies dans le fichier (ou les récupère dans un cache sur votre ordinateur) et écrit le fichier *obj/project.assets.json*, nécessaire pour compiler et exécuter l’exemple.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-135">NuGet analyzes the *Hello.csproj* file, downloads the dependencies defined in the file (or grabs them from a cache on your machine), and writes the *obj/project.assets.json* file, which is necessary to compile and run the sample.</span></span> 
   
   > [!IMPORTANT]
   > <span data-ttu-id="bd2c5-136">Si vous utilisez une version .NET Core 1.x du SDK, vous devrez appeler `dotnet restore` vous-même après l’appel de `dotnet new`.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-136">If you're using a .NET Core 1.x version of the SDK, you'll have to call `dotnet restore` yourself after calling `dotnet new`.</span></span>

2. `$ dotnet run`

   <span data-ttu-id="bd2c5-137">[`dotnet run`](../tools/dotnet-run.md) appelle [`dotnet build`](../tools/dotnet-build.md) pour garantir que les cibles de génération ont été générées, puis appelle `dotnet <assembly.dll>` pour exécuter l’application cible.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-137">[`dotnet run`](../tools/dotnet-run.md) calls [`dotnet build`](../tools/dotnet-build.md) to ensure that the build targets have been built, and then calls `dotnet <assembly.dll>` to run the target application.</span></span>

    ```console
    $ dotnet run
    Hello World!
    ```

    <span data-ttu-id="bd2c5-138">Si vous préférez, vous pouvez exécuter [`dotnet build`](../tools/dotnet-build.md) pour compiler le code sans exécuter les applications console de la build.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-138">Alternatively, you can also execute [`dotnet build`](../tools/dotnet-build.md) to compile the code without running the build console applications.</span></span> <span data-ttu-id="bd2c5-139">Il en résulte une application compilée sous forme de fichier DLL qui peut être exécutée avec `dotnet bin\Debug\netcoreapp2.1\Hello.dll` sur Windows (utilisez `/` sur les autres systèmes).</span><span class="sxs-lookup"><span data-stu-id="bd2c5-139">This results in a compiled application as a DLL file that can be run with `dotnet bin\Debug\netcoreapp2.1\Hello.dll` on Windows (use `/` for non-Windows systems).</span></span> <span data-ttu-id="bd2c5-140">Vous pouvez également spécifier des arguments pour l’application, comme nous le verrons par la suite dans la rubrique.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-140">You may also specify arguments to the application as you'll see later on the topic.</span></span>
    ```console
    $ dotnet bin\Debug\netcoreapp2.1\Hello.dll
    Hello World!
    ```

    <span data-ttu-id="bd2c5-141">Dans le cadre d’un scénario avancé, vous pouvez générer l’application comme un ensemble autonome de fichiers spécifiques à la plateforme qui peuvent être déployés et exécutés sur un ordinateur sur lequel .NET Core n’est pas nécessairement installé.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-141">As an advanced scenario, it's possible to build the application as a self-contained set of platform-specific files that can be deployed and run to a machine that doesn't necessarily have .NET Core installed.</span></span> <span data-ttu-id="bd2c5-142">Pour plus d’informations, consultez [Déploiement d’applications .NET Core](../deploying/index.md).</span><span class="sxs-lookup"><span data-stu-id="bd2c5-142">See [.NET Core Application Deployment](../deploying/index.md) for details.</span></span>

### <a name="augmenting-the-program"></a><span data-ttu-id="bd2c5-143">Augmentation du programme</span><span class="sxs-lookup"><span data-stu-id="bd2c5-143">Augmenting the program</span></span>

<span data-ttu-id="bd2c5-144">Modifions un peu le programme.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-144">Let's change the program a bit.</span></span> <span data-ttu-id="bd2c5-145">Les nombres de Fibonacci sont amusants, nous allons donc les ajouter en plus de l’argument pour accueillir la personne qui exécute l’application.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-145">Fibonacci numbers are fun, so let's add that in addition to use the argument to greet the person running the app.</span></span>

1. <span data-ttu-id="bd2c5-146">Remplacez le contenu du fichier *Program.cs* par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="bd2c5-146">Replace the contents of your *Program.cs*  file with the following code:</span></span>

   [!code-csharp[Fibonacci](../../../samples/core/console-apps/fibonacci-msbuild/Program.cs)]

2. <span data-ttu-id="bd2c5-147">Exécutez [`dotnet build`](../tools/dotnet-build.md) pour compiler les modifications.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-147">Execute [`dotnet build`](../tools/dotnet-build.md) to compile the changes.</span></span>

3. <span data-ttu-id="bd2c5-148">Exécutez le programme en passant un paramètre à l’application :</span><span class="sxs-lookup"><span data-stu-id="bd2c5-148">Run the program passing a parameter to the app:</span></span>

   ```console
   $ dotnet run -- John
   Hello John!
   Fibonacci Numbers 1-15:
   1: 0
   2: 1
   3: 1
   4: 2
   5: 3
   6: 5
   7: 8
   8: 13
   9: 21
   10: 34
   11: 55
   12: 89
   13: 144
   14: 233
   15: 377
   ```

<span data-ttu-id="bd2c5-149">Et voilà !</span><span class="sxs-lookup"><span data-stu-id="bd2c5-149">And that's it!</span></span>  <span data-ttu-id="bd2c5-150">Vous pouvez augmenter `Program.cs` comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-150">You can augment `Program.cs` any way you like.</span></span>

## <a name="working-with-multiple-files"></a><span data-ttu-id="bd2c5-151">Utilisation de plusieurs fichiers</span><span class="sxs-lookup"><span data-stu-id="bd2c5-151">Working with multiple files</span></span>

<span data-ttu-id="bd2c5-152">Les fichiers uniques conviennent à des programmes simples et ponctuels, mais si vous créez une application plus complexe, vous avez probablement plusieurs fichiers sources dans votre projet. Reprenons l’exemple précédent de Fibonacci en mettant en cache certaines valeurs de Fibonacci et en ajoutant des fonctionnalités récursives.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-152">Single files are fine for simple one-off programs, but if you're building a more complex app, you're probably going to have multiple source files on your project Let's build off of the previous Fibonacci example by caching some Fibonacci values and add some recursive features.</span></span>

1. <span data-ttu-id="bd2c5-153">Ajoutez un nouveau fichier nommé *FibonacciGenerator.cs* dans le répertoire *Hello* avec le code suivant :</span><span class="sxs-lookup"><span data-stu-id="bd2c5-153">Add a new file inside the *Hello* directory named *FibonacciGenerator.cs* with the following code:</span></span>

   [!code-csharp[Fibonacci Generator](../../../samples/core/console-apps/FibonacciBetterMsBuild/FibonacciGenerator.cs)]

2. <span data-ttu-id="bd2c5-154">Modifiez la méthode `Main` dans votre fichier *Program.cs* pour instancier la nouvelle classe et appelez sa méthode comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="bd2c5-154">Change the `Main` method in your *Program.cs* file to instantiate the new class and call its method as in the following example:</span></span>

   [!code-csharp[New Program.cs](../../../samples/core/console-apps/FibonacciBetterMsBuild/Program.cs)]

3. <span data-ttu-id="bd2c5-155">Exécutez [`dotnet build`](../tools/dotnet-build.md) pour compiler les modifications.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-155">Execute [`dotnet build`](../tools/dotnet-build.md) to compile the changes.</span></span>

4. <span data-ttu-id="bd2c5-156">Exécutez votre application en exécutant [`dotnet run`](../tools/dotnet-run.md).</span><span class="sxs-lookup"><span data-stu-id="bd2c5-156">Run your app by executing [`dotnet run`](../tools/dotnet-run.md).</span></span> <span data-ttu-id="bd2c5-157">Voici la sortie du programme :</span><span class="sxs-lookup"><span data-stu-id="bd2c5-157">The following shows the program output:</span></span>

   ```console
   $ dotnet run
   0
   1
   1
   2
   3
   5
   8
   13
   21
   34
   55
   89
   144
   233
   377
   ```

<span data-ttu-id="bd2c5-158">Et voilà !</span><span class="sxs-lookup"><span data-stu-id="bd2c5-158">And that's it!</span></span> <span data-ttu-id="bd2c5-159">À présent, vous pouvez commencer à utiliser les concepts de base que vous avez appris ici pour créer vos propres programmes.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-159">Now, you can start using the basic concepts learned here to create your own programs.</span></span>

<span data-ttu-id="bd2c5-160">Notez que les commandes et les étapes indiquées dans ce didacticiel pour exécuter votre application sont utilisées uniquement au moment du développement.</span><span class="sxs-lookup"><span data-stu-id="bd2c5-160">Note that the commands and steps shown in this tutorial to run your application are used during development time only.</span></span> <span data-ttu-id="bd2c5-161">Une fois que vous êtes prêt à déployer votre application, consultez les différentes [stratégies de déploiement](../deploying/index.md) pour les applications .NET Core et la commande [`dotnet publish`](../tools/dotnet-publish.md).</span><span class="sxs-lookup"><span data-stu-id="bd2c5-161">Once you're ready to deploy your app, you'll want to take a look at the different [deployment strategies](../deploying/index.md) for .NET Core apps and the [`dotnet publish`](../tools/dotnet-publish.md) command.</span></span>

## <a name="see-also"></a><span data-ttu-id="bd2c5-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd2c5-162">See also</span></span>

* [<span data-ttu-id="bd2c5-163">Organisation et test de projets avec les outils CLI .NET Core</span><span class="sxs-lookup"><span data-stu-id="bd2c5-163">Organizing and testing projects with the .NET Core CLI tools</span></span>](testing-with-cli.md)
