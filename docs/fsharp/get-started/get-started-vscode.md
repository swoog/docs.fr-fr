---
title: 'Bien démarrer avec F # dans Visual Studio Code'
description: 'Découvrez comment utiliser F # avec Visual Studio Code et la suite de plug-in Ionide.'
ms.date: 05/28/2018
ms.openlocfilehash: e962be2796cf0d6eb90d459730659e492f864716
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "50192666"
---
# <a name="get-started-with-f-in-visual-studio-code"></a><span data-ttu-id="95698-103">Bien démarrer avec F # dans Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="95698-103">Get Started with F# in Visual Studio Code</span></span>

<span data-ttu-id="95698-104">Vous pouvez écrire F # dans [Visual Studio Code](https://code.visualstudio.com) avec la [plug-in Ionide](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fsharp) pour obtenir une bonne expérience d’un environnement de développement intégré (IDE), multiplateforme et léger, des IntelliSense et le code de base refactorisations.</span><span class="sxs-lookup"><span data-stu-id="95698-104">You can write F# in [Visual Studio Code](https://code.visualstudio.com) with the [Ionide plugin](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fsharp) to get a great cross-platform, lightweight Integrated Development Environment (IDE) experience with IntelliSense and basic code refactorings.</span></span> <span data-ttu-id="95698-105">Visitez [Ionide.io](http://ionide.io) pour en savoir plus sur le plug-in.</span><span class="sxs-lookup"><span data-stu-id="95698-105">Visit [Ionide.io](http://ionide.io) to learn more about the plugin.</span></span>

<span data-ttu-id="95698-106">Pour commencer, assurez-vous d’avoir [F # et le plug-in Ionide correctement installé](install-fsharp.md#install-f-with-visual-studio-code).</span><span class="sxs-lookup"><span data-stu-id="95698-106">To begin, ensure that you have [F# and the Ionide plugin correctly installed](install-fsharp.md#install-f-with-visual-studio-code).</span></span>

## <a name="creating-your-first-project-with-ionide"></a><span data-ttu-id="95698-107">Créer votre premier projet avec Ionide</span><span class="sxs-lookup"><span data-stu-id="95698-107">Creating your first project with Ionide</span></span>

<span data-ttu-id="95698-108">Pour créer un nouveau projet F #, ouvrez Visual Studio Code dans un nouveau dossier (vous pouvez le nommer comme vous le souhaitez).</span><span class="sxs-lookup"><span data-stu-id="95698-108">To create a new F# project, open Visual Studio Code in a new folder (you can name it whatever you like).</span></span>

<span data-ttu-id="95698-109">Ensuite, ouvrez la palette de commandes (**vue > Palette de commandes**) et tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="95698-109">Next, open the command palette (**View > Command Palette**) and type the following:</span></span>

```
> F# new project
```

<span data-ttu-id="95698-110">Cela est alimenté par le [FORGE](https://github.com/fsharp-editing/Forge) projet.</span><span class="sxs-lookup"><span data-stu-id="95698-110">This is powered by the [FORGE](https://github.com/fsharp-editing/Forge) project.</span></span>

> [!NOTE]
<span data-ttu-id="95698-111">Si vous ne voyez pas les options de modèle, essayez d’actualiser les modèles en exécutant la commande suivante dans la Palette de commandes : `>F#: Refresh Project Templates`.</span><span class="sxs-lookup"><span data-stu-id="95698-111">If you don't see template options, try refreshing templates by running the following command in the Command Palette: `>F#: Refresh Project Templates`.</span></span>

<span data-ttu-id="95698-112">Sélectionnez « F #: nouveau projet » en appuyant sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="95698-112">Select "F#: New Project" by hitting **Enter**.</span></span> <span data-ttu-id="95698-113">Vous accédez à l’étape suivante, ce qui concerne la sélection d’un modèle de projet.</span><span class="sxs-lookup"><span data-stu-id="95698-113">This takes you to the next step, which is for selecting a project template.</span></span>

<span data-ttu-id="95698-114">Choisir le `classlib` modèle et le positionnement **entrée**.</span><span class="sxs-lookup"><span data-stu-id="95698-114">Pick the `classlib` template and hit **Enter**.</span></span>

<span data-ttu-id="95698-115">Ensuite, choisissez un répertoire pour créer le projet dans.</span><span class="sxs-lookup"><span data-stu-id="95698-115">Next, pick a directory to create the project in.</span></span> <span data-ttu-id="95698-116">Si vous laissez vide, il utilise le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="95698-116">If you leave it blank, it uses the current directory.</span></span>

<span data-ttu-id="95698-117">Enfin, nommez votre projet dans l’étape finale.</span><span class="sxs-lookup"><span data-stu-id="95698-117">Finally, name your project in the final step.</span></span> <span data-ttu-id="95698-118">F # utilise [casse Pascal](http://c2.com/cgi/wiki?PascalCase) pour les noms de projet.</span><span class="sxs-lookup"><span data-stu-id="95698-118">F# uses [Pascal case](http://c2.com/cgi/wiki?PascalCase) for project names.</span></span> <span data-ttu-id="95698-119">Cet article utilise `ClassLibraryDemo` comme nom.</span><span class="sxs-lookup"><span data-stu-id="95698-119">This article uses `ClassLibraryDemo` as the name.</span></span> <span data-ttu-id="95698-120">Une fois que vous avez entré le nom souhaité pour votre projet, appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="95698-120">Once you've entered the name you want for your project, hit **Enter**.</span></span>

<span data-ttu-id="95698-121">Si vous avez suivi l’étape précédente, vous devez obtenir le Visual Studio Code espace de travail sur le côté gauche apparaissent avec les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="95698-121">If you followed the previous step, you should get the Visual Studio Code Workspace on the left-hand side to appear with the following:</span></span>

1. <span data-ttu-id="95698-122">F # projet lui-même, en dessous du `ClassLibraryDemo` dossier.</span><span class="sxs-lookup"><span data-stu-id="95698-122">The F# project itself, underneath the `ClassLibraryDemo` folder.</span></span>
2. <span data-ttu-id="95698-123">La structure de répertoire correct pour l’ajout de packages via [ `Paket` ](https://fsprojects.github.io/Paket/).</span><span class="sxs-lookup"><span data-stu-id="95698-123">The correct directory structure for adding packages via [`Paket`](https://fsprojects.github.io/Paket/).</span></span>
3. <span data-ttu-id="95698-124">Un multiplates-générer le script avec [ `FAKE` ](https://fsharp.github.io/FAKE/).</span><span class="sxs-lookup"><span data-stu-id="95698-124">A cross-platform build script with [`FAKE`](https://fsharp.github.io/FAKE/).</span></span>
4. <span data-ttu-id="95698-125">Le `paket.exe` exécutable qui peut extraire les packages et résoudre les dépendances pour vous.</span><span class="sxs-lookup"><span data-stu-id="95698-125">The `paket.exe` executable that can fetch packages and resolve dependencies for you.</span></span>
5. <span data-ttu-id="95698-126">Un `.gitignore` fichier si vous souhaitez ajouter ce projet au contrôle de code source Git.</span><span class="sxs-lookup"><span data-stu-id="95698-126">A `.gitignore` file if you wish to add this project to Git-based source control.</span></span>

## <a name="writing-some-code"></a><span data-ttu-id="95698-127">Écrire du code</span><span class="sxs-lookup"><span data-stu-id="95698-127">Writing some code</span></span>

<span data-ttu-id="95698-128">Ouvrez le *ClassLibraryDemo* dossier.</span><span class="sxs-lookup"><span data-stu-id="95698-128">Open the *ClassLibraryDemo* folder.</span></span>  <span data-ttu-id="95698-129">Vous devez voir les fichiers suivants :</span><span class="sxs-lookup"><span data-stu-id="95698-129">You should see the following files:</span></span>

1. <span data-ttu-id="95698-130">`ClassLibraryDemo.fs`, un fichier d’implémentation F # avec une classe définie.</span><span class="sxs-lookup"><span data-stu-id="95698-130">`ClassLibraryDemo.fs`, an F# implementation file with a class defined.</span></span>
2. <span data-ttu-id="95698-131">`ClassLibraryDemo.fsproj`, un fichier de projet F # est utilisé pour générer ce projet.</span><span class="sxs-lookup"><span data-stu-id="95698-131">`ClassLibraryDemo.fsproj`, an F# project file used to build this project.</span></span>
3. <span data-ttu-id="95698-132">`Script.fsx`, un fichier de script F # qui charge le fichier source.</span><span class="sxs-lookup"><span data-stu-id="95698-132">`Script.fsx`, an F# script file that loads the source file.</span></span>
4. <span data-ttu-id="95698-133">`paket.references`, un fichier Paket qui spécifie les dépendances du projet.</span><span class="sxs-lookup"><span data-stu-id="95698-133">`paket.references`, a Paket file that specifies the project dependencies.</span></span>

<span data-ttu-id="95698-134">Ouvrez `Script.fsx`et ajoutez le code suivant à la fin de celle-ci :</span><span class="sxs-lookup"><span data-stu-id="95698-134">Open `Script.fsx`, and add the following code at the end of it:</span></span>

[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/to-pig-latin.fsx)]

<span data-ttu-id="95698-135">Cette fonction convertit un mot à un formulaire de [Pig Latin](https://en.wikipedia.org/wiki/Pig_Latin).</span><span class="sxs-lookup"><span data-stu-id="95698-135">This function converts a word to a form of [Pig Latin](https://en.wikipedia.org/wiki/Pig_Latin).</span></span> <span data-ttu-id="95698-136">L’étape suivante consiste à évaluer à l’aide de F # Interactive (FSI).</span><span class="sxs-lookup"><span data-stu-id="95698-136">The next step is to evaluate it using F# Interactive (FSI).</span></span>

<span data-ttu-id="95698-137">Mettez en surbrillance de la fonction entière (il doit être 11 lignes longues).</span><span class="sxs-lookup"><span data-stu-id="95698-137">Highlight the entire function (it should be 11 lines long).</span></span> <span data-ttu-id="95698-138">Une fois qu’elle est mise en surbrillance, maintenez la **Alt** clé, puis appuyez sur **entrée**.</span><span class="sxs-lookup"><span data-stu-id="95698-138">Once it is highlighted, hold the **Alt** key and hit **Enter**.</span></span> <span data-ttu-id="95698-139">Vous remarquerez une fenêtre contextuelle ci-dessous, et il doit s’afficher quelque chose comme ceci :</span><span class="sxs-lookup"><span data-stu-id="95698-139">You'll notice a window pop up below, and it should show something like this:</span></span>

![Exemple de sortie de F # Interactive avec Ionide](media/getting-started-vscode/vscode-fsi.png)

<span data-ttu-id="95698-141">Cela fait trois choses :</span><span class="sxs-lookup"><span data-stu-id="95698-141">This did three things:</span></span>

1. <span data-ttu-id="95698-142">Il a démarré le processus FSI.</span><span class="sxs-lookup"><span data-stu-id="95698-142">It started the FSI process.</span></span>
2. <span data-ttu-id="95698-143">Il envoyé le code que vous avez sélectionnée sur le processus FSI.</span><span class="sxs-lookup"><span data-stu-id="95698-143">It sent the code you highlighted over the FSI process.</span></span>
3. <span data-ttu-id="95698-144">Le processus FSI évalué le code que vous avez envoyé via.</span><span class="sxs-lookup"><span data-stu-id="95698-144">The FSI process evaluated the code you sent over.</span></span>

<span data-ttu-id="95698-145">Étant donné que ce que vous avez envoyé via a été un [fonction](../language-reference/functions/index.md), vous pouvez maintenant appeler cette fonction avec FSI !</span><span class="sxs-lookup"><span data-stu-id="95698-145">Because what you sent over was a [function](../language-reference/functions/index.md), you can now call that function with FSI!</span></span> <span data-ttu-id="95698-146">Dans la fenêtre interactive, tapez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="95698-146">In the interactive window, type the following:</span></span>

```fsharp
toPigLatin "banana";;
```

<span data-ttu-id="95698-147">Vous devez voir le résultat suivant :</span><span class="sxs-lookup"><span data-stu-id="95698-147">You should see the following result:</span></span>

```fsharp
val it : string = "ananabay"
```

<span data-ttu-id="95698-148">À présent, essayons avec une voyelle en tant que la première lettre.</span><span class="sxs-lookup"><span data-stu-id="95698-148">Now, let's try with a vowel as the first letter.</span></span> <span data-ttu-id="95698-149">Entrez les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="95698-149">Enter the following:</span></span>

```fsharp
toPigLatin "apple";;
```

<span data-ttu-id="95698-150">Vous devez voir le résultat suivant :</span><span class="sxs-lookup"><span data-stu-id="95698-150">You should see the following result:</span></span>

```fsharp
val it : string = "appleyay"
```

<span data-ttu-id="95698-151">La fonction semble fonctionner comme prévu.</span><span class="sxs-lookup"><span data-stu-id="95698-151">The function appears to be working as expected.</span></span> <span data-ttu-id="95698-152">Félicitations, que vous venez d’écrire votre première fonction F # dans Visual Studio Code et il évaluée avec FSI !</span><span class="sxs-lookup"><span data-stu-id="95698-152">Congratulations, you just wrote your first F# function in Visual Studio Code and evaluated it with FSI!</span></span>

>[!NOTE]
<span data-ttu-id="95698-153">Comme vous l’avez peut-être remarqué, les lignes dans FSI sont terminent par `;;`.</span><span class="sxs-lookup"><span data-stu-id="95698-153">As you may have noticed, the lines in FSI are terminated with `;;`.</span></span> <span data-ttu-id="95698-154">Il s’agit, car FSI vous permet d’entrer plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="95698-154">This is because FSI allows you to enter multiple lines.</span></span> <span data-ttu-id="95698-155">Le `;;` à la fin informe FSI lorsque le code est terminé.</span><span class="sxs-lookup"><span data-stu-id="95698-155">The `;;` at the end lets FSI know when the code is finished.</span></span>

## <a name="explaining-the-code"></a><span data-ttu-id="95698-156">Explication du code</span><span class="sxs-lookup"><span data-stu-id="95698-156">Explaining the code</span></span>

<span data-ttu-id="95698-157">Si vous n’êtes pas sûr de ce que le code est en fait, Voici un pas à pas.</span><span class="sxs-lookup"><span data-stu-id="95698-157">If you're not sure about what the code is actually doing, here's a step-by-step.</span></span>

<span data-ttu-id="95698-158">Comme vous pouvez le voir, `toPigLatin` est une fonction qui accepte un mot comme entrée et le convertit en une représentation sous forme de Pig Latin de ce mot.</span><span class="sxs-lookup"><span data-stu-id="95698-158">As you can see, `toPigLatin` is a function that takes a word as its input and converts it to a Pig-Latin representation of that word.</span></span> <span data-ttu-id="95698-159">Les règles pour ce sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="95698-159">The rules for this are as follows:</span></span>

<span data-ttu-id="95698-160">Si le premier caractère dans un mot commence par une voyelle, ajoutez « hourra » à la fin du mot.</span><span class="sxs-lookup"><span data-stu-id="95698-160">If the first character in a word starts with a vowel, add "yay" to the end of the word.</span></span> <span data-ttu-id="95698-161">Si elle ne commence pas par une voyelle, déplacer ce premier caractère à la fin du mot et « ay » lui ajouter.</span><span class="sxs-lookup"><span data-stu-id="95698-161">If it doesn't start with a vowel, move that first character to the end of the word and add "ay" to it.</span></span>

<span data-ttu-id="95698-162">Vous avez peut-être remarqué ce qui suit dans FSI :</span><span class="sxs-lookup"><span data-stu-id="95698-162">You may have noticed the following in FSI:</span></span>

```fsharp
val toPigLatin : word:string -> string
```

<span data-ttu-id="95698-163">Cela indique que `toPigLatin` est une fonction qui accepte un `string` en tant qu’entrée (appelé `word`), ainsi qu’un autre `string`.</span><span class="sxs-lookup"><span data-stu-id="95698-163">This states that `toPigLatin` is a function that takes in a `string` as input (called `word`), and returns another `string`.</span></span> <span data-ttu-id="95698-164">Il s’agit du [signature de type de la fonction](https://fsharpforfunandprofit.com/posts/function-signatures/), un élément fondamental de F # qui est essentiel à comprendre le code F #.</span><span class="sxs-lookup"><span data-stu-id="95698-164">This is known as the [type signature of the function](https://fsharpforfunandprofit.com/posts/function-signatures/), a fundamental piece of F# that's key to understanding F# code.</span></span> <span data-ttu-id="95698-165">Vous pouvez également constater si vous pointez sur la fonction dans Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="95698-165">You'll also notice this if you hover over the function in Visual Studio Code.</span></span>

<span data-ttu-id="95698-166">Dans le corps de la fonction, vous remarquerez deux parties distinctes :</span><span class="sxs-lookup"><span data-stu-id="95698-166">In the body of the function, you'll notice two distinct parts:</span></span>

1. <span data-ttu-id="95698-167">Une fonction interne, appelée `isVowel`, qui détermine si un caractère donné (`c`) est une voyelle en vérifiant si elle correspond à un des modèles fournis par le biais de [critères spéciaux](../language-reference/pattern-matching.md):</span><span class="sxs-lookup"><span data-stu-id="95698-167">An inner function, called `isVowel`, that determines if a given character (`c`) is a vowel by checking if it matches one of the provided patterns via [Pattern Matching](../language-reference/pattern-matching.md):</span></span>

   [!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/to-pig-latin.fsx#L2-L6)]

2. <span data-ttu-id="95698-168">Un [ `if..then..else` ](../language-reference/conditional-expressions-if-then-else.md) expression qui vérifie si le premier caractère est une voyelle et les constructions de la valeur renvoyée hors les caractères d’entrée selon que le premier caractère a été une voyelle ou non :</span><span class="sxs-lookup"><span data-stu-id="95698-168">An [`if..then..else`](../language-reference/conditional-expressions-if-then-else.md) expression that checks if the first character is a vowel, and constructs a return value out of the input characters based on if the first character was a vowel or not:</span></span>

   [!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/to-pig-latin.fsx#L8-L11)]

<span data-ttu-id="95698-169">Le flux de `toPigLatin` est donc :</span><span class="sxs-lookup"><span data-stu-id="95698-169">The flow of `toPigLatin` is thus:</span></span>

<span data-ttu-id="95698-170">Vérifiez si le premier caractère du mot d’entrée est une voyelle.</span><span class="sxs-lookup"><span data-stu-id="95698-170">Check if the first character of the input word is a vowel.</span></span> <span data-ttu-id="95698-171">Dans le cas, attachez « hourra » à la fin du mot.</span><span class="sxs-lookup"><span data-stu-id="95698-171">If it is, attach "yay" to the end of the word.</span></span> <span data-ttu-id="95698-172">Sinon, déplacez ce premier caractère à la fin du mot et « ay » lui ajouter.</span><span class="sxs-lookup"><span data-stu-id="95698-172">Otherwise, move that first character to the end of the word and add "ay" to it.</span></span>

<span data-ttu-id="95698-173">Il existe une dernière chose à noter à ce sujet : il n’existe aucune instruction explicite à retourner à partir de la fonction, contrairement à nombreux autres langages disponibles.</span><span class="sxs-lookup"><span data-stu-id="95698-173">There's one final thing to notice about this: there's no explicit instruction to return from the function, unlike many other languages out there.</span></span> <span data-ttu-id="95698-174">Il s’agit comme F # est basée sur une Expression et la dernière expression dans le corps d’une fonction est la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="95698-174">This is because F# is Expression-based, and the last expression in the body of a function is the return value.</span></span> <span data-ttu-id="95698-175">Étant donné que `if..then..else` lui-même est une expression, le corps de la `then` bloc ou dans le corps de la `else` bloc s’affichera en fonction de la valeur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="95698-175">Because `if..then..else` is itself an expression, the body of the `then` block or the body of the `else` block will be returned depending on the input value.</span></span>

## <a name="moving-your-script-code-into-the-implementation-file"></a><span data-ttu-id="95698-176">Déplacement de votre code de script dans le fichier d’implémentation</span><span class="sxs-lookup"><span data-stu-id="95698-176">Moving your script code into the implementation file</span></span>

<span data-ttu-id="95698-177">Les sections précédentes de cet article démontré une première étape dans l’écriture de code F # courantes : écriture d’une fonction initiale et l’exécuter interactivement avec FSI.</span><span class="sxs-lookup"><span data-stu-id="95698-177">The previous sections in this article demonstrated a common first step in writing F# code: writing an initial function and executing it interactively with FSI.</span></span> <span data-ttu-id="95698-178">On parle de développement piloté par les REPL, où [REPL](https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop) est l’acronyme « Read-Evaluate-Print boucle ».</span><span class="sxs-lookup"><span data-stu-id="95698-178">This is known as REPL-driven development, where [REPL](https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop) stands for "Read-Evaluate-Print Loop".</span></span> <span data-ttu-id="95698-179">Il est un excellent moyen de faire des essais avec des fonctionnalités jusqu'à ce que vous avez quelque chose fonctionne.</span><span class="sxs-lookup"><span data-stu-id="95698-179">It's a great way to experiment with functionality until you have something working.</span></span>

<span data-ttu-id="95698-180">L’étape suivante dans le développement piloté par REPL consiste à déplacer le code de travail dans un fichier d’implémentation F #.</span><span class="sxs-lookup"><span data-stu-id="95698-180">The next step in REPL-driven development is to move working code into an F# implementation file.</span></span> <span data-ttu-id="95698-181">Il peut ensuite être compilé par le compilateur F # dans un assembly qui peut être exécuté.</span><span class="sxs-lookup"><span data-stu-id="95698-181">It can then be compiled by the F# compiler into an assembly that can be executed.</span></span>

<span data-ttu-id="95698-182">Pour commencer, ouvrez `ClassLibraryDemo.fs`.</span><span class="sxs-lookup"><span data-stu-id="95698-182">To begin, open `ClassLibraryDemo.fs`.</span></span>  <span data-ttu-id="95698-183">Vous remarquerez que du code existe déjà dans.</span><span class="sxs-lookup"><span data-stu-id="95698-183">You'll notice that some code is already in there.</span></span> <span data-ttu-id="95698-184">Continuer et supprimer la définition de classe, mais veillez à laisser le [ `namespace` ](../language-reference/namespaces.md) déclaration en haut.</span><span class="sxs-lookup"><span data-stu-id="95698-184">Go ahead and delete the class definition, but make sure to leave the [`namespace`](../language-reference/namespaces.md) declaration at the top.</span></span>

<span data-ttu-id="95698-185">Ensuite, créez un nouveau [ `module` ](../language-reference/modules.md) appelé `PigLatin` et copiez le `toPigLatin` fonction dedans ainsi :</span><span class="sxs-lookup"><span data-stu-id="95698-185">Next, create a new [`module`](../language-reference/modules.md) called `PigLatin` and copy the `toPigLatin` function into it as such:</span></span>

[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/pig-latin.fs#L1-L14)]

<span data-ttu-id="95698-186">Ensuite, ouvrez le `Script.fsx` à nouveau de fichiers et de supprimer l’intégralité de `toPigLatin` de fonctionner, mais veillez à conserver les deux lignes suivantes dans le fichier :</span><span class="sxs-lookup"><span data-stu-id="95698-186">Next, open the `Script.fsx` file again, and delete the entire `toPigLatin` function, but make sure to keep the following two lines in the file:</span></span>

```fsharp
#load "ClassLibraryDemo.fs"
open ClassLibraryDemo
```

<span data-ttu-id="95698-187">La première ligne est nécessaire pour FSI de script pour charger `ClassLibraryDemo.fs`.</span><span class="sxs-lookup"><span data-stu-id="95698-187">The first line is needed for FSI scripting to load `ClassLibraryDemo.fs`.</span></span> <span data-ttu-id="95698-188">La deuxième ligne est une commodité : en l’omettant est facultative, mais vous devrez taper `open ClassLibraryDemo` dans une fenêtre FSI si vous souhaitez mettre le `ToPigLatin` module dans la portée.</span><span class="sxs-lookup"><span data-stu-id="95698-188">The second line is a convenience: omitting it is optional, but you will need to type `open ClassLibraryDemo` in an FSI window if you wish to bring the `ToPigLatin` module into scope.</span></span>

<span data-ttu-id="95698-189">Ensuite, dans la fenêtre FSI, appelez la fonction avec le `PigLatin` module que vous avez défini précédemment :</span><span class="sxs-lookup"><span data-stu-id="95698-189">Next, in the FSI window, call the function with the `PigLatin` module that you defined earlier:</span></span>

```
> PigLatin.toPigLatin "banana";;
val it : string = "ananabay"
> PigLatin.toPigLatin "apple";;
val it : string = "appleyay"
```

<span data-ttu-id="95698-190">Opération réussie</span><span class="sxs-lookup"><span data-stu-id="95698-190">Success!</span></span> <span data-ttu-id="95698-191">Vous obtenez les mêmes résultats en tant qu’avant, mais maintenant chargé à partir d’un fichier d’implémentation F #.</span><span class="sxs-lookup"><span data-stu-id="95698-191">You get the same results as before, but now loaded from an F# implementation file.</span></span> <span data-ttu-id="95698-192">La principale différence ici est que les fichiers de code source F # sont compilés dans des assemblys qui peuvent être exécutées n’importe où, pas seulement dans FSI.</span><span class="sxs-lookup"><span data-stu-id="95698-192">The major difference here is that F# source files are compiled into assemblies that can be executed anywhere, not just in FSI.</span></span>

## <a name="summary"></a><span data-ttu-id="95698-193">Récapitulatif</span><span class="sxs-lookup"><span data-stu-id="95698-193">Summary</span></span>

<span data-ttu-id="95698-194">Dans cet article, vous avez appris :</span><span class="sxs-lookup"><span data-stu-id="95698-194">In this article, you've learned:</span></span>

1. <span data-ttu-id="95698-195">Comment configurer Visual Studio Code avec Ionide.</span><span class="sxs-lookup"><span data-stu-id="95698-195">How to set up Visual Studio Code with Ionide.</span></span>
2. <span data-ttu-id="95698-196">Comment créer votre premier projet F # avec Ionide.</span><span class="sxs-lookup"><span data-stu-id="95698-196">How to create your first F# project with Ionide.</span></span>
3. <span data-ttu-id="95698-197">Comment utiliser F # script pour écrire votre première fonction F # dans Ionide puis l’exécuter dans FSI.</span><span class="sxs-lookup"><span data-stu-id="95698-197">How to use F# Scripting to write your first F# function in Ionide and then execute it in FSI.</span></span>
4. <span data-ttu-id="95698-198">Comment migrer votre code de script vers le code source F #, puis appelez ce code à partir de FSI.</span><span class="sxs-lookup"><span data-stu-id="95698-198">How to migrate your script code to F# source and then call that code from FSI.</span></span>

<span data-ttu-id="95698-199">Vous êtes désormais équipés pour écrire du code F # beaucoup plus à l’aide de Visual Studio Code et Ionide.</span><span class="sxs-lookup"><span data-stu-id="95698-199">You're now equipped to write much more F# code using Visual Studio Code and Ionide.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="95698-200">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="95698-200">Troubleshooting</span></span>

<span data-ttu-id="95698-201">Voici quelques façons que vous pouvez résoudre certains problèmes que vous pouvez rencontrer :</span><span class="sxs-lookup"><span data-stu-id="95698-201">Here are a few ways you can troubleshoot certain problems that you might run into:</span></span>

1. <span data-ttu-id="95698-202">Pour obtenir les fonctionnalités de Ionide de modification du code, vos fichiers F # doivent être enregistrés sur disque et à l’intérieur d’un dossier qui est ouvert dans l’espace de travail Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="95698-202">To get the code editing features of Ionide, your F# files need to be saved to disk and inside of a folder that is open in the Visual Studio Code workspace.</span></span>
2. <span data-ttu-id="95698-203">Si vous avez apporté des modifications à votre système ou installé des composants requis de Ionide avec Visual Studio Code open, redémarrez Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="95698-203">If you've made changes to your system or installed Ionide prerequisites with Visual Studio Code open, restart Visual Studio Code.</span></span>
3. <span data-ttu-id="95698-204">Vérifiez que vous pouvez utiliser le compilateur F # et F # interactive à partir de la ligne de commande sans un chemin d’accès qualifié complet.</span><span class="sxs-lookup"><span data-stu-id="95698-204">Check that you can use the F# compiler and F# interactive from the command line without a fully-qualified path.</span></span> <span data-ttu-id="95698-205">Vous pouvez le faire en tapant `fsc` dans une ligne de commande pour le compilateur F #, et `fsi` ou `fsharpi` pour Visual F # tools sur Windows et Mono sur Mac/Linux, respectivement.</span><span class="sxs-lookup"><span data-stu-id="95698-205">You can do so by typing `fsc` in a command line for the F# compiler, and `fsi` or `fsharpi` for the Visual F# tools on Windows and Mono on Mac/Linux, respectively.</span></span>
4. <span data-ttu-id="95698-206">Si vous avez des caractères non valides dans vos répertoires de projet, Ionide peut ne pas fonctionne.</span><span class="sxs-lookup"><span data-stu-id="95698-206">If you have invalid characters in your project directories, Ionide might not work.</span></span>  <span data-ttu-id="95698-207">Renommez vos répertoires de projet si c’est le cas.</span><span class="sxs-lookup"><span data-stu-id="95698-207">Rename your project directories if this is the case.</span></span>
5. <span data-ttu-id="95698-208">Si aucun des commandes Ionide travaillez, vérifiez votre [les combinaisons de touches Visual Studio Code](https://code.visualstudio.com/docs/customization/keybindings#_customizing-shortcuts) pour voir si vous êtes les remplaçant par inadvertance.</span><span class="sxs-lookup"><span data-stu-id="95698-208">If none of the Ionide commands are working, check your [Visual Studio Code keybindings](https://code.visualstudio.com/docs/customization/keybindings#_customizing-shortcuts) to see if you're overriding them by accident.</span></span>
6. <span data-ttu-id="95698-209">Si Ionide est rompue sur votre ordinateur et aucun d'entre eux a résolu votre problème, essayez de supprimer le `ionide-fsharp` répertoire sur votre ordinateur et réinstaller la suite de plug-in.</span><span class="sxs-lookup"><span data-stu-id="95698-209">If Ionide is broken on your machine and none of the above has fixed your problem, try removing the `ionide-fsharp` directory on your machine and reinstall the plugin suite.</span></span>

<span data-ttu-id="95698-210">Ionide est un projet open source construit et géré par les membres de la Communauté F #.</span><span class="sxs-lookup"><span data-stu-id="95698-210">Ionide is an open source project built and maintained by members of the F# community.</span></span> <span data-ttu-id="95698-211">Veuillez signaler des problèmes et n’hésitez pas à contribuer à la [Ionide-VSCode : dépôt GitHub de FSharp](https://github.com/ionide/ionide-vscode-fsharp).</span><span class="sxs-lookup"><span data-stu-id="95698-211">Please report issues and feel free to contribute at the [Ionide-VSCode: FSharp GitHub repository](https://github.com/ionide/ionide-vscode-fsharp).</span></span>

<span data-ttu-id="95698-212">Si vous rencontrez un problème au rapport, suivez [les instructions pour obtenir les journaux à utiliser lorsque vous signalez un problème](https://github.com/ionide/ionide-vscode-fsharp#how-to-get-logs-for-debugging--issue-reporting).</span><span class="sxs-lookup"><span data-stu-id="95698-212">If you have an issue to report, please follow [the instructions for getting logs to use when reporting an issue](https://github.com/ionide/ionide-vscode-fsharp#how-to-get-logs-for-debugging--issue-reporting).</span></span>

<span data-ttu-id="95698-213">Vous pouvez également demander de l’aide supplémentaire des développeurs de Ionide et de la Communauté F # dans le [Ionide Gitter canal](https://gitter.im/ionide/ionide-project).</span><span class="sxs-lookup"><span data-stu-id="95698-213">You can also ask for further help from the Ionide developers and F# community in the [Ionide Gitter channel](https://gitter.im/ionide/ionide-project).</span></span>

## <a name="next-steps"></a><span data-ttu-id="95698-214">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="95698-214">Next steps</span></span>

<span data-ttu-id="95698-215">Pour en savoir plus sur F # et les fonctionnalités du langage, consultez [visite guidée de F #](../tour.md).</span><span class="sxs-lookup"><span data-stu-id="95698-215">To learn more about F# and the features of the language, check out [Tour of F#](../tour.md).</span></span>
