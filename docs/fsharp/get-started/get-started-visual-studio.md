---
title: Prise en main F# dans Visual Studio
description: Découvrez comment utiliser F# avec Visual Studio.
ms.date: 07/03/2018
ms.openlocfilehash: 020e5d32b3aa5d5a2195c19d70d8fe684fbd56ef
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59331908"
---
# <a name="get-started-with-f-in-visual-studio"></a><span data-ttu-id="fe5f0-103">Prise en main F# dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fe5f0-103">Get started with F# in Visual Studio</span></span>

<span data-ttu-id="fe5f0-104">F#et le visuel F# outils sont pris en charge dans l’IDE Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-104">F# and the Visual F# tooling are supported in the Visual Studio IDE.</span></span>

<span data-ttu-id="fe5f0-105">Pour commencer, assurez-vous d’avoir [Visual Studio installé avec F# ](install-fsharp.md#install-f-with-visual-studio).</span><span class="sxs-lookup"><span data-stu-id="fe5f0-105">To begin, ensure that you have [Visual Studio installed with F#](install-fsharp.md#install-f-with-visual-studio).</span></span>

## <a name="creating-a-console-application"></a><span data-ttu-id="fe5f0-106">Création d’une application de console</span><span class="sxs-lookup"><span data-stu-id="fe5f0-106">Creating a console application</span></span>

<span data-ttu-id="fe5f0-107">Un des projets plus simples dans Visual Studio est l’Application de Console.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-107">One of the most basic projects in Visual Studio is the Console Application.</span></span>  <span data-ttu-id="fe5f0-108">Voici comment faire.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-108">Here's how to do it.</span></span>  <span data-ttu-id="fe5f0-109">Une fois que Visual Studio est ouvert :</span><span class="sxs-lookup"><span data-stu-id="fe5f0-109">Once Visual Studio is open:</span></span>

1. <span data-ttu-id="fe5f0-110">Sur le **fichier** menu, pointez sur **New**, puis choisissez **projet**.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-110">On the **File** menu, point to **New**, and then choose **Project**.</span></span>

2. <span data-ttu-id="fe5f0-111">Dans la nouvelle boîte de dialogue projet, sous **modèles**, vous devez voir **Visual F#** .</span><span class="sxs-lookup"><span data-stu-id="fe5f0-111">In the New Project dialog, under **Templates**, you should see **Visual F#**.</span></span>  <span data-ttu-id="fe5f0-112">Choisissez cette option pour afficher le F# modèles.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-112">Choose this to show the F# templates.</span></span>

3. <span data-ttu-id="fe5f0-113">Sélectionnez **.NET Core application Console** ou **application Console**.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-113">Select either **.NET Core Console app** or **Console app**.</span></span>

3. <span data-ttu-id="fe5f0-114">Choisissez le **OK** bouton permettant de créer le F# projet !</span><span class="sxs-lookup"><span data-stu-id="fe5f0-114">Choose the **Okay** button to create the F# project!</span></span>  <span data-ttu-id="fe5f0-115">Vous devriez maintenant voir un F# projet dans l’Explorateur de solutions.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-115">You should now see an F# project in the Solution Explorer.</span></span>

## <a name="writing-your-code"></a><span data-ttu-id="fe5f0-116">Écrivez votre code</span><span class="sxs-lookup"><span data-stu-id="fe5f0-116">Writing your code</span></span>

<span data-ttu-id="fe5f0-117">Commençons par écrire du code tout d’abord.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-117">Let's get started by writing some code first.</span></span>  <span data-ttu-id="fe5f0-118">Assurez-vous que le `Program.fs` fichier est ouvert, puis remplacez son contenu par le code suivant :</span><span class="sxs-lookup"><span data-stu-id="fe5f0-118">Make sure that the `Program.fs` file is open, and then replace its contents with the following:</span></span>

[!code-fsharp[HelloSquare](../../../samples/snippets/fsharp/getting-started/hello-square.fs)]

<span data-ttu-id="fe5f0-119">Dans l’exemple de code précédent, une fonction `square` a été trouvé qui accepte une entrée nommée `x` et le multiplie par lui-même.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-119">In the previous code sample, a function `square` has been defined which takes an input named `x` and multiplies it by itself.</span></span>  <span data-ttu-id="fe5f0-120">Étant donné que F# utilise [l’inférence de Type](../language-reference/type-inference.md), le type de `x` n’a pas besoin d’être spécifié.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-120">Because F# uses [Type Inference](../language-reference/type-inference.md), the type of `x` doesn't need to be specified.</span></span>  <span data-ttu-id="fe5f0-121">Le F# compilateur comprend les types où la multiplication est valide et affectera un type à `x` selon la façon dont `square` est appelée.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-121">The F# compiler understands the types where multiplication is valid, and will assign a type to `x` based on how `square` is called.</span></span>  <span data-ttu-id="fe5f0-122">Si vous pointez sur `square`, vous devez voir les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="fe5f0-122">If you hover over `square`, you should see the following:</span></span>

```
val square: x:int -> int
```

<span data-ttu-id="fe5f0-123">C’est ce qui est appelé signature de type de la fonction.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-123">This is what is known as the function's type signature.</span></span>  <span data-ttu-id="fe5f0-124">Il peut être lu comme suit : « Carré est une fonction qui prend un entier nommé x et produit un entier ».</span><span class="sxs-lookup"><span data-stu-id="fe5f0-124">It can be read like this: "Square is a function which takes an integer named x and produces an integer".</span></span>  <span data-ttu-id="fe5f0-125">Notez que le compilateur retournait `square` le `int` type pour le moment - il s’agit, car la multiplication n’est pas générique sur *tous les* types, mais plutôt générique entre un ensemble fermé de types.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-125">Note that the compiler gave `square` the `int` type for now - this is because multiplication is not generic across *all* types, but rather is generic across a closed set of types.</span></span>  <span data-ttu-id="fe5f0-126">Le F# compilateur prélevé `int` sur ce point, mais il ajuste la signature de type si vous appelez `square` avec un autre type d’entrée, comme un `float`.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-126">The F# compiler picked `int` at this point, but it will adjust the type signature if you call `square` with a different input type, such as a `float`.</span></span>

<span data-ttu-id="fe5f0-127">Une autre fonction, `main`, est défini, ce qui est décoré avec le `EntryPoint` attribut pour indiquer la F# compilateur que l’exécution du programme doit commencer.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-127">Another function, `main`, is defined, which is decorated with the `EntryPoint` attribute to tell the F# compiler that program execution should start there.</span></span>  <span data-ttu-id="fe5f0-128">Il suit la même convention que les autres [les langages de programmation de style C](https://en.wikipedia.org/wiki/Entry_point#C_and_C.2B.2B), où les arguments de ligne de commande peuvent être passés à cette fonction, et un code entier est retourné (généralement `0`).</span><span class="sxs-lookup"><span data-stu-id="fe5f0-128">It follows the same convention as other [C-style programming languages](https://en.wikipedia.org/wiki/Entry_point#C_and_C.2B.2B), where command-line arguments can be passed to this function, and an integer code is returned (typically `0`).</span></span>

<span data-ttu-id="fe5f0-129">Il se trouve dans cette fonction que nous appelons le `square` fonction avec un argument de `12`.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-129">It is in this function that we call the `square` function with an argument of `12`.</span></span>  <span data-ttu-id="fe5f0-130">Le F# compilateur puis assigne le type de `square` être `int -> int` (autrement dit, une fonction qui prend un `int` et produit un `int`).</span><span class="sxs-lookup"><span data-stu-id="fe5f0-130">The F# compiler then assigns the type of `square` to be `int -> int` (that is, a function which takes an `int` and produces an `int`).</span></span>  <span data-ttu-id="fe5f0-131">L’appel à `printfn` est une fonction d’impression mis en forme qui utilise une chaîne de format, similaire aux langages de programmation de style C, les paramètres qui correspondent à celles spécifiées dans la chaîne de format et imprime ensuite le résultat et une nouvelle ligne.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-131">The call to `printfn` is a formatted printing function which uses a format string, similar to C-style programming languages, parameters which correspond to those specified in the format string, and then prints the result and a new line.</span></span>

## <a name="running-your-code"></a><span data-ttu-id="fe5f0-132">Exécution de votre code</span><span class="sxs-lookup"><span data-stu-id="fe5f0-132">Running your code</span></span>

<span data-ttu-id="fe5f0-133">Vous pouvez exécuter le code et afficher les résultats en appuyant sur **Ctrl**+**F5**.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-133">You can run the code and see results by pressing **Ctrl**+**F5**.</span></span>  <span data-ttu-id="fe5f0-134">Cela exécute le programme sans débogage et vous permet de voir les résultats.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-134">This runs the program without debugging and allows you to see the results.</span></span>  <span data-ttu-id="fe5f0-135">Vous pouvez également choisir le **déboguer** menu de niveau supérieur d’élément dans Visual Studio et choisissez **démarrer sans débogage**.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-135">Alternatively, you can choose the **Debug** top-level menu item in Visual Studio and choose **Start Without Debugging**.</span></span>

<span data-ttu-id="fe5f0-136">Vous devez maintenant voir ce qui suit imprimé dans la fenêtre de console Visual Studio de s’afficher :</span><span class="sxs-lookup"><span data-stu-id="fe5f0-136">You should now see the following printed to the console window that Visual Studio popped up:</span></span>

```
12 squared is 144!
```

<span data-ttu-id="fe5f0-137">Félicitations !</span><span class="sxs-lookup"><span data-stu-id="fe5f0-137">Congratulations!</span></span>  <span data-ttu-id="fe5f0-138">Vous avez créé votre premier F# projet dans Visual Studio, écrit un F# fonction Imprimer les résultats de l’appel de fonction, puis exécutez le projet pour voir des résultats.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-138">You've created your first F# project in Visual Studio, written an F# function printed the results of calling that function, and run the project to see some results.</span></span>

## <a name="next-steps"></a><span data-ttu-id="fe5f0-139">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="fe5f0-139">Next steps</span></span>

<span data-ttu-id="fe5f0-140">Si vous n’avez pas déjà, consultez le [visite guidée de F# ](../tour.md), qui aborde certaines des principales fonctionnalités de la F# langage.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-140">If you haven't already, check out the [Tour of F#](../tour.md), which covers some of the core features of the F# language.</span></span>  <span data-ttu-id="fe5f0-141">Il vous donnera une vue d’ensemble de certaines des fonctionnalités de F#et fournissent des exemples de code suffisamment que vous pouvez copier dans Visual Studio et exécuter.</span><span class="sxs-lookup"><span data-stu-id="fe5f0-141">It will give you an overview of some of the capabilities of F#, and provide ample code samples that you can copy into Visual Studio and run.</span></span>  <span data-ttu-id="fe5f0-142">Il existe également des ressources exceptionnelles externes, vous pouvez utiliser, présentée dans le [ F# Guide](../index.md).</span><span class="sxs-lookup"><span data-stu-id="fe5f0-142">There are also some great external resources you can use, showcased in the [F# Guide](../index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="fe5f0-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe5f0-143">See also</span></span>

- [<span data-ttu-id="fe5f0-144">Visite guidée de F#</span><span class="sxs-lookup"><span data-stu-id="fe5f0-144">Tour of F#</span></span>](../tour.md)
- [<span data-ttu-id="fe5f0-145">F#référence du langage</span><span class="sxs-lookup"><span data-stu-id="fe5f0-145">F# language reference</span></span>](../language-reference/index.md)
- [<span data-ttu-id="fe5f0-146">Inférence de type</span><span class="sxs-lookup"><span data-stu-id="fe5f0-146">Type inference</span></span>](../language-reference/type-inference.md)
- [<span data-ttu-id="fe5f0-147">Référence des symboles et d’opérateur</span><span class="sxs-lookup"><span data-stu-id="fe5f0-147">Symbol and operator reference</span></span>](../language-reference/symbol-and-operator-reference/index.md)
