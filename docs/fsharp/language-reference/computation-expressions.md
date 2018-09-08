---
title: Expressions de calcul (F#)
description: 'Découvrez comment créer une syntaxe pratique pour l’écriture de calculs en F # qui peuvent être séquencés et combinés à l’aide de liaisons et constructions de flux de contrôle.'
ms.date: 07/27/2018
ms.openlocfilehash: ce81af7966a436b3973de277fb2a78ec06f4c471
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44200062"
---
# <a name="computation-expressions"></a><span data-ttu-id="0e6cf-103">Expressions de calcul</span><span class="sxs-lookup"><span data-stu-id="0e6cf-103">Computation Expressions</span></span>

<span data-ttu-id="0e6cf-104">Expressions de calcul en F # fournissent une syntaxe pratique pour l’écriture de calculs qui peuvent être séquencés et combinés à l’aide de liaisons et constructions de flux de contrôle.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-104">Computation expressions in F# provide a convenient syntax for writing computations that can be sequenced and combined using control flow constructs and bindings.</span></span> <span data-ttu-id="0e6cf-105">En fonction du type d’expression de calcul, elles peuvent être considérés comme un moyen d’exprimer monades, monoids, monad transformateurs et les functors applicative.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-105">Depending on the kind of computation expression, they can be thought of as a way to express monads, monoids, monad transformers, and applicative functors.</span></span> <span data-ttu-id="0e6cf-106">Cependant, contrairement à d’autres langages (tels que *-notation* de Haskell), ils ne sont pas liées à une simple abstraction et que vous ne comptez pas sur les macros ou d’autres formes de métaprogrammation pour accomplir une syntaxe pratique et sensible au contexte.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-106">However, unlike other languages (such as *do-notation* in Haskell), they are not tied to a single abstraction, and do not rely on macros or other forms of metaprogramming to accomplish a convenient and context-sensitive syntax.</span></span>

## <a name="overview"></a><span data-ttu-id="0e6cf-107">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="0e6cf-107">Overview</span></span>

<span data-ttu-id="0e6cf-108">Les calculs peuvent prendre différentes formes.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-108">Computations can take many forms.</span></span> <span data-ttu-id="0e6cf-109">La forme la plus courante de calcul est une exécution monothread, qui est facile à comprendre et à modifier.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-109">The most common form of computation is single-threaded execution, which is easy to understand and modify.</span></span> <span data-ttu-id="0e6cf-110">Toutefois, pas toutes les formes de calcul sont aussi simples que d’une exécution monothread.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-110">However, not all forms of computation are as straightforward as single-threaded execution.</span></span> <span data-ttu-id="0e6cf-111">Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="0e6cf-111">Some examples include:</span></span>

* <span data-ttu-id="0e6cf-112">Calculs non déterministes</span><span class="sxs-lookup"><span data-stu-id="0e6cf-112">Non-deterministic computations</span></span>
* <span data-ttu-id="0e6cf-113">Calculs asynchrones</span><span class="sxs-lookup"><span data-stu-id="0e6cf-113">Asynchronous computations</span></span>
* <span data-ttu-id="0e6cf-114">Calculs effectful</span><span class="sxs-lookup"><span data-stu-id="0e6cf-114">Effectful computations</span></span>
* <span data-ttu-id="0e6cf-115">Calculs générative</span><span class="sxs-lookup"><span data-stu-id="0e6cf-115">Generative computations</span></span>

<span data-ttu-id="0e6cf-116">En règle générale, il existe *contextuelle* calculs que vous devez effectuer dans certaines parties d’une application.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-116">More generally, there are *context-sensitive* computations that you must perform in certain parts of an application.</span></span> <span data-ttu-id="0e6cf-117">Écrire du code contextuelle peut être difficile, car il est facile de calculs de « fuite » en dehors d’un contexte donné sans abstractions pour vous éviter de le faire.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-117">Writing context-sensitive code can be challenging, as it is easy to "leak" computations outside of a given context without abstractions to prevent you from doing so.</span></span> <span data-ttu-id="0e6cf-118">Ces abstractions sont souvent difficile à écrire vous-même, c’est pourquoi F # a une méthode généralisée pour faire ce qu’on appelle **expressions de calcul**.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-118">These abstractions are often challenging to write by yourself, which is why F# has a generalized way to do so called **computation expressions**.</span></span>

<span data-ttu-id="0e6cf-119">Expressions de calcul offrent un modèle uniforme de syntaxe et d’abstraction pour l’encodage des calculs contextuelles.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-119">Computation expressions offer a uniform syntax and abstraction model for encoding context-sensitive computations.</span></span>

<span data-ttu-id="0e6cf-120">Chaque expression de calcul est soutenue par un *Générateur* type.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-120">Every computation expression is backed by a *builder* type.</span></span> <span data-ttu-id="0e6cf-121">Le type de générateur de rapports définit les opérations qui sont disponibles pour l’expression de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-121">The builder type defines the operations that are available for the computation expression.</span></span> <span data-ttu-id="0e6cf-122">Consultez [création d’un nouveau Type d’Expression de calcul](computation-expressions.md#creating-a-new-type-of-computation-expression), qui montre comment créer une expression de calcul personnalisé.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-122">See [Creating a New Type of Computation Expression](computation-expressions.md#creating-a-new-type-of-computation-expression), which shows how to create a custom computation expression.</span></span>

### <a name="syntax-overview"></a><span data-ttu-id="0e6cf-123">Vue d’ensemble de la syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e6cf-123">Syntax overview</span></span>

<span data-ttu-id="0e6cf-124">Toutes les expressions de calcul ont la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="0e6cf-124">All computation expressions have the following form:</span></span>

```
builder-expr { cexper }
```

<span data-ttu-id="0e6cf-125">où `builder-expr` est le nom d’un type de générateur qui définit l’expression de calcul, et `cexper` est le corps de l’expression de l’expression de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-125">where `builder-expr` is the name of a builder type that defines the computation expression, and `cexper` is the expression body of the computation expression.</span></span> <span data-ttu-id="0e6cf-126">Par exemple, `async` code d’expression de calcul peut ressembler à ceci :</span><span class="sxs-lookup"><span data-stu-id="0e6cf-126">For example, `async` computation expression code can look like this:</span></span>

```fsharp
let fetchAndDownload url =
    async {
        let! data = downloadData url

        let processedData = processData data

        return processedData
    }
```

<span data-ttu-id="0e6cf-127">Une syntaxe spéciale, supplémentaire est disponible au sein d’une expression de calcul, comme indiqué dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-127">There is a special, additional syntax available within a computation expression, as shown in the previous example.</span></span> <span data-ttu-id="0e6cf-128">Les formes d’expression suivantes sont possibles avec les expressions de calcul :</span><span class="sxs-lookup"><span data-stu-id="0e6cf-128">The following expression forms are possible with computation expressions:</span></span>

```fsharp
expr { let! ... }
expr { do! ... }
expr { yield ... }
expr { yield! ... }
expr { return ... }
expr { return! ... }
expr { match! ... }
```

<span data-ttu-id="0e6cf-129">Chacune de ces mots clés et d’autres mots clés F # standard sont uniquement disponibles dans une expression de calcul s’ils ont été définis dans le type de générateur de rapports de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-129">Each of these keywords, and other standard F# keywords are only available in a computation expression if they have been defined in the backing builder type.</span></span> <span data-ttu-id="0e6cf-130">La seule exception à cela est `match!`, qui est lui-même liant syntaxique pour l’utilisation de `let!` suivie d’une correspondance de modèle sur le résultat.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-130">The only exception to this is `match!`, which is itself syntactic sugar for the use of `let!` followed by a pattern match on the result.</span></span>

<span data-ttu-id="0e6cf-131">Le type de générateur est un objet qui définit des méthodes spéciales qui régissent la manière de que combiner les fragments de l’expression de calcul ; Autrement dit, ses méthodes contrôlent le comportement de l’expression de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-131">The builder type is an object that defines special methods that govern the way the fragments of the computation expression are combined; that is, its methods control how the computation expression behaves.</span></span> <span data-ttu-id="0e6cf-132">Un autre moyen de décrire une classe de générateur est à dire qu’il vous permet de personnaliser l’opération de nombreuses constructions F #, telles que des boucles et des liaisons.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-132">Another way to describe a builder class is to say that it enables you to customize the operation of many F# constructs, such as loops and bindings.</span></span>

### `let!`

<span data-ttu-id="0e6cf-133">Le `let!` mot clé lie le résultat d’un appel à une autre expression de calcul à un nom :</span><span class="sxs-lookup"><span data-stu-id="0e6cf-133">The `let!` keyword binds the result of a call to another computation expression to a name:</span></span>

```fsharp
let doThingsAsync url =
    async {
        let! data = getDataAsync url
        ...
    }
```

<span data-ttu-id="0e6cf-134">Si vous liez l’appel à une expression de calcul avec `let`, vous n’obtiendrez pas le résultat de l’expression de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-134">If you bind the call to a computation expression with `let`, you will not get the result of the computation expression.</span></span> <span data-ttu-id="0e6cf-135">Au lieu de cela, vous serez l’avez liée la valeur de la *non réalisés* l’appel à cette expression de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-135">Instead, you will have bound the value of the *unrealized* call to that computation expression.</span></span> <span data-ttu-id="0e6cf-136">Utilisez `let!` à lier au résultat.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-136">Use `let!` to bind to the result.</span></span>

<span data-ttu-id="0e6cf-137">`let!` est défini par le `Bind(x, f)` membre sur le type de générateur de rapports.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-137">`let!` is defined by the `Bind(x, f)` member on the builder type.</span></span>

### `do!`

<span data-ttu-id="0e6cf-138">Le `do!` mot clé est pour l’appel d’une expression de calcul qui retourne un `unit`-comme type (défini par le `Zero` membre sur le générateur) :</span><span class="sxs-lookup"><span data-stu-id="0e6cf-138">The `do!` keyword is for calling a computation expression that returns a `unit`-like type (defined by the `Zero` member on the builder):</span></span>

```fsharp
let doThingsAsync data url =
    async {
        do! sumbitData data url
        ...
    }
```

<span data-ttu-id="0e6cf-139">Pour le [async workflow](asynchronous-workflows.md), ce type est `Async<unit>`.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-139">For the [async workflow](asynchronous-workflows.md), this type is `Async<unit>`.</span></span> <span data-ttu-id="0e6cf-140">Pour les autres expressions de calcul, le type est susceptible d’être `CExpType<unit>`.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-140">For other computation expressions, the type is likely to be `CExpType<unit>`.</span></span>

<span data-ttu-id="0e6cf-141">`do!` est défini par le `Bind(x, f)` membre sur le type de générateur de rapports, où `f` génère un `unit`.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-141">`do!` is defined by the `Bind(x, f)` member on the builder type, where `f` produces a `unit`.</span></span>

### `yield`

<span data-ttu-id="0e6cf-142">Le `yield` mot clé est de retourner une valeur à partir de l’expression de calcul afin qu’il peut être utilisé comme un <xref:System.Collections.Generic.IEnumerable%601>:</span><span class="sxs-lookup"><span data-stu-id="0e6cf-142">The `yield` keyword is for returning a value from the computation expression so that it can be consumed as an <xref:System.Collections.Generic.IEnumerable%601>:</span></span>

```fsharp
let squares =
    seq {
        for i in 1..10 do
            yield i * i
    }

for sq in squares do
    printfn "%d" sq
```

<span data-ttu-id="0e6cf-143">Comme avec la [yield mot clé dans C#](../../csharp/language-reference/keywords/yield.md), chaque élément dans l’expression de calcul est cédée car elle est itérée.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-143">As with the [yield keyword in C#](../../csharp/language-reference/keywords/yield.md), each element in the computation expression is yielded back as it is iterated.</span></span>

<span data-ttu-id="0e6cf-144">`yield` est défini par le `Yield(x)` membre sur le type de générateur de rapports, où `x` est l’élément à générer de nouveau.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-144">`yield` is defined by the `Yield(x)` member on the builder type, where `x` is the item to yield back.</span></span>

### `yield!`

<span data-ttu-id="0e6cf-145">Le `yield!` mot clé est pour la mise à plat une collection de valeurs à partir d’une expression de calcul :</span><span class="sxs-lookup"><span data-stu-id="0e6cf-145">The `yield!` keyword is for flattening a collection of values from a computation expression:</span></span>

```fsharp
let squares =
    seq {
        for i in 1..3 -> i * i
    }

let cubes =
    seq {
        for i in 1..3 -> i * i * i
    }

let squaresAndCubes =
    seq {
        yield! squares
        yield! cubes
    }

printfn "%A" squaresAndCubes // Prints - 1; 4; 9; 1; 8; 27
```

<span data-ttu-id="0e6cf-146">Lors de l’évaluation, l’expression de calcul appelées par `yield!` seront vous ses éléments a différé un par un, le résultat de mise à plat.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-146">When evaluated, the computation expression called by `yield!` will have its items yielded back one-by-one, flattening the result.</span></span>

<span data-ttu-id="0e6cf-147">`yield!` est défini par le `YieldFrom(x)` membre sur le type de générateur de rapports, où `x` est une collection de valeurs.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-147">`yield!` is defined by the `YieldFrom(x)` member on the builder type, where `x` is a collection of values.</span></span>

### `return`

<span data-ttu-id="0e6cf-148">Le `return` mot clé encapsule une valeur dans le type correspondant à l’expression de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-148">The `return` keyword wraps a value in the type corresponding to the computation expression.</span></span> <span data-ttu-id="0e6cf-149">Outre les expressions de calcul à l’aide de `yield`, il est utilisé pour une expression de calcul « terminé » :</span><span class="sxs-lookup"><span data-stu-id="0e6cf-149">Aside from computation expressions using `yield`, it is used to "complete" a computation expression:</span></span>

```fsharp
let req = // 'req' is of type is 'Async<data>'
    async {
        let! data = fetch url
        return data
    }

// 'result' is of type 'data'
let result = Async.RunSynchronously req
```

<span data-ttu-id="0e6cf-150">`return` est défini par le `Return(x)` membre sur le type de générateur de rapports, où `x` est l’élément à encapsuler.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-150">`return` is defined by the `Return(x)` member on the builder type, where `x` is the item to wrap.</span></span>

### `return!`

<span data-ttu-id="0e6cf-151">Le `return!` mot clé se rend compte de la valeur d’une expression de calcul et encapsule ce résultat dans le type correspondant à l’expression de calcul :</span><span class="sxs-lookup"><span data-stu-id="0e6cf-151">The `return!` keyword realizes the value of a computation expression and wraps that result in the type corresponding to the computation expression:</span></span>

```fsharp
let req = // 'req' is of type is 'Async<data>'
    async {
        return! fetch url
    }

// 'result' is of type 'data'
let result = Async.RunSynchronously req
```

<span data-ttu-id="0e6cf-152">`return!` est défini par le `ReturnFrom(x)` membre sur le type de générateur de rapports, où `x` est une autre expression de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-152">`return!` is defined by the `ReturnFrom(x)` member on the builder type, where `x` is another computation expression.</span></span>

### `match!`

<span data-ttu-id="0e6cf-153">En commençant par F # 4.5, le `match!` mot clé vous permet d’inline un appel à une autre correspondance d’expression et le modèle de calcul sur son résultat :</span><span class="sxs-lookup"><span data-stu-id="0e6cf-153">Starting with F# 4.5, the `match!` keyword allows you to inline a call to another computation expression and pattern match on its result:</span></span>

```fsharp
let doThingsAsync url =
    async {
        match! callService url with
        | Some data -> ...
        | None -> ...
    }
```

<span data-ttu-id="0e6cf-154">Lors de l’appel d’une expression de calcul avec `match!`, elle réalisera le résultat de l’appel comme `let!`.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-154">When calling a computation expression with `match!`, it will realize the result of the call like `let!`.</span></span> <span data-ttu-id="0e6cf-155">Il est souvent utilisé lors de l’appel à une expression de calcul où le résultat est un [facultatif](options.md).</span><span class="sxs-lookup"><span data-stu-id="0e6cf-155">This is often used when calling a computation expression where the result is an [optional](options.md).</span></span>

## <a name="built-in-computation-expressions"></a><span data-ttu-id="0e6cf-156">Expressions de calcul intégré</span><span class="sxs-lookup"><span data-stu-id="0e6cf-156">Built-in computation expressions</span></span>

<span data-ttu-id="0e6cf-157">La bibliothèque principale F # définit trois expressions de calcul intégré : [Expressions de séquence](sequences.md), [flux de travail asynchrones](asynchronous-workflows.md), et [Expressions de requête](query-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="0e6cf-157">The F# core library defines three built-in computation expressions: [Sequence Expressions](sequences.md), [Asynchronous Workflows](asynchronous-workflows.md), and [Query Expressions](query-expressions.md).</span></span>

## <a name="creating-a-new-type-of-computation-expression"></a><span data-ttu-id="0e6cf-158">Création d’un nouveau Type d’Expression de calcul</span><span class="sxs-lookup"><span data-stu-id="0e6cf-158">Creating a New Type of Computation Expression</span></span>

<span data-ttu-id="0e6cf-159">Vous pouvez définir les caractéristiques de vos propres expressions de calcul en créant une classe de générateur et en définissant certaines méthodes spéciales sur la classe.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-159">You can define the characteristics of your own computation expressions by creating a builder class and defining certain special methods on the class.</span></span> <span data-ttu-id="0e6cf-160">La classe de générateur peut éventuellement définir les méthodes comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-160">The builder class can optionally define the methods as listed in the following table.</span></span>

<span data-ttu-id="0e6cf-161">Le tableau suivant décrit les méthodes qui peuvent être utilisées dans une classe de générateur de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-161">The following table describes methods that can be used in a workflow builder class.</span></span>

|<span data-ttu-id="0e6cf-162">**Méthode**</span><span class="sxs-lookup"><span data-stu-id="0e6cf-162">**Method**</span></span>|<span data-ttu-id="0e6cf-163">**Signatures typiques**</span><span class="sxs-lookup"><span data-stu-id="0e6cf-163">**Typical signature(s)**</span></span>|<span data-ttu-id="0e6cf-164">**Description**</span><span class="sxs-lookup"><span data-stu-id="0e6cf-164">**Description**</span></span>|
|----|----|----|
|`Bind`|`M<'T> * ('T -> M<'U>) -> M<'U>`|<span data-ttu-id="0e6cf-165">Appelé pour `let!` et `do!` dans les expressions de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-165">Called for `let!` and `do!` in computation expressions.</span></span>|
|`Delay`|`(unit -> M<'T>) -> M<'T>`|<span data-ttu-id="0e6cf-166">Encapsule une expression de calcul en tant que fonction.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-166">Wraps a computation expression as a function.</span></span>|
|`Return`|`'T -> M<'T>`|<span data-ttu-id="0e6cf-167">Appelé pour `return` dans les expressions de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-167">Called for `return` in computation expressions.</span></span>|
|`ReturnFrom`|`M<'T> -> M<'T>`|<span data-ttu-id="0e6cf-168">Appelé pour `return!` dans les expressions de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-168">Called for `return!` in computation expressions.</span></span>|
|`Run`|<span data-ttu-id="0e6cf-169">`M<'T> -> M<'T>` ou</span><span class="sxs-lookup"><span data-stu-id="0e6cf-169">`M<'T> -> M<'T>` or</span></span><br /><br />`M<'T> -> 'T`|<span data-ttu-id="0e6cf-170">Exécute une expression de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-170">Executes a computation expression.</span></span>|
|`Combine`|<span data-ttu-id="0e6cf-171">`M<'T> * M<'T> -> M<'T>` ou</span><span class="sxs-lookup"><span data-stu-id="0e6cf-171">`M<'T> * M<'T> -> M<'T>` or</span></span><br /><br />`M<unit> * M<'T> -> M<'T>`|<span data-ttu-id="0e6cf-172">Appelée pour le séquencement dans les expressions de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-172">Called for sequencing in computation expressions.</span></span>|
|`For`|<span data-ttu-id="0e6cf-173">`seq<'T> * ('T -> M<'U>) -> M<'U>` ou</span><span class="sxs-lookup"><span data-stu-id="0e6cf-173">`seq<'T> * ('T -> M<'U>) -> M<'U>` or</span></span><br /><br />`seq<'T> * ('T -> M<'U>) -> seq<M<'U>>`|<span data-ttu-id="0e6cf-174">Appelé pour `for...do` expressions dans les expressions de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-174">Called for `for...do` expressions in computation expressions.</span></span>|
|`TryFinally`|`M<'T> * (unit -> unit) -> M<'T>`|<span data-ttu-id="0e6cf-175">Appelé pour `try...finally` expressions dans les expressions de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-175">Called for `try...finally` expressions in computation expressions.</span></span>|
|`TryWith`|`M<'T> * (exn -> M<'T>) -> M<'T>`|<span data-ttu-id="0e6cf-176">Appelé pour `try...with` expressions dans les expressions de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-176">Called for `try...with` expressions in computation expressions.</span></span>|
|`Using`|`'T * ('T -> M<'U>) -> M<'U> when 'U :> IDisposable`|<span data-ttu-id="0e6cf-177">Appelé pour `use` liaisons dans les expressions de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-177">Called for `use` bindings in computation expressions.</span></span>|
|`While`|`(unit -> bool) * M<'T> -> M<'T>`|<span data-ttu-id="0e6cf-178">Appelé pour `while...do` expressions dans les expressions de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-178">Called for `while...do` expressions in computation expressions.</span></span>|
|`Yield`|`'T -> M<'T>`|<span data-ttu-id="0e6cf-179">Appelé pour `yield` expressions dans les expressions de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-179">Called for `yield` expressions in computation expressions.</span></span>|
|`YieldFrom`|`M<'T> -> M<'T>`|<span data-ttu-id="0e6cf-180">Appelé pour `yield!` expressions dans les expressions de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-180">Called for `yield!` expressions in computation expressions.</span></span>|
|`Zero`|`unit -> M<'T>`|<span data-ttu-id="0e6cf-181">Appelé pour vide `else` branches de `if...then` expressions dans les expressions de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-181">Called for empty `else` branches of `if...then` expressions in computation expressions.</span></span>|

<span data-ttu-id="0e6cf-182">La plupart des méthodes dans une classe de générateur utilisent et retournent un `M<'T>` construct, qui est généralement un type défini séparément qui caractérise le genre des calculs combinés, par exemple, `Async<'T>` pour les flux de travail asynchrones et `Seq<'T>` pour les workflows de la séquence.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-182">Many of the methods in a builder class use and return an `M<'T>` construct, which is typically a separately defined type that characterizes the kind of computations being combined, for example, `Async<'T>` for asynchronous workflows and `Seq<'T>` for sequence workflows.</span></span> <span data-ttu-id="0e6cf-183">Les signatures de ces méthodes activez-les être combinées et imbriquées avec les autres, afin que l’objet de flux de travail retourné d’une construction qui peut être passé à la suivante.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-183">The signatures of these methods enable them to be combined and nested with each other, so that the workflow object returned from one construct can be passed to the next.</span></span> <span data-ttu-id="0e6cf-184">Le compilateur, lorsqu’il analyse une expression de calcul, convertit l’expression en une série d’appels de fonction imbriquée en utilisant les méthodes dans le tableau précédent et le code dans l’expression de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-184">The compiler, when it parses a computation expression, converts the expression into a series of nested function calls by using the methods in the preceding table and the code in the computation expression.</span></span>

<span data-ttu-id="0e6cf-185">L’expression imbriquée est au format suivant :</span><span class="sxs-lookup"><span data-stu-id="0e6cf-185">The nested expression is of the following form:</span></span>

```fsharp
builder.Run(builder.Delay(fun () -> {| cexpr |}))
```

<span data-ttu-id="0e6cf-186">Dans le code ci-dessus, les appels à `Run` et `Delay` sont omis s’ils ne sont pas définis dans la classe de générateur d’expression calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-186">In the above code, the calls to `Run` and `Delay` are omitted if they are not defined in the computation expression builder class.</span></span> <span data-ttu-id="0e6cf-187">Le corps de l’expression de calcul, désignée ici comme `{| cexpr |}`, est convertie en appels impliquant les méthodes de la classe de générateur de rapports par les traductions décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-187">The body of the computation expression, here denoted as `{| cexpr |}`, is translated into calls involving the methods of the builder class by the translations described in the following table.</span></span> <span data-ttu-id="0e6cf-188">L’expression de calcul `{| cexpr |}` est définie de manière récursive en fonction de ces traductions où `expr` est une expression F # et `cexpr` est une expression de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-188">The computation expression `{| cexpr |}` is defined recursively according to these translations where `expr` is an F# expression and `cexpr` is a computation expression.</span></span>

|<span data-ttu-id="0e6cf-189">Expression</span><span class="sxs-lookup"><span data-stu-id="0e6cf-189">Expression</span></span>|<span data-ttu-id="0e6cf-190">Traduction</span><span class="sxs-lookup"><span data-stu-id="0e6cf-190">Translation</span></span>|
|----------|-----------|
|<code>{&#124; let binding in cexpr &#124;}</code>|<code>let binding in {&#124; cexpr &#124;}</code>|
|<code>{&#124; let! pattern = expr in cexpr &#124;}</code>|<code>builder.Bind(expr, (fun pattern -> {&#124; cexpr &#124;}))</code>|
|<code>{&#124; do! expr in cexpr &#124;}</code>|<code>builder.Bind(expr, (fun () -> {&#124; cexpr &#124;}))</code>|
|<code>{&#124; yield expr &#124;}</code>|`builder.Yield(expr)`|
|<code>{&#124; yield! expr &#124;}</code>|`builder.YieldFrom(expr)`|
|<code>{&#124; return expr &#124;}</code>|`builder.Return(expr)`|
|<code>{&#124; return! expr &#124;}</code>|`builder.ReturnFrom(expr)`|
|<code>{&#124; use pattern = expr in cexpr &#124;}</code>|<code>builder.Using(expr, (fun pattern -> {&#124; cexpr &#124;}))</code>|
|<code>{&#124; use! value = expr in cexpr &#124;}</code>|<code>builder.Bind(expr, (fun value -> builder.Using(value, (fun value -> {&#124; cexpr &#124;}))))</code>|
|<code>{&#124; if expr then cexpr0 &#124;}</code>|<code>if expr then {&#124; cexpr0 &#124;} else binder.Zero()</code>|
|<code>{&#124; if expr then cexpr0 else cexpr1 &#124;}</code>|<code>if expr then {&#124; cexpr0 &#124;} else {&#124; cexpr1 &#124;}</code>|
|<code>{&#124; match expr with &#124; pattern_i -> cexpr_i &#124;}</code>|<code>match expr with &#124; pattern_i -> {&#124; cexpr_i &#124;}</code>|
|<code>{&#124; for pattern in expr do cexpr &#124;}</code>|<code>builder.For(enumeration, (fun pattern -> {&#124; cexpr &#124;}))</code>|
|<code>{&#124; for identifier = expr1 to expr2 do cexpr &#124;}</code>|<code>builder.For(enumeration, (fun identifier -> {&#124; cexpr &#124;}))</code>|
|<code>{&#124; while expr do cexpr &#124;}</code>|<code>builder.While(fun () -> expr), builder.Delay({&#124;cexpr &#124;})</code>|
|<code>{&#124; try cexpr with &#124; pattern_i -> expr_i &#124;}</code>|<code>builder.TryWith(builder.Delay({&#124; cexpr &#124;}), (fun value -> match value with &#124; pattern_i -> expr_i &#124; exn -> reraise exn)))</code>|
|<code>{&#124; try cexpr finally expr &#124;}</code>|<code>builder.TryFinally(builder.Delay( {&#124; cexpr &#124;}), (fun () -> expr))</code>|
|<code>{&#124; cexpr1; cexpr2 &#124;}</code>|<code>builder.Combine({&#124;cexpr1 &#124;}, {&#124; cexpr2 &#124;})</code>|
|<code>{&#124; other-expr; cexpr &#124;}</code>|<code>expr; {&#124; cexpr &#124;}</code>|
|<code>{&#124; other-expr &#124;}</code>|`expr; builder.Zero()`|
<span data-ttu-id="0e6cf-191">Dans le tableau précédent, `other-expr` décrit une expression qui ne figure pas dans le cas contraire dans la table.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-191">In the previous table, `other-expr` describes an expression that is not otherwise listed in the table.</span></span> <span data-ttu-id="0e6cf-192">Une classe de générateur est inutile d’implémenter toutes les méthodes et de prendre en charge toutes les traductions répertoriées dans le tableau précédent.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-192">A builder class does not need to implement all of the methods and support all of the translations listed in the previous table.</span></span> <span data-ttu-id="0e6cf-193">Ces constructions qui ne sont pas implémentées ne sont pas disponibles dans les expressions de calcul de ce type.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-193">Those constructs that are not implemented are not available in computation expressions of that type.</span></span> <span data-ttu-id="0e6cf-194">Par exemple, si vous ne souhaitez pas prendre en charge la `use` mot clé dans les expressions de calcul, vous pouvez omettre la définition de `Use` dans votre classe de générateur de rapports.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-194">For example, if you do not want to support the `use` keyword in your computation expressions, you can omit the definition of `Use` in your builder class.</span></span>

<span data-ttu-id="0e6cf-195">L’exemple de code suivant montre une expression de calcul qui encapsule un calcul telle qu’une série d’étapes qui peut être évaluée une seule étape à la fois.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-195">The following code example shows a computation expression that encapsulates a computation as a series of steps that can be evaluated one step at a time.</span></span> <span data-ttu-id="0e6cf-196">Un type d’union, de différencier `OkOrException`, encode l’état d’erreur de l’expression, telle qu’évaluée jusqu'à présent.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-196">A discriminated union type, `OkOrException`, encodes the error state of the expression as evaluated so far.</span></span> <span data-ttu-id="0e6cf-197">Ce code illustre plusieurs modèles classiques que vous pouvez utiliser dans vos expressions de calcul, telles que des implémentations de réutilisable de certaines des méthodes de générateur de rapports.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-197">This code demonstrates several typical patterns that you can use in your computation expressions, such as boilerplate implementations of some of the builder methods.</span></span>

```fsharp
// Computations that can be run step by step
type Eventually<'T> =
    | Done of 'T
    | NotYetDone of (unit -> Eventually<'T>)

module Eventually =
    // The bind for the computations. Append 'func' to the
    // computation.
    let rec bind func expr =
        match expr with
        | Done value -> NotYetDone (fun () -> func value)
        | NotYetDone work -> NotYetDone (fun () -> bind func (work()))

    // Return the final value wrapped in the Eventually type.
    let result value = Done value

    type OkOrException<'T> =
        | Ok of 'T
        | Exception of System.Exception

    // The catch for the computations. Stitch try/with throughout
    // the computation, and return the overall result as an OkOrException.
    let rec catch expr =
        match expr with
        | Done value -> result (Ok value)
        | NotYetDone work ->
            NotYetDone (fun () ->
                let res = try Ok(work()) with | exn -> Exception exn
                match res with
                | Ok cont -> catch cont // note, a tailcall
                | Exception exn -> result (Exception exn))

    // The delay operator.
    let delay func = NotYetDone (fun () -> func())

    // The stepping action for the computations.
    let step expr =
        match expr with
        | Done _ -> expr
        | NotYetDone func -> func ()

    // The rest of the operations are boilerplate.
    // The tryFinally operator.
    // This is boilerplate in terms of "result", "catch", and "bind".
    let tryFinally expr compensation =
        catch (expr)
        |> bind (fun res -> 
            compensation();
            match res with
            | Ok value -> result value
            | Exception exn -> raise exn)

    // The tryWith operator.
    // This is boilerplate in terms of "result", "catch", and "bind".
    let tryWith exn handler =
        catch exn
        |> bind (function Ok value -> result value | Exception exn -> handler exn)

    // The whileLoop operator.
    // This is boilerplate in terms of "result" and "bind".
    let rec whileLoop pred body =
        if pred() then body |> bind (fun _ -> whileLoop pred body)
        else result ()

    // The sequential composition operator.
    // This is boilerplate in terms of "result" and "bind".
    let combine expr1 expr2 =
        expr1 |> bind (fun () -> expr2)

    // The using operator.
    let using (resource: #System.IDisposable) func =
        tryFinally (func resource) (fun () -> resource.Dispose())

    // The forLoop operator.
    // This is boilerplate in terms of "catch", "result", and "bind".
    let forLoop (collection:seq<_>) func =
        let ie = collection.GetEnumerator()
        tryFinally 
            (whileLoop 
                (fun () -> ie.MoveNext()) 
                (delay (fun () -> let value = ie.Current in func value)))
            (fun () -> ie.Dispose())

// The builder class.
type EventuallyBuilder() =
    member x.Bind(comp, func) = Eventually.bind func comp
    member x.Return(value) = Eventually.result value
    member x.ReturnFrom(value) = value
    member x.Combine(expr1, expr2) = Eventually.combine expr1 expr2
    member x.Delay(func) = Eventually.delay func
    member x.Zero() = Eventually.result ()
    member x.TryWith(expr, handler) = Eventually.tryWith expr handler
    member x.TryFinally(expr, compensation) = Eventually.tryFinally expr compensation
    member x.For(coll:seq<_>, func) = Eventually.forLoop coll func
    member x.Using(resource, expr) = Eventually.using resource expr

let eventually = new EventuallyBuilder()

let comp = eventually {
    for x in 1..2 do
        printfn " x = %d" x
    return 3 + 4 }

// Try the remaining lines in F# interactive to see how this
// computation expression works in practice.
let step x = Eventually.step x

// returns "NotYetDone <closure>"
comp |> step

// prints "x = 1"
// returns "NotYetDone <closure>"
comp |> step |> step

// prints "x = 1"
// prints "x = 2"
// returns "NotYetDone <closure>"
comp |> step |> step |> step |> step |> step |> step

// prints "x = 1"
// prints "x = 2"
// returns "Done 7"
comp |> step |> step |> step |> step |> step |> step |> step |> step
```

<span data-ttu-id="0e6cf-198">Une expression de calcul a un type sous-jacent, ce qui retourne l’expression.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-198">A computation expression has an underlying type, which the expression returns.</span></span> <span data-ttu-id="0e6cf-199">Le type sous-jacent peut représenter un résultat du calcul ou un calcul retardé qui peut être effectué, ou elle peut fournir un moyen pour effectuer une itération dans un type de collection.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-199">The underlying type may represent a computed result or a delayed computation that can be performed, or it may provide a way to iterate through some type of collection.</span></span> <span data-ttu-id="0e6cf-200">Dans l’exemple précédent, le type sous-jacent a été **finalement**.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-200">In the previous example, the underlying type was **Eventually**.</span></span> <span data-ttu-id="0e6cf-201">Pour une expression de séquence, le type sous-jacent est <xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-201">For a sequence expression, the underlying type is <xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType>.</span></span> <span data-ttu-id="0e6cf-202">Pour une expression de requête, le type sous-jacent est <xref:System.Linq.IQueryable?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-202">For a query expression, the underlying type is <xref:System.Linq.IQueryable?displayProperty=nameWithType>.</span></span> <span data-ttu-id="0e6cf-203">Pour un flux de travail asynchrone, le type sous-jacent est [ `Async` ](https://msdn.microsoft.com/library/03eb4d12-a01a-4565-a077-5e83f17cf6f7).</span><span class="sxs-lookup"><span data-stu-id="0e6cf-203">For an asynchronous workflow, the underlying type is [`Async`](https://msdn.microsoft.com/library/03eb4d12-a01a-4565-a077-5e83f17cf6f7).</span></span> <span data-ttu-id="0e6cf-204">Le `Async` objet représente le travail à effectuer pour calculer le résultat.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-204">The `Async` object represents the work to be performed to compute the result.</span></span> <span data-ttu-id="0e6cf-205">Par exemple, vous appelez [ `Async.RunSynchronously` ](https://msdn.microsoft.com/library/0a6663a9-50f2-4d38-8bf3-cefd1a51fd6b) pour effectuer un calcul et de retourner le résultat.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-205">For example, you call [`Async.RunSynchronously`](https://msdn.microsoft.com/library/0a6663a9-50f2-4d38-8bf3-cefd1a51fd6b) to execute a computation and return the result.</span></span>

## <a name="custom-operations"></a><span data-ttu-id="0e6cf-206">Opérations personnalisées</span><span class="sxs-lookup"><span data-stu-id="0e6cf-206">Custom Operations</span></span>

<span data-ttu-id="0e6cf-207">Vous pouvez définir une opération personnalisée sur une expression de calcul et utiliser une opération personnalisée en tant qu’opérateur dans une expression de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-207">You can define a custom operation on a computation expression and use a custom operation as an operator in a computation expression.</span></span> <span data-ttu-id="0e6cf-208">Par exemple, vous pouvez inclure un opérateur de requête dans une expression de requête.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-208">For example, you can include a query operator in a query expression.</span></span> <span data-ttu-id="0e6cf-209">Lorsque vous définissez une opération personnalisée, vous devez définir le rendement et les méthodes dans l’expression de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-209">When you define a custom operation, you must define the Yield and For methods in the computation expression.</span></span> <span data-ttu-id="0e6cf-210">Pour définir une opération personnalisée, placez-le dans une classe de générateur pour l’expression de calcul, puis appliquer le [ `CustomOperationAttribute` ](https://msdn.microsoft.com/library/199f3927-79df-484b-ba66-85f58cc49b19).</span><span class="sxs-lookup"><span data-stu-id="0e6cf-210">To define a custom operation, put it in a builder class for the computation expression, and then apply the [`CustomOperationAttribute`](https://msdn.microsoft.com/library/199f3927-79df-484b-ba66-85f58cc49b19).</span></span> <span data-ttu-id="0e6cf-211">Cet attribut prend une chaîne en tant qu’argument, qui est le nom à utiliser dans une opération personnalisée.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-211">This attribute takes a string as an argument, which is the name to be used in a custom operation.</span></span> <span data-ttu-id="0e6cf-212">Ce nom est fourni dans la portée au début de l’accolade ouvrante de l’expression de calcul.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-212">This name comes into scope at the start of the opening curly brace of the computation expression.</span></span> <span data-ttu-id="0e6cf-213">Par conséquent, vous ne devez pas utiliser des identificateurs qui ont le même nom qu’une opération personnalisée dans ce bloc.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-213">Therefore, you shouldn’t use identifiers that have the same name as a custom operation in this block.</span></span> <span data-ttu-id="0e6cf-214">Par exemple, évitez l’utilisation des identificateurs comme `all` ou `last` dans les expressions de requête.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-214">For example, avoid the use of identifiers such as `all` or `last` in query expressions.</span></span>

### <a name="extending-existing-builders-with-new-custom-operations"></a><span data-ttu-id="0e6cf-215">Extension des générateurs existants avec les nouvelles opérations personnalisé</span><span class="sxs-lookup"><span data-stu-id="0e6cf-215">Extending existing Builders with new Custom Operations</span></span>

<span data-ttu-id="0e6cf-216">Si vous avez déjà une classe de générateur, ses opérations personnalisées peuvent être étendues d’en dehors de cette classe de générateur de rapports.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-216">If you already have a builder class, its custom operations can be extended from outside of this builder class.</span></span> <span data-ttu-id="0e6cf-217">Les extensions doivent être déclarées dans des modules.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-217">Extensions must be declared in modules.</span></span> <span data-ttu-id="0e6cf-218">Espaces de noms ne peut pas contenir de membres d’extension à l’exception dans le même fichier et le même groupe de déclaration d’espace de noms dans lequel le type est défini.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-218">Namespaces cannot contain extension members except in the same file and the same namespace declaration group where the type is defined.</span></span>

<span data-ttu-id="0e6cf-219">L’exemple suivant montre l’extension existants `Microsoft.FSharp.Linq.QueryBuilder` classe.</span><span class="sxs-lookup"><span data-stu-id="0e6cf-219">The following example shows the extension of the existing `Microsoft.FSharp.Linq.QueryBuilder` class.</span></span>

```fsharp
type Microsoft.FSharp.Linq.QueryBuilder with

    [<CustomOperation("existsNot")>]
    member __.ExistsNot (source: QuerySource<'T, 'Q>, predicate) =
        Enumerable.Any (source.Source, Func<_,_>(predicate)) |> not
```

## <a name="see-also"></a><span data-ttu-id="0e6cf-220">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e6cf-220">See also</span></span>

- [<span data-ttu-id="0e6cf-221">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="0e6cf-221">F# Language Reference</span></span>](index.md)
- [<span data-ttu-id="0e6cf-222">Flux de travail asynchrones</span><span class="sxs-lookup"><span data-stu-id="0e6cf-222">Asynchronous Workflows</span></span>](asynchronous-workflows.md)
- [<span data-ttu-id="0e6cf-223">Séquences</span><span class="sxs-lookup"><span data-stu-id="0e6cf-223">Sequences</span></span>](https://msdn.microsoft.com/library/6b773b6b-9c9a-4af8-bd9e-d96585c166db)
- [<span data-ttu-id="0e6cf-224">Expressions de requête</span><span class="sxs-lookup"><span data-stu-id="0e6cf-224">Query Expressions</span></span>](query-expressions.md)
