---
title: 'Le mot clé Fixed (F #)'
description: 'Découvrez comment vous pouvez « pin » une variable locale dans la pile pour empêcher la collecte avec F # « fixed » mot clé.'
ms.date: 04/24/2017
ms.openlocfilehash: 1bf1b2ad67d2dd7f854e569cfca7c06e8aec7f4c
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "44039282"
---
# <a name="the-fixed-keyword"></a>Le mot clé Fixed

F # 4.1 introduit le `fixed` mot clé, qui vous permet de « épingler » une variable locale dans la pile pour éviter d’être collectées ou déplacé pendant le garbage collection.  Il est utilisé pour les scénarios de programmation de bas niveau.

## <a name="syntax"></a>Syntaxe

```fsharp
use ptr = fixed expression
```

## <a name="remarks"></a>Notes

Cela permet d’étendre la syntaxe des expressions pour permettre l’extraction d’un pointeur et le lier à un nom qui ne peut pas être collectées ou déplacé pendant le garbage collection.  

Correction d’un pointeur à partir d’une expression via la `fixed` mot clé est lié à un identificateur via le `use` mot clé.  La sémantique de cela est similaire à la gestion des ressources via les `use` mot clé.  Le pointeur est résolu pendant qu’il est dans la portée et une fois qu’il est hors de portée, il est fixe n’est plus.  `fixed` ne peut pas être utilisé en dehors du contexte d’un `use` liaison.  Vous devez lier le pointeur à un nom avec `use`.

Utilisation de `fixed` doivent se produire dans une expression dans une fonction ou une méthode.  Il ne peut pas être utilisé dans une étendue au niveau du script ou au niveau du module.

Comme tout code de pointeur, cela est une fonctionnalité unsafe et émet un avertissement lorsqu’il est utilisé.

## <a name="example"></a>Exemple

```fsharp
open Microsoft.FSharp.NativeInterop

type Point = { mutable X: int; mutable Y: int}

let squareWithPointer (p: nativeptr<int>) =
    // Dereference the pointer at the 0th address.
    let mutable value = NativePtr.get p 0

    // Perform some work
    value <- value * value

    // Set the value in the pointer at the 0th address.
    NativePtr.set p 0 value

let pnt = { X = 1; Y = 2 }
printfn "pnt before - X: %d Y: %d" pnt.X pnt.Y // prints 1 and 2

// Note that the use of 'fixed' is inside a function.
// You cannot fix a pointer at a script-level or module-level scope.
let doPointerWork() =
    use ptr = fixed &pnt.Y

    // Square the Y value
    squareWithPointer ptr
    printfn "pnt after - X: %d Y: %d" pnt.X pnt.Y // prints 1 and 4

doPointerWork()
```

## <a name="see-also"></a>Voir aussi

- [NativePtr (Module)](https://msdn.microsoft.com/visualfsharpdocs/conceptual/nativeinterop.nativeptr-module-%5Bfsharp%5D)
