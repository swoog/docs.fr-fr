---
title: Prise en main F# dans Visual Studio pour Mac
description: Découvrez comment utiliser F# avec Visual Studio pour Mac.
ms.date: 07/03/2018
ms.openlocfilehash: a6997f139d7e6c5fdf77878442db0b0b75b3d727
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59331861"
---
# <a name="get-started-with-f-in-visual-studio-for-mac"></a><span data-ttu-id="5786a-103">Prise en main F# dans Visual Studio pour Mac</span><span class="sxs-lookup"><span data-stu-id="5786a-103">Get started with F# in Visual Studio for Mac</span></span>

<span data-ttu-id="5786a-104">F#et le visuel F# outils sont pris en charge dans Visual Studio pour Mac IDE.</span><span class="sxs-lookup"><span data-stu-id="5786a-104">F# and the Visual F# tooling are supported in the Visual Studio for Mac IDE.</span></span> <span data-ttu-id="5786a-105">Assurez-vous d’avoir [Visual Studio pour Mac installé](install-fsharp.md#install-f-with-visual-studio-for-mac).</span><span class="sxs-lookup"><span data-stu-id="5786a-105">Ensure that you have [Visual Studio for Mac installed](install-fsharp.md#install-f-with-visual-studio-for-mac).</span></span>

## <a name="creating-a-console-application"></a><span data-ttu-id="5786a-106">Création d’une application de console</span><span class="sxs-lookup"><span data-stu-id="5786a-106">Creating a console application</span></span>

<span data-ttu-id="5786a-107">Un des projets plus simples dans Visual Studio pour Mac est l’Application de Console.</span><span class="sxs-lookup"><span data-stu-id="5786a-107">One of the most basic projects in Visual Studio for Mac is the Console Application.</span></span>  <span data-ttu-id="5786a-108">Voici comment faire.</span><span class="sxs-lookup"><span data-stu-id="5786a-108">Here's how to do it.</span></span>  <span data-ttu-id="5786a-109">Une fois que Visual Studio pour Mac est ouvert :</span><span class="sxs-lookup"><span data-stu-id="5786a-109">Once Visual Studio for Mac is open:</span></span>

1. <span data-ttu-id="5786a-110">Sur le **fichier** menu, pointez sur **nouvelle Solution**.</span><span class="sxs-lookup"><span data-stu-id="5786a-110">On the **File** menu, point to **New Solution**.</span></span>

2. <span data-ttu-id="5786a-111">Dans la boîte de dialogue Nouveau projet, il existe 2 différents modèles d’Application de Console.</span><span class="sxs-lookup"><span data-stu-id="5786a-111">In the New Project dialog, there are 2 different templates for Console Application.</span></span>  <span data-ttu-id="5786a-112">Il y a un sous autre -> .NET qui cible le .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="5786a-112">There is one under Other -> .NET which targets the .NET Framework.</span></span>  <span data-ttu-id="5786a-113">L’autre modèle est sous .NET Core -> application qui cible .NET Core.</span><span class="sxs-lookup"><span data-stu-id="5786a-113">The other template is under .NET Core -> App which targets .NET Core.</span></span>  <span data-ttu-id="5786a-114">Un modèle doit fonctionner pour les besoins de cet article.</span><span class="sxs-lookup"><span data-stu-id="5786a-114">Either template should work for the purpose of this article.</span></span>

3. <span data-ttu-id="5786a-115">Sous l’application de console, modifiez C# à F# si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="5786a-115">Under console app, change C# to F# if needed.</span></span>  <span data-ttu-id="5786a-116">Choisissez le **suivant** bouton Déplacer vers l’avant !</span><span class="sxs-lookup"><span data-stu-id="5786a-116">Choose the **Next** button to move forward!</span></span>  

4. <span data-ttu-id="5786a-117">Donnez un nom à votre projet, puis choisissez les options souhaitées pour l’application.</span><span class="sxs-lookup"><span data-stu-id="5786a-117">Give your project a name, and choose the options you want for the app.</span></span>  <span data-ttu-id="5786a-118">Notez, le volet de visualisation vers le côté de l’écran qui affiche la structure de répertoires qui est créée en fonction des options sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="5786a-118">Notice, the preview pane to the side of the screen that will show the directory structure that will be created based on the options selected.</span></span>  

5. <span data-ttu-id="5786a-119">Cliquez sur **Créer**.</span><span class="sxs-lookup"><span data-stu-id="5786a-119">Click **Create**.</span></span>  <span data-ttu-id="5786a-120">Vous devriez maintenant voir un F# projet dans l’Explorateur de solutions.</span><span class="sxs-lookup"><span data-stu-id="5786a-120">You should now see an F# project in the Solution Explorer.</span></span>

## <a name="writing-your-code"></a><span data-ttu-id="5786a-121">Écrivez votre code</span><span class="sxs-lookup"><span data-stu-id="5786a-121">Writing your code</span></span>

<span data-ttu-id="5786a-122">Commençons par écrire du code tout d’abord.</span><span class="sxs-lookup"><span data-stu-id="5786a-122">Let's get started by writing some code first.</span></span>  <span data-ttu-id="5786a-123">Assurez-vous que le `Program.fs` fichier est ouvert, puis remplacez son contenu par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="5786a-123">Make sure that the `Program.fs` file is open, and then replace its contents with the following:</span></span>

[!code-fsharp[HelloSquare](../../../samples/snippets/fsharp/getting-started/hello-square.fs)]

<span data-ttu-id="5786a-124">Dans l’exemple de code précédent, une fonction `square` a été trouvé qui accepte une entrée nommée `x` et le multiplie par lui-même.</span><span class="sxs-lookup"><span data-stu-id="5786a-124">In the previous code sample, a function `square` has been defined which takes an input named `x` and multiplies it by itself.</span></span>  <span data-ttu-id="5786a-125">Étant donné que F# utilise [l’inférence de Type](../language-reference/type-inference.md), le type de `x` n’a pas besoin d’être spécifié.</span><span class="sxs-lookup"><span data-stu-id="5786a-125">Because F# uses [Type Inference](../language-reference/type-inference.md), the type of `x` doesn't need to be specified.</span></span>  <span data-ttu-id="5786a-126">Le F# compilateur comprend les types où la multiplication est valide et affectera un type à `x` selon la façon dont `square` est appelée.</span><span class="sxs-lookup"><span data-stu-id="5786a-126">The F# compiler understands the types where multiplication is valid, and will assign a type to `x` based on how `square` is called.</span></span>  <span data-ttu-id="5786a-127">Si vous pointez sur `square`, vous devez voir les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="5786a-127">If you hover over `square`, you should see the following:</span></span>

```
val square: x:int -> int
```

<span data-ttu-id="5786a-128">C’est ce qui est appelé signature de type de la fonction.</span><span class="sxs-lookup"><span data-stu-id="5786a-128">This is what is known as the function's type signature.</span></span>  <span data-ttu-id="5786a-129">Il peut être lu comme suit : « Carré est une fonction qui prend un entier nommé x et produit un entier ».</span><span class="sxs-lookup"><span data-stu-id="5786a-129">It can be read like this: "Square is a function which takes an integer named x and produces an integer".</span></span>  <span data-ttu-id="5786a-130">Notez que le compilateur retournait `square` le `int` type pour le moment - il s’agit, car la multiplication n’est pas générique sur *tous les* types, mais plutôt générique entre un ensemble fermé de types.</span><span class="sxs-lookup"><span data-stu-id="5786a-130">Note that the compiler gave `square` the `int` type for now - this is because multiplication is not generic across *all* types, but rather is generic across a closed set of types.</span></span>  <span data-ttu-id="5786a-131">Le F# compilateur prélevé `int` sur ce point, mais il ajuste la signature de type si vous appelez `square` avec un autre type d’entrée, comme un `float`.</span><span class="sxs-lookup"><span data-stu-id="5786a-131">The F# compiler picked `int` at this point, but it will adjust the type signature if you call `square` with a different input type, such as a `float`.</span></span>

<span data-ttu-id="5786a-132">Une autre fonction, `main`, est défini, ce qui est décoré avec le `EntryPoint` attribut pour indiquer la F# compilateur que l’exécution du programme doit commencer.</span><span class="sxs-lookup"><span data-stu-id="5786a-132">Another function, `main`, is defined, which is decorated with the `EntryPoint` attribute to tell the F# compiler that program execution should start there.</span></span>  <span data-ttu-id="5786a-133">Il suit la même convention que les autres [les langages de programmation de style C](https://en.wikipedia.org/wiki/Entry_point#C_and_C.2B.2B), où les arguments de ligne de commande peuvent être passés à cette fonction, et un code entier est retourné (généralement `0`).</span><span class="sxs-lookup"><span data-stu-id="5786a-133">It follows the same convention as other [C-style programming languages](https://en.wikipedia.org/wiki/Entry_point#C_and_C.2B.2B), where command-line arguments can be passed to this function, and an integer code is returned (typically `0`).</span></span>

<span data-ttu-id="5786a-134">Il se trouve dans cette fonction que nous appelons le `square` fonction avec un argument de `12`.</span><span class="sxs-lookup"><span data-stu-id="5786a-134">It is in this function that we call the `square` function with an argument of `12`.</span></span>  <span data-ttu-id="5786a-135">Le F# compilateur puis assigne le type de `square` être `int -> int` (autrement dit, une fonction qui prend un `int` et produit un `int`).</span><span class="sxs-lookup"><span data-stu-id="5786a-135">The F# compiler then assigns the type of `square` to be `int -> int` (that is, a function which takes an `int` and produces an `int`).</span></span>  <span data-ttu-id="5786a-136">L’appel à `printfn` est une fonction d’impression mis en forme qui utilise une chaîne de format, similaire aux langages de programmation de style C, les paramètres qui correspondent à celles spécifiées dans la chaîne de format et imprime ensuite le résultat et une nouvelle ligne.</span><span class="sxs-lookup"><span data-stu-id="5786a-136">The call to `printfn` is a formatted printing function which uses a format string, similar to C-style programming languages, parameters which correspond to those specified in the format string, and then prints the result and a new line.</span></span>

## <a name="running-your-code"></a><span data-ttu-id="5786a-137">Exécution de votre code</span><span class="sxs-lookup"><span data-stu-id="5786a-137">Running your code</span></span>

<span data-ttu-id="5786a-138">Vous pouvez exécuter le code et afficher les résultats en cliquant sur **exécuter** dans le menu de niveau supérieur, puis **démarrer sans débogage**.</span><span class="sxs-lookup"><span data-stu-id="5786a-138">You can run the code and see results by clicking on **Run** from the top level menu and then **Start Without Debugging**.</span></span>  <span data-ttu-id="5786a-139">Cela exécutera le programme sans débogage et vous permet de voir les résultats.</span><span class="sxs-lookup"><span data-stu-id="5786a-139">This will run the program without debugging and allows you to see the results.</span></span>

<span data-ttu-id="5786a-140">Vous devez maintenant voir ce qui suit imprimé dans la fenêtre de console Visual Studio pour Mac est apparue :</span><span class="sxs-lookup"><span data-stu-id="5786a-140">You should now see the following printed to the console window that Visual Studio for Mac popped up:</span></span>

```
12 squared is 144!
```

<span data-ttu-id="5786a-141">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="5786a-141">Congratulations!</span></span>  <span data-ttu-id="5786a-142">Vous avez créé votre premier F# projet dans Visual Studio pour Mac, écrit un F# fonction Imprimer les résultats de l’appel de fonction, puis exécutez le projet pour voir des résultats.</span><span class="sxs-lookup"><span data-stu-id="5786a-142">You've created your first F# project in Visual Studio for Mac, written an F# function printed the results of calling that function, and run the project to see some results.</span></span>

## <a name="using-f-interactive"></a><span data-ttu-id="5786a-143">À l’aide de F# Interactive</span><span class="sxs-lookup"><span data-stu-id="5786a-143">Using F# Interactive</span></span>

<span data-ttu-id="5786a-144">Une des meilleures fonctionnalités de l’élément visuel F# outils dans Visual Studio pour Mac est la F# fenêtre Interactive.</span><span class="sxs-lookup"><span data-stu-id="5786a-144">One of the best features of the Visual F# tooling in Visual Studio for Mac is the F# Interactive Window.</span></span>  <span data-ttu-id="5786a-145">Il vous permet d’envoyer le code sur à un processus dans lequel vous pouvez appeler ce code et afficher le résultat de manière interactive.</span><span class="sxs-lookup"><span data-stu-id="5786a-145">It allows you to send code over to a process where you can call that code and see the result interactively.</span></span>

<span data-ttu-id="5786a-146">Pour commencer à l’utiliser, mettez en surbrillance le `square` fonction définie dans votre code.</span><span class="sxs-lookup"><span data-stu-id="5786a-146">To begin using it, highlight the `square` function defined in your code.</span></span>  <span data-ttu-id="5786a-147">Ensuite, cliquez sur **modifier** dans le menu de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="5786a-147">Next, click on **Edit** from the top level menu.</span></span>  <span data-ttu-id="5786a-148">Sélectionnez ensuite **envoyer la sélection à F# Interactive**.</span><span class="sxs-lookup"><span data-stu-id="5786a-148">Next select **Send selection to F# Interactive**.</span></span>  <span data-ttu-id="5786a-149">Cela exécute le code dans le F# fenêtre Interactive.</span><span class="sxs-lookup"><span data-stu-id="5786a-149">This executes the code in the F# Interactive Window.</span></span>  <span data-ttu-id="5786a-150">Ou bien, vous pouvez cliquez avec le bouton droit sur la sélection et choisissez **envoyer la sélection à F# Interactive**.</span><span class="sxs-lookup"><span data-stu-id="5786a-150">Alternatively, you can right click on the selection and choose **Send selection to F# Interactive**.</span></span>  <span data-ttu-id="5786a-151">Vous devez voir le F# fenêtre Interactive s’affichent par le code suivant dans celui-ci :</span><span class="sxs-lookup"><span data-stu-id="5786a-151">You should see the F# Interactive Window appear with the following in it:</span></span>

```
>

val square : x:int -> int

>
```

<span data-ttu-id="5786a-152">Cela montre la même signature de fonction pour le `square` (fonction), vous l’avez vu précédemment lorsque vous pointez sur la fonction.</span><span class="sxs-lookup"><span data-stu-id="5786a-152">This shows the same function signature for the `square` function, which you saw earlier when you hovered over the function.</span></span>  <span data-ttu-id="5786a-153">Étant donné que `square` est maintenant définie dans le F# processus interactif, vous pouvez l’appeler avec des valeurs différentes :</span><span class="sxs-lookup"><span data-stu-id="5786a-153">Because `square` is now defined in the F# Interactive process, you can call it with different values:</span></span>

```
> square 12;;
val it : int = 144
>square 13;;
val it : int = 169
```

<span data-ttu-id="5786a-154">Cela exécute la fonction, lie le résultat vers un nouveau nom `it`et affiche le type et la valeur de `it`.</span><span class="sxs-lookup"><span data-stu-id="5786a-154">This executes the function, binds the result to a new name `it`, and displays the type and value of `it`.</span></span>  <span data-ttu-id="5786a-155">Notez que vous devez terminer chaque ligne avec `;;`.</span><span class="sxs-lookup"><span data-stu-id="5786a-155">Note that you must terminate each line with `;;`.</span></span>  <span data-ttu-id="5786a-156">Voici comment F# Interactive sait quand votre appel de fonction est terminée.</span><span class="sxs-lookup"><span data-stu-id="5786a-156">This is how F# Interactive knows when your function call is finished.</span></span>  <span data-ttu-id="5786a-157">Vous pouvez également définir des nouvelles fonctions dans F# Interactive :</span><span class="sxs-lookup"><span data-stu-id="5786a-157">You can also define new functions in F# Interactive:</span></span>

```
> let isOdd x = x % 2 <> 0;;

val isOdd : x:int -> bool

> isOdd 12;;
val it : bool = false
```

<span data-ttu-id="5786a-158">La méthode ci-dessus définit une nouvelle fonction, `isOdd`, qui accepte un `int` et vérifie s’il est impair !</span><span class="sxs-lookup"><span data-stu-id="5786a-158">The above defines a new function, `isOdd`, which takes an `int` and checks to see if it's odd!</span></span>  <span data-ttu-id="5786a-159">Vous pouvez appeler cette fonction pour afficher sa valeur de retour avec des entrées différentes.</span><span class="sxs-lookup"><span data-stu-id="5786a-159">You can call this function to see what it returns with different inputs.</span></span>  <span data-ttu-id="5786a-160">Vous pouvez appeler des fonctions dans les appels de fonction :</span><span class="sxs-lookup"><span data-stu-id="5786a-160">You can call functions within function calls:</span></span>

```
> isOdd (square 15);;
val it : bool = true
```

<span data-ttu-id="5786a-161">Vous pouvez également utiliser le [opérateur de canal-forward](../language-reference/symbol-and-operator-reference/index.md) au pipeline de la valeur dans les deux fonctions :</span><span class="sxs-lookup"><span data-stu-id="5786a-161">You can also use the [pipe-forward operator](../language-reference/symbol-and-operator-reference/index.md) to pipeline the value into the two functions:</span></span>

```
> 15 |> square |> isOdd;;
val it : bool = true
```

<span data-ttu-id="5786a-162">L’opérateur de redirection de canal et bien plus encore, sont traités dans les didacticiels suivants.</span><span class="sxs-lookup"><span data-stu-id="5786a-162">The pipe-forward operator, and more, are covered in later tutorials.</span></span>

<span data-ttu-id="5786a-163">Il s’agit uniquement d’un aperçu dans ce que vous pouvez faire avec F# Interactive.</span><span class="sxs-lookup"><span data-stu-id="5786a-163">This is only a glimpse into what you can do with F# Interactive.</span></span>  <span data-ttu-id="5786a-164">Pour plus d’informations, consultez [programmation Interactive avec F# ](../tutorials/fsharp-interactive/index.md).</span><span class="sxs-lookup"><span data-stu-id="5786a-164">To learn more, check out [Interactive Programming with F#](../tutorials/fsharp-interactive/index.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="5786a-165">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="5786a-165">Next steps</span></span>

<span data-ttu-id="5786a-166">Si vous n’avez pas déjà, consultez le [visite guidée de F# ](../tour.md), qui aborde certaines des principales fonctionnalités de la F# langage.</span><span class="sxs-lookup"><span data-stu-id="5786a-166">If you haven't already, check out the [Tour of F#](../tour.md), which covers some of the core features of the F# language.</span></span>  <span data-ttu-id="5786a-167">Il vous donnera une vue d’ensemble de certaines des fonctionnalités de F#et fournissent des exemples de code suffisamment que vous pouvez copier dans Visual Studio pour Mac et d’exécution.</span><span class="sxs-lookup"><span data-stu-id="5786a-167">It will give you an overview of some of the capabilities of F#, and provide ample code samples that you can copy into Visual Studio for Mac and run.</span></span>  <span data-ttu-id="5786a-168">Il existe également des ressources exceptionnelles externes, vous pouvez utiliser, présentée dans le [ F# Guide](../index.md).</span><span class="sxs-lookup"><span data-stu-id="5786a-168">There are also some great external resources you can use, showcased in the [F# Guide](../index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5786a-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5786a-169">See also</span></span>

- [<span data-ttu-id="5786a-170">Visual F#</span><span class="sxs-lookup"><span data-stu-id="5786a-170">Visual F#</span></span>](../index.md)
- [<span data-ttu-id="5786a-171">Présentation de F#</span><span class="sxs-lookup"><span data-stu-id="5786a-171">Tour of F#</span></span>](../tour.md)
- [<span data-ttu-id="5786a-172">F#référence du langage</span><span class="sxs-lookup"><span data-stu-id="5786a-172">F# language reference</span></span>](../language-reference/index.md)
- [<span data-ttu-id="5786a-173">Inférence de type</span><span class="sxs-lookup"><span data-stu-id="5786a-173">Type inference</span></span>](../language-reference/type-inference.md)
- [<span data-ttu-id="5786a-174">Référence des symboles et d’opérateur</span><span class="sxs-lookup"><span data-stu-id="5786a-174">Symbol and operator reference</span></span>](../language-reference/symbol-and-operator-reference/index.md)
