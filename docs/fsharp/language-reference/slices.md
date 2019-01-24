---
title: Tranches (F#)
description: En savoir plus sur l’utilisation des tranches pour existant F# types de données et comment définir vos propres sections pour les autres types de données.
ms.date: 01/22/2019
ms.openlocfilehash: c204c6cbb195b33998b92dd940313a132ecc321d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54746706"
---
# <a name="slices"></a>Tranches

Dans F#, une tranche est un sous-ensemble d’un type de données. Pour être en mesure de prendre une tranche à partir d’un type de données, le type de données doit définir soit un `GetSlice` méthode ou dans un [tapez extension](type-extensions.md) qui est dans la portée. Cet article explique comment prendre des tranches d’existant F# types et comment définir les vôtres.

Les tranches sont similaires aux [indexeurs](members/indexed-properties.md), mais au lieu de donner une valeur unique à partir de la structure de données sous-jacente, ils produisent plusieurs.

F#n’a actuellement une prise en charge intrinsèque pour le découpage des chaînes, des listes, des tableaux et des tableaux 2D.

## <a name="basic-slicing-with-f-lists-and-arrays"></a>Segmentation de base avec F# listes et des tableaux

Types de données les plus courants sont découpées sont F# listes et des tableaux. L’exemple suivant montre comment effectuer cette opération avec des listes :

```fsharp
// Generate a list of 100 integers
let fullList = [ 1 .. 100 ]

// Create a slice from indices 1-5 (inclusive)
let smallSlice = fullList.[1..5]
printfn "Small slice: %A" smallSlice

// Create a slice from the beginning to index 5 (inclusive)
let unboundedBeginning = fullList.[..5]
printfn "Unbounded beginning slice: %A" unboundedBeginning

// Create a slice from an index to the end of the list
let unboundedEnd = fullList.[94..]
printfn "Unbounded end slice: %A" unboundedEnd
```

Tableaux de découpage s’apparente à découpage des listes :

```fsharp
// Generate an array of 100 integers
let fullArray = [| 1 .. 100 |]

// Create a slice from indices 1-5 (inclusive)
let smallSlice = fullArray.[1..5]
printfn "Small slice: %A" smallSlice

// Create a slice from the beginning to index 5 (inclusive)
let unboundedBeginning = fullArray.[..5]
printfn "Unbounded beginning slice: %A" unboundedBeginning

// Create a slice from an index to the end of the list
let unboundedEnd = fullArray.[94..]
printfn "Unbounded end slice: %A" unboundedEnd
```

## <a name="slicing-multidimensional-arrays"></a>Découpage de tableaux multidimensionnels

F#prend en charge les tableaux multidimensionnels dans le F# bibliothèque principale. Comme avec les tableaux unidimensionnels, les tranches de tableaux multidimensionnels peuvent également être utiles. Toutefois, l’introduction des dimensions supplémentaires impose une syntaxe légèrement différente afin que vous puissiez prendre les tranches de lignes et colonnes spécifiques.

Les exemples suivants montrent comment segmenter un tableau 2D :

```fsharp
// Generate a 3x3 2D matrix
let A = array2D [[1;2;3];[4;5;6];[7;8;9]]
printfn "Full matrix:\n %A" A

// Take the first row
let row0 = A.[0,*]
printfn "Row 0: %A" row0

// Take the first column
let col0 = A.[*,0]
printfn "Column 0: %A" col0

// Take all rows but only two columns
let subA = A.[*,0..1]
printfn "%A" subA

// Take two rows and all columns
let subA' = A.[0..1,*]
printfn "%A" subA'

// Slice a 2x2 matrix out of the full 3x3 matrix
let twoByTwo = A.[0..1,0..1]
printfn "%A" twobyTwo
```

Le F# ne définit pas de bibliothèque principale `GetSlice`pour les tableaux 3D. Si vous souhaitez découper ceux ou autres tableaux de plusieurs dimensions, vous devez définir le `GetSlice` membre vous-même.

## <a name="defining-slices-for-other-data-structures"></a>Définition des tranches pour les autres structures de données

Le F# bibliothèque principale définit les tranches pour un ensemble limité de types. Si vous souhaitez définir des coupes de plusieurs types de données, vous pouvez le faire dans la définition de type ou dans une extension de type.

Par exemple, voici comment vous pouvez définir des tranches pour la <xref:System.ArraySegment`1> classe permettant d’autoriser pour la manipulation des données pratique :

```fsharp
open System

type ArraySegment<'TItem> with
    member segment.GetSlice(?start, ?finish) =
        let start = defaultArg start 0
        let finish = defaultArg finish segment.Count
        ArraySegment(segment.Array, segment.Offset + start, finish - start)

let arr = ArraySegment [| 1 .. 10 |]
let slice = arr.[2..5] //[ 3; 4; 5]
```

### <a name="use-inlining-to-avoid-boxing-if-it-is-necessary"></a>Utilisez cette fonctionnalité pour éviter le boxing s’il est nécessaire

Si vous définissez des tranches pour un type qui est en fait un struct, il est recommandé que vous `inline` le `GetSlice` membre. Le F# compilateur optimise les arguments facultatifs, en évitant les allocations de tas à la suite de découpage. Cela est extrêmement important de découpage tel que les constructions <xref:System.Span`1> qui ne peut pas être être alloués sur le tas.

```fsharp
open System

type Span<'T> with
    // Note the 'inline' in the member definition
    member inline sp.GetSlice(startIdx, endIdx) =
        let s = defaultArg startIdx 0
        let e = defaultArg endIdx sp.Length
        sp.Slice(s, e)

let printSpan (sp: Span<int>) =
    let arr = sp.ToArray()
    printfn "%A" arr

let sp = [| 1; 2; 3; 4; 5 |].AsSpan()
printSpan sp.[0..] // [|1; 2; 3; 4; 5|]
printSpan sp.[..5] // [|1; 2; 3; 4; 5|]
printSpan sp.[0..3] // [|1; 2; 3|]
printSpan sp.[1..2] // |2; 3|]
```

## <a name="see-also"></a>Voir aussi

- [Propriétés indexées](members/indexed-properties.md)