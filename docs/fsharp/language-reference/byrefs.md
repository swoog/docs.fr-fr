---
title: ByRef
description: En savoir plus sur byref et les types byref dans F#, qui sont utilisés pour la programmation de bas niveau.
ms.date: 09/02/2018
ms.openlocfilehash: c0bad26672fbb9eb315eee1c3e275183ddeb9297
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59055363"
---
# <a name="byrefs"></a><span data-ttu-id="9e9ec-103">ByRef</span><span class="sxs-lookup"><span data-stu-id="9e9ec-103">Byrefs</span></span>

<span data-ttu-id="9e9ec-104">F#a deux principaux domaines de fonctionnalités qui traitent dans l’espace de programmation de bas niveau :</span><span class="sxs-lookup"><span data-stu-id="9e9ec-104">F# has two major feature areas that deal in the space of low-level programming:</span></span>

* <span data-ttu-id="9e9ec-105">Le `byref` / `inref` / `outref` types, qui sont des pointeurs managés.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-105">The `byref`/`inref`/`outref` types, which are a managed pointers.</span></span> <span data-ttu-id="9e9ec-106">Ils ont des restrictions sur l’utilisation afin que vous ne pouvez pas compiler un programme qui n’est pas valide lors de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-106">They have restrictions on usage so that you cannot compile a program that is invalid at runtime.</span></span>
* <span data-ttu-id="9e9ec-107">Un `byref`-comme struct, qui est un [structure](structures.md) qui a une sémantique similaire et les mêmes restrictions de compilation que `byref<'T>`.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-107">A `byref`-like struct, which is a [structure](structures.md) that has similar semantics and the same compile-time restrictions as `byref<'T>`.</span></span> <span data-ttu-id="9e9ec-108">Par exemple, <xref:System.Span%601>.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-108">One example is <xref:System.Span%601>.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e9ec-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e9ec-109">Syntax</span></span>

```fsharp
// Byref types as parameters
let f (x: byref<'T>) = ()
let g (x: inref<'T>) = ()
let h (x: outref<'T>) = ()

// Calling a function with a byref parameter
let mutable x = 3
f &x

// Declaring a byref-like struct
open System.Runtime.CompilerServices

[<Struct; IsByRefLike>]
type S(count1: int, count2: int) =
    member x.Count1 = count1
    member x.Count2 = count2
```

## <a name="byref-inref-and-outref"></a><span data-ttu-id="9e9ec-110">ByRef, inref et outref</span><span class="sxs-lookup"><span data-stu-id="9e9ec-110">Byref, inref, and outref</span></span>

<span data-ttu-id="9e9ec-111">Il existe trois formes de `byref`:</span><span class="sxs-lookup"><span data-stu-id="9e9ec-111">There are three forms of `byref`:</span></span>

* <span data-ttu-id="9e9ec-112">`inref<'T>`, un pointeur managé pour lire la valeur sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-112">`inref<'T>`, a managed pointer for reading the underlying value.</span></span>
* <span data-ttu-id="9e9ec-113">`outref<'T>`, un pointeur managé pour écrire dans la valeur sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-113">`outref<'T>`, a managed pointer for writing to the underlying value.</span></span>
* <span data-ttu-id="9e9ec-114">`byref<'T>`, un pointeur managé pour lire et écrire la valeur sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-114">`byref<'T>`, a managed pointer for reading and writing the underlying value.</span></span>

<span data-ttu-id="9e9ec-115">Un `byref<'T>` peuvent être passés où un `inref<'T>` est attendu.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-115">A `byref<'T>` can be passed where an `inref<'T>` is expected.</span></span> <span data-ttu-id="9e9ec-116">De même, un `byref<'T>` peuvent être passés où un `outref<'T>` est attendu.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-116">Similarly, a `byref<'T>` can be passed where an `outref<'T>` is expected.</span></span>

## <a name="using-byrefs"></a><span data-ttu-id="9e9ec-117">À l’aide de valeurs ByRef</span><span class="sxs-lookup"><span data-stu-id="9e9ec-117">Using byrefs</span></span>

<span data-ttu-id="9e9ec-118">Pour utiliser un `inref<'T>`, vous devez obtenir une valeur de pointeur avec `&`:</span><span class="sxs-lookup"><span data-stu-id="9e9ec-118">To use a `inref<'T>`, you need to get a pointer value with `&`:</span></span>

```fsharp
open System

let f (dt: inref<DateTime>) =
    printfn "Now: %s" (dt.ToString())
    
let usage =
    let dt = DateTime.Now
    f &dt // Pass a pointer to 'dt'
```

<span data-ttu-id="9e9ec-119">Pour écrire dans le pointeur en utilisant un `outref<'T>` ou `byref<'T>`, vous devez également rendre la valeur que vous saisissez un pointeur vers `mutable`.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-119">To write to the pointer by using an `outref<'T>` or `byref<'T>`, you must also make the value you grab a pointer to `mutable`.</span></span>

```fsharp
open System

let f (dt: byref<DateTime>) =
    printfn "Now: %s" (dt.ToString())
    dt <- DateTime.Now

// Make 'dt' mutable
let mutable dt = DateTime.Now

// Now you can pass the pointer to 'dt'
f &dt
```

<span data-ttu-id="9e9ec-120">Si vous écrivez uniquement le pointeur au lieu de lire, envisagez d’utiliser `outref<'T>` au lieu de `byref<'T>`.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-120">If you are only writing the pointer instead of reading it, consider using `outref<'T>` instead of `byref<'T>`.</span></span>

### <a name="inref-semantics"></a><span data-ttu-id="9e9ec-121">Sémantique de Inref</span><span class="sxs-lookup"><span data-stu-id="9e9ec-121">Inref semantics</span></span>

<span data-ttu-id="9e9ec-122">Examinons le code ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-122">Consider the following code:</span></span>

```fsharp
let f (x: inref<SomeStruct>) = x.SomeField
```

<span data-ttu-id="9e9ec-123">Sémantiquement, cela signifie que les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="9e9ec-123">Semantically, this means the following:</span></span>

* <span data-ttu-id="9e9ec-124">Le titulaire de la `x` pointeur peut uniquement utiliser pour lire la valeur.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-124">The holder of the `x` pointer may only use it to read the value.</span></span>
* <span data-ttu-id="9e9ec-125">N’importe quel pointeur acquis à `struct` champs imbriqués `SomeStruct` sont de type donné `inref<_>`.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-125">Any pointer acquired to `struct` fields nested within `SomeStruct` are given type `inref<_>`.</span></span>

<span data-ttu-id="9e9ec-126">Les éléments suivants sont également vrai :</span><span class="sxs-lookup"><span data-stu-id="9e9ec-126">The following is also true:</span></span>

* <span data-ttu-id="9e9ec-127">Il est sans implication que d’autres threads ou alias n’ont pas accès en écriture à `x`.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-127">There is no implication that other threads or aliases do not have write access to `x`.</span></span>
* <span data-ttu-id="9e9ec-128">Il n’existe aucune implication qui `SomeStruct` est immuable en raison de `x` en cours un `inref`.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-128">There is no implication that `SomeStruct` is immutable by virtue of `x` being an `inref`.</span></span>

<span data-ttu-id="9e9ec-129">Toutefois, pour F# types valeur **sont** immuable, le `this` pointeur est déduit comme étant un `inref`.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-129">However, for F# value types that **are** immutable, the `this` pointer is inferred to be an `inref`.</span></span>

<span data-ttu-id="9e9ec-130">Toutes ces règles ensemble signifient que le titulaire d’un `inref` pointeur ne peut pas modifier le contenu immédiat de la mémoire qui est pointé.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-130">All of these rules together mean that the holder of an `inref` pointer may not modify the immediate contents of the memory being pointed to.</span></span>

### <a name="outref-semantics"></a><span data-ttu-id="9e9ec-131">Sémantique de Outref</span><span class="sxs-lookup"><span data-stu-id="9e9ec-131">Outref semantics</span></span>

<span data-ttu-id="9e9ec-132">L’objectif de `outref<'T>` consiste à indiquer que le pointeur doit uniquement être lu.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-132">The purpose of `outref<'T>` is to indicate that the pointer should only be read from.</span></span> <span data-ttu-id="9e9ec-133">De façon inattendue, `outref<'T>` autorise lecture sous-jacent valeur malgré son nom.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-133">Unexpectedly, `outref<'T>` permits reading the underlying value despite its name.</span></span> <span data-ttu-id="9e9ec-134">Il s’agit pour des raisons de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-134">This is for compatibility purposes.</span></span> <span data-ttu-id="9e9ec-135">Sémantiquement, `outref<'T>` n’est pas différent de celui `byref<'T>`.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-135">Semantically, `outref<'T>` is no different than `byref<'T>`.</span></span>

### <a name="interop-with-c"></a><span data-ttu-id="9e9ec-136">Interopérabilité avec C\#</span><span class="sxs-lookup"><span data-stu-id="9e9ec-136">Interop with C\#</span></span>

<span data-ttu-id="9e9ec-137">C# prend en charge la `in ref` et `out ref` mots clés, en plus de `ref` retourne.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-137">C# supports the `in ref` and `out ref` keywords, in addition to `ref` returns.</span></span> <span data-ttu-id="9e9ec-138">Le tableau suivant montre comment F# interprète ce que C# émet :</span><span class="sxs-lookup"><span data-stu-id="9e9ec-138">The following table shows how F# interprets what C# emits:</span></span>

|<span data-ttu-id="9e9ec-139">Construction de c#</span><span class="sxs-lookup"><span data-stu-id="9e9ec-139">C# construct</span></span>|<span data-ttu-id="9e9ec-140">F#déduit</span><span class="sxs-lookup"><span data-stu-id="9e9ec-140">F# infers</span></span>|
|------------|---------|
|<span data-ttu-id="9e9ec-141">`ref` Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9e9ec-141">`ref` return value</span></span>|`outref<'T>`|
|<span data-ttu-id="9e9ec-142">`ref readonly` Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9e9ec-142">`ref readonly` return value</span></span>|`inref<'T>`|
|<span data-ttu-id="9e9ec-143">`in ref` Paramètre</span><span class="sxs-lookup"><span data-stu-id="9e9ec-143">`in ref` parameter</span></span>|`inref<'T>`|
|<span data-ttu-id="9e9ec-144">`out ref` Paramètre</span><span class="sxs-lookup"><span data-stu-id="9e9ec-144">`out ref` parameter</span></span>|`outref<'T>`|

<span data-ttu-id="9e9ec-145">Le tableau suivant montre à quoi F# émet :</span><span class="sxs-lookup"><span data-stu-id="9e9ec-145">The following table shows what F# emits:</span></span>

|<span data-ttu-id="9e9ec-146">F#construction</span><span class="sxs-lookup"><span data-stu-id="9e9ec-146">F# construct</span></span>|<span data-ttu-id="9e9ec-147">Construction émise</span><span class="sxs-lookup"><span data-stu-id="9e9ec-147">Emitted construct</span></span>|
|------------|-----------------|
|<span data-ttu-id="9e9ec-148">`inref<'T>` argument</span><span class="sxs-lookup"><span data-stu-id="9e9ec-148">`inref<'T>` argument</span></span>|<span data-ttu-id="9e9ec-149">`[In]` attribut de l’argument</span><span class="sxs-lookup"><span data-stu-id="9e9ec-149">`[In]` attribute on argument</span></span>|
|<span data-ttu-id="9e9ec-150">`inref<'T>` retour</span><span class="sxs-lookup"><span data-stu-id="9e9ec-150">`inref<'T>` return</span></span>|<span data-ttu-id="9e9ec-151">`modreq` attribut de valeur</span><span class="sxs-lookup"><span data-stu-id="9e9ec-151">`modreq` attribute on value</span></span>|
|<span data-ttu-id="9e9ec-152">`inref<'T>` dans emplacement abstrait ou implémentation</span><span class="sxs-lookup"><span data-stu-id="9e9ec-152">`inref<'T>` in abstract slot or implementation</span></span>|<span data-ttu-id="9e9ec-153">`modreq` sur l’argument ou de retour</span><span class="sxs-lookup"><span data-stu-id="9e9ec-153">`modreq` on argument or return</span></span>|
|<span data-ttu-id="9e9ec-154">`outref<'T>` argument</span><span class="sxs-lookup"><span data-stu-id="9e9ec-154">`outref<'T>` argument</span></span>|<span data-ttu-id="9e9ec-155">`[Out]` attribut de l’argument</span><span class="sxs-lookup"><span data-stu-id="9e9ec-155">`[Out]` attribute on argument</span></span>|

### <a name="type-inference-and-overloading-rules"></a><span data-ttu-id="9e9ec-156">Inférence de type et les règles de surcharge</span><span class="sxs-lookup"><span data-stu-id="9e9ec-156">Type inference and overloading rules</span></span>

<span data-ttu-id="9e9ec-157">Un `inref<'T>` type est déduit par le F# compilateur dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="9e9ec-157">An `inref<'T>` type is inferred by the F# compiler in the following cases:</span></span>

1. <span data-ttu-id="9e9ec-158">Un type de paramètre ou de retour de .NET qui a un `IsReadOnly` attribut.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-158">A .NET parameter or return type that has an `IsReadOnly` attribute.</span></span>
2. <span data-ttu-id="9e9ec-159">Le `this` pointeur sur un type struct qui ne comporte aucun champ mutable.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-159">The `this` pointer on a struct type that has no mutable fields.</span></span>
3. <span data-ttu-id="9e9ec-160">L’adresse d’un emplacement mémoire dérivé d’un autre `inref<_>` pointeur.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-160">The address of a memory location derived from another `inref<_>` pointer.</span></span>

<span data-ttu-id="9e9ec-161">Lorsqu’une adresse implicite d’un `inref` est effectuée, une surcharge avec un argument de type `SomeType` est préférable à une surcharge avec un argument de type `inref<SomeType>`.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-161">When an implicit address of an `inref` is being taken, an overload with an argument of type `SomeType` is preferred to an overload with an argument of type `inref<SomeType>`.</span></span> <span data-ttu-id="9e9ec-162">Exemple :</span><span class="sxs-lookup"><span data-stu-id="9e9ec-162">For example:</span></span>

```fsharp
type C() =
    static member M(x: System.DateTime) = x.AddDays(1.0)
    static member M(x: inref<System.DateTime>) = x.AddDays(2.0)
    static member M2(x: System.DateTime, y: int) = x.AddDays(1.0)
    static member M2(x: inref<System.DateTime>, y: int) = x.AddDays(2.0)

let res = System.DateTime.Now
let v =  C.M(res)
let v2 =  C.M2(res, 4)
```

<span data-ttu-id="9e9ec-163">Dans les deux cas, les surcharges prenant `System.DateTime` sont résolues au lieu des surcharges prenant `inref<System.DateTime>`.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-163">In both cases, the overloads taking `System.DateTime` are resolved rather than the overloads taking `inref<System.DateTime>`.</span></span>

## <a name="byref-like-structs"></a><span data-ttu-id="9e9ec-164">Structs de type ByRef</span><span class="sxs-lookup"><span data-stu-id="9e9ec-164">Byref-like structs</span></span>

<span data-ttu-id="9e9ec-165">Outre le `byref` / `inref` / `outref` trio, vous pouvez définir vos propres structs peuvent adhérer à `byref`-comme la sémantique.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-165">In addition to the `byref`/`inref`/`outref` trio, you can define your own structs that can adhere to `byref`-like semantics.</span></span> <span data-ttu-id="9e9ec-166">Cette opération est effectuée avec la <xref:System.Runtime.CompilerServices.IsByRefLikeAttribute> attribut :</span><span class="sxs-lookup"><span data-stu-id="9e9ec-166">This is done with the <xref:System.Runtime.CompilerServices.IsByRefLikeAttribute> attribute:</span></span>

```fsharp
open System
open System.Runtime.CompilerServices

[<IsByRefLike; Struct>]
type S(count1: Span<int>, count2: Span<int>) =
    member x.Count1 = count1
    member x.Count2 = count2
```

<span data-ttu-id="9e9ec-167">`IsByRefLike` n’implique pas `Struct`.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-167">`IsByRefLike` does not imply `Struct`.</span></span> <span data-ttu-id="9e9ec-168">Les deux doivent être présents sur le type.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-168">Both must be present on the type.</span></span>

<span data-ttu-id="9e9ec-169">Un «`byref`-comme « struct dans F# est un type de valeur de limite de la pile.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-169">A "`byref`-like" struct in F# is a stack-bound value type.</span></span> <span data-ttu-id="9e9ec-170">Elle n’est jamais allouée sur le tas managé.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-170">It is never allocated on the managed heap.</span></span> <span data-ttu-id="9e9ec-171">Un `byref`-comme struct est utile pour la programmation de hautes performances, car elle est appliquée avec l’ensemble de vérifications fortes sur la durée de vie et de non capture.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-171">A `byref`-like struct is useful for high-performance programming, as it is enforced with set of strong checks about lifetime and non-capture.</span></span> <span data-ttu-id="9e9ec-172">Les règles sont :</span><span class="sxs-lookup"><span data-stu-id="9e9ec-172">The rules are:</span></span>

* <span data-ttu-id="9e9ec-173">Elles peuvent servir comme paramètres de fonction, les paramètres de méthode, les variables locales, méthode est retournée.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-173">They can be used as function parameters, method parameters, local variables, method returns.</span></span>
* <span data-ttu-id="9e9ec-174">Ils ne peuvent pas être statiques ou membres d’une classe ou un struct normal d’instance.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-174">They cannot be static or instance members of a class or normal struct.</span></span>
* <span data-ttu-id="9e9ec-175">Ils ne peuvent pas être capturés par n’importe quelle construction de fermeture (`async` méthodes ou expressions lambda).</span><span class="sxs-lookup"><span data-stu-id="9e9ec-175">They cannot be captured by any closure construct (`async` methods or lambda expressions).</span></span>
* <span data-ttu-id="9e9ec-176">Ils ne peuvent pas être utilisés comme un paramètre générique.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-176">They cannot be used as a generic parameter.</span></span>

<span data-ttu-id="9e9ec-177">Ce dernier point est crucial pour F# programmation de style de pipeline, comme `|>` est une fonction générique qui paramètre selon ses types d’entrée.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-177">This last point is crucial for F# pipeline-style programming, as `|>` is a generic function that parameterizes its input types.</span></span> <span data-ttu-id="9e9ec-178">Cette restriction peut être assouplie pour `|>` à l’avenir, car elle est en ligne et ne fait pas tous les appels aux fonctions génériques non inline dans son corps.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-178">This restriction may be relaxed for `|>` in the future, as it is inline and does not make any calls to non-inlined generic functions in its body.</span></span>

<span data-ttu-id="9e9ec-179">Bien que ces règles limiter fortement l’utilisation, elles ne remplissent la promesse de l’informatique hautes performances de manière sécurisée.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-179">Although these rules very strongly restrict usage, they do so to fulfill the promise of high-performance computing in a safe manner.</span></span>

## <a name="byref-returns"></a><span data-ttu-id="9e9ec-180">Retours ByRef</span><span class="sxs-lookup"><span data-stu-id="9e9ec-180">Byref returns</span></span>

<span data-ttu-id="9e9ec-181">Retours ByRef à partir de F# fonctions ou les membres peuvent être générés et consommées.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-181">Byref returns from F# functions or members can be produced and consumed.</span></span> <span data-ttu-id="9e9ec-182">Lors de l’utilisation un `byref`-méthode de retour, la valeur est déréférencée implicitement.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-182">When consuming a `byref`-returning method, the value is implicitly dereferenced.</span></span> <span data-ttu-id="9e9ec-183">Exemple :</span><span class="sxs-lookup"><span data-stu-id="9e9ec-183">For example:</span></span>

```fsharp
let safeSum(bytes: Span<byte>) =
    let mutable sum = 0
    for i in 0 .. bytes.Length - 1 do
        sum <- sum + int bytes.[i]
    sum

let sum = safeSum(mySpanOfBytes)
printfn "%d" sum // 'sum' is of type 'int'
```

<span data-ttu-id="9e9ec-184">Pour éviter le déréférencement implicites, telles que la transmission d’une référence via plusieurs appels chaînées, utilisez `&x` (où `x` est la valeur).</span><span class="sxs-lookup"><span data-stu-id="9e9ec-184">To avoid the implicit dereference, such as passing a reference through multiple chained calls, use `&x` (where `x` is the value).</span></span>

<span data-ttu-id="9e9ec-185">Vous pouvez également directement affecter à un retour `byref`.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-185">You can also directly assign to a return `byref`.</span></span> <span data-ttu-id="9e9ec-186">Prenons le programme (hautement impératif) suivant :</span><span class="sxs-lookup"><span data-stu-id="9e9ec-186">Consider the following (highly imperative) program:</span></span>

```fsharp
type C() =
    let mutable nums = [| 1; 3; 7; 15; 31; 63; 127; 255; 511; 1023 |]

    override __.ToString() = String.Join(' ', nums)

    member __.FindLargestSmallerThan(target: int) =
        let mutable ctr = nums.Length - 1

        while ctr > 0 && nums.[ctr] >= target do ctr <- ctr - 1

        if ctr > 0 then &nums.[ctr] else &nums.[0]

[<EntryPoint>]
let main argv =
    let c = C()
    printfn "Original sequence: %s" (c.ToString())

    let v = &c.FindLargestSmallerThan 16

    v <- v*2 // Directly assign to the byref return

    printfn "New sequence:      %s" (c.ToString())

    0 // return an integer exit code
```

<span data-ttu-id="9e9ec-187">Il s'agit de la sortie :</span><span class="sxs-lookup"><span data-stu-id="9e9ec-187">This is the output:</span></span>

```console
Original sequence: 1 3 7 15 31 63 127 255 511 1023
New sequence:      1 3 7 30 31 63 127 255 511 1023
```

## <a name="scoping-for-byrefs"></a><span data-ttu-id="9e9ec-188">L’étendue de valeurs ByRef</span><span class="sxs-lookup"><span data-stu-id="9e9ec-188">Scoping for byrefs</span></span>

<span data-ttu-id="9e9ec-189">Un `let`-valeur liée ne peut pas avoir à sa référence dépassent la portée dans laquelle il a été défini.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-189">A `let`-bound value cannot have its reference exceed the scope in which it was defined.</span></span> <span data-ttu-id="9e9ec-190">Par exemple, ce qui suit n’est pas autorisé :</span><span class="sxs-lookup"><span data-stu-id="9e9ec-190">For example, the following is disallowed:</span></span>

```fsharp
let test2 () =
    let x = 12
    &x // Error: 'x' exceeds its defined scope!

let test () =
    let x =
        let y = 1
        &y // Error: `y` exceeds its defined scope!
    ()
```

<span data-ttu-id="9e9ec-191">Cela vous empêche d’obtenir des résultats différents si vous compilez avec les optimisations activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="9e9ec-191">This prevents you from getting different results depending on if you compile with optimizations on or off.</span></span>
