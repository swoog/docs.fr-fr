---
title: 'Expressions conditionnelles : if... then...else (F#)'
description: 'Découvrez comment écrire des expressions conditionnelles en F # pour exécuter les différentes branches de code.'
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: dotnet-fsharp
ms.devlang: fsharp
ms.openlocfilehash: bfb985f09be91034894e1d3eba88cebef6bb3fd4
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="conditional-expressions-ifthenelse"></a><span data-ttu-id="0da3d-103">Expressions conditionnelles : `if...then...else`</span><span class="sxs-lookup"><span data-stu-id="0da3d-103">Conditional Expressions: `if...then...else`</span></span>

<span data-ttu-id="0da3d-104">Le `if...then...else` expression exécute différentes branches de code et prend une valeur différente selon l’expression booléenne donnée.</span><span class="sxs-lookup"><span data-stu-id="0da3d-104">The `if...then...else` expression runs different branches of code and also evaluates to a different value depending on the Boolean expression given.</span></span>


## <a name="syntax"></a><span data-ttu-id="0da3d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0da3d-105">Syntax</span></span>

```fsharp
if boolean-expression then expression1 [ else expression2 ]
```

## <a name="remarks"></a><span data-ttu-id="0da3d-106">Notes</span><span class="sxs-lookup"><span data-stu-id="0da3d-106">Remarks</span></span>
<span data-ttu-id="0da3d-107">Dans la syntaxe précédente, *expression1* s’exécute lorsque l’expression booléenne renvoie `true`; sinon, *expression2* s’exécute.</span><span class="sxs-lookup"><span data-stu-id="0da3d-107">In the previous syntax, *expression1* runs when the Boolean expression evaluates to `true`; otherwise, *expression2* runs.</span></span>

<span data-ttu-id="0da3d-108">Contrairement à d’autres langages, les `if...then...else` construction est une expression, pas une instruction.</span><span class="sxs-lookup"><span data-stu-id="0da3d-108">Unlike in other languages, the `if...then...else` construct is an expression, not a statement.</span></span> <span data-ttu-id="0da3d-109">Cela signifie qu’il génère une valeur, ce qui est la valeur de la dernière expression dans la branche qui s’exécute.</span><span class="sxs-lookup"><span data-stu-id="0da3d-109">That means that it produces a value, which is the value of the last expression in the branch that executes.</span></span> <span data-ttu-id="0da3d-110">Les types des valeurs produites dans chaque branche doivent correspondre.</span><span class="sxs-lookup"><span data-stu-id="0da3d-110">The types of the values produced in each branch must match.</span></span> <span data-ttu-id="0da3d-111">S’il existe n’explicite `else` , son type est `unit`.</span><span class="sxs-lookup"><span data-stu-id="0da3d-111">If there is no explicit `else` branch, its type is `unit`.</span></span> <span data-ttu-id="0da3d-112">Par conséquent, si le type de la `then` branche est d’un type autre que `unit`, il doit y avoir un `else` branche avec le même type de retour.</span><span class="sxs-lookup"><span data-stu-id="0da3d-112">Therefore, if the type of the `then` branch is any type other than `unit`, there must be an `else` branch with the same return type.</span></span> <span data-ttu-id="0da3d-113">Lors du chaînage `if...then...else` expressions ensemble, vous pouvez utiliser le mot clé `elif` au lieu de `else if`; ils sont équivalents.</span><span class="sxs-lookup"><span data-stu-id="0da3d-113">When chaining `if...then...else` expressions together, you can use the keyword `elif` instead of `else if`; they are equivalent.</span></span>

## <a name="example"></a><span data-ttu-id="0da3d-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="0da3d-114">Example</span></span>
<span data-ttu-id="0da3d-115">L’exemple suivant illustre comment utiliser le `if...then...else` expression.</span><span class="sxs-lookup"><span data-stu-id="0da3d-115">The following example illustrates how to use the `if...then...else` expression.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4501.fs)]

```
10 is less than 20
What is your name? John
How old are you? 9
You are only 9 years old and already learning F#? Wow!
```

## <a name="see-also"></a><span data-ttu-id="0da3d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0da3d-116">See Also</span></span>
[<span data-ttu-id="0da3d-117">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="0da3d-117">F# Language Reference</span></span>](index.md)

