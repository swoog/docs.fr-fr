---
title: Paramètres et arguments (F#)
description: 'En savoir plus sur F # prise en charge linguistique pour la définition de paramètres et de passer des arguments aux fonctions, des méthodes et propriétés.'
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: dotnet-fsharp
ms.devlang: fsharp
ms.openlocfilehash: e146ec4e877bb89f10e2f3daad2d8356c29fa81f
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="parameters-and-arguments"></a><span data-ttu-id="5941c-103">Paramètres et arguments</span><span class="sxs-lookup"><span data-stu-id="5941c-103">Parameters and Arguments</span></span>

<span data-ttu-id="5941c-104">Cette rubrique décrit la prise en charge de langage de définition de paramètres et de passer des arguments aux fonctions, des méthodes et propriétés.</span><span class="sxs-lookup"><span data-stu-id="5941c-104">This topic describes language support for defining parameters and passing arguments to functions, methods, and properties.</span></span> <span data-ttu-id="5941c-105">Il inclut des informations sur le passage par référence et comment définir et utiliser des méthodes qui peuvent prendre un nombre variable d’arguments.</span><span class="sxs-lookup"><span data-stu-id="5941c-105">It includes information about how to pass by reference, and how to define and use methods that can take a variable number of arguments.</span></span>


## <a name="parameters-and-arguments"></a><span data-ttu-id="5941c-106">Paramètres et arguments</span><span class="sxs-lookup"><span data-stu-id="5941c-106">Parameters and Arguments</span></span>
<span data-ttu-id="5941c-107">Le terme *paramètre* est utilisé pour décrire les noms des valeurs qui sont censées être fournies.</span><span class="sxs-lookup"><span data-stu-id="5941c-107">The term *parameter* is used to describe the names for values that are expected to be supplied.</span></span> <span data-ttu-id="5941c-108">Le terme *argument* est utilisé pour les valeurs fournies pour chaque paramètre.</span><span class="sxs-lookup"><span data-stu-id="5941c-108">The term *argument* is used for the values provided for each parameter.</span></span>

<span data-ttu-id="5941c-109">Paramètres peuvent être spécifiés sous forme de tuple ou curryfiés, ou dans une combinaison des deux.</span><span class="sxs-lookup"><span data-stu-id="5941c-109">Parameters can be specified in tuple or curried form, or in some combination of the two.</span></span> <span data-ttu-id="5941c-110">Vous pouvez passer des arguments à l’aide d’un nom de paramètre explicite.</span><span class="sxs-lookup"><span data-stu-id="5941c-110">You can pass arguments by using an explicit parameter name.</span></span> <span data-ttu-id="5941c-111">Les paramètres des méthodes peuvent être spécifiés comme étant facultatifs et une valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="5941c-111">Parameters of methods can be specified as optional and given a default value.</span></span>


## <a name="parameter-patterns"></a><span data-ttu-id="5941c-112">Modèles de paramètre</span><span class="sxs-lookup"><span data-stu-id="5941c-112">Parameter Patterns</span></span>
<span data-ttu-id="5941c-113">En règle générale, les paramètres fournis à des fonctions et méthodes sont des modèles séparés par des espaces.</span><span class="sxs-lookup"><span data-stu-id="5941c-113">Parameters supplied to functions and methods are, in general, patterns separated by spaces.</span></span> <span data-ttu-id="5941c-114">Cela signifie que, en principe, les modèles décrits dans [Expressions de correspondance](match-expressions.md) peut être utilisé dans une liste de paramètres pour une fonction ou un membre.</span><span class="sxs-lookup"><span data-stu-id="5941c-114">This means that, in principle, any of the patterns described in [Match Expressions](match-expressions.md) can be used in a parameter list for a function or member.</span></span>

<span data-ttu-id="5941c-115">Les méthodes utilisent généralement la forme de tuple de passage d’arguments.</span><span class="sxs-lookup"><span data-stu-id="5941c-115">Methods usually use the tuple form of passing arguments.</span></span> <span data-ttu-id="5941c-116">Cela permet d’obtenir un résultat plus clair de la perspective d’autres langages .NET, car la forme de tuple correspond à la façon d’arguments sont passés dans les méthodes .NET.</span><span class="sxs-lookup"><span data-stu-id="5941c-116">This achieves a clearer result from the perspective of other .NET languages because the tuple form matches the way arguments are passed in .NET methods.</span></span>

<span data-ttu-id="5941c-117">Le formulaire curryfié est souvent utilisé avec des fonctions créées à l’aide de `let` liaisons.</span><span class="sxs-lookup"><span data-stu-id="5941c-117">The curried form is most often used with functions created by using `let` bindings.</span></span>

<span data-ttu-id="5941c-118">Le pseudo-code suivant montre des exemples de tuple et d’arguments curryfiés.</span><span class="sxs-lookup"><span data-stu-id="5941c-118">The following pseudocode shows examples of tuple and curried arguments.</span></span>

```fsharp
// Tuple form.
member this.SomeMethod(param1, param2) = ...
// Curried form.
let function1 param1 param2 = ...
```

<span data-ttu-id="5941c-119">Combiner les formes sont possibles lorsque certains arguments sont dans des tuples et que certains ne sont pas.</span><span class="sxs-lookup"><span data-stu-id="5941c-119">Combined forms are possible when some arguments are in tuples and some are not.</span></span>

```fsharp
let function2 param1 (param2a, param2b) param3 = ...
```

<span data-ttu-id="5941c-120">Autres modèles peuvent également servir dans les listes de paramètres, mais si le modèle de paramètre ne correspond pas à toutes les entrées possibles, il peut être une correspondance incomplète au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="5941c-120">Other patterns can also be used in parameter lists, but if the parameter pattern does not match all possible inputs, there might be an incomplete match at run time.</span></span> <span data-ttu-id="5941c-121">L’exception `MatchFailureException` est généré lorsque la valeur d’un argument ne correspond pas les modèles spécifiés dans la liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="5941c-121">The exception `MatchFailureException` is generated when the value of an argument does not match the patterns specified in the parameter list.</span></span> <span data-ttu-id="5941c-122">Le compilateur émet un avertissement lorsqu’un modèle de paramètre accepte des correspondances incomplètes.</span><span class="sxs-lookup"><span data-stu-id="5941c-122">The compiler issues a warning when a parameter pattern allows for incomplete matches.</span></span> <span data-ttu-id="5941c-123">Au moins un autre modèle est souvent utile pour les listes de paramètres, et qui est le modèle de caractère générique.</span><span class="sxs-lookup"><span data-stu-id="5941c-123">At least one other pattern is commonly useful for parameter lists, and that is the wildcard pattern.</span></span> <span data-ttu-id="5941c-124">Vous utilisez le modèle de caractère générique dans une liste de paramètres lorsque vous souhaitez simplement ignorer tous les arguments sont fournis.</span><span class="sxs-lookup"><span data-stu-id="5941c-124">You use the wildcard pattern in a parameter list when you simply want to ignore any arguments that are supplied.</span></span> <span data-ttu-id="5941c-125">Le code suivant illustre l’utilisation du modèle de caractère générique dans une liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="5941c-125">The following code illustrates the use of the wildcard pattern in an argument list.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3801.fs)]

<span data-ttu-id="5941c-126">Le modèle de caractère générique peut être utile chaque fois que vous n’avez pas besoin des arguments transmis, comme dans le point d’entrée principal à un programme, lorsque vous n’êtes pas intéressé par les arguments de ligne de commande fournis normalement en tant que tableau de chaînes, comme dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="5941c-126">The wildcard pattern can be useful whenever you do not need the arguments passed in, such as in the main entry point to a program, when you are not interested in the command-line arguments that are normally supplied as a string array, as in the following code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3802.fs)]

<span data-ttu-id="5941c-127">Autres modèles sont parfois utilisées dans les arguments sont les `as` modèle et les modèles d’identificateur associés aux unions discriminées et les modèles actifs.</span><span class="sxs-lookup"><span data-stu-id="5941c-127">Other patterns that are sometimes used in arguments are the `as` pattern, and identifier patterns associated with discriminated unions and active patterns.</span></span> <span data-ttu-id="5941c-128">Vous pouvez utiliser le modèle d’union discriminée seul cas comme suit.</span><span class="sxs-lookup"><span data-stu-id="5941c-128">You can use the single-case discriminated union pattern as follows.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3803.fs)]

<span data-ttu-id="5941c-129">La sortie est la suivante.</span><span class="sxs-lookup"><span data-stu-id="5941c-129">The output is as follows.</span></span>

```
Data begins at 0 and ends at 4 in string Et tu, Brute?
Et tu
```

<span data-ttu-id="5941c-130">Modèles actifs peuvent être utiles en tant que paramètres, par exemple, lors de la transformation d’un argument en un format de votre choix, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="5941c-130">Active patterns can be useful as parameters, for example, when transforming an argument into a desired format, as in the following example:</span></span>

```fsharp
type Point = { x : float; y : float }

let (| Polar |) { x = x; y = y} =
    ( sqrt (x*x + y*y), System.Math.Atan (y/ x) )

let radius (Polar(r, _)) = r
let angle (Polar(_, theta)) = theta
```

<span data-ttu-id="5941c-131">Vous pouvez utiliser la `as` modèle pour stocker une valeur correspondante comme valeur locale, comme indiqué dans la ligne de code suivante.</span><span class="sxs-lookup"><span data-stu-id="5941c-131">You can use the `as` pattern to store a matched value as a local value, as is shown in the following line of code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3805.fs)]

<span data-ttu-id="5941c-132">Un autre modèle utilisé parfois est une fonction qui laisse le dernier argument sans nom en fournissant, en tant que le corps de la fonction, une expression lambda qui exécute immédiatement une correspondance de modèle sur l’argument implicite.</span><span class="sxs-lookup"><span data-stu-id="5941c-132">Another pattern that is used occasionally is a function that leaves the last argument unnamed by providing, as the body of the function, a lambda expression that immediately performs a pattern match on the implicit argument.</span></span> <span data-ttu-id="5941c-133">Ceci est la ligne de code suivante.</span><span class="sxs-lookup"><span data-stu-id="5941c-133">An example of this is the following line of code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3804.fs)]

<span data-ttu-id="5941c-134">Ce code définit une fonction qui accepte une liste générique et retourne `true` si la liste est vide, et `false` dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5941c-134">This code defines a function that takes a generic list and returns `true` if the list is empty, and `false` otherwise.</span></span> <span data-ttu-id="5941c-135">L’utilisation de ces techniques permettre rendre le code plus difficile à lire.</span><span class="sxs-lookup"><span data-stu-id="5941c-135">The use of such techniques can make code more difficult to read.</span></span>

<span data-ttu-id="5941c-136">Parfois, les modèles qui impliquent des correspondances incomplètes sont utiles, par exemple, si vous savez que les listes dans votre programme ont uniquement trois éléments, vous pouvez utiliser un modèle semblable à la suivante dans une liste de paramètres.</span><span class="sxs-lookup"><span data-stu-id="5941c-136">Occasionally, patterns that involve incomplete matches are useful, for example, if you know that the lists in your program have only three elements, you might use a pattern like the following in a parameter list.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3806.fs)]

<span data-ttu-id="5941c-137">L’utilisation de modèles qui ont des correspondances incomplètes est mieux réservée pour une création rapide de prototypes et d’autres utilisations temporaires.</span><span class="sxs-lookup"><span data-stu-id="5941c-137">The use of patterns that have incomplete matches is best reserved for quick prototyping and other temporary uses.</span></span> <span data-ttu-id="5941c-138">Le compilateur émet un avertissement pour ce code.</span><span class="sxs-lookup"><span data-stu-id="5941c-138">The compiler will issue a warning for such code.</span></span> <span data-ttu-id="5941c-139">Ces modèles ne peuvent pas couvrir le cas général de toutes les entrées possibles et par conséquent ne conviennent pas aux API de composant.</span><span class="sxs-lookup"><span data-stu-id="5941c-139">Such patterns cannot cover the general case of all possible inputs and therefore are not suitable for component APIs.</span></span>

## <a name="named-arguments"></a><span data-ttu-id="5941c-140">Arguments nommés</span><span class="sxs-lookup"><span data-stu-id="5941c-140">Named Arguments</span></span>
<span data-ttu-id="5941c-141">Les arguments de méthodes peuvent être spécifiés par position dans une liste d’arguments séparée par des virgules, ou passés explicitement à une méthode en fournissant le nom, suivi par un signe égal et la valeur à passer dans.</span><span class="sxs-lookup"><span data-stu-id="5941c-141">Arguments for methods can be specified by position in a comma-separated argument list, or they can be passed to a method explicitly by providing the name, followed by an equal sign and the value to be passed in.</span></span> <span data-ttu-id="5941c-142">S’il est spécifié en fournissant le nom, ils peuvent apparaître dans un ordre différent de celui utilisé dans la déclaration.</span><span class="sxs-lookup"><span data-stu-id="5941c-142">If specified by providing the name, they can appear in a different order from that used in the declaration.</span></span>

<span data-ttu-id="5941c-143">Arguments nommés peuvent rendre le code plus lisible et plus adaptable à certains types de modifications dans l’API, telles que la réorganisation des paramètres de méthode.</span><span class="sxs-lookup"><span data-stu-id="5941c-143">Named arguments can make code more readable and more adaptable to certain types of changes in the API, such as a reordering of method parameters.</span></span>

<span data-ttu-id="5941c-144">Arguments nommés sont autorisés uniquement pour les méthodes, pas pour `let`-lié des fonctions, des valeurs de fonction ou des expressions lambda.</span><span class="sxs-lookup"><span data-stu-id="5941c-144">Named arguments are allowed only for methods, not for `let`-bound functions, function values, or lambda expressions.</span></span>

<span data-ttu-id="5941c-145">L’exemple de code suivant illustre l’utilisation d’arguments nommés.</span><span class="sxs-lookup"><span data-stu-id="5941c-145">The following code example demonstrates the use of named arguments.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3807.fs)]

<span data-ttu-id="5941c-146">Dans un appel à un constructeur de classe, vous pouvez définir les valeurs des propriétés de la classe à l’aide d’une syntaxe similaire à celle des arguments nommés.</span><span class="sxs-lookup"><span data-stu-id="5941c-146">In a call to a class constructor, you can set the values of properties of the class by using a syntax similar to that of named arguments.</span></span> <span data-ttu-id="5941c-147">L’exemple suivant illustre cette syntaxe.</span><span class="sxs-lookup"><span data-stu-id="5941c-147">The following example shows this syntax.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet3506.fs)]

<span data-ttu-id="5941c-148">Pour plus d’informations, consultez [constructeurs (F #)](https://msdn.microsoft.com/library/2cd0ed07-d214-4125-8317-4f288af99f05).</span><span class="sxs-lookup"><span data-stu-id="5941c-148">For more information, see [Constructors (F#)](https://msdn.microsoft.com/library/2cd0ed07-d214-4125-8317-4f288af99f05).</span></span>

## <a name="optional-parameters"></a><span data-ttu-id="5941c-149">Paramètres facultatifs</span><span class="sxs-lookup"><span data-stu-id="5941c-149">Optional Parameters</span></span>
<span data-ttu-id="5941c-150">Vous pouvez spécifier un paramètre facultatif pour une méthode à l’aide d’un point d’interrogation devant le nom du paramètre.</span><span class="sxs-lookup"><span data-stu-id="5941c-150">You can specify an optional parameter for a method by using a question mark in front of the parameter name.</span></span> <span data-ttu-id="5941c-151">Paramètres facultatifs sont interprétés comme le type d’option F #, vous pouvez les interroger normalement que les types d’options sont interrogées à l’aide un `match` expression avec `Some` et `None`.</span><span class="sxs-lookup"><span data-stu-id="5941c-151">Optional parameters are interpreted as the F# option type, so you can query them in the regular way that option types are queried, by using a `match` expression with `Some` and `None`.</span></span> <span data-ttu-id="5941c-152">Paramètres facultatifs sont autorisés uniquement sur les membres, et non sur les fonctions créées à l’aide de `let` liaisons.</span><span class="sxs-lookup"><span data-stu-id="5941c-152">Optional parameters are permitted only on members, not on functions created by using `let` bindings.</span></span>

<span data-ttu-id="5941c-153">Vous pouvez également utiliser une fonction `defaultArg`, qui définit une valeur par défaut d’un argument facultatif.</span><span class="sxs-lookup"><span data-stu-id="5941c-153">You can also use a function `defaultArg`, which sets a default value of an optional argument.</span></span> <span data-ttu-id="5941c-154">Le `defaultArg` fonction prend le paramètre facultatif comme premier argument et la valeur par défaut en tant que la seconde.</span><span class="sxs-lookup"><span data-stu-id="5941c-154">The `defaultArg` function takes the optional parameter as the first argument and the default value as the second.</span></span>

<span data-ttu-id="5941c-155">L’exemple suivant illustre l’utilisation des paramètres optionnels.</span><span class="sxs-lookup"><span data-stu-id="5941c-155">The following example illustrates the use of optional parameters.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3808.fs)]

<span data-ttu-id="5941c-156">La sortie est la suivante.</span><span class="sxs-lookup"><span data-stu-id="5941c-156">The output is as follows.</span></span>

```
Baud Rate: 9600 Duplex: Full Parity: false
Baud Rate: 4800 Duplex: Half Parity: false
Baud Rate: 300 Duplex: Half Parity: true
```

## <a name="passing-by-reference"></a><span data-ttu-id="5941c-157">Le passage par référence</span><span class="sxs-lookup"><span data-stu-id="5941c-157">Passing by Reference</span></span>
<span data-ttu-id="5941c-158">F # prend en charge le `byref` mot clé, qui spécifie qu’un paramètre est passé par référence.</span><span class="sxs-lookup"><span data-stu-id="5941c-158">F# supports the `byref` keyword, which specifies that a parameter is passed by reference.</span></span> <span data-ttu-id="5941c-159">Cela signifie que toute modification apportée à la valeur est conservées après l’exécution de la fonction.</span><span class="sxs-lookup"><span data-stu-id="5941c-159">This means that any changes to the value are retained after the execution of the function.</span></span> <span data-ttu-id="5941c-160">Les valeurs fournies pour un `byref` paramètre doit être mutable.</span><span class="sxs-lookup"><span data-stu-id="5941c-160">Values provided to a `byref` parameter must be mutable.</span></span> <span data-ttu-id="5941c-161">Vous pouvez également passer des cellules de référence du type approprié.</span><span class="sxs-lookup"><span data-stu-id="5941c-161">Alternatively, you can pass reference cells of the appropriate type.</span></span>

<span data-ttu-id="5941c-162">Passage par référence dans les langages .NET est devenu un moyen de retourner plusieurs valeurs à partir d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="5941c-162">Passing by reference in .NET languages evolved as a way to return more than one value from a function.</span></span> <span data-ttu-id="5941c-163">En F #, vous pouvez retourner un tuple à cette fin, ou utiliser une cellule de référence mutable en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="5941c-163">In F#, you can return a tuple for this purpose, or use a mutable reference cell as a parameter.</span></span> <span data-ttu-id="5941c-164">Le `byref` paramètre est fourni principalement pour l’interopérabilité avec les bibliothèques .NET.</span><span class="sxs-lookup"><span data-stu-id="5941c-164">The `byref` parameter is mainly provided for interoperability with .NET libraries.</span></span>

<span data-ttu-id="5941c-165">Les exemples suivants illustrent l’utilisation de la `byref` (mot clé).</span><span class="sxs-lookup"><span data-stu-id="5941c-165">The following examples illustrate the use of the `byref` keyword.</span></span> <span data-ttu-id="5941c-166">Notez que lorsque vous utilisez une cellule de référence en tant que paramètre, vous devez créer une cellule de référence comme valeur nommée et utiliser comme paramètre, non seulement ajouter la `ref` opérateur, comme indiqué dans le premier appel à `Increment` dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="5941c-166">Note that when you use a reference cell as a parameter, you must create a reference cell as a named value and use that as the parameter, not just add the `ref` operator as shown in the first call to `Increment` in the following code.</span></span> <span data-ttu-id="5941c-167">Étant donné que la création d’une cellule de référence crée une copie de la valeur sous-jacente, le premier appel incrémente simplement une valeur temporaire.</span><span class="sxs-lookup"><span data-stu-id="5941c-167">Because creating a reference cell creates a copy of the underlying value, the first call just increments a temporary value.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3809.fs)]

<span data-ttu-id="5941c-168">Vous pouvez utiliser un tuple comme valeur de retour pour stocker les `out` paramètres dans les méthodes de bibliothèque .NET.</span><span class="sxs-lookup"><span data-stu-id="5941c-168">You can use a tuple as a return value to store any `out` parameters in .NET library methods.</span></span> <span data-ttu-id="5941c-169">Vous pouvez également traiter les `out` paramètre comme un `byref` paramètre.</span><span class="sxs-lookup"><span data-stu-id="5941c-169">Alternatively, you can treat the `out` parameter as a `byref` parameter.</span></span> <span data-ttu-id="5941c-170">L’exemple de code suivant illustre deux façons.</span><span class="sxs-lookup"><span data-stu-id="5941c-170">The following code example illustrates both ways.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-1/snippet3810.fs)]

## <a name="parameter-arrays"></a><span data-ttu-id="5941c-171">Tableaux de paramètres</span><span class="sxs-lookup"><span data-stu-id="5941c-171">Parameter Arrays</span></span>
<span data-ttu-id="5941c-172">Il est parfois nécessaire de définir une fonction qui accepte un nombre arbitraire de paramètres de type hétérogène.</span><span class="sxs-lookup"><span data-stu-id="5941c-172">Occasionally it is necessary to define a function that takes an arbitrary number of parameters of heterogeneous type.</span></span> <span data-ttu-id="5941c-173">Il ne serait pas pratique de créer toutes les méthodes surchargées possibles pour prendre en compte pour tous les types qui peuvent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="5941c-173">It would not be practical to create all the possible overloaded methods to account for all the types that could be used.</span></span> <span data-ttu-id="5941c-174">Les implémentations .NET prennent en charge ces méthodes via la fonctionnalité de tableau de paramètres.</span><span class="sxs-lookup"><span data-stu-id="5941c-174">The .NET implementations provide support for such methods through the parameter array feature.</span></span> <span data-ttu-id="5941c-175">Une méthode qui prend un tableau de paramètres dans sa signature peut être fournie avec un nombre arbitraire de paramètres.</span><span class="sxs-lookup"><span data-stu-id="5941c-175">A method that takes a parameter array in its signature can be provided with an arbitrary number of parameters.</span></span> <span data-ttu-id="5941c-176">Les paramètres sont placés dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="5941c-176">The parameters are put into an array.</span></span> <span data-ttu-id="5941c-177">Le type des éléments du tableau détermine les types de paramètres qui peuvent être passés à la fonction.</span><span class="sxs-lookup"><span data-stu-id="5941c-177">The type of the array elements determines the parameter types that can be passed to the function.</span></span> <span data-ttu-id="5941c-178">Si vous définissez le tableau de paramètres avec `System.Object` comme type d’élément, puis le code client peut passer des valeurs de n’importe quel type.</span><span class="sxs-lookup"><span data-stu-id="5941c-178">If you define the parameter array with `System.Object` as the element type, then client code can pass values of any type.</span></span>

<span data-ttu-id="5941c-179">En F #, les tableaux de paramètres peuvent uniquement être définies dans les méthodes.</span><span class="sxs-lookup"><span data-stu-id="5941c-179">In F#, parameter arrays can only be defined in methods.</span></span> <span data-ttu-id="5941c-180">Ils ne peut pas être utilisés dans des fonctions autonomes ou des fonctions qui sont définies dans des modules.</span><span class="sxs-lookup"><span data-stu-id="5941c-180">They cannot be used in standalone functions or functions that are defined in modules.</span></span>

<span data-ttu-id="5941c-181">Vous définissez un tableau de paramètres à l’aide de la `ParamArray` attribut.</span><span class="sxs-lookup"><span data-stu-id="5941c-181">You define a parameter array by using the `ParamArray` attribute.</span></span> <span data-ttu-id="5941c-182">Le `ParamArray` attribut ne peut être appliqué qu’au dernier paramètre.</span><span class="sxs-lookup"><span data-stu-id="5941c-182">The `ParamArray` attribute can only be applied to the last parameter.</span></span>

<span data-ttu-id="5941c-183">Le code suivant illustre l’appel à une méthode .NET qui prend un tableau de paramètres et de la définition d’un type en F # qui a une méthode qui prend un tableau de paramètres.</span><span class="sxs-lookup"><span data-stu-id="5941c-183">The following code illustrates both calling a .NET method that takes a parameter array and the definition of a type in F# that has a method that takes a parameter array.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/parameters-and-arguments-2/snippet3811.fs)]

<span data-ttu-id="5941c-184">Lors de l’exécution dans un projet, la sortie du code précédent est comme suit :</span><span class="sxs-lookup"><span data-stu-id="5941c-184">When run in a project, the output of the previous code is as follows:</span></span>

```
a 1 10 Hello world 1 True
"a"
1
10.0
"Hello world"
1u
true
```

## <a name="see-also"></a><span data-ttu-id="5941c-185">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5941c-185">See Also</span></span>
[<span data-ttu-id="5941c-186">Membres</span><span class="sxs-lookup"><span data-stu-id="5941c-186">Members</span></span>](members/index.md)
