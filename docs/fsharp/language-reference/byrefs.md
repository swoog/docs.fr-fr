---
title: 'ByRef (F #)'
description: 'Découvrez byref et byref types en F #, qui sont utilisés pour la programmation de bas niveau.'
ms.date: 09/02/2018
ms.openlocfilehash: 7d4138649ee39a0d342db2828ad4d32fbded978c
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2018
ms.locfileid: "44514434"
---
# <a name="byrefs"></a>ByRef

F # a deux principaux domaines de fonctionnalités qui traitent dans l’espace de programmation de bas niveau :

* Le `byref` / `inref` / `outref` types, qui sont des pointeurs managés. Ils ont des restrictions sur l’utilisation afin que vous ne pouvez pas compiler un programme qui n’est pas valide lors de l’exécution.
* Un `byref`-comme struct, qui est un [structure](structures.md) qui a une sémantique similaire et les mêmes restrictions de compilation que `byref<'T>`. Par exemple, <xref:System.Span%601>.

## <a name="syntax"></a>Syntaxe

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

## <a name="byref-inref-and-outref"></a>ByRef, inref et outref

Il existe trois formes de `byref`:

* `inref<'T>`, un pointeur managé pour lire la valeur sous-jacente.
* `outref<'T>`, un pointeur managé pour écrire dans la valeur sous-jacente.
* `byref<'T>`, un pointeur managé pour lire et écrire la valeur sous-jacente.

Un `byref<'T>` peuvent être passés où un `inref<'T>` est attendu. De même, un `byref<'T>` peuvent être passés où un `outref<'T>` est attendu.

## <a name="using-byrefs"></a>À l’aide de valeurs ByRef

Pour utiliser un `inref<'T>`, vous devez obtenir une valeur de pointeur avec `&`:

```fsharp
open System

let f (dt: inref<DateTime>) =
    printfn "Now: %s" (dt.ToString())

let dt = DateTime.Now
f &dt // Pass a pointer to 'dt'
```

Pour écrire dans le pointeur en utilisant un `outref<'T>` ou `byref<'T>`, vous devez également rendre la valeur que vous saisissez un pointeur vers `mutable`.

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

Si vous écrivez uniquement le pointeur au lieu de lire, envisagez d’utiliser `outref<'T>` au lieu de `byref<'T>`.

### <a name="inref-semantics"></a>Sémantique de Inref

Examinons le code ci-dessous.

```fsharp
let f (x: inref<SomeStruct>) = s.SomeField
```

Sémantiquement, cela signifie que les éléments suivants :

* Le titulaire de la `x` pointeur peut uniquement utiliser pour lire la valeur.
* N’importe quel pointeur acquis à `struct` champs imbriqués `SomeStruct` sont de type donné `inref<_>`.

Les éléments suivants sont également vrai :

* Il est sans implication que d’autres threads ou alias n’ont pas accès en écriture à `x`.
* Il n’existe aucune implication qui `SomeStruct` est immuable en raison de `x` en cours un `inref`.

Toutefois, pour F # types valeur **sont** immuable, le `this` pointeur est déduit comme étant un `inref`.

Toutes ces règles ensemble signifient que le titulaire d’un `inref` pointeur ne peut pas modifier le contenu immédiat de la mémoire qui est pointé.

### <a name="outref-semantics"></a>Sémantique de Outref

L’objectif de `outref<'T>` consiste à indiquer que le pointeur doit uniquement être lu. De façon inattendue, `outref<'T>` autorise lecture sous-jacent valeur malgré son nom. Il s’agit pour des raisons de compatibilité. Sémantiquement, `outref<'T>` n’est pas différent de celui `byref<'T>`.

### <a name="interop-with-c"></a>Interopérabilité avec C #

C# prend en charge la `in ref` et `out ref` mots clés, en plus de `ref` retourne. Le tableau suivant montre comment F # interprète ce que c# émet :

|Construction de c#|F # déduit|
|------------|---------|
|`ref` Valeur de retour|`outref<'T>`|
|`ref readonly` Valeur de retour|`inref<'T>`|
|`in ref` Paramètre|`inref<'T>`|
|`out ref` Paramètre|`outref<'T>`|

Le tableau suivant montre ce que F # émet :

|Construction F #|Construction émise|
|------------|-----------------|
|`inref<'T>` argument|`[In]` attribut de l’argument|
|`inref<'T>` retour|`modreq` attribut de valeur|
|`inref<'T>` dans emplacement abstrait ou implémentation|`modreq` sur l’argument ou de retour|
|`outref<'T>` argument|`[Out]` attribut de l’argument|

### <a name="type-inference-and-overloading-rules"></a>Inférence de type et les règles de surcharge

Un `inref<'T>` type est déduit par le compilateur F # dans les cas suivants :

1. Un type de paramètre ou de retour de .NET qui a un `IsReadOnly` attribut.
2. Le `this` pointeur sur un type struct qui ne comporte aucun champ mutable.
3. L’adresse d’un emplacement mémoire dérivé d’un autre `inref<_>` pointeur.

Lorsqu’une adresse implicite d’un `inref` est effectuée, une surcharge avec un argument de type `SomeType` est préférable à une surcharge avec un argument de type `inref<SomeType>`. Exemple :

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

Dans les deux cas, les surcharges prenant `System.DateTime` sont résolues au lieu des surcharges prenant `inref<System.DateTime>`.

## <a name="byref-like-structs"></a>Structs de type ByRef

Outre le `byref` / `inref` / `outref` trio, vous pouvez définir vos propres structs peuvent adhérer à `byref`-comme la sémantique. Cette opération est effectuée avec la <xref:System.Runtime.CompilerServices.IsByRefLikeAttribute> attribut :

```fsharp
open System
open System.Runtime.CompilerServices

[<IsByRefLike; Struct>]
type S(count1: Span<int>, count2: Span<int>) =
    member x.Count1 = count1
    member x.Count2 = count2
```

`IsByRefLike` n’implique pas `Struct`. Les deux doivent être présents sur le type.

Un «`byref`-comme « struct en F # est un type de valeur de limite de la pile. Elle n’est jamais allouée sur le tas managé. Un `byref`-comme struct est utile pour la programmation de hautes performances, car elle est appliquée avec l’ensemble de vérifications fortes sur la durée de vie et de non capture. Les règles sont :

* Elles peuvent servir comme paramètres de fonction, les paramètres de méthode, les variables locales, méthode est retournée.
* Ils ne peuvent pas être statiques ou membres d’une classe ou un struct normal d’instance.
* Ils ne peuvent pas être capturés par n’importe quelle construction de fermeture (`async` méthodes ou expressions lambda).
* Ils ne peuvent pas être utilisés comme un paramètre générique.

Ce dernier point est essentiel pour la programmation de style de pipeline F #, en tant que `|>` est une fonction générique qui paramètre selon ses types d’entrée. Cette restriction peut être assouplie pour `|>` à l’avenir, car elle est en ligne et ne fait pas tous les appels aux fonctions génériques non inline dans son corps.

Bien que ces règles limiter fortement l’utilisation, elles ne remplissent la promesse de l’informatique hautes performances de manière sécurisée.

## <a name="byref-returns"></a>Retours ByRef

Retours ByRef à partir de fonctions F # ou membres peuvent être générés et consommées. Lors de l’utilisation un `byref`-méthode de retour, la valeur est déréférencée implicitement. Exemple :

```fsharp
let safeSum(bytes: Span<byte>) =
    let mutable sum = 0
    for i in 0 .. bytes.Length - 1 do
        sum <- sum + int bytes.[i]
    sum

let sum = safeSum(mySpanOfBytes)
printfn "%d" sum // 'sum' is of type 'int'
```

Pour éviter le déréférencement implicites, telles que la transmission d’une référence via plusieurs appels chaînées, utilisez `&x` (où `x` est la valeur).

Vous pouvez également directement affecter à un retour `byref`. Prenons le programme (hautement impératif) suivant :

```fsharp
ype C() =
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

Il s'agit de la sortie :

```console
Original sequence: 1 3 7 15 31 63 127 255 511 1023
New sequence:      1 3 7 30 31 63 127 255 511 1023
```

## <a name="scoping-for-byrefs"></a>L’étendue de valeurs ByRef

Un `let`-valeur liée ne peut pas avoir à sa référence dépassent la portée dans laquelle il a été défini. Par exemple, ce qui suit n’est pas autorisé :

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

Cela vous empêche d’obtenir des résultats différents si vous compilez avec les optimisations activé ou désactivé.