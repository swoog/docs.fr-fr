---
title: Paramètres et arguments (F#)
description: 'En savoir plus sur F # prise en charge linguistique pour la définition de paramètres et en transmettant des arguments aux fonctions, méthodes et propriétés.'
ms.date: 05/16/2016
ms.openlocfilehash: 9744339110314e4e6b3c3cf8d49b1c988bc25e3c
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43471979"
---
# <a name="parameters-and-arguments"></a><span data-ttu-id="3833c-103">Paramètres et arguments</span><span class="sxs-lookup"><span data-stu-id="3833c-103">Parameters and Arguments</span></span>

<span data-ttu-id="3833c-104">Cette rubrique décrit la prise en charge de langage de définition de paramètres et en transmettant des arguments aux fonctions, méthodes et propriétés.</span><span class="sxs-lookup"><span data-stu-id="3833c-104">This topic describes language support for defining parameters and passing arguments to functions, methods, and properties.</span></span> <span data-ttu-id="3833c-105">Il inclut des informations sur le passage par référence et comment définir et utiliser des méthodes qui peuvent prendre un nombre variable d’arguments.</span><span class="sxs-lookup"><span data-stu-id="3833c-105">It includes information about how to pass by reference, and how to define and use methods that can take a variable number of arguments.</span></span>


## <a name="parameters-and-arguments"></a><span data-ttu-id="3833c-106">Paramètres et arguments</span><span class="sxs-lookup"><span data-stu-id="3833c-106">Parameters and Arguments</span></span>
<span data-ttu-id="3833c-107">Le terme *paramètre* est utilisé pour décrire les noms des valeurs qui sont censées être fournies.</span><span class="sxs-lookup"><span data-stu-id="3833c-107">The term *parameter* is used to describe the names for values that are expected to be supplied.</span></span> <span data-ttu-id="3833c-108">Le terme *argument* est utilisé pour les valeurs fournies pour chaque paramètre.</span><span class="sxs-lookup"><span data-stu-id="3833c-108">The term *argument* is used for the values provided for each parameter.</span></span>

<span data-ttu-id="3833c-109">Paramètres peuvent être spécifiés sous forme de tuple ou curryfiés ou dans une combinaison des deux.</span><span class="sxs-lookup"><span data-stu-id="3833c-109">Parameters can be specified in tuple or curried form, or in some combination of the two.</span></span> <span data-ttu-id="3833c-110">Vous pouvez passer des arguments à l’aide d’un nom de paramètre explicite.</span><span class="sxs-lookup"><span data-stu-id="3833c-110">You can pass arguments by using an explicit parameter name.</span></span> <span data-ttu-id="3833c-111">Les paramètres des méthodes peuvent être spécifiés comme étant facultatifs et une valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="3833c-111">Parameters of methods can be specified as optional and given a default value.</span></span>


## <a name="parameter-patterns"></a><span data-ttu-id="3833c-112">Modèles de paramètre</span><span class="sxs-lookup"><span data-stu-id="3833c-112">Parameter Patterns</span></span>
<span data-ttu-id="3833c-113">En règle générale, les paramètres fournis à des fonctions et méthodes sont des modèles en les séparant par des espaces.</span><span class="sxs-lookup"><span data-stu-id="3833c-113">Parameters supplied to functions and methods are, in general, patterns separated by spaces.</span></span> <span data-ttu-id="3833c-114">Cela signifie que, en principe, les modèles décrits dans [Expressions de correspondance](match-expressions.md) peut être utilisé dans une liste de paramètres pour une fonction ou un membre.</span><span class="sxs-lookup"><span data-stu-id="3833c-114">This means that, in principle, any of the patterns described in [Match Expressions](match-expressions.md) can be used in a parameter list for a function or member.</span></span>

<span data-ttu-id="3833c-115">Méthodes utilisent généralement la forme de tuple de passage d’arguments.</span><span class="sxs-lookup"><span data-stu-id="3833c-115">Methods usually use the tuple form of passing arguments.</span></span> <span data-ttu-id="3833c-116">Cela permet d’obtenir un résultat plus clair à partir de la perspective d’autres langages .NET, car la forme de tuple correspond à la façon d’arguments sont passés dans les méthodes .NET.</span><span class="sxs-lookup"><span data-stu-id="3833c-116">This achieves a clearer result from the perspective of other .NET languages because the tuple form matches the way arguments are passed in .NET methods.</span></span>

<span data-ttu-id="3833c-117">La forme curryfiée est souvent utilisée avec des fonctions créées à l’aide de `let` liaisons.</span><span class="sxs-lookup"><span data-stu-id="3833c-117">The curried form is most often used with functions created by using `let` bindings.</span></span>

<span data-ttu-id="3833c-118">Le pseudo-code suivant montre des exemples de tuple et d’arguments curryfiés.</span><span class="sxs-lookup"><span data-stu-id="3833c-118">The following pseudocode shows examples of tuple and curried arguments.</span></span>

```fsharp
// Tuple form.
member this.SomeMethod(param1, param2) = ...
// Curried form.
let function1 param1 param2 = ...
```

<span data-ttu-id="3833c-119">Combiner les formes sont possibles lorsque certains arguments sont dans des tuples et d’autres pas.</span><span class="sxs-lookup"><span data-stu-id="3833c-119">Combined forms are possible when some arguments are in tuples and some are not.</span></span>

```fsharp
let function2 param1 (param2a, param2b) param3 = ...
```

<span data-ttu-id="3833c-120">Autres modèles peuvent également servir dans les listes de paramètres, mais si le modèle de paramètre ne correspond pas à toutes les entrées possibles, il peut y avoir une correspondance incomplète en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="3833c-120">Other patterns can also be used in parameter lists, but if the parameter pattern does not match all possible inputs, there might be an incomplete match at run time.</span></span> <span data-ttu-id="3833c-121">L’exception `MatchFailureException` est générée lorsque la valeur d’un argument ne correspond pas aux modèles spécifiés dans la liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="3833c-121">The exception `MatchFailureException` is generated when the value of an argument does not match the patterns specified in the parameter list.</span></span> <span data-ttu-id="3833c-122">Le compilateur émet un avertissement lorsqu’un modèle de paramètre accepte des correspondances incomplètes.</span><span class="sxs-lookup"><span data-stu-id="3833c-122">The compiler issues a warning when a parameter pattern allows for incomplete matches.</span></span> <span data-ttu-id="3833c-123">Au moins un autre modèle est souvent utile pour les listes de paramètres, et c’est le modèle de caractère générique.</span><span class="sxs-lookup"><span data-stu-id="3833c-123">At least one other pattern is commonly useful for parameter lists, and that is the wildcard pattern.</span></span> <span data-ttu-id="3833c-124">Vous utilisez le modèle de caractère générique dans une liste de paramètres lorsque vous souhaitez simplement ignorer tous les arguments sont fournis.</span><span class="sxs-lookup"><span data-stu-id="3833c-124">You use the wildcard pattern in a parameter list when you simply want to ignore any arguments that are supplied.</span></span> <span data-ttu-id="3833c-125">Le code suivant illustre l’utilisation du modèle de caractère générique dans une liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="3833c-125">The following code illustrates the use of the wildcard pattern in an argument list.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3801.fs)]

<span data-ttu-id="3833c-126">Le modèle de caractère générique peut être utile chaque fois que vous n’avez pas besoin des arguments transmis, comme illustré dans le point d’entrée principal pour un programme, lorsque vous n’êtes pas intéressé par les arguments de ligne de commande qui sont normalement fournis en tant que tableau de chaînes, comme dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="3833c-126">The wildcard pattern can be useful whenever you do not need the arguments passed in, such as in the main entry point to a program, when you are not interested in the command-line arguments that are normally supplied as a string array, as in the following code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3802.fs)]

<span data-ttu-id="3833c-127">Autres modèles qui sont parfois utilisés dans les arguments sont les `as` modèle et les modèles d’identificateur associés aux unions discriminées et modèles actifs.</span><span class="sxs-lookup"><span data-stu-id="3833c-127">Other patterns that are sometimes used in arguments are the `as` pattern, and identifier patterns associated with discriminated unions and active patterns.</span></span> <span data-ttu-id="3833c-128">Vous pouvez utiliser le modèle d’union discriminée cas unique comme suit.</span><span class="sxs-lookup"><span data-stu-id="3833c-128">You can use the single-case discriminated union pattern as follows.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3803.fs)]

<span data-ttu-id="3833c-129">La sortie est la suivante.</span><span class="sxs-lookup"><span data-stu-id="3833c-129">The output is as follows.</span></span>

```
Data begins at 0 and ends at 4 in string Et tu, Brute?
Et tu
```

<span data-ttu-id="3833c-130">Modèles actifs peuvent être utiles en tant que paramètres, par exemple, lors de la transformation d’un argument dans un format de votre choix, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="3833c-130">Active patterns can be useful as parameters, for example, when transforming an argument into a desired format, as in the following example:</span></span>

```fsharp
type Point = { x : float; y : float }

let (| Polar |) { x = x; y = y} =
    ( sqrt (x*x + y*y), System.Math.Atan (y/ x) )

let radius (Polar(r, _)) = r
let angle (Polar(_, theta)) = theta
```

<span data-ttu-id="3833c-131">Vous pouvez utiliser la `as` modèle pour stocker une valeur mise en correspondance comme une valeur locale, comme indiqué dans la ligne de code suivante.</span><span class="sxs-lookup"><span data-stu-id="3833c-131">You can use the `as` pattern to store a matched value as a local value, as is shown in the following line of code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3805.fs)]

<span data-ttu-id="3833c-132">Un autre modèle qui est parfois utilisé est une fonction qui laisse le dernier argument sans nom en fournissant, en tant que le corps de la fonction, une expression lambda qui exécute immédiatement une correspondance de modèle sur l’argument implicite.</span><span class="sxs-lookup"><span data-stu-id="3833c-132">Another pattern that is used occasionally is a function that leaves the last argument unnamed by providing, as the body of the function, a lambda expression that immediately performs a pattern match on the implicit argument.</span></span> <span data-ttu-id="3833c-133">Un exemple de ceci est la ligne de code suivante.</span><span class="sxs-lookup"><span data-stu-id="3833c-133">An example of this is the following line of code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3804.fs)]

<span data-ttu-id="3833c-134">Ce code définit une fonction qui prend une liste générique et retourne `true` si la liste est vide, et `false` dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="3833c-134">This code defines a function that takes a generic list and returns `true` if the list is empty, and `false` otherwise.</span></span> <span data-ttu-id="3833c-135">L’utilisation de telles techniques peut rendre le code plus difficile à lire.</span><span class="sxs-lookup"><span data-stu-id="3833c-135">The use of such techniques can make code more difficult to read.</span></span>

<span data-ttu-id="3833c-136">Parfois, les modèles qui impliquent des correspondances incomplètes sont utiles, par exemple, si vous savez que les listes dans votre programme uniquement trois éléments, vous pouvez utiliser un modèle semblable à la suivante dans une liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="3833c-136">Occasionally, patterns that involve incomplete matches are useful, for example, if you know that the lists in your program have only three elements, you might use a pattern like the following in a parameter list.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3806.fs)]

<span data-ttu-id="3833c-137">L’utilisation de modèles avec des correspondances incomplètes doit être réservée aux prototypage rapide et d’autres utilisations temporaires.</span><span class="sxs-lookup"><span data-stu-id="3833c-137">The use of patterns that have incomplete matches is best reserved for quick prototyping and other temporary uses.</span></span> <span data-ttu-id="3833c-138">Le compilateur émet un avertissement pour ce code.</span><span class="sxs-lookup"><span data-stu-id="3833c-138">The compiler will issue a warning for such code.</span></span> <span data-ttu-id="3833c-139">Ces modèles ne peuvent pas couvrir le cas général de toutes les entrées possibles et par conséquent ne conviennent pas pour les API de composant.</span><span class="sxs-lookup"><span data-stu-id="3833c-139">Such patterns cannot cover the general case of all possible inputs and therefore are not suitable for component APIs.</span></span>

## <a name="named-arguments"></a><span data-ttu-id="3833c-140">Arguments nommés</span><span class="sxs-lookup"><span data-stu-id="3833c-140">Named Arguments</span></span>
<span data-ttu-id="3833c-141">Les arguments de méthodes peuvent être spécifiés par position dans une liste d’arguments séparés par des virgules, ou passés explicitement à une méthode en fournissant le nom, suivi par un signe égal et la valeur à passer dans.</span><span class="sxs-lookup"><span data-stu-id="3833c-141">Arguments for methods can be specified by position in a comma-separated argument list, or they can be passed to a method explicitly by providing the name, followed by an equal sign and the value to be passed in.</span></span> <span data-ttu-id="3833c-142">S’il est spécifié en fournissant le nom, ils peuvent apparaître dans un ordre différent de celui utilisé dans la déclaration.</span><span class="sxs-lookup"><span data-stu-id="3833c-142">If specified by providing the name, they can appear in a different order from that used in the declaration.</span></span>

<span data-ttu-id="3833c-143">Arguments nommés peuvent rendre code plus lisible et plus adaptable à certains types de modifications dans l’API, telles que la réorganisation des paramètres de méthode.</span><span class="sxs-lookup"><span data-stu-id="3833c-143">Named arguments can make code more readable and more adaptable to certain types of changes in the API, such as a reordering of method parameters.</span></span>

<span data-ttu-id="3833c-144">Arguments nommés sont autorisés uniquement pour les méthodes, pas pour `let`-lié des fonctions, des valeurs de fonction ou des expressions lambda.</span><span class="sxs-lookup"><span data-stu-id="3833c-144">Named arguments are allowed only for methods, not for `let`-bound functions, function values, or lambda expressions.</span></span>

<span data-ttu-id="3833c-145">L’exemple de code suivant illustre l’utilisation d’arguments nommés.</span><span class="sxs-lookup"><span data-stu-id="3833c-145">The following code example demonstrates the use of named arguments.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3807.fs)]

<span data-ttu-id="3833c-146">Dans un appel à un constructeur de classe, vous pouvez définir les valeurs des propriétés de la classe à l’aide d’une syntaxe similaire à celle des arguments nommés.</span><span class="sxs-lookup"><span data-stu-id="3833c-146">In a call to a class constructor, you can set the values of properties of the class by using a syntax similar to that of named arguments.</span></span> <span data-ttu-id="3833c-147">L’exemple suivant illustre cette syntaxe.</span><span class="sxs-lookup"><span data-stu-id="3833c-147">The following example shows this syntax.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet3506.fs)]

<span data-ttu-id="3833c-148">Pour plus d’informations, consultez [constructeurs (F #)](https://msdn.microsoft.com/library/2cd0ed07-d214-4125-8317-4f288af99f05).</span><span class="sxs-lookup"><span data-stu-id="3833c-148">For more information, see [Constructors (F#)](https://msdn.microsoft.com/library/2cd0ed07-d214-4125-8317-4f288af99f05).</span></span>

## <a name="optional-parameters"></a><span data-ttu-id="3833c-149">Paramètres facultatifs</span><span class="sxs-lookup"><span data-stu-id="3833c-149">Optional Parameters</span></span>
<span data-ttu-id="3833c-150">Vous pouvez spécifier un paramètre facultatif pour une méthode à l’aide d’un point d’interrogation devant le nom du paramètre.</span><span class="sxs-lookup"><span data-stu-id="3833c-150">You can specify an optional parameter for a method by using a question mark in front of the parameter name.</span></span> <span data-ttu-id="3833c-151">Paramètres facultatifs sont interprétés comme le type d’option F #, vous pouvez les interroger de façon habituelle que les types d’option sont interrogées, à l’aide un `match` expression avec `Some` et `None`.</span><span class="sxs-lookup"><span data-stu-id="3833c-151">Optional parameters are interpreted as the F# option type, so you can query them in the regular way that option types are queried, by using a `match` expression with `Some` and `None`.</span></span> <span data-ttu-id="3833c-152">Paramètres facultatifs sont autorisés uniquement sur les membres, et non sur les fonctions créées à l’aide de `let` liaisons.</span><span class="sxs-lookup"><span data-stu-id="3833c-152">Optional parameters are permitted only on members, not on functions created by using `let` bindings.</span></span>

<span data-ttu-id="3833c-153">Vous pouvez également utiliser une fonction `defaultArg`, qui définit une valeur par défaut d’un argument facultatif.</span><span class="sxs-lookup"><span data-stu-id="3833c-153">You can also use a function `defaultArg`, which sets a default value of an optional argument.</span></span> <span data-ttu-id="3833c-154">Le `defaultArg` fonction prend le paramètre facultatif comme premier argument et la valeur par défaut en tant que la seconde.</span><span class="sxs-lookup"><span data-stu-id="3833c-154">The `defaultArg` function takes the optional parameter as the first argument and the default value as the second.</span></span>

<span data-ttu-id="3833c-155">L’exemple suivant illustre l’utilisation de paramètres facultatifs.</span><span class="sxs-lookup"><span data-stu-id="3833c-155">The following example illustrates the use of optional parameters.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3808.fs)]

<span data-ttu-id="3833c-156">La sortie est la suivante.</span><span class="sxs-lookup"><span data-stu-id="3833c-156">The output is as follows.</span></span>

```
Baud Rate: 9600 Duplex: Full Parity: false
Baud Rate: 4800 Duplex: Half Parity: false
Baud Rate: 300 Duplex: Half Parity: true
```

## <a name="passing-by-reference"></a><span data-ttu-id="3833c-157">Passage par référence</span><span class="sxs-lookup"><span data-stu-id="3833c-157">Passing by Reference</span></span>
<span data-ttu-id="3833c-158">Passage d’une valeur de F # par référence implique la `byref` mot clé, qui spécifie que le paramètre est en fait un pointeur vers la valeur passée par référence.</span><span class="sxs-lookup"><span data-stu-id="3833c-158">Passing an F# value by reference involves the `byref` keyword, which specifies that the parameter is actually a pointer to the value being passed by reference.</span></span> <span data-ttu-id="3833c-159">Toute valeur passée dans une méthode avec un `byref` comme l’argument doit être `mutable`.</span><span class="sxs-lookup"><span data-stu-id="3833c-159">Any value passed into a method with a `byref` as the argument must be `mutable`.</span></span>

<span data-ttu-id="3833c-160">Étant donné que le paramètre est un pointeur et la valeur est mutable, les modifications apportées à la valeur sont conservées après l’exécution de la fonction.</span><span class="sxs-lookup"><span data-stu-id="3833c-160">Because the parameter is a pointer and the value is mutable, any changes to the value are retained after the execution of the function.</span></span>

<span data-ttu-id="3833c-161">Vous pouvez accomplir la même chose avec [cellules de référence](reference-cells.md), mais il est important de noter que **cellules de référence et `byref`s ne sont pas la même chose**.</span><span class="sxs-lookup"><span data-stu-id="3833c-161">You can accomplish the same thing with [Reference Cells](reference-cells.md), but it's important to note that **reference cells and `byref`s are not the same thing**.</span></span> <span data-ttu-id="3833c-162">Une cellule de référence est un conteneur pour une valeur que vous pouvez examiner et modifier le contenu de, mais cette valeur se trouve sur le tas et équivaut à disposer d’un enregistrement avec une valeur mutable qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="3833c-162">A reference cell is a container for a value that you can inspect and change the contents of, but this value lives on the heap and is equivalent to having a record with a mutable value contained within it.</span></span> <span data-ttu-id="3833c-163">Un `byref` un pointeur réels, il s’agit donc une sémantique sous-jacente différente et des règles d’utilisation (ce qui peuvent être assez restrictives).</span><span class="sxs-lookup"><span data-stu-id="3833c-163">A `byref` is an actual pointer, so it is different underlying semantics and usage rules (which can be quite restrictive).</span></span>

<span data-ttu-id="3833c-164">Les exemples suivants illustrent l’utilisation de la `byref` mot clé.</span><span class="sxs-lookup"><span data-stu-id="3833c-164">The following examples illustrate the use of the `byref` keyword.</span></span> <span data-ttu-id="3833c-165">Notez que lorsque vous utilisez une cellule de référence en tant que paramètre, vous devez créer une cellule de référence comme une valeur nommée et l’utiliser comme paramètre, pas seulement ajouter la `ref` comme indiqué dans le premier appel à `Increment` dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="3833c-165">Note that when you use a reference cell as a parameter, you must create a reference cell as a named value and use that as the parameter, not just add the `ref` operator as shown in the first call to `Increment` in the following code.</span></span> <span data-ttu-id="3833c-166">Étant donné que la création d’une cellule de référence crée une copie de la valeur sous-jacente, le premier appel incrémente simplement une valeur temporaire.</span><span class="sxs-lookup"><span data-stu-id="3833c-166">Because creating a reference cell creates a copy of the underlying value, the first call just increments a temporary value.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3809.fs)]

<span data-ttu-id="3833c-167">Vous pouvez utiliser un tuple comme valeur de retour pour stocker les `out` paramètres dans les méthodes de la bibliothèque .NET.</span><span class="sxs-lookup"><span data-stu-id="3833c-167">You can use a tuple as a return value to store any `out` parameters in .NET library methods.</span></span> <span data-ttu-id="3833c-168">Vous pouvez également traiter les `out` paramètre comme un `byref` paramètre.</span><span class="sxs-lookup"><span data-stu-id="3833c-168">Alternatively, you can treat the `out` parameter as a `byref` parameter.</span></span> <span data-ttu-id="3833c-169">L’exemple de code suivant illustre les deux sens.</span><span class="sxs-lookup"><span data-stu-id="3833c-169">The following code example illustrates both ways.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3810.fs)]

## <a name="parameter-arrays"></a><span data-ttu-id="3833c-170">Tableaux de paramètres</span><span class="sxs-lookup"><span data-stu-id="3833c-170">Parameter Arrays</span></span>
<span data-ttu-id="3833c-171">Parfois, il est nécessaire de définir une fonction qui accepte un nombre arbitraire de paramètres de type hétérogène.</span><span class="sxs-lookup"><span data-stu-id="3833c-171">Occasionally it is necessary to define a function that takes an arbitrary number of parameters of heterogeneous type.</span></span> <span data-ttu-id="3833c-172">Il ne serait pas pratique de créer toutes les méthodes surchargées possibles pour prendre en compte pour tous les types qui peuvent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="3833c-172">It would not be practical to create all the possible overloaded methods to account for all the types that could be used.</span></span> <span data-ttu-id="3833c-173">Les implémentations de .NET prennent en charge ces méthodes via la fonctionnalité de tableau de paramètre.</span><span class="sxs-lookup"><span data-stu-id="3833c-173">The .NET implementations provide support for such methods through the parameter array feature.</span></span> <span data-ttu-id="3833c-174">Une méthode qui prend un tableau de paramètres dans sa signature peut être fournie avec un nombre arbitraire de paramètres.</span><span class="sxs-lookup"><span data-stu-id="3833c-174">A method that takes a parameter array in its signature can be provided with an arbitrary number of parameters.</span></span> <span data-ttu-id="3833c-175">Les paramètres sont placés dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="3833c-175">The parameters are put into an array.</span></span> <span data-ttu-id="3833c-176">Le type des éléments du tableau détermine les types de paramètres qui peuvent être passés à la fonction.</span><span class="sxs-lookup"><span data-stu-id="3833c-176">The type of the array elements determines the parameter types that can be passed to the function.</span></span> <span data-ttu-id="3833c-177">Si vous définissez le tableau de paramètres avec `System.Object` en tant que le type d’élément, puis le code client peut passer des valeurs de n’importe quel type.</span><span class="sxs-lookup"><span data-stu-id="3833c-177">If you define the parameter array with `System.Object` as the element type, then client code can pass values of any type.</span></span>

<span data-ttu-id="3833c-178">En F #, les tableaux de paramètres peuvent uniquement être définies dans les méthodes.</span><span class="sxs-lookup"><span data-stu-id="3833c-178">In F#, parameter arrays can only be defined in methods.</span></span> <span data-ttu-id="3833c-179">Ils ne peuvent pas être utilisés dans des fonctions autonomes ou des fonctions qui sont définies dans les modules.</span><span class="sxs-lookup"><span data-stu-id="3833c-179">They cannot be used in standalone functions or functions that are defined in modules.</span></span>

<span data-ttu-id="3833c-180">Vous définissez un tableau de paramètres à l’aide de la `ParamArray` attribut.</span><span class="sxs-lookup"><span data-stu-id="3833c-180">You define a parameter array by using the `ParamArray` attribute.</span></span> <span data-ttu-id="3833c-181">Le `ParamArray` attribut peut uniquement être appliqué au dernier paramètre.</span><span class="sxs-lookup"><span data-stu-id="3833c-181">The `ParamArray` attribute can only be applied to the last parameter.</span></span>

<span data-ttu-id="3833c-182">Le code suivant illustre l’appel à une méthode .NET qui prend un tableau de paramètres et la définition d’un type en F # qui a une méthode qui prend un tableau de paramètres.</span><span class="sxs-lookup"><span data-stu-id="3833c-182">The following code illustrates both calling a .NET method that takes a parameter array and the definition of a type in F# that has a method that takes a parameter array.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-2/snippet3811.fs)]

<span data-ttu-id="3833c-183">Lorsque vous exécutez dans un projet, la sortie du code précédent est comme suit :</span><span class="sxs-lookup"><span data-stu-id="3833c-183">When run in a project, the output of the previous code is as follows:</span></span>

```
a 1 10 Hello world 1 True
"a"
1
10.0
"Hello world"
1u
true
```

## <a name="see-also"></a><span data-ttu-id="3833c-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3833c-184">See Also</span></span>
[<span data-ttu-id="3833c-185">Membres</span><span class="sxs-lookup"><span data-stu-id="3833c-185">Members</span></span>](members/index.md)
