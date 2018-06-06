---
title: 'Prise en main) (F # dans Visual Studio Code'
description: 'Découvrez comment utiliser F # avec Code Visual Studio et la suite de plug-in Ionide.'
ms.date: 05/28/2018
ms.openlocfilehash: e56274caf36be231338876ded5a6d7c7968906b0
ms.sourcegitcommit: bbf70abe6b46073148f78cbf0619de6092b5800c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2018
ms.locfileid: "34728626"
---
# <a name="get-started-with-f-in-visual-studio-code"></a><span data-ttu-id="86663-103">Prise en main) (F # dans Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="86663-103">Get Started with F# in Visual Studio Code</span></span>

<span data-ttu-id="86663-104">Vous pouvez écrire F # dans [Visual Studio Code](https://code.visualstudio.com) avec la [plug-in Ionide](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fsharp), afin d’obtenir une expérience d’un environnement de développement intégré (IDE) inter-plateformes et léger optimale avec IntelliSense et le code de base refactorisations.</span><span class="sxs-lookup"><span data-stu-id="86663-104">You can write F# in [Visual Studio Code](https://code.visualstudio.com) with the [Ionide plugin](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fsharp), to get a great cross-platform, lightweight Integrated Development Environment (IDE) experience with IntelliSense and basic code refactorings.</span></span> <span data-ttu-id="86663-105">Visitez [Ionide.io](http://ionide.io) pour en savoir plus sur la suite de plug-in.</span><span class="sxs-lookup"><span data-stu-id="86663-105">Visit [Ionide.io](http://ionide.io) to learn more about the plugin suite.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="86663-106">Prérequis</span><span class="sxs-lookup"><span data-stu-id="86663-106">Prerequisites</span></span>

<span data-ttu-id="86663-107">Vous devez disposer [git installé](https://git-scm.com/download) et disponible sur votre chemin d’accès permettent d’utiliser des modèles de projet Ionide.</span><span class="sxs-lookup"><span data-stu-id="86663-107">You must have [git installed](https://git-scm.com/download) and available on your PATH to make use of project templates in Ionide.</span></span> <span data-ttu-id="86663-108">Vous pouvez vérifier qu’il est correctement installé en tapant `git --version` à l’invite de commandes et en appuyant sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="86663-108">You can verify that it is installed correctly by typing `git --version` at a command prompt and pressing **Enter**.</span></span>

### <a name="macostabmacos"></a>[<span data-ttu-id="86663-109">macOS</span><span class="sxs-lookup"><span data-stu-id="86663-109">macOS</span></span>](#tab/macos)

<span data-ttu-id="86663-110">Ionide utilise [Mono](http://www.mono-project.com).</span><span class="sxs-lookup"><span data-stu-id="86663-110">Ionide uses [Mono](http://www.mono-project.com).</span></span> <span data-ttu-id="86663-111">Le moyen le plus simple pour installer Mono sur macOS est via Homebrew.</span><span class="sxs-lookup"><span data-stu-id="86663-111">The easiest way to install Mono on macOS is via Homebrew.</span></span> <span data-ttu-id="86663-112">Tapez simplement la commande suivante dans votre terminal :</span><span class="sxs-lookup"><span data-stu-id="86663-112">Simply type the following into your terminal:</span></span>

```
brew install mono
```

<span data-ttu-id="86663-113">Vous devez également installer le [le Kit de développement .NET Core](https://www.microsoft.com/net/download).</span><span class="sxs-lookup"><span data-stu-id="86663-113">You must also install the [.NET Core SDK](https://www.microsoft.com/net/download).</span></span>

### <a name="linuxtablinux"></a>[<span data-ttu-id="86663-114">Linux</span><span class="sxs-lookup"><span data-stu-id="86663-114">Linux</span></span>](#tab/linux)

<span data-ttu-id="86663-115">Sur Linux, Ionide utilise également [Mono](https://www.mono-project.com).</span><span class="sxs-lookup"><span data-stu-id="86663-115">On Linux, Ionide also uses [Mono](https://www.mono-project.com).</span></span> <span data-ttu-id="86663-116">Si vous êtes sur Debian ou Ubuntu, vous pouvez utiliser les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="86663-116">If you're on Debian or Ubuntu, you can use the following:</span></span>

```
sudo apt-get update
sudo apt-get install mono-complete fsharp
```

<span data-ttu-id="86663-117">Vous devez également installer le [le Kit de développement .NET Core](https://www.microsoft.com/net/download).</span><span class="sxs-lookup"><span data-stu-id="86663-117">You must also install the [.NET Core SDK](https://www.microsoft.com/net/download).</span></span>

### <a name="windowstabwindows"></a>[<span data-ttu-id="86663-118">Fenêtres</span><span class="sxs-lookup"><span data-stu-id="86663-118">Windows</span></span>](#tab/windows)

<span data-ttu-id="86663-119">Si vous êtes sous Windows, vous devez [installer Visual Studio avec prise en charge F #](get-started-visual-studio.md#installing-f).</span><span class="sxs-lookup"><span data-stu-id="86663-119">If you're on Windows, you must [install Visual Studio with F# support](get-started-visual-studio.md#installing-f).</span></span> <span data-ttu-id="86663-120">Cette commande installe tous les composants nécessaires pour écrire, compiler et exécuter du code F #.</span><span class="sxs-lookup"><span data-stu-id="86663-120">This installs all the necessary components to write, compile, and execute F# code.</span></span>

<span data-ttu-id="86663-121">Vous devez également installer le [le Kit de développement .NET Core](https://www.microsoft.com/net/download/).</span><span class="sxs-lookup"><span data-stu-id="86663-121">You must also install the [.NET Core SDK](https://www.microsoft.com/net/download/).</span></span>

---

## <a name="installing-visual-studio-code-and-the-ionide-plugin"></a><span data-ttu-id="86663-122">L’installation de Visual Studio Code et le plug-in Ionide</span><span class="sxs-lookup"><span data-stu-id="86663-122">Installing Visual Studio Code and the Ionide plugin</span></span>

<span data-ttu-id="86663-123">Vous pouvez installer Visual Studio Code, à partir de la [code.visualstudio.com](https://code.visualstudio.com) site Web.</span><span class="sxs-lookup"><span data-stu-id="86663-123">You can install Visual Studio Code from the [code.visualstudio.com](https://code.visualstudio.com) website.</span></span>

<span data-ttu-id="86663-124">Ensuite, cliquez sur l’icône des Extensions et recherchez « Ionide » :</span><span class="sxs-lookup"><span data-stu-id="86663-124">Next, click the Extensions icon and search for "Ionide":</span></span>

<span data-ttu-id="86663-125">Le plug-in uniquement requis pour la prise en charge F # dans Visual Studio Code est [Ionide-fsharp](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fsharp).</span><span class="sxs-lookup"><span data-stu-id="86663-125">The only plugin required for F# support in Visual Studio Code is [Ionide-fsharp](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fsharp).</span></span> <span data-ttu-id="86663-126">Toutefois, vous pouvez également installer [Ionide-FAKE](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-FAKE) pour obtenir [faux](https://fsharp.github.io/FAKE/) prennent en charge et [Ionide-Paket](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-Paket) pour obtenir [Paket](https://fsprojects.github.io/Paket/) prennent en charge.</span><span class="sxs-lookup"><span data-stu-id="86663-126">However, you can also install [Ionide-FAKE](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-FAKE) to get [FAKE](https://fsharp.github.io/FAKE/) support and [Ionide-Paket](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-Paket) to get [Paket](https://fsprojects.github.io/Paket/) support.</span></span> <span data-ttu-id="86663-127">FAUX et Paket sont F # Communauté des outils supplémentaires pour la création de projets et de gestion des dépendances, respectivement.</span><span class="sxs-lookup"><span data-stu-id="86663-127">FAKE and Paket are additional F# community tools for building projects and managing dependencies, respectively.</span></span>

## <a name="creating-your-first-project-with-ionide"></a><span data-ttu-id="86663-128">Créer votre premier projet avec Ionide</span><span class="sxs-lookup"><span data-stu-id="86663-128">Creating your first project with Ionide</span></span>

<span data-ttu-id="86663-129">Pour créer un projet F #, ouvrez Visual Studio Code dans un nouveau dossier (vous pouvez appeler comme vous le souhaitez).</span><span class="sxs-lookup"><span data-stu-id="86663-129">To create a new F# project, open Visual Studio Code in a new folder (you can name it whatever you like).</span></span>

<span data-ttu-id="86663-130">Ensuite, ouvrez la palette de commandes (**vue > commande palette**) et tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="86663-130">Next, open the command pallette (**View > Command Pallette**) and type the following:</span></span>

```
> F# new project
```

<span data-ttu-id="86663-131">Il est alimenté par le [FORGE](https://github.com/fsharp-editing/Forge) projet.</span><span class="sxs-lookup"><span data-stu-id="86663-131">This is powered by the [FORGE](https://github.com/fsharp-editing/Forge) project.</span></span>

> [!NOTE]
<span data-ttu-id="86663-132">Si vous ne voyez pas les options de modèle, essayez d’actualiser les modèles en exécutant la commande suivante dans la Palette de commandes : `>F#: Refresh Project Templates`.</span><span class="sxs-lookup"><span data-stu-id="86663-132">If you don't see template options, try refreshing templates by running the following command in the Command Palette: `>F#: Refresh Project Templates`.</span></span>

<span data-ttu-id="86663-133">Sélectionnez « F #: nouveau projet » en appuyant sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="86663-133">Select "F#: New Project" by hitting **Enter**.</span></span> <span data-ttu-id="86663-134">Vous accédez à l’étape suivante, ce qui concerne la sélection d’un modèle de projet.</span><span class="sxs-lookup"><span data-stu-id="86663-134">This takes you to the next step, which is for selecting a project template.</span></span>

<span data-ttu-id="86663-135">Choisir le `classlib` modèle et appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="86663-135">Pick the `classlib` template and hit **Enter**.</span></span>

<span data-ttu-id="86663-136">Ensuite, sélectionnez un répertoire pour créer le projet dans.</span><span class="sxs-lookup"><span data-stu-id="86663-136">Next, pick a directory to create the project in.</span></span> <span data-ttu-id="86663-137">Si vous laissez ce champ vide, il utilise le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="86663-137">If you leave it blank, it uses the current directory.</span></span>

<span data-ttu-id="86663-138">Enfin, nommez votre projet dans l’étape finale.</span><span class="sxs-lookup"><span data-stu-id="86663-138">Finally, name your project in the final step.</span></span> <span data-ttu-id="86663-139">F # utilise [casse Pascal](http://c2.com/cgi/wiki?PascalCase) pour les noms de projet.</span><span class="sxs-lookup"><span data-stu-id="86663-139">F# uses [Pascal case](http://c2.com/cgi/wiki?PascalCase) for project names.</span></span> <span data-ttu-id="86663-140">Cet article utilise `ClassLibraryDemo` comme nom.</span><span class="sxs-lookup"><span data-stu-id="86663-140">This article uses `ClassLibraryDemo` as the name.</span></span> <span data-ttu-id="86663-141">Une fois que vous avez entré le nom souhaité pour votre projet, appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="86663-141">Once you've entered the name you want for your project, hit **Enter**.</span></span>

<span data-ttu-id="86663-142">Si vous avez suivi l’étape précédente, vous devez obtenir Visual Studio Code espace de travail sur le côté gauche apparaissent avec les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="86663-142">If you followed the previous step, you should get the Visual Studio Code Workspace on the left-hand side to appear with the following:</span></span>

1. <span data-ttu-id="86663-143">F # de projet, sous la `ClassLibraryDemo` dossier.</span><span class="sxs-lookup"><span data-stu-id="86663-143">The F# project itself, underneath the `ClassLibraryDemo` folder.</span></span>
2. <span data-ttu-id="86663-144">La structure de répertoire correct pour l’ajout de packages via [ `Paket` ](https://fsprojects.github.io/Paket/).</span><span class="sxs-lookup"><span data-stu-id="86663-144">The correct directory structure for adding packages via [`Paket`](https://fsprojects.github.io/Paket/).</span></span>
3. <span data-ttu-id="86663-145">Un inter-plateformes générer le script avec [ `FAKE` ](https://fsharp.github.io/FAKE/).</span><span class="sxs-lookup"><span data-stu-id="86663-145">A cross-platform build script with [`FAKE`](https://fsharp.github.io/FAKE/).</span></span>
4. <span data-ttu-id="86663-146">Le `paket.exe` exécutable qui peut récupérer des packages et résoudre les dépendances pour vous.</span><span class="sxs-lookup"><span data-stu-id="86663-146">The `paket.exe` executable that can fetch packages and resolve dependencies for you.</span></span>
5. <span data-ttu-id="86663-147">A `.gitignore` fichier si vous souhaitez ajouter ce projet au contrôle de code source basée sur Git.</span><span class="sxs-lookup"><span data-stu-id="86663-147">A `.gitignore` file if you wish to add this project to Git-based source control.</span></span>

## <a name="writing-some-code"></a><span data-ttu-id="86663-148">Écrire du code</span><span class="sxs-lookup"><span data-stu-id="86663-148">Writing some code</span></span>

<span data-ttu-id="86663-149">Ouvrez le *ClassLibraryDemo* dossier.</span><span class="sxs-lookup"><span data-stu-id="86663-149">Open the *ClassLibraryDemo* folder.</span></span>  <span data-ttu-id="86663-150">Vous devez voir les fichiers suivants :</span><span class="sxs-lookup"><span data-stu-id="86663-150">You should see the following files:</span></span>

1. <span data-ttu-id="86663-151">`ClassLibraryDemo.fs`, un fichier d’implémentation F # avec une classe définie.</span><span class="sxs-lookup"><span data-stu-id="86663-151">`ClassLibraryDemo.fs`, an F# implementation file with a class defined.</span></span>
2. <span data-ttu-id="86663-152">`ClassLibraryDemo.fsproj`, un fichier de projet F # est utilisé pour générer ce projet.</span><span class="sxs-lookup"><span data-stu-id="86663-152">`ClassLibraryDemo.fsproj`, an F# project file used to build this project.</span></span>
3. <span data-ttu-id="86663-153">`Script.fsx`, un fichier de script F # qui charge le fichier source.</span><span class="sxs-lookup"><span data-stu-id="86663-153">`Script.fsx`, an F# script file that loads the source file.</span></span>
4. <span data-ttu-id="86663-154">`paket.references`, un fichier Paket qui spécifie les dépendances du projet.</span><span class="sxs-lookup"><span data-stu-id="86663-154">`paket.references`, a Paket file that specifies the project dependencies.</span></span>

<span data-ttu-id="86663-155">Ouvrez `Script.fsx`et ajoutez le code suivant à la fin de celle-ci :</span><span class="sxs-lookup"><span data-stu-id="86663-155">Open `Script.fsx`, and add the following code at the end of it:</span></span>

[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/to-pig-latin.fsx)]

<span data-ttu-id="86663-156">Cette fonction convertit un mot à un formulaire de [Pig Latin](https://en.wikipedia.org/wiki/Pig_Latin).</span><span class="sxs-lookup"><span data-stu-id="86663-156">This function converts a word to a form of [Pig Latin](https://en.wikipedia.org/wiki/Pig_Latin).</span></span> <span data-ttu-id="86663-157">L’étape suivante consiste à évaluer à l’aide de F # Interactive (FSI).</span><span class="sxs-lookup"><span data-stu-id="86663-157">The next step is to evaluate it using F# Interactive (FSI).</span></span>

<span data-ttu-id="86663-158">Mettez en surbrillance de la fonction entière (il doit être 11 lignes).</span><span class="sxs-lookup"><span data-stu-id="86663-158">Highlight the entire function (it should be 11 lines long).</span></span> <span data-ttu-id="86663-159">Une fois qu’il est mis en surbrillance, maintenez la **Alt** clé, puis appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="86663-159">Once it is highlighted, hold the **Alt** key and hit **Enter**.</span></span> <span data-ttu-id="86663-160">Vous remarquerez une fenêtre contextuelle ci-dessous, et il doit afficher quelque chose comme ceci :</span><span class="sxs-lookup"><span data-stu-id="86663-160">You'll notice a window pop up below, and it should show something like this:</span></span>

![Exemple de sortie de F # Interactive avec Ionide](media/getting-started-vscode/vscode-fsi.png)

<span data-ttu-id="86663-162">Cela a trois opérations :</span><span class="sxs-lookup"><span data-stu-id="86663-162">This did three things:</span></span>

1. <span data-ttu-id="86663-163">Il a démarré le processus FSI.</span><span class="sxs-lookup"><span data-stu-id="86663-163">It started the FSI process.</span></span>
2. <span data-ttu-id="86663-164">Il envoyé le code que vous avez sélectionnée sur le processus FSI.</span><span class="sxs-lookup"><span data-stu-id="86663-164">It sent the code you highlighted over the FSI process.</span></span>
3. <span data-ttu-id="86663-165">Le processus FSI évaluer le code que vous avez envoyé via.</span><span class="sxs-lookup"><span data-stu-id="86663-165">The FSI process evaluated the code you sent over.</span></span>

<span data-ttu-id="86663-166">Étant donné que ce que vous avez envoyé via a été un [fonction](../language-reference/functions/index.md), vous pouvez maintenant appeler cette fonction avec FSI !</span><span class="sxs-lookup"><span data-stu-id="86663-166">Because what you sent over was a [function](../language-reference/functions/index.md), you can now call that function with FSI!</span></span> <span data-ttu-id="86663-167">Dans la fenêtre interactive, tapez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="86663-167">In the interactive window, type the following:</span></span>

```fsharp
toPigLatin "banana";;
```

<span data-ttu-id="86663-168">Vous devez voir le résultat suivant :</span><span class="sxs-lookup"><span data-stu-id="86663-168">You should see the following result:</span></span>

```fsharp
val it : string = "ananabay"
```

<span data-ttu-id="86663-169">Maintenant, essayons avec une voyelle en tant que la première lettre.</span><span class="sxs-lookup"><span data-stu-id="86663-169">Now, let's try with a vowel as the first letter.</span></span> <span data-ttu-id="86663-170">Entrez les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="86663-170">Enter the following:</span></span>

```fsharp
toPigLatin "apple";;
```

<span data-ttu-id="86663-171">Vous devez voir le résultat suivant :</span><span class="sxs-lookup"><span data-stu-id="86663-171">You should see the following result:</span></span>

```fsharp
val it : string = "appleyay"
```

<span data-ttu-id="86663-172">La fonction semble fonctionner comme prévu.</span><span class="sxs-lookup"><span data-stu-id="86663-172">The function appears to be working as expected.</span></span> <span data-ttu-id="86663-173">Félicitations, vous venez d’écriture de votre première fonction) (F # dans Visual Studio Code et il évaluée avec FSI.</span><span class="sxs-lookup"><span data-stu-id="86663-173">Congratulations, you just wrote your first F# function in Visual Studio Code and evaluated it with FSI!</span></span>

>[!NOTE]
<span data-ttu-id="86663-174">Comme vous l’avez peut-être remarqué, les lignes de FSI sont terminent par `;;`.</span><span class="sxs-lookup"><span data-stu-id="86663-174">As you may have noticed, the lines in FSI are terminated with `;;`.</span></span> <span data-ttu-id="86663-175">Il s’agit, car FSI vous permet d’entrer plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="86663-175">This is because FSI allows you to enter multiple lines.</span></span> <span data-ttu-id="86663-176">Le `;;` à la fin informe FSI lorsque le code est terminé.</span><span class="sxs-lookup"><span data-stu-id="86663-176">The `;;` at the end lets FSI know when the code is finished.</span></span>

## <a name="explaining-the-code"></a><span data-ttu-id="86663-177">Explique le code</span><span class="sxs-lookup"><span data-stu-id="86663-177">Explaining the code</span></span>

<span data-ttu-id="86663-178">Si vous n’êtes pas sûr de ce que le code est en fait, Voici un pas à pas.</span><span class="sxs-lookup"><span data-stu-id="86663-178">If you're not sure about what the code is actually doing, here's a step-by-step.</span></span>

<span data-ttu-id="86663-179">Comme vous pouvez le voir, `toPigLatin` est une fonction qui prend un mot en entrée et la convertit en une représentation sous forme de Pig-Latin de ce mot.</span><span class="sxs-lookup"><span data-stu-id="86663-179">As you can see, `toPigLatin` is a function that takes a word as its input and converts it to a Pig-Latin representation of that word.</span></span> <span data-ttu-id="86663-180">Les règles pour ce sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="86663-180">The rules for this are as follows:</span></span>

<span data-ttu-id="86663-181">Si le premier caractère dans un mot commence par une voyelle, ajoutez « hourra » à la fin du mot.</span><span class="sxs-lookup"><span data-stu-id="86663-181">If the first character in a word starts with a vowel, add "yay" to the end of the word.</span></span> <span data-ttu-id="86663-182">Si elle ne commence pas par une voyelle, déplacez le premier caractère à la fin du mot et ajoutez-y « ay ».</span><span class="sxs-lookup"><span data-stu-id="86663-182">If it doesn't start with a vowel, move that first character to the end of the word and add "ay" to it.</span></span>

<span data-ttu-id="86663-183">Vous avez peut-être remarqué les éléments suivants dans FSI :</span><span class="sxs-lookup"><span data-stu-id="86663-183">You may have noticed the following in FSI:</span></span>

```fsharp
val toPigLatin : word:string -> string
```

<span data-ttu-id="86663-184">Cela indique que `toPigLatin` est une fonction qui accepte un `string` en tant qu’entrée (appelé `word`), ainsi qu’un autre `string`.</span><span class="sxs-lookup"><span data-stu-id="86663-184">This states that `toPigLatin` is a function that takes in a `string` as input (called `word`), and returns another `string`.</span></span> <span data-ttu-id="86663-185">Il s’agit du [signature de type de la fonction](https://fsharpforfunandprofit.com/posts/function-signatures/), un élément fondamental de F #, qui est la clé pour comprendre le code F #.</span><span class="sxs-lookup"><span data-stu-id="86663-185">This is known as the [type signature of the function](https://fsharpforfunandprofit.com/posts/function-signatures/), a fundamental piece of F# that's key to understanding F# code.</span></span> <span data-ttu-id="86663-186">Vous pouvez également constater si vous pointez sur la fonction dans le Code de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="86663-186">You'll also notice this if you hover over the function in Visual Studio Code.</span></span>

<span data-ttu-id="86663-187">Dans le corps de la fonction, vous pouvez remarquer que les deux parties distinctes :</span><span class="sxs-lookup"><span data-stu-id="86663-187">In the body of the function, you'll notice two distinct parts:</span></span>

1. <span data-ttu-id="86663-188">Une fonction interne, appelée `isVowel`, qui détermine si un caractère donné (`c`) est une voyelle en vérifiant si elle correspond à un des modèles fournis via [recherche de correspondance](../language-reference/pattern-matching.md):</span><span class="sxs-lookup"><span data-stu-id="86663-188">An inner function, called `isVowel`, that determines if a given character (`c`) is a vowel by checking if it matches one of the provided patterns via [Pattern Matching](../language-reference/pattern-matching.md):</span></span>

   [!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/to-pig-latin.fsx#L2-L6)]

2. <span data-ttu-id="86663-189">Un [ `if..then..else` ](../language-reference/conditional-expressions-if-then-else.md) expression qui vérifie si le premier caractère est une voyelle et les constructions de la valeur renvoyée en dehors des caractères d’entrée selon que le premier caractère a une voyelle ou non :</span><span class="sxs-lookup"><span data-stu-id="86663-189">An [`if..then..else`](../language-reference/conditional-expressions-if-then-else.md) expression that checks if the first character is a vowel, and constructs a return value out of the input characters based on if the first character was a vowel or not:</span></span>

   [!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/to-pig-latin.fsx#L8-L11)]

<span data-ttu-id="86663-190">Le flux de `toPigLatin` est donc :</span><span class="sxs-lookup"><span data-stu-id="86663-190">The flow of `toPigLatin` is thus:</span></span>

<span data-ttu-id="86663-191">Vérifiez si le premier caractère du mot d’entrée est une voyelle.</span><span class="sxs-lookup"><span data-stu-id="86663-191">Check if the first character of the input word is a vowel.</span></span> <span data-ttu-id="86663-192">S’il s’agit, attachez « hourra » à la fin du mot.</span><span class="sxs-lookup"><span data-stu-id="86663-192">If it is, attach "yay" to the end of the word.</span></span> <span data-ttu-id="86663-193">Sinon, déplacez le premier caractère à la fin du mot et « ay » lui ajouter.</span><span class="sxs-lookup"><span data-stu-id="86663-193">Otherwise, move that first character to the end of the word and add "ay" to it.</span></span>

<span data-ttu-id="86663-194">Il existe une dernière chose à noter à ce sujet : il n’existe aucune instruction explicite à retourner à partir de la fonction, contrairement à nombreux autres langages très utiles.</span><span class="sxs-lookup"><span data-stu-id="86663-194">There's one final thing to notice about this: there's no explicit instruction to return from the function, unlike many other languages out there.</span></span> <span data-ttu-id="86663-195">Cela est que F # est basé sur une Expression, et la dernière expression dans le corps d’une fonction est la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="86663-195">This is because F# is Expression-based, and the last expression in the body of a function is the return value.</span></span> <span data-ttu-id="86663-196">Car `if..then..else` lui-même est une expression, le corps de la `then` bloc ou le corps de la `else` bloc s’affichera en fonction de la valeur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="86663-196">Because `if..then..else` is itself an expression, the body of the `then` block or the body of the `else` block will be returned depending on the input value.</span></span>

## <a name="moving-your-script-code-into-the-implementation-file"></a><span data-ttu-id="86663-197">Déplacement de votre code de script dans le fichier d’implémentation</span><span class="sxs-lookup"><span data-stu-id="86663-197">Moving your script code into the implementation file</span></span>

<span data-ttu-id="86663-198">Les sections précédentes de cet article présenté une première étape dans l’écriture de code F # courants : écrire une fonction initiale et l’exécuter interactivement avec FSI.</span><span class="sxs-lookup"><span data-stu-id="86663-198">The previous sections in this article demonstrated a common first step in writing F# code: writing an initial function and executing it interactively with FSI.</span></span> <span data-ttu-id="86663-199">Développement piloté par réplication, il s’agit où [REPL](https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop) signifie « Boucle en lecture-évaluation-impression ».</span><span class="sxs-lookup"><span data-stu-id="86663-199">This is known as REPL-driven development, where [REPL](https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop) stands for "Read-Evaluate-Print Loop".</span></span> <span data-ttu-id="86663-200">Il s’agit d’un excellent moyen de faire des essais avec des fonctionnalités jusqu'à ce que vous ayez un élément de travail.</span><span class="sxs-lookup"><span data-stu-id="86663-200">It's a great way to experiment with functionality until you have something working.</span></span>

<span data-ttu-id="86663-201">L’étape suivante de développement piloté par REPL consiste à déplacer de code opérationnel dans un fichier d’implémentation F #.</span><span class="sxs-lookup"><span data-stu-id="86663-201">The next step in REPL-driven development is to move working code into an F# implementation file.</span></span> <span data-ttu-id="86663-202">Il peut ensuite être compilé par le compilateur F # dans un assembly qui peut être exécuté.</span><span class="sxs-lookup"><span data-stu-id="86663-202">It can then be compiled by the F# compiler into an assembly that can be executed.</span></span>

<span data-ttu-id="86663-203">Pour commencer, ouvrez `ClassLibraryDemo.fs`.</span><span class="sxs-lookup"><span data-stu-id="86663-203">To begin, open `ClassLibraryDemo.fs`.</span></span>  <span data-ttu-id="86663-204">Vous remarquerez que du code existe déjà dans.</span><span class="sxs-lookup"><span data-stu-id="86663-204">You'll notice that some code is already in there.</span></span> <span data-ttu-id="86663-205">Continuer et supprimer la définition de classe, mais veillez à laisser le [ `namespace` ](../language-reference/namespaces.md) déclaration en haut.</span><span class="sxs-lookup"><span data-stu-id="86663-205">Go ahead and delete the class definition, but make sure to leave the [`namespace`](../language-reference/namespaces.md) declaration at the top.</span></span>

<span data-ttu-id="86663-206">Ensuite, créez un nouveau [ `module` ](../language-reference/modules.md) appelé `PigLatin` et copiez le `toPigLatin` fonction en tant que tel dans celui-ci :</span><span class="sxs-lookup"><span data-stu-id="86663-206">Next, create a new [`module`](../language-reference/modules.md) called `PigLatin` and copy the `toPigLatin` function into it as such:</span></span>

[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/pig-latin.fs#L1-L14)]

<span data-ttu-id="86663-207">Ensuite, ouvrez le `Script.fsx` à nouveau de fichiers et supprimez la totalité de `toPigLatin` de fonctionner, mais veillez à conserver les deux lignes suivantes dans le fichier :</span><span class="sxs-lookup"><span data-stu-id="86663-207">Next, open the `Script.fsx` file again, and delete the entire `toPigLatin` function, but make sure to keep the following two lines in the file:</span></span>

```fsharp
#load "ClassLibraryDemo.fs"
open ClassLibraryDemo
```

<span data-ttu-id="86663-208">La première ligne est nécessaire pour écrire un script pour charger de FSI `ClassLibraryDemo.fs`.</span><span class="sxs-lookup"><span data-stu-id="86663-208">The first line is needed for FSI scripting to load `ClassLibraryDemo.fs`.</span></span> <span data-ttu-id="86663-209">La deuxième ligne est une commodité : omettant est facultative, mais vous devez taper `open ClassLibraryDemo` dans une fenêtre FSI si vous souhaitez mettre le `ToPigLatin` module dans la portée.</span><span class="sxs-lookup"><span data-stu-id="86663-209">The second line is a convenience: omitting it is optional, but you will need to type `open ClassLibraryDemo` in an FSI window if you wish to bring the `ToPigLatin` module into scope.</span></span>

<span data-ttu-id="86663-210">Ensuite, dans la fenêtre FSI, appelez la fonction avec le `PigLatin` module que vous avez défini précédemment :</span><span class="sxs-lookup"><span data-stu-id="86663-210">Next, in the FSI window, call the function with the `PigLatin` module that you defined earlier:</span></span>

```
> PigLatin.toPigLatin "banana";;
val it : string = "ananabay"
> PigLatin.toPigLatin "apple";;
val it : string = "appleyay"
```

<span data-ttu-id="86663-211">Opération réussie</span><span class="sxs-lookup"><span data-stu-id="86663-211">Success!</span></span> <span data-ttu-id="86663-212">Vous obtenez les mêmes résultats qu’avant, mais maintenant chargé à partir d’un fichier d’implémentation F #.</span><span class="sxs-lookup"><span data-stu-id="86663-212">You get the same results as before, but now loaded from an F# implementation file.</span></span> <span data-ttu-id="86663-213">La principale différence ici est que les fichiers de code source F # sont compilés dans des assemblys qui peuvent être exécutées n’importe où, pas seulement dans FSI.</span><span class="sxs-lookup"><span data-stu-id="86663-213">The major difference here is that F# source files are compiled into assemblies that can be executed anywhere, not just in FSI.</span></span>

## <a name="summary"></a><span data-ttu-id="86663-214">Récapitulatif</span><span class="sxs-lookup"><span data-stu-id="86663-214">Summary</span></span>

<span data-ttu-id="86663-215">Dans cet article, vous avez appris :</span><span class="sxs-lookup"><span data-stu-id="86663-215">In this article, you've learned:</span></span>

1. <span data-ttu-id="86663-216">Comment configurer le Code de Visual Studio avec Ionide.</span><span class="sxs-lookup"><span data-stu-id="86663-216">How to set up Visual Studio Code with Ionide.</span></span>
2. <span data-ttu-id="86663-217">Comment créer votre premier projet F # avec Ionide.</span><span class="sxs-lookup"><span data-stu-id="86663-217">How to create your first F# project with Ionide.</span></span>
3. <span data-ttu-id="86663-218">Comment utiliser F # script pour écrire votre première fonction) (F # dans Ionide puis l’exécuter dans FSI.</span><span class="sxs-lookup"><span data-stu-id="86663-218">How to use F# Scripting to write your first F# function in Ionide and then execute it in FSI.</span></span>
4. <span data-ttu-id="86663-219">Comment migrer votre code de script pour le code source F #, puis appelez ce code à partir de FSI.</span><span class="sxs-lookup"><span data-stu-id="86663-219">How to migrate your script code to F# source and then call that code from FSI.</span></span>

<span data-ttu-id="86663-220">Vous êtes désormais équipés pour écrire du code F # beaucoup plus à l’aide de Code Visual Studio et Ionide.</span><span class="sxs-lookup"><span data-stu-id="86663-220">You're now equipped to write much more F# code using Visual Studio Code and Ionide.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="86663-221">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="86663-221">Troubleshooting</span></span>

<span data-ttu-id="86663-222">Voici quelques manières que vous pouvez résoudre certains problèmes que vous pouvez rencontrer :</span><span class="sxs-lookup"><span data-stu-id="86663-222">Here are a few ways you can troubleshoot certain problems that you might run into:</span></span>

1. <span data-ttu-id="86663-223">Pour obtenir les fonctionnalités de Ionide de modification du code, vos fichiers F # doivent être enregistrés sur disque et à l’intérieur d’un dossier qui est ouvert dans l’espace de travail de Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="86663-223">To get the code editing features of Ionide, your F# files need to be saved to disk and inside of a folder that is open in the Visual Studio Code workspace.</span></span>
2. <span data-ttu-id="86663-224">Si vous avez apporté des modifications à votre système ou installé des composants requis de Ionide avec Code Visual Studio ouvert, redémarrez Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="86663-224">If you've made changes to your system or installed Ionide prerequisites with Visual Studio Code open, restart Visual Studio Code.</span></span>
3. <span data-ttu-id="86663-225">Vérifiez que vous pouvez utiliser le compilateur F # et F # interactive à partir de la ligne de commande sans un chemin d’accès qualifié complet.</span><span class="sxs-lookup"><span data-stu-id="86663-225">Check that you can use the F# compiler and F# interactive from the command line without a fully-qualified path.</span></span> <span data-ttu-id="86663-226">Vous pouvez le faire en tapant `fsc` dans une ligne de commande pour le compilateur F #, et `fsi` ou `fsharpi` pour Visual F # outils sur Windows et Mono sur Mac/Linux, respectivement.</span><span class="sxs-lookup"><span data-stu-id="86663-226">You can do so by typing `fsc` in a command line for the F# compiler, and `fsi` or `fsharpi` for the Visual F# tools on Windows and Mono on Mac/Linux, respectively.</span></span>
4. <span data-ttu-id="86663-227">Si vous avez des caractères non valides dans les répertoires de votre projet, Ionide peut ne pas fonctionner.</span><span class="sxs-lookup"><span data-stu-id="86663-227">If you have invalid characters in your project directories, Ionide might not work.</span></span>  <span data-ttu-id="86663-228">Renommer les répertoires de votre projet si c’est le cas.</span><span class="sxs-lookup"><span data-stu-id="86663-228">Rename your project directories if this is the case.</span></span>
5. <span data-ttu-id="86663-229">Si aucun des commandes Ionide ne fonctionnent pas, vérifiez votre [Visual Studio Code keybindings](https://code.visualstudio.com/docs/customization/keybindings#_customizing-shortcuts) pour voir si vous les remplacez par inadvertance.</span><span class="sxs-lookup"><span data-stu-id="86663-229">If none of the Ionide commands are working, check your [Visual Studio Code keybindings](https://code.visualstudio.com/docs/customization/keybindings#_customizing-shortcuts) to see if you're overriding them by accident.</span></span>
6. <span data-ttu-id="86663-230">Si Ionide est rompue sur votre ordinateur et qu’aucun d'entre eux a résolu votre problème, essayez de supprimer le `ionide-fsharp` répertoire sur votre ordinateur et réinstallez la suite de plug-in.</span><span class="sxs-lookup"><span data-stu-id="86663-230">If Ionide is broken on your machine and none of the above has fixed your problem, try removing the `ionide-fsharp` directory on your machine and reinstall the plugin suite.</span></span>

<span data-ttu-id="86663-231">Ionide est un projet open source créé et géré par les membres de la Communauté F #.</span><span class="sxs-lookup"><span data-stu-id="86663-231">Ionide is an open source project built and maintained by members of the F# community.</span></span> <span data-ttu-id="86663-232">Veuillez signaler des problèmes et n’hésitez pas à contribuer à la [Ionide-VSCode : référentiel GitHub de FSharp](https://github.com/ionide/ionide-vscode-fsharp).</span><span class="sxs-lookup"><span data-stu-id="86663-232">Please report issues and feel free to contribute at the [Ionide-VSCode: FSharp GitHub repository](https://github.com/ionide/ionide-vscode-fsharp).</span></span>

<span data-ttu-id="86663-233">Si vous avez un problème de rapport, veuillez suivre [les instructions pour l’obtention de journaux à utiliser lors de la déclaration d’un problème](https://github.com/ionide/ionide-vscode-fsharp#how-to-get-logs-for-debugging--issue-reporting).</span><span class="sxs-lookup"><span data-stu-id="86663-233">If you have an issue to report, please follow [the instructions for getting logs to use when reporting an issue](https://github.com/ionide/ionide-vscode-fsharp#how-to-get-logs-for-debugging--issue-reporting).</span></span>

<span data-ttu-id="86663-234">Vous pouvez également demander à pour plus d’informations à partir de la Ionide développeurs et de F # dans le [Ionide Gitter canal](https://gitter.im/ionide/ionide-project).</span><span class="sxs-lookup"><span data-stu-id="86663-234">You can also ask for further help from the Ionide developers and F# community in the [Ionide Gitter channel](https://gitter.im/ionide/ionide-project).</span></span>

## <a name="next-steps"></a><span data-ttu-id="86663-235">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="86663-235">Next steps</span></span>

<span data-ttu-id="86663-236">Pour en savoir plus sur F # et les fonctionnalités du langage, consultez [visite guidée de F #](../tour.md).</span><span class="sxs-lookup"><span data-stu-id="86663-236">To learn more about F# and the features of the language, check out [Tour of F#](../tour.md).</span></span>
