---
title: Expressions différées
description: Découvrez comment F# expressions différées peuvent améliorer les performances de vos applications et les bibliothèques.
ms.date: 03/13/2019
ms.openlocfilehash: 6d53d53093f4e93f53e1c956b94e2f1e4a1bbd55
ms.sourcegitcommit: 69bf8b719d4c289eec7b45336d0b933dd7927841
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57853323"
---
# <a name="lazy-expressions"></a><span data-ttu-id="87cf0-103">Expressions différées</span><span class="sxs-lookup"><span data-stu-id="87cf0-103">Lazy Expressions</span></span>

<span data-ttu-id="87cf0-104">*Expressions différées* sont des expressions qui ne sont pas évaluées immédiatement, mais sont évaluées à la place lorsque le résultat est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="87cf0-104">*Lazy expressions* are expressions that are not evaluated immediately, but are instead evaluated when the result is needed.</span></span> <span data-ttu-id="87cf0-105">Cela peut contribuer à améliorer les performances de votre code.</span><span class="sxs-lookup"><span data-stu-id="87cf0-105">This can help to improve the performance of your code.</span></span>

## <a name="syntax"></a><span data-ttu-id="87cf0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87cf0-106">Syntax</span></span>

```fsharp
let identifier = lazy ( expression )
```

## <a name="remarks"></a><span data-ttu-id="87cf0-107">Notes</span><span class="sxs-lookup"><span data-stu-id="87cf0-107">Remarks</span></span>

<span data-ttu-id="87cf0-108">Dans la syntaxe précédente, *expression* est le code qui est évaluée uniquement lorsqu’un résultat est requis, et *identificateur* est une valeur qui stocke le résultat.</span><span class="sxs-lookup"><span data-stu-id="87cf0-108">In the previous syntax, *expression* is code that is evaluated only when a result is required, and *identifier* is a value that stores the result.</span></span> <span data-ttu-id="87cf0-109">La valeur est de type [ `Lazy<'T>` ](https://msdn.microsoft.com/library/b29d0af5-6efb-4a55-a278-2662a4ecc489), où le type réel qui est utilisé pour `'T` est déterminé à partir du résultat de l’expression.</span><span class="sxs-lookup"><span data-stu-id="87cf0-109">The value is of type [`Lazy<'T>`](https://msdn.microsoft.com/library/b29d0af5-6efb-4a55-a278-2662a4ecc489), where the actual type that is used for `'T` is determined from the result of the expression.</span></span>

<span data-ttu-id="87cf0-110">Expressions différées permettent d’améliorer les performances en limitant l’exécution de des expressions aux seules situations dans lesquelles un résultat est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="87cf0-110">Lazy expressions enable you to improve performance by restricting the execution of an expressions to only those situations in which a result is needed.</span></span>

<span data-ttu-id="87cf0-111">Pour forcer les expressions à effectuer, vous appelez la méthode `Force`.</span><span class="sxs-lookup"><span data-stu-id="87cf0-111">To force the expressions to be performed, you call the method `Force`.</span></span> <span data-ttu-id="87cf0-112">`Force` entraîne l’exécution à effectuer qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="87cf0-112">`Force` causes the execution to be performed only one time.</span></span> <span data-ttu-id="87cf0-113">Les appels suivants à `Force` retournent le même résultat, mais n’exécutent pas le code.</span><span class="sxs-lookup"><span data-stu-id="87cf0-113">Subsequent calls to `Force` return the same result, but do not execute any code.</span></span>

<span data-ttu-id="87cf0-114">Le code suivant illustre l’utilisation d’expressions différées et l’utilisation de `Force`.</span><span class="sxs-lookup"><span data-stu-id="87cf0-114">The following code illustrates the use of lazy expressions and the use of `Force`.</span></span> <span data-ttu-id="87cf0-115">Dans ce code, le type de `result` est `Lazy<int>`et le `Force` méthode retourne un `int`.</span><span class="sxs-lookup"><span data-stu-id="87cf0-115">In this code, the type of `result` is `Lazy<int>`, and the `Force` method returns an `int`.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet73011.fs)]

<span data-ttu-id="87cf0-116">L’évaluation différée, mais pas le `Lazy` type, est également utilisé pour les séquences.</span><span class="sxs-lookup"><span data-stu-id="87cf0-116">Lazy evaluation, but not the `Lazy` type, is also used for sequences.</span></span> <span data-ttu-id="87cf0-117">Pour plus d’informations, consultez [séquences](sequences.md).</span><span class="sxs-lookup"><span data-stu-id="87cf0-117">For more information, see [Sequences](sequences.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="87cf0-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87cf0-118">See also</span></span>

- [<span data-ttu-id="87cf0-119">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="87cf0-119">F# Language Reference</span></span>](index.md)
- [<span data-ttu-id="87cf0-120">LazyExtensions (module)</span><span class="sxs-lookup"><span data-stu-id="87cf0-120">LazyExtensions module</span></span>](https://msdn.microsoft.com/library/86671f40-84a0-402a-867d-ae596218d948)
