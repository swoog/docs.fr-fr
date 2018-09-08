---
title: Calculs tardifs (F#)
description: 'Découvrez comment les calculs tardifs F # peuvent améliorer les performances de vos applications et les bibliothèques.'
ms.date: 05/16/2016
ms.openlocfilehash: 8afe815f26978de96291a52973d54a9dbcc5eaf2
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44201624"
---
# <a name="lazy-computations"></a><span data-ttu-id="b73c3-103">Calculs tardifs</span><span class="sxs-lookup"><span data-stu-id="b73c3-103">Lazy Computations</span></span>

<span data-ttu-id="b73c3-104">*Calculs tardifs* sont des calculs qui ne sont pas évalués immédiatement, mais sont évaluées à la place lorsque le résultat est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b73c3-104">*Lazy computations* are computations that are not evaluated immediately, but are instead evaluated when the result is needed.</span></span> <span data-ttu-id="b73c3-105">Cela peut contribuer à améliorer les performances de votre code.</span><span class="sxs-lookup"><span data-stu-id="b73c3-105">This can help to improve the performance of your code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b73c3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b73c3-106">Syntax</span></span>

```fsharp
let identifier = lazy ( expression )
```

## <a name="remarks"></a><span data-ttu-id="b73c3-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b73c3-107">Remarks</span></span>

<span data-ttu-id="b73c3-108">Dans la syntaxe précédente, *expression* est le code qui est évaluée uniquement lorsqu’un résultat est requis, et *identificateur* est une valeur qui stocke le résultat.</span><span class="sxs-lookup"><span data-stu-id="b73c3-108">In the previous syntax, *expression* is code that is evaluated only when a result is required, and *identifier* is a value that stores the result.</span></span> <span data-ttu-id="b73c3-109">La valeur est de type [ `Lazy<'T>` ](https://msdn.microsoft.com/library/b29d0af5-6efb-4a55-a278-2662a4ecc489), où le type réel qui est utilisé pour `'T` est déterminé à partir du résultat de l’expression.</span><span class="sxs-lookup"><span data-stu-id="b73c3-109">The value is of type [`Lazy<'T>`](https://msdn.microsoft.com/library/b29d0af5-6efb-4a55-a278-2662a4ecc489), where the actual type that is used for `'T` is determined from the result of the expression.</span></span>

<span data-ttu-id="b73c3-110">Calculs tardifs permettent d’améliorer les performances en limitant l’exécution d’un calcul aux seules situations dans lesquelles un résultat est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b73c3-110">Lazy computations enable you to improve performance by restricting the execution of a computation to only those situations in which a result is needed.</span></span>

<span data-ttu-id="b73c3-111">Pour forcer l’exécution du calcul, vous appelez la méthode `Force`.</span><span class="sxs-lookup"><span data-stu-id="b73c3-111">To force the computation to be performed, you call the method `Force`.</span></span> <span data-ttu-id="b73c3-112">`Force` entraîne l’exécution à effectuer qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="b73c3-112">`Force` causes the execution to be performed only one time.</span></span> <span data-ttu-id="b73c3-113">Les appels suivants à `Force` retournent le même résultat, mais n’exécutent pas le code.</span><span class="sxs-lookup"><span data-stu-id="b73c3-113">Subsequent calls to `Force` return the same result, but do not execute any code.</span></span>

<span data-ttu-id="b73c3-114">Le code suivant illustre l’utilisation du calcul tardif et l’utilisation de `Force`.</span><span class="sxs-lookup"><span data-stu-id="b73c3-114">The following code illustrates the use of lazy computation and the use of `Force`.</span></span> <span data-ttu-id="b73c3-115">Dans ce code, le type de `result` est `Lazy<int>`et le `Force` méthode retourne un `int`.</span><span class="sxs-lookup"><span data-stu-id="b73c3-115">In this code, the type of `result` is `Lazy<int>`, and the `Force` method returns an `int`.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet73011.fs)]

<span data-ttu-id="b73c3-116">L’évaluation différée, mais pas le `Lazy` type, est également utilisé pour les séquences.</span><span class="sxs-lookup"><span data-stu-id="b73c3-116">Lazy evaluation, but not the `Lazy` type, is also used for sequences.</span></span> <span data-ttu-id="b73c3-117">Pour plus d’informations, consultez [séquences](sequences.md).</span><span class="sxs-lookup"><span data-stu-id="b73c3-117">For more information, see [Sequences](sequences.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b73c3-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b73c3-118">See also</span></span>

- [<span data-ttu-id="b73c3-119">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="b73c3-119">F# Language Reference</span></span>](index.md)
- [<span data-ttu-id="b73c3-120">LazyExtensions (module)</span><span class="sxs-lookup"><span data-stu-id="b73c3-120">LazyExtensions module</span></span>](https://msdn.microsoft.com/library/86671f40-84a0-402a-867d-ae596218d948)
