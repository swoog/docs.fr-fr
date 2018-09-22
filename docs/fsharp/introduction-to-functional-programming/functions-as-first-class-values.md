---
title: Fonctions comme valeurs de première classe (F#)
description: 'Découvrez comment les fonctions sont élevés au rang d’état de première classe dans le langage de programmation F #.'
ms.date: 05/16/2016
ms.openlocfilehash: 45b65ab2454a592d38c80fd367e7243635614727
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2018
ms.locfileid: "46586894"
---
# <a name="functions-as-first-class-values"></a><span data-ttu-id="4c872-103">Fonctions comme valeurs de première classe</span><span class="sxs-lookup"><span data-stu-id="4c872-103">Functions as First-Class Values</span></span>

<span data-ttu-id="4c872-104">Une caractéristique des langages de programmation fonctionnelle est l’élévation des fonctions à l’état de première classe.</span><span class="sxs-lookup"><span data-stu-id="4c872-104">A defining characteristic of functional programming languages is the elevation of functions to first-class status.</span></span> <span data-ttu-id="4c872-105">Vous pourrez faire avec une fonction, comme vous pouvez faire avec les valeurs des autres types intégrés et être en mesure de le faire avec un degré comparable d’effort.</span><span class="sxs-lookup"><span data-stu-id="4c872-105">You should be able to do with a function whatever you can do with values of the other built-in types, and be able to do so with a comparable degree of effort.</span></span>

<span data-ttu-id="4c872-106">Les mesures de l’état de première classe courantes sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="4c872-106">Typical measures of first-class status include the following:</span></span>

- <span data-ttu-id="4c872-107">Vous liez des fonctions aux identificateurs ?</span><span class="sxs-lookup"><span data-stu-id="4c872-107">Can you bind functions to identifiers?</span></span> <span data-ttu-id="4c872-108">Autrement dit, pouvez vous donner les noms ?</span><span class="sxs-lookup"><span data-stu-id="4c872-108">That is, can you give them names?</span></span>

- <span data-ttu-id="4c872-109">Peut stocker des fonctions dans les structures de données, comme dans une liste ?</span><span class="sxs-lookup"><span data-stu-id="4c872-109">Can you store functions in data structures, such as in a list?</span></span>

- <span data-ttu-id="4c872-110">Vous passez une fonction en tant qu’argument dans un appel de fonction ?</span><span class="sxs-lookup"><span data-stu-id="4c872-110">Can you pass a function as an argument in a function call?</span></span>

- <span data-ttu-id="4c872-111">Vous pouvez retourner une fonction à partir d’un appel de fonction ?</span><span class="sxs-lookup"><span data-stu-id="4c872-111">Can you return a function from a function call?</span></span>

<span data-ttu-id="4c872-112">Les deux dernières mesures définissent ce que l'on *opérations d’ordre supérieur* ou *fonctions d’ordre supérieur*.</span><span class="sxs-lookup"><span data-stu-id="4c872-112">The last two measures define what are known as *higher-order operations* or *higher-order functions*.</span></span> <span data-ttu-id="4c872-113">Fonctions d’ordre supérieur acceptent des fonctions en tant qu’arguments et retournent des fonctions en tant que la valeur des appels de fonction.</span><span class="sxs-lookup"><span data-stu-id="4c872-113">Higher-order functions accept functions as arguments and return functions as the value of function calls.</span></span> <span data-ttu-id="4c872-114">Ces opérations prennent en charge les éléments aussi essentiels de la programmation fonctionnelle que le mappage des fonctions et la composition de fonctions.</span><span class="sxs-lookup"><span data-stu-id="4c872-114">These operations support such mainstays of functional programming as mapping functions and composition of functions.</span></span>

## <a name="give-the-value-a-name"></a><span data-ttu-id="4c872-115">Donnez un nom à la valeur</span><span class="sxs-lookup"><span data-stu-id="4c872-115">Give the Value a Name</span></span>

<span data-ttu-id="4c872-116">Si une fonction est une valeur de première classe, vous devez être en mesure de nom, tout comme vous pouvez nommer les entiers, chaînes et autres types intégrés.</span><span class="sxs-lookup"><span data-stu-id="4c872-116">If a function is a first-class value, you must be able to name it, just as you can name integers, strings, and other built-in types.</span></span> <span data-ttu-id="4c872-117">Cela s’appelle dans la programmation fonctionnelle en tant que liant un identificateur à une valeur.</span><span class="sxs-lookup"><span data-stu-id="4c872-117">This is referred to in functional programming literature as binding an identifier to a value.</span></span> <span data-ttu-id="4c872-118">F # utilise [ `let` liaisons](../language-reference/functions/let-bindings.md) pour lier des noms aux valeurs : `let <identifier> = <value>`.</span><span class="sxs-lookup"><span data-stu-id="4c872-118">F# uses [`let` bindings](../language-reference/functions/let-bindings.md) to bind names to values: `let <identifier> = <value>`.</span></span> <span data-ttu-id="4c872-119">Le code suivant montre deux exemples.</span><span class="sxs-lookup"><span data-stu-id="4c872-119">The following code shows two examples.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet20.fs)]

<span data-ttu-id="4c872-120">Vous pouvez nommer une fonction aussi facilement.</span><span class="sxs-lookup"><span data-stu-id="4c872-120">You can name a function just as easily.</span></span> <span data-ttu-id="4c872-121">L’exemple suivant définit une fonction nommée `squareIt` en liant l’identificateur `squareIt` à la [expression lambda](../language-reference/functions/lambda-expressions-the-fun-keyword.md) `fun n -> n * n`.</span><span class="sxs-lookup"><span data-stu-id="4c872-121">The following example defines a function named `squareIt` by binding the identifier `squareIt` to the [lambda expression](../language-reference/functions/lambda-expressions-the-fun-keyword.md) `fun n -> n * n`.</span></span> <span data-ttu-id="4c872-122">Fonction `squareIt` a un paramètre, `n`, et elle retourne le carré de ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="4c872-122">Function `squareIt` has one parameter, `n`, and it returns the square of that parameter.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet21.fs)]

<span data-ttu-id="4c872-123">F # fournit une syntaxe plus concise pour obtenir le même résultat avec moins de frappe.</span><span class="sxs-lookup"><span data-stu-id="4c872-123">F# provides the following more concise syntax to achieve the same result with less typing.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet22.fs)]

<span data-ttu-id="4c872-124">Les exemples qui suivent principalement utilisent le premier style, `let <function-name> = <lambda-expression>`, pour mettre en évidence les similitudes entre la déclaration de fonctions et la déclaration d’autres types de valeurs.</span><span class="sxs-lookup"><span data-stu-id="4c872-124">The examples that follow mostly use the first style, `let <function-name> = <lambda-expression>`, to emphasize the similarities between the declaration of functions and the declaration of other types of values.</span></span> <span data-ttu-id="4c872-125">Toutefois, toutes les fonctions nommées peuvent également être écrits avec la syntaxe concise.</span><span class="sxs-lookup"><span data-stu-id="4c872-125">However, all the named functions can also be written with the concise syntax.</span></span> <span data-ttu-id="4c872-126">Certains exemples sont écrits dans les deux sens.</span><span class="sxs-lookup"><span data-stu-id="4c872-126">Some of the examples are written in both ways.</span></span>

## <a name="store-the-value-in-a-data-structure"></a><span data-ttu-id="4c872-127">Store de la valeur dans une Structure de données</span><span class="sxs-lookup"><span data-stu-id="4c872-127">Store the Value in a Data Structure</span></span>

<span data-ttu-id="4c872-128">Une valeur de première classe peut être stockée dans une structure de données.</span><span class="sxs-lookup"><span data-stu-id="4c872-128">A first-class value can be stored in a data structure.</span></span> <span data-ttu-id="4c872-129">Le code suivant montre des exemples qui stockent des valeurs dans les listes et des tuples.</span><span class="sxs-lookup"><span data-stu-id="4c872-129">The following code shows examples that store values in lists and in tuples.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet23.fs)]

<span data-ttu-id="4c872-130">Pour vérifier qu’un nom de fonction stocké dans un tuple correspond en fait à une fonction, l’exemple suivant utilise le `fst` et `snd` opérateurs pour extraire le premier et le second élément de tuple `funAndArgTuple`.</span><span class="sxs-lookup"><span data-stu-id="4c872-130">To verify that a function name stored in a tuple does in fact evaluate to a function, the following example uses the `fst` and `snd` operators to extract the first and second elements from tuple `funAndArgTuple`.</span></span> <span data-ttu-id="4c872-131">Le premier élément du tuple est `squareIt` et le deuxième élément est `num`.</span><span class="sxs-lookup"><span data-stu-id="4c872-131">The first element in the tuple is `squareIt` and the second element is `num`.</span></span> <span data-ttu-id="4c872-132">Identificateur `num` est liée dans un exemple précédent à l’entier 10, un argument valide pour le `squareIt` (fonction).</span><span class="sxs-lookup"><span data-stu-id="4c872-132">Identifier `num` is bound in a previous example to integer 10, a valid argument for the `squareIt` function.</span></span> <span data-ttu-id="4c872-133">La deuxième expression applique le premier élément du tuple au deuxième élément du tuple : `squareIt num`.</span><span class="sxs-lookup"><span data-stu-id="4c872-133">The second expression applies the first element in the tuple to the second element in the tuple: `squareIt num`.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet24.fs)]

<span data-ttu-id="4c872-134">Tout comme l’identificateur `num` et entière 10 peut être utilisés indifféremment, peut donc identificateur `squareIt` et expression lambda `fun n -> n * n`.</span><span class="sxs-lookup"><span data-stu-id="4c872-134">Similarly, just as identifier `num` and integer 10 can be used interchangeably, so can identifier `squareIt` and lambda expression `fun n -> n * n`.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet25.fs)]

## <a name="pass-the-value-as-an-argument"></a><span data-ttu-id="4c872-135">Passez la valeur en tant qu’Argument</span><span class="sxs-lookup"><span data-stu-id="4c872-135">Pass the Value as an Argument</span></span>

<span data-ttu-id="4c872-136">Si une valeur a un état de première classe dans un langage, vous pouvez le passer en tant qu’argument à une fonction.</span><span class="sxs-lookup"><span data-stu-id="4c872-136">If a value has first-class status in a language, you can pass it as an argument to a function.</span></span> <span data-ttu-id="4c872-137">Par exemple, il est courant pour passer des entiers et des chaînes en tant qu’arguments.</span><span class="sxs-lookup"><span data-stu-id="4c872-137">For example, it is common to pass integers and strings as arguments.</span></span> <span data-ttu-id="4c872-138">Le code suivant montre des entiers et les chaînes passées comme arguments en F #.</span><span class="sxs-lookup"><span data-stu-id="4c872-138">The following code shows integers and strings passed as arguments in F#.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet26.fs)]

<span data-ttu-id="4c872-139">Si les fonctions ont un état de première classe, vous devez être en mesure de les passer en tant qu’arguments de la même façon.</span><span class="sxs-lookup"><span data-stu-id="4c872-139">If functions have first-class status, you must be able to pass them as arguments in the same way.</span></span> <span data-ttu-id="4c872-140">N’oubliez pas qu’il s’agit de la première caractéristique des fonctions d’ordre supérieur.</span><span class="sxs-lookup"><span data-stu-id="4c872-140">Remember that this is the first characteristic of higher-order functions.</span></span>

<span data-ttu-id="4c872-141">Dans l’exemple suivant, fonction `applyIt` a deux paramètres, `op` et `arg`.</span><span class="sxs-lookup"><span data-stu-id="4c872-141">In the following example, function `applyIt` has two parameters, `op` and `arg`.</span></span> <span data-ttu-id="4c872-142">Si vous envoyez une fonction qui a un paramètre pour `op` et un argument approprié pour la fonction `arg`, la fonction retourne le résultat de l’application `op` à `arg`.</span><span class="sxs-lookup"><span data-stu-id="4c872-142">If you send in a function that has one parameter for `op` and an appropriate argument for the function to `arg`, the function returns the result of applying `op` to `arg`.</span></span> <span data-ttu-id="4c872-143">Dans l’exemple suivant, l’argument de fonction et l’argument entier sont envoyées de la même façon, à l’aide de leurs noms.</span><span class="sxs-lookup"><span data-stu-id="4c872-143">In the following example, both the function argument and the integer argument are sent in the same way, by using their names.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet27.fs)]

<span data-ttu-id="4c872-144">Permet d’envoyer une fonction en tant qu’argument à une autre fonction se trouve sous les abstractions communes dans les langages de programmation fonctionnelle, telles que les opérations de mappage ou de filtrage.</span><span class="sxs-lookup"><span data-stu-id="4c872-144">The ability to send a function as an argument to another function underlies common abstractions in functional programming languages, such as map or filter operations.</span></span> <span data-ttu-id="4c872-145">Une opération de mappage, par exemple, est une fonction d’ordre supérieur qui capture le calcul partagé par les fonctions dans une liste, effectuer une opération sur chaque élément et puis retournent une liste des résultats.</span><span class="sxs-lookup"><span data-stu-id="4c872-145">A map operation, for example, is a higher-order function that captures the computation shared by functions that step through a list, do something to each element, and then return a list of the results.</span></span> <span data-ttu-id="4c872-146">Vous pouvez faire pour incrémenter chaque élément dans une liste d’entiers, ou à un carré de chaque élément ou pour convertir chaque élément dans une liste de chaînes en majuscules.</span><span class="sxs-lookup"><span data-stu-id="4c872-146">You might want to increment each element in a list of integers, or to square each element, or to change each element in a list of strings to uppercase.</span></span> <span data-ttu-id="4c872-147">La partie sujette aux erreurs du calcul est le processus récursif qui parcourt la liste et génère une liste des résultats à retourner.</span><span class="sxs-lookup"><span data-stu-id="4c872-147">The error-prone part of the computation is the recursive process that steps through the list and builds a list of the results to return.</span></span> <span data-ttu-id="4c872-148">Cette partie est capturée dans la fonction de mappage.</span><span class="sxs-lookup"><span data-stu-id="4c872-148">That part is captured in the mapping function.</span></span> <span data-ttu-id="4c872-149">Il vous suffit d’écrire pour une application particulière est la fonction que vous souhaitez appliquer individuellement à chaque élément de liste (ajout, mise au carré, changement de casse).</span><span class="sxs-lookup"><span data-stu-id="4c872-149">All you have to write for a particular application is the function that you want to apply to each list element individually (adding, squaring, changing case).</span></span> <span data-ttu-id="4c872-150">Cette fonction est envoyée en tant qu’argument à la fonction de mappage, tout comme `squareIt` est envoyé à `applyIt` dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="4c872-150">That function is sent as an argument to the mapping function, just as `squareIt` is sent to `applyIt` in the previous example.</span></span>

<span data-ttu-id="4c872-151">F # fournit des méthodes de mappage pour la plupart des types de collection, notamment [répertorie](../language-reference/lists.md), [tableaux](../language-reference/arrays.md), et [séquences](../language-reference/sequences.md).</span><span class="sxs-lookup"><span data-stu-id="4c872-151">F# provides map methods for most collection types, including [lists](../language-reference/lists.md), [arrays](../language-reference/arrays.md), and [sequences](../language-reference/sequences.md).</span></span> <span data-ttu-id="4c872-152">Les exemples suivants utilisent des listes.</span><span class="sxs-lookup"><span data-stu-id="4c872-152">The following examples use lists.</span></span> <span data-ttu-id="4c872-153">La syntaxe est `List.map <the function> <the list>`.</span><span class="sxs-lookup"><span data-stu-id="4c872-153">The syntax is `List.map <the function> <the list>`.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet28.fs)]

<span data-ttu-id="4c872-154">Pour plus d’informations, consultez [répertorie](../language-reference/lists.md).</span><span class="sxs-lookup"><span data-stu-id="4c872-154">For more information, see [Lists](../language-reference/lists.md).</span></span>

## <a name="return-the-value-from-a-function-call"></a><span data-ttu-id="4c872-155">Retourner la valeur d’un appel de fonction</span><span class="sxs-lookup"><span data-stu-id="4c872-155">Return the Value from a Function Call</span></span>

<span data-ttu-id="4c872-156">Enfin, si une fonction a un état de première classe dans un langage, vous devez être en mesure de renvoyer la valeur d’un appel de fonction, tout comme retourner d’autres types, tels que des entiers et des chaînes.</span><span class="sxs-lookup"><span data-stu-id="4c872-156">Finally, if a function has first-class status in a language, you must be able to return it as the value of a function call, just as you return other types, such as integers and strings.</span></span>

<span data-ttu-id="4c872-157">Les appels de fonction suivants retournent des entiers et les affichent.</span><span class="sxs-lookup"><span data-stu-id="4c872-157">The following function calls return integers and display them.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet29.fs)]

<span data-ttu-id="4c872-158">L’appel de fonction suivant retourne une chaîne.</span><span class="sxs-lookup"><span data-stu-id="4c872-158">The following function call returns a string.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet30.fs)]

<span data-ttu-id="4c872-159">L’appel de fonction suivant, déclaré inline, retourne une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="4c872-159">The following function call, declared inline, returns a Boolean value.</span></span> <span data-ttu-id="4c872-160">La valeur affichée est `True`.</span><span class="sxs-lookup"><span data-stu-id="4c872-160">The value displayed is `True`.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet31.fs)]

<span data-ttu-id="4c872-161">La possibilité de retourner une fonction en tant que la valeur d’un appel de fonction est la deuxième caractéristique des fonctions d’ordre supérieur.</span><span class="sxs-lookup"><span data-stu-id="4c872-161">The ability to return a function as the value of a function call is the second characteristic of higher-order functions.</span></span> <span data-ttu-id="4c872-162">Dans l’exemple suivant, `checkFor` est défini comme étant une fonction qui accepte un seul argument, `item`et retourne une nouvelle fonction en tant que sa valeur.</span><span class="sxs-lookup"><span data-stu-id="4c872-162">In the following example, `checkFor` is defined to be a function that takes one argument, `item`, and returns a new function as its value.</span></span> <span data-ttu-id="4c872-163">La fonction retournée prend une liste comme argument, `lst`et recherche `item` dans `lst`.</span><span class="sxs-lookup"><span data-stu-id="4c872-163">The returned function takes a list as its argument, `lst`, and searches for `item` in `lst`.</span></span> <span data-ttu-id="4c872-164">Si `item` est présent, la fonction retourne `true`.</span><span class="sxs-lookup"><span data-stu-id="4c872-164">If `item` is present, the function returns `true`.</span></span> <span data-ttu-id="4c872-165">Si `item` n’est pas présent, la fonction retourne `false`.</span><span class="sxs-lookup"><span data-stu-id="4c872-165">If `item` is not present, the function returns `false`.</span></span> <span data-ttu-id="4c872-166">Comme dans la section précédente, le code suivant utilise une fonction de la liste fournie, [List.exists](https://msdn.microsoft.com/library/15a3ebd5-98f0-44c0-8220-7dedec3e68a8), pour rechercher la liste.</span><span class="sxs-lookup"><span data-stu-id="4c872-166">As in the previous section, the following code uses a provided list function, [List.exists](https://msdn.microsoft.com/library/15a3ebd5-98f0-44c0-8220-7dedec3e68a8), to search the list.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet32.fs)]

<span data-ttu-id="4c872-167">Le code suivant utilise `checkFor` pour créer une nouvelle fonction qui accepte un seul argument, une liste et recherche 7 dans la liste.</span><span class="sxs-lookup"><span data-stu-id="4c872-167">The following code uses `checkFor` to create a new function that takes one argument, a list, and searches for 7 in the list.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet33.fs)]

<span data-ttu-id="4c872-168">L’exemple suivant utilise l’état de première classe de fonctions en F # pour déclarer une fonction, `compose`, qui retourne une composition de deux arguments de fonction.</span><span class="sxs-lookup"><span data-stu-id="4c872-168">The following example uses the first-class status of functions in F# to declare a function, `compose`, that returns a composition of two function arguments.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet34.fs)]

>[!NOTE]
<span data-ttu-id="4c872-169">Pour obtenir une version encore plus courte, consultez la section suivante, « Fonctions curryfiées ».</span><span class="sxs-lookup"><span data-stu-id="4c872-169">For an even shorter version, see the following section, "Curried Functions."</span></span>

<span data-ttu-id="4c872-170">Le code suivant envoie deux fonctions en tant qu’arguments à `compose`, à la fois de qui acceptent un argument unique du même type.</span><span class="sxs-lookup"><span data-stu-id="4c872-170">The following code sends two functions as arguments to `compose`, both of which take a single argument of the same type.</span></span> <span data-ttu-id="4c872-171">La valeur de retour est une nouvelle fonction qui est une composition de deux arguments de fonction.</span><span class="sxs-lookup"><span data-stu-id="4c872-171">The return value is a new function that is a composition of the two function arguments.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet35.fs)]

>[!NOTE]
<span data-ttu-id="4c872-172">F # fournit deux opérateurs, `<<` et `>>`, qui composent des fonctions.</span><span class="sxs-lookup"><span data-stu-id="4c872-172">F# provides two operators, `<<` and `>>`, that compose functions.</span></span> <span data-ttu-id="4c872-173">Par exemple, `let squareAndDouble2 = doubleIt << squareIt` équivaut à `let squareAndDouble = compose doubleIt squareIt` dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="4c872-173">For example, `let squareAndDouble2 = doubleIt << squareIt` is equivalent to `let squareAndDouble = compose doubleIt squareIt` in the previous example.</span></span>

<span data-ttu-id="4c872-174">L’exemple de retour d’une fonction en tant que la valeur d’un appel de fonction suivant crée un jeu d’estimation simple.</span><span class="sxs-lookup"><span data-stu-id="4c872-174">The following example of returning a function as the value of a function call creates a simple guessing game.</span></span> <span data-ttu-id="4c872-175">Pour créer un jeu, appelez `makeGame` avec la valeur que vous voulez que quelqu'un à deviner envoyé pour `target`.</span><span class="sxs-lookup"><span data-stu-id="4c872-175">To create a game, call `makeGame` with the value that you want someone to guess sent in for `target`.</span></span> <span data-ttu-id="4c872-176">La valeur de retour à partir de la fonction `makeGame` est une fonction qui prend un argument (l’estimation) et indique si l’estimation est correcte.</span><span class="sxs-lookup"><span data-stu-id="4c872-176">The return value from function `makeGame` is a function that takes one argument (the guess) and reports whether the guess is correct.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet36.fs)]

<span data-ttu-id="4c872-177">Le code suivant appelle `makeGame`, envoi de la valeur `7` pour `target`.</span><span class="sxs-lookup"><span data-stu-id="4c872-177">The following code calls `makeGame`, sending the value `7` for `target`.</span></span> <span data-ttu-id="4c872-178">Identificateur `playGame` est lié à l’expression lambda retournée.</span><span class="sxs-lookup"><span data-stu-id="4c872-178">Identifier `playGame` is bound to the returned lambda expression.</span></span> <span data-ttu-id="4c872-179">Par conséquent, `playGame` est une fonction qui prend comme une argument valeur pour `guess`.</span><span class="sxs-lookup"><span data-stu-id="4c872-179">Therefore, `playGame` is a function that takes as its one argument a value for `guess`.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet37.fs)]

## <a name="curried-functions"></a><span data-ttu-id="4c872-180">Fonctions curryfiées</span><span class="sxs-lookup"><span data-stu-id="4c872-180">Curried Functions</span></span>

<span data-ttu-id="4c872-181">La plupart des exemples dans la section précédente peuvent être écrites plus concise en tirant parti de l’implicite *curryfication* dans les déclarations de fonction F #.</span><span class="sxs-lookup"><span data-stu-id="4c872-181">Many of the examples in the previous section can be written more concisely by taking advantage of the implicit *currying* in F# function declarations.</span></span> <span data-ttu-id="4c872-182">La curryfication est un processus qui transforme une fonction qui a plusieurs paramètres dans une série de fonctions intégrées, chacun d’eux possède un seul paramètre.</span><span class="sxs-lookup"><span data-stu-id="4c872-182">Currying is a process that transforms a function that has more than one parameter into a series of embedded functions, each of which has a single parameter.</span></span> <span data-ttu-id="4c872-183">En F #, les fonctions qui ont plusieurs paramètres sont intrinsèquement curryfiées.</span><span class="sxs-lookup"><span data-stu-id="4c872-183">In F#, functions that have more than one parameter are inherently curried.</span></span> <span data-ttu-id="4c872-184">Par exemple, `compose` à partir de la section précédente peut être écrite comme indiqué dans le style concis suivant, avec trois paramètres.</span><span class="sxs-lookup"><span data-stu-id="4c872-184">For example, `compose` from the previous section can be written as shown in the following concise style, with three parameters.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet38.fs)]

<span data-ttu-id="4c872-185">Toutefois, le résultat est une fonction d’un paramètre qui retourne une fonction d’un paramètre qui retourne à son tour une autre fonction d’un paramètre, comme indiqué dans `compose4curried`.</span><span class="sxs-lookup"><span data-stu-id="4c872-185">However, the result is a function of one parameter that returns a function of one parameter that in turn returns another function of one parameter, as shown in `compose4curried`.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet39.fs)]

<span data-ttu-id="4c872-186">Vous pouvez accéder à cette fonction de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="4c872-186">You can access this function in several ways.</span></span> <span data-ttu-id="4c872-187">Chacun des exemples suivants retourne et affiche 18.</span><span class="sxs-lookup"><span data-stu-id="4c872-187">Each of the following examples returns and displays 18.</span></span> <span data-ttu-id="4c872-188">Vous pouvez remplacer `compose4` avec `compose4curried` dans chacun des exemples.</span><span class="sxs-lookup"><span data-stu-id="4c872-188">You can replace `compose4` with `compose4curried` in any of the examples.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet40.fs)]

<span data-ttu-id="4c872-189">Pour vérifier que la fonction fonctionne toujours comme avant, essayez à nouveau les cas de test d’origine.</span><span class="sxs-lookup"><span data-stu-id="4c872-189">To verify that the function still works as it did before, try the original test cases again.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet41.fs)]

>[!NOTE]
<span data-ttu-id="4c872-190">Vous pouvez limiter la curryfication en englobant les paramètres dans les tuples.</span><span class="sxs-lookup"><span data-stu-id="4c872-190">You can restrict currying by enclosing parameters in tuples.</span></span> <span data-ttu-id="4c872-191">Pour plus d’informations, consultez « Modèles de paramètre » dans [paramètres et Arguments](../language-reference/parameters-and-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="4c872-191">For more information, see "Parameter Patterns" in [Parameters and Arguments](../language-reference/parameters-and-arguments.md).</span></span>

<span data-ttu-id="4c872-192">L’exemple suivant utilise des curryfication implicite pour écrire une version plus courte de `makeGame`.</span><span class="sxs-lookup"><span data-stu-id="4c872-192">The following example uses implicit currying to write a shorter version of `makeGame`.</span></span> <span data-ttu-id="4c872-193">Les détails de la façon `makeGame` construit et retourne le `game` fonction n’est pas explicitement dans ce format, mais vous pouvez vérifier en utilisant les cas de test d’origine que le résultat est le même.</span><span class="sxs-lookup"><span data-stu-id="4c872-193">The details of how `makeGame` constructs and returns the `game` function are less explicit in this format, but you can verify by using the original test cases that the result is the same.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet42.fs)]

<span data-ttu-id="4c872-194">Pour plus d’informations sur la curryfication, consultez « Application partielle d’Arguments » dans [fonctions](../language-reference/functions/index.md).</span><span class="sxs-lookup"><span data-stu-id="4c872-194">For more information about currying, see "Partial Application of Arguments" in [Functions](../language-reference/functions/index.md).</span></span>

## <a name="identifier-and-function-definition-are-interchangeable"></a><span data-ttu-id="4c872-195">Identificateur et la définition de fonction sont interchangeables</span><span class="sxs-lookup"><span data-stu-id="4c872-195">Identifier and Function Definition Are Interchangeable</span></span>

<span data-ttu-id="4c872-196">Le nom de variable `num` dans les précédents exemples évalue à l’entier 10, et il n’est pas surprenant dans laquelle `num` est valide, 10 est également valide.</span><span class="sxs-lookup"><span data-stu-id="4c872-196">The variable name `num` in the previous examples evaluates to the integer 10, and it is no surprise that where `num` is valid, 10 is also valid.</span></span> <span data-ttu-id="4c872-197">Cela vaut identificateurs de fonction et leurs valeurs : partout où le nom de la fonction peut être utilisé, l’expression lambda à laquelle il est lié peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="4c872-197">The same is true of function identifiers and their values: anywhere the name of the function can be used, the lambda expression to which it is bound can be used.</span></span>

<span data-ttu-id="4c872-198">L’exemple suivant définit un `Boolean` fonction appelée `isNegative`, puis utilise le nom de la fonction et la définition de la fonction indifféremment.</span><span class="sxs-lookup"><span data-stu-id="4c872-198">The following example defines a `Boolean` function called `isNegative`, and then uses the name of the function and the definition of the function interchangeably.</span></span> <span data-ttu-id="4c872-199">Les trois exemples suivants retournent et affichent tous `False`.</span><span class="sxs-lookup"><span data-stu-id="4c872-199">The next three examples all return and display `False`.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet43.fs)]

<span data-ttu-id="4c872-200">Pour aller plus loin il une seule étape, remplacez la valeur qui `applyIt` lié à pour `applyIt`.</span><span class="sxs-lookup"><span data-stu-id="4c872-200">To take it one step further, substitute the value that `applyIt` is bound to for `applyIt`.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet44.fs)]

## <a name="functions-are-first-class-values-in-f"></a><span data-ttu-id="4c872-201">Les fonctions sont des valeurs de première classe f\#</span><span class="sxs-lookup"><span data-stu-id="4c872-201">Functions Are First-Class Values in F\#</span></span>

<span data-ttu-id="4c872-202">Les exemples dans les sections précédentes montrent que les fonctions en F # satisfont les critères de valeurs de première classe en F #:</span><span class="sxs-lookup"><span data-stu-id="4c872-202">The examples in the previous sections demonstrate that functions in F# satisfy the criteria for being first-class values in F#:</span></span>

- <span data-ttu-id="4c872-203">Vous pouvez lier un identificateur à une définition de fonction.</span><span class="sxs-lookup"><span data-stu-id="4c872-203">You can bind an identifier to a function definition.</span></span>
[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet21.fs)]

- <span data-ttu-id="4c872-204">Vous pouvez stocker une fonction dans une structure de données.</span><span class="sxs-lookup"><span data-stu-id="4c872-204">You can store a function in a data structure.</span></span>
[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet45.fs)]

- <span data-ttu-id="4c872-205">Vous pouvez passer une fonction en tant qu’argument.</span><span class="sxs-lookup"><span data-stu-id="4c872-205">You can pass a function as an argument.</span></span>
[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet46.fs)]

- <span data-ttu-id="4c872-206">Vous pouvez retourner une fonction en tant que la valeur d’un appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="4c872-206">You can return a function as the value of a function call.</span></span>
[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet32.fs)]

<span data-ttu-id="4c872-207">Pour plus d’informations sur F #, consultez le [référence du langage F #](../language-reference/index.md).</span><span class="sxs-lookup"><span data-stu-id="4c872-207">For more information about F#, see the [F# Language Reference](../language-reference/index.md).</span></span>

## <a name="example"></a><span data-ttu-id="4c872-208">Exemple</span><span class="sxs-lookup"><span data-stu-id="4c872-208">Example</span></span>

### <a name="description"></a><span data-ttu-id="4c872-209">Description</span><span class="sxs-lookup"><span data-stu-id="4c872-209">Description</span></span>

<span data-ttu-id="4c872-210">Le code suivant contient tous les exemples dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="4c872-210">The following code contains all the examples in this topic.</span></span>

### <a name="code"></a><span data-ttu-id="4c872-211">Code</span><span class="sxs-lookup"><span data-stu-id="4c872-211">Code</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/contour/snippet47.fs)]

## <a name="see-also"></a><span data-ttu-id="4c872-212">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c872-212">See also</span></span>

- [<span data-ttu-id="4c872-213">Listes</span><span class="sxs-lookup"><span data-stu-id="4c872-213">Lists</span></span>](../language-reference/lists.md)
- [<span data-ttu-id="4c872-214">Tuples</span><span class="sxs-lookup"><span data-stu-id="4c872-214">Tuples</span></span>](../language-reference/tuples.md)
- [<span data-ttu-id="4c872-215">Fonctions</span><span class="sxs-lookup"><span data-stu-id="4c872-215">Functions</span></span>](../language-reference/functions/index.md)
- [<span data-ttu-id="4c872-216">`let` liaisons</span><span class="sxs-lookup"><span data-stu-id="4c872-216">`let` Bindings</span></span>](../language-reference/functions/let-bindings.md)
- [<span data-ttu-id="4c872-217">Expressions lambda : Le `fun` mot clé</span><span class="sxs-lookup"><span data-stu-id="4c872-217">Lambda Expressions: The `fun` Keyword</span></span>](../language-reference/functions/lambda-expressions-the-fun-keyword.md)
