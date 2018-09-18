---
title: Fonctions inline (F#)
description: 'Découvrez comment utiliser les fonctions F # inline qui sont intégrées directement dans le code appelant.'
ms.date: 05/16/2016
ms.openlocfilehash: 47fca0fe34630792aeb0908b0cee02a927e2567d
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45745943"
---
# <a name="inline-functions"></a><span data-ttu-id="1a34b-103">Fonctions inline</span><span class="sxs-lookup"><span data-stu-id="1a34b-103">Inline Functions</span></span>

<span data-ttu-id="1a34b-104">*Les fonctions inline* sont des fonctions qui sont intégrées directement dans le code appelant.</span><span class="sxs-lookup"><span data-stu-id="1a34b-104">*Inline functions* are functions that are integrated directly into the calling code.</span></span>

## <a name="using-inline-functions"></a><span data-ttu-id="1a34b-105">À l’aide de fonctions Inline</span><span class="sxs-lookup"><span data-stu-id="1a34b-105">Using Inline Functions</span></span>

<span data-ttu-id="1a34b-106">Lorsque vous utilisez des paramètres de type statique, toutes les fonctions qui sont paramétrées par les paramètres de type doivent être inline.</span><span class="sxs-lookup"><span data-stu-id="1a34b-106">When you use static type parameters, any functions that are parameterized by type parameters must be inline.</span></span> <span data-ttu-id="1a34b-107">Cela garantit que le compilateur peut résoudre ces paramètres de type.</span><span class="sxs-lookup"><span data-stu-id="1a34b-107">This guarantees that the compiler can resolve these type parameters.</span></span> <span data-ttu-id="1a34b-108">Lorsque vous utilisez des paramètres de type générique ordinaire, il n’existe aucune restriction de ce type.</span><span class="sxs-lookup"><span data-stu-id="1a34b-108">When you use ordinary generic type parameters, there is no such restriction.</span></span>

<span data-ttu-id="1a34b-109">Permettent l’utilisation de contraintes de membre, les fonctions inline peuvent être utiles pour optimiser le code.</span><span class="sxs-lookup"><span data-stu-id="1a34b-109">Other than enabling the use of member constraints, inline functions can be helpful in optimizing code.</span></span> <span data-ttu-id="1a34b-110">Toutefois, utilisation abusive des fonctions inline peut rendre votre code moins résistant aux modifications dans les optimisations du compilateur et l’implémentation de fonctions de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="1a34b-110">However, overuse of inline functions can cause your code to be less resistant to changes in compiler optimizations and the implementation of library functions.</span></span> <span data-ttu-id="1a34b-111">Pour cette raison, évitez d’utiliser des fonctions inline pour l’optimisation, sauf si vous avez essayé toutes les autres techniques d’optimisation.</span><span class="sxs-lookup"><span data-stu-id="1a34b-111">For this reason, you should avoid using inline functions for optimization unless you have tried all other optimization techniques.</span></span> <span data-ttu-id="1a34b-112">Rendre une fonction ou méthode inline peut parfois améliorer les performances, mais qui n’est pas toujours le cas.</span><span class="sxs-lookup"><span data-stu-id="1a34b-112">Making a function or method inline can sometimes improve performance, but that is not always the case.</span></span> <span data-ttu-id="1a34b-113">Par conséquent, vous devez également utiliser les mesures de performances pour vérifier que la fabrication d’une fonction donnée inline n’a en fait un effet positif.</span><span class="sxs-lookup"><span data-stu-id="1a34b-113">Therefore, you should also use performance measurements to verify that making any given function inline does in fact have a positive effect.</span></span>

<span data-ttu-id="1a34b-114">Le `inline` modificateur peut être appliqué aux fonctions au niveau supérieur, au niveau du module ou au niveau de la méthode dans une classe.</span><span class="sxs-lookup"><span data-stu-id="1a34b-114">The `inline` modifier can be applied to functions at the top level, at the module level, or at the method level in a class.</span></span>

<span data-ttu-id="1a34b-115">L’exemple de code suivant illustre une fonction inline au niveau supérieur, une méthode d’instance inline et une méthode statique inline.</span><span class="sxs-lookup"><span data-stu-id="1a34b-115">The following code example illustrates an inline function at the top level, an inline instance method, and an inline static method.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-3/snippet201.fs)]

## <a name="inline-functions-and-type-inference"></a><span data-ttu-id="1a34b-116">Les fonctions inline et inférence de Type</span><span class="sxs-lookup"><span data-stu-id="1a34b-116">Inline Functions and Type Inference</span></span>

<span data-ttu-id="1a34b-117">La présence de `inline` affecte l’inférence de type.</span><span class="sxs-lookup"><span data-stu-id="1a34b-117">The presence of `inline` affects type inference.</span></span> <span data-ttu-id="1a34b-118">Il s’agit, car les fonctions inline peuvent avoir résolus statiquement des paramètres de type, tandis que les fonctions non inline ne peut pas.</span><span class="sxs-lookup"><span data-stu-id="1a34b-118">This is because inline functions can have statically resolved type parameters, whereas non-inline functions cannot.</span></span> <span data-ttu-id="1a34b-119">L’exemple de code suivant illustre un cas où `inline` est utile, car vous utilisez une fonction qui a un paramètre de type résolus statiquement, le `float` opérateur de conversion.</span><span class="sxs-lookup"><span data-stu-id="1a34b-119">The following code example shows a case where `inline` is helpful because you are using a function that has a statically resolved type parameter, the `float` conversion operator.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-3/snippet202.fs)]

<span data-ttu-id="1a34b-120">Sans le `inline` modificateur, l’inférence de type force la fonction à prendre un type spécifique, dans ce cas `int`.</span><span class="sxs-lookup"><span data-stu-id="1a34b-120">Without the `inline` modifier, type inference forces the function to take a specific type, in this case `int`.</span></span> <span data-ttu-id="1a34b-121">Mais avec la `inline` modificateur, la fonction est également déduit pour avoir un paramètre de type résolus statiquement.</span><span class="sxs-lookup"><span data-stu-id="1a34b-121">But with the `inline` modifier, the function is also inferred to have a statically resolved type parameter.</span></span> <span data-ttu-id="1a34b-122">Avec le `inline` modificateur, le type déduit est ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="1a34b-122">With the `inline` modifier, the type is inferred to be the following:</span></span>

```fsharp
^a -> unit when ^a : (static member op_Explicit : ^a -> float)
```

<span data-ttu-id="1a34b-123">Cela signifie que la fonction accepte n’importe quel type qui prend en charge une conversion vers **float**.</span><span class="sxs-lookup"><span data-stu-id="1a34b-123">This means that the function accepts any type that supports a conversion to **float**.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a34b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a34b-124">See also</span></span>

- [<span data-ttu-id="1a34b-125">Fonctions</span><span class="sxs-lookup"><span data-stu-id="1a34b-125">Functions</span></span>](index.md)
- [<span data-ttu-id="1a34b-126">Contraintes</span><span class="sxs-lookup"><span data-stu-id="1a34b-126">Constraints</span></span>](../generics/constraints.md)
- [<span data-ttu-id="1a34b-127">Paramètres de type résolus statiquement</span><span class="sxs-lookup"><span data-stu-id="1a34b-127">Statically Resolved Type Parameters</span></span>](../generics/statically-resolved-type-parameters.md)
