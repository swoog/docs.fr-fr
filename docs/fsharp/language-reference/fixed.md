---
title: 'Le mot clé Fixed (F #)'
description: 'Découvrez comment vous pouvez « pin » locale sur la pile pour empêcher la collection avec F # « fixed » (mot clé).'
ms.date: 04/24/2017
ms.openlocfilehash: 913ee4d7b0f6b2437793d4788e53556d6be6c4db
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33563874"
---
# <a name="the-fixed-keyword"></a><span data-ttu-id="fc0ca-103">Le mot clé Fixed</span><span class="sxs-lookup"><span data-stu-id="fc0ca-103">The Fixed Keyword</span></span>

<span data-ttu-id="fc0ca-104">F # 4.1 introduit le `fixed` mot clé, qui vous permet de « épingler » locale sur la pile pour l’empêcher d’être collectées ou déplacé pendant le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="fc0ca-104">F# 4.1 introduces the `fixed` keyword, which allows you to "pin" a local onto the stack to prevent it from being collected or moved during garbage-collection.</span></span>  <span data-ttu-id="fc0ca-105">Il est utilisé pour les scénarios de programmation de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="fc0ca-105">It is used for low-level programming scenarios.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc0ca-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc0ca-106">Syntax</span></span>

```fsharp
use ptr = fixed expression
```

## <a name="remarks"></a><span data-ttu-id="fc0ca-107">Notes</span><span class="sxs-lookup"><span data-stu-id="fc0ca-107">Remarks</span></span>

<span data-ttu-id="fc0ca-108">Cela permet d’étendre la syntaxe des expressions pour permettre l’extraction d’un pointeur et le lier à un nom qui ne peut pas être collectées ou déplacé pendant le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="fc0ca-108">This extends the syntax of expressions to allow extracting a pointer and binding it to a name which is prevented from being collected or moved during garbage-collection.</span></span>  

<span data-ttu-id="fc0ca-109">Un pointeur à partir d’une expression est fixe la `fixed` (mot clé) est liée à un identificateur via le `use` (mot clé).</span><span class="sxs-lookup"><span data-stu-id="fc0ca-109">A pointer from an expression is fixed via the `fixed` keyword is bound to an identifier via the `use` keyword.</span></span>  <span data-ttu-id="fc0ca-110">La sémantique de cela est similaire à la gestion des ressources via les `use` (mot clé).</span><span class="sxs-lookup"><span data-stu-id="fc0ca-110">The semantics of this are similar to resource management via the `use` keyword.</span></span>  <span data-ttu-id="fc0ca-111">Le pointeur est fixe tandis qu’il est dans la portée, une fois qu’elle est hors de portée, il est fixe n’est plus.</span><span class="sxs-lookup"><span data-stu-id="fc0ca-111">The pointer is fixed while it is in scope, and once it is out of scope, it is no longer fixed.</span></span>  <span data-ttu-id="fc0ca-112">`fixed` ne peut pas être utilisé en dehors du contexte d’un `use` liaison.</span><span class="sxs-lookup"><span data-stu-id="fc0ca-112">`fixed` cannot be used outside the context of a `use` binding.</span></span>  <span data-ttu-id="fc0ca-113">Vous devez lier le pointeur sur un nom avec `use`.</span><span class="sxs-lookup"><span data-stu-id="fc0ca-113">You must bind the pointer to a name with `use`.</span></span>

<span data-ttu-id="fc0ca-114">Utilisation de `fixed` doivent se produire dans une expression dans une fonction ou une méthode.</span><span class="sxs-lookup"><span data-stu-id="fc0ca-114">Use of `fixed` must occur within an expression in a function or a method.</span></span>  <span data-ttu-id="fc0ca-115">Il ne peut pas être utilisé avec une portée au niveau du script ou au niveau du module.</span><span class="sxs-lookup"><span data-stu-id="fc0ca-115">It cannot be used at a script-level or module-level scope.</span></span>

<span data-ttu-id="fc0ca-116">Comme tout code de pointeur, ceci est une fonctionnalité non sécurisée et émet un avertissement lorsqu’il est utilisé.</span><span class="sxs-lookup"><span data-stu-id="fc0ca-116">Like all pointer code, this is an unsafe feature and will emit a warning when used.</span></span>

## <a name="example"></a><span data-ttu-id="fc0ca-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="fc0ca-117">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="fc0ca-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc0ca-118">See Also</span></span>

[<span data-ttu-id="fc0ca-119">NativePtr (Module)</span><span class="sxs-lookup"><span data-stu-id="fc0ca-119">NativePtr Module</span></span>](https://msdn.microsoft.com/visualfsharpdocs/conceptual/nativeinterop.nativeptr-module-%5Bfsharp%5D)
