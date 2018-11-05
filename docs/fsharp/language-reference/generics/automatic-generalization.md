---
title: Généralisation automatique (F#)
description: 'Découvrez comment F # généralise automatiquement les arguments et les types de fonctions afin qu’ils fonctionnent avec plusieurs types lorsque cela est possible.'
ms.date: 05/16/2016
ms.openlocfilehash: 84de9cbb2b9fcf2488393f7dbdfc3b610cdcffb0
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "43855775"
---
# <a name="automatic-generalization"></a><span data-ttu-id="0fca1-103">Généralisation automatique</span><span class="sxs-lookup"><span data-stu-id="0fca1-103">Automatic Generalization</span></span>

<span data-ttu-id="0fca1-104">F # utilise l’inférence de type pour évaluer les types de fonctions et d’expressions.</span><span class="sxs-lookup"><span data-stu-id="0fca1-104">F# uses type inference to evaluate the types of functions and expressions.</span></span> <span data-ttu-id="0fca1-105">Cette rubrique décrit comment F # généralise automatiquement les arguments et les types de fonctions afin qu’ils fonctionnent avec plusieurs types lorsque cela est possible.</span><span class="sxs-lookup"><span data-stu-id="0fca1-105">This topic describes how F# automatically generalizes the arguments and types of functions so that they work with multiple types when this is possible.</span></span>

## <a name="automatic-generalization"></a><span data-ttu-id="0fca1-106">Généralisation automatique</span><span class="sxs-lookup"><span data-stu-id="0fca1-106">Automatic Generalization</span></span>

<span data-ttu-id="0fca1-107">Le compilateur F #, lorsqu’il effectue l’inférence de type sur une fonction, détermine si un paramètre donné peut être générique.</span><span class="sxs-lookup"><span data-stu-id="0fca1-107">The F# compiler, when it performs type inference on a function, determines whether a given parameter can be generic.</span></span> <span data-ttu-id="0fca1-108">Le compilateur examine chaque paramètre et détermine si la fonction a une dépendance sur le type spécifique de ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="0fca1-108">The compiler examines each parameter and determines whether the function has a dependency on the specific type of that parameter.</span></span> <span data-ttu-id="0fca1-109">Si elle n’est pas le cas, le type est déduit de manière générique.</span><span class="sxs-lookup"><span data-stu-id="0fca1-109">If it does not, the type is inferred to be generic.</span></span>

<span data-ttu-id="0fca1-110">L’exemple de code suivant illustre une fonction que le compilateur déduit pour être générique.</span><span class="sxs-lookup"><span data-stu-id="0fca1-110">The following code example illustrates a function that the compiler infers to be generic.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-3/snippet101.fs)]

<span data-ttu-id="0fca1-111">Le type est déduit pour être `'a -> 'a -> 'a`.</span><span class="sxs-lookup"><span data-stu-id="0fca1-111">The type is inferred to be `'a -> 'a -> 'a`.</span></span>

<span data-ttu-id="0fca1-112">Le type indique qu’il s’agit d’une fonction qui accepte deux arguments du même type inconnu et retourne une valeur de ce même type.</span><span class="sxs-lookup"><span data-stu-id="0fca1-112">The type indicates that this is a function that takes two arguments of the same unknown type and returns a value of that same type.</span></span> <span data-ttu-id="0fca1-113">Une des raisons qui la fonction précédente peut être générique est que le plus grand-que l’opérateur (`>`) lui-même est générique.</span><span class="sxs-lookup"><span data-stu-id="0fca1-113">One of the reasons that the previous function can be generic is that the greater-than operator (`>`) is itself generic.</span></span> <span data-ttu-id="0fca1-114">Le plus grand-que l’opérateur a la signature `'a -> 'a -> bool`.</span><span class="sxs-lookup"><span data-stu-id="0fca1-114">The greater-than operator has the signature `'a -> 'a -> bool`.</span></span> <span data-ttu-id="0fca1-115">Tous les opérateurs ne sont génériques, et si le code dans une fonction utilise un type de paramètre avec une fonction non générique ou un opérateur, ce type de paramètre ne peut pas être généralisé.</span><span class="sxs-lookup"><span data-stu-id="0fca1-115">Not all operators are generic, and if the code in a function uses a parameter type together with a non-generic function or operator, that parameter type cannot be generalized.</span></span>

<span data-ttu-id="0fca1-116">Étant donné que `max` est générique, il peut être utilisé avec types tels que `int`, `float`, et ainsi de suite, comme indiqué dans les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="0fca1-116">Because `max` is generic, it can be used with types such as `int`, `float`, and so on, as shown in the following examples.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-3/snippet102.fs)]

<span data-ttu-id="0fca1-117">Toutefois, les deux arguments doivent être du même type.</span><span class="sxs-lookup"><span data-stu-id="0fca1-117">However, the two arguments must be of the same type.</span></span> <span data-ttu-id="0fca1-118">La signature est `'a -> 'a -> 'a`, et non `'a -> 'b -> 'a`.</span><span class="sxs-lookup"><span data-stu-id="0fca1-118">The signature is `'a -> 'a -> 'a`, not `'a -> 'b -> 'a`.</span></span> <span data-ttu-id="0fca1-119">Par conséquent, le code suivant génère une erreur car les types ne correspondent pas.</span><span class="sxs-lookup"><span data-stu-id="0fca1-119">Therefore, the following code produces an error because the types do not match.</span></span>

```fsharp
// Error: type mismatch.
let biggestIntFloat = max 2.0 3
```

<span data-ttu-id="0fca1-120">Le `max` fonction fonctionne également avec tout type qui prend en charge la plus grande-que l’opérateur.</span><span class="sxs-lookup"><span data-stu-id="0fca1-120">The `max` function also works with any type that supports the greater-than operator.</span></span> <span data-ttu-id="0fca1-121">Par conséquent, vous pouvez également l’utiliser sur une chaîne, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="0fca1-121">Therefore, you could also use it on a string, as shown in the following code.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-3/snippet104.fs)]

## <a name="value-restriction"></a><span data-ttu-id="0fca1-122">Restriction de valeur</span><span class="sxs-lookup"><span data-stu-id="0fca1-122">Value Restriction</span></span>

<span data-ttu-id="0fca1-123">Le compilateur exécute la généralisation automatique uniquement sur les définitions de fonction complètes qui ont des arguments explicites et sur des valeurs immuables simples.</span><span class="sxs-lookup"><span data-stu-id="0fca1-123">The compiler performs automatic generalization only on complete function definitions that have explicit arguments, and on simple immutable values.</span></span>

<span data-ttu-id="0fca1-124">Cela signifie que le compilateur émet une erreur si vous essayez de compiler le code qui n’est pas suffisamment contraint à être un type spécifique, mais est également pas généralisable.</span><span class="sxs-lookup"><span data-stu-id="0fca1-124">This means that the compiler issues an error if you try to compile code that is not sufficiently constrained to be a specific type, but is also not generalizable.</span></span> <span data-ttu-id="0fca1-125">Pour résoudre ce problème, le message d’erreur fait référence à cette restriction sur la généralisation automatique pour les valeurs en tant que le *restriction de valeur*.</span><span class="sxs-lookup"><span data-stu-id="0fca1-125">The error message for this problem refers to this restriction on automatic generalization for values as the *value restriction*.</span></span>

<span data-ttu-id="0fca1-126">En règle générale, l’erreur de restriction de valeur se produit lorsqu’une construction de manière générique, mais le compilateur comprend des informations insuffisantes pour la généraliser, ou lorsque vous omettez involontairement des informations de type suffisantes dans une construction non générique.</span><span class="sxs-lookup"><span data-stu-id="0fca1-126">Typically, the value restriction error occurs either when you want a construct to be generic but the compiler has insufficient information to generalize it, or when you unintentionally omit sufficient type information in a nongeneric construct.</span></span> <span data-ttu-id="0fca1-127">La solution à l’erreur de restriction de valeur consiste à fournir des informations plus explicites pour contraindre plus en détail le problème de l’inférence de type, dans une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="0fca1-127">The solution to the value restriction error is to provide more explicit information to more fully constrain the type inference problem, in one of the following ways:</span></span>

- <span data-ttu-id="0fca1-128">Contraindre un type à être générique en ajoutant une annotation de type explicite à une valeur ou un paramètre.</span><span class="sxs-lookup"><span data-stu-id="0fca1-128">Constrain a type to be nongeneric by adding an explicit type annotation to a value or parameter.</span></span>

- <span data-ttu-id="0fca1-129">Si le problème utilise une construction non généralisable pour définir une fonction générique, par exemple une composition de fonction ou incomplète des arguments de fonction curryfiée appliqués, essayez de réécrire la fonction comme une définition de fonction ordinaire.</span><span class="sxs-lookup"><span data-stu-id="0fca1-129">If the problem is using a nongeneralizable construct to define a generic function, such as a function composition or incompletely applied curried function arguments, try to rewrite the function as an ordinary function definition.</span></span>

- <span data-ttu-id="0fca1-130">Si le problème est une expression qui est trop complexe pour être généralisée, rendre une fonction en ajoutant un paramètre supplémentaire inutilisé.</span><span class="sxs-lookup"><span data-stu-id="0fca1-130">If the problem is an expression that is too complex to be generalized, make it into a function by adding an extra, unused parameter.</span></span>

- <span data-ttu-id="0fca1-131">Ajouter des paramètres de type générique explicites.</span><span class="sxs-lookup"><span data-stu-id="0fca1-131">Add explicit generic type parameters.</span></span> <span data-ttu-id="0fca1-132">Cette option est rarement utilisée.</span><span class="sxs-lookup"><span data-stu-id="0fca1-132">This option is rarely used.</span></span>

- <span data-ttu-id="0fca1-133">Les exemples de code suivants illustrent chacun de ces scénarios.</span><span class="sxs-lookup"><span data-stu-id="0fca1-133">The following code examples illustrate each of these scenarios.</span></span>

<span data-ttu-id="0fca1-134">Cas 1 : Expression trop complexe.</span><span class="sxs-lookup"><span data-stu-id="0fca1-134">Case 1: Too complex an expression.</span></span> <span data-ttu-id="0fca1-135">Dans cet exemple, la liste `counter` est destinée à être `int option ref`, mais il n’est pas défini comme une valeur immuable simple.</span><span class="sxs-lookup"><span data-stu-id="0fca1-135">In this example, the list `counter` is intended to be `int option ref`, but it is not defined as a simple immutable value.</span></span>

```fsharp
let counter = ref None
// Adding a type annotation fixes the problem:
let counter : int option ref = ref None
```

<span data-ttu-id="0fca1-136">Cas 2 : Utilisation d’une construction non généralisable pour définir une fonction générique.</span><span class="sxs-lookup"><span data-stu-id="0fca1-136">Case 2: Using a nongeneralizable construct to define a generic function.</span></span> <span data-ttu-id="0fca1-137">Dans cet exemple, la construction est non généralisable, car il implique l’application partielle d’arguments de fonction.</span><span class="sxs-lookup"><span data-stu-id="0fca1-137">In this example, the construct is nongeneralizable because it involves partial application of function arguments.</span></span>

```fsharp
let maxhash = max << hash
// The following is acceptable because the argument for maxhash is explicit:
let maxhash obj = (max << hash) obj
```

<span data-ttu-id="0fca1-138">Cas 3 : Ajout d’un paramètre supplémentaire inutilisé.</span><span class="sxs-lookup"><span data-stu-id="0fca1-138">Case 3: Adding an extra, unused parameter.</span></span> <span data-ttu-id="0fca1-139">Étant donné que cette expression n’est pas assez simple pour la généralisation, le compilateur émet l’erreur de restriction de valeur.</span><span class="sxs-lookup"><span data-stu-id="0fca1-139">Because this expression is not simple enough for generalization, the compiler issues the value restriction error.</span></span>

```fsharp
let emptyList10 = Array.create 10 []
// Adding an extra (unused) parameter makes it a function, which is generalizable.
let emptyList10 () = Array.create 10 []
```

<span data-ttu-id="0fca1-140">Cas 4 : Ajout type de paramètres.</span><span class="sxs-lookup"><span data-stu-id="0fca1-140">Case 4: Adding type parameters.</span></span>

```fsharp
let arrayOf10Lists = Array.create 10 []
// Adding a type parameter and type annotation lets you write a generic value.
let arrayOf10Lists<'T> = Array.create 10 ([]:'T list)
```

<span data-ttu-id="0fca1-141">Dans le dernier cas, la valeur devient une fonction de type, qui peut être utilisée pour créer des valeurs de nombreux types différents, par exemple comme suit :</span><span class="sxs-lookup"><span data-stu-id="0fca1-141">In the last case, the value becomes a type function, which may be used to create values of many different types, for example as follows:</span></span>

```fsharp
let intLists = arrayOf10Lists<int>
let floatLists = arrayOf10Lists<float>
```

## <a name="see-also"></a><span data-ttu-id="0fca1-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fca1-142">See also</span></span>

- [<span data-ttu-id="0fca1-143">Inférence de type</span><span class="sxs-lookup"><span data-stu-id="0fca1-143">Type Inference</span></span>](../type-inference.md)
- [<span data-ttu-id="0fca1-144">Génériques</span><span class="sxs-lookup"><span data-stu-id="0fca1-144">Generics</span></span>](index.md)
- [<span data-ttu-id="0fca1-145">Paramètres de type résolus statiquement</span><span class="sxs-lookup"><span data-stu-id="0fca1-145">Statically Resolved Type Parameters</span></span>](statically-resolved-type-parameters.md)
- [<span data-ttu-id="0fca1-146">Contraintes</span><span class="sxs-lookup"><span data-stu-id="0fca1-146">Constraints</span></span>](constraints.md)
