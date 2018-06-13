---
title: 'Boucles : expression for...to (F#)'
description: 'Voir comment la boucle for) (F #.. à l’expression est utilisé pour itérer au sein d’une boucle sur une plage de valeurs d’une variable de boucle.'
ms.date: 05/16/2016
ms.openlocfilehash: 841c7d557abc11e0253cb87ab8081cc77671b44b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33563400"
---
# <a name="loops-forto-expression"></a><span data-ttu-id="b81f2-103">Boucles : expression for...to</span><span class="sxs-lookup"><span data-stu-id="b81f2-103">Loops: for...to Expression</span></span>

<span data-ttu-id="b81f2-104">Le `for...to` expression est utilisée pour itérer au sein d’une boucle sur une plage de valeurs d’une variable de boucle.</span><span class="sxs-lookup"><span data-stu-id="b81f2-104">The `for...to` expression is used to iterate in a loop over a range of values of a loop variable.</span></span>


## <a name="syntax"></a><span data-ttu-id="b81f2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b81f2-105">Syntax</span></span>

```fsharp
for identifier = start [ to | downto ] finish do
    body-expression
```

## <a name="remarks"></a><span data-ttu-id="b81f2-106">Notes</span><span class="sxs-lookup"><span data-stu-id="b81f2-106">Remarks</span></span>
<span data-ttu-id="b81f2-107">Le type de l’identificateur est déduit du type de la *Démarrer* et *Terminer* expressions.</span><span class="sxs-lookup"><span data-stu-id="b81f2-107">The type of the identifier is inferred from the type of the *start* and *finish* expressions.</span></span> <span data-ttu-id="b81f2-108">Types pour ces expressions doivent être des entiers 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b81f2-108">Types for these expressions must be 32-bit integers.</span></span>

<span data-ttu-id="b81f2-109">Bien que techniquement d’une expression, `for...to` plus à une instruction traditionnelle dans un langage de programmation impérative.</span><span class="sxs-lookup"><span data-stu-id="b81f2-109">Although technically an expression, `for...to` is more like a traditional statement in an imperative programming language.</span></span> <span data-ttu-id="b81f2-110">Le type de retour pour la *expression de corps* doit être `unit`.</span><span class="sxs-lookup"><span data-stu-id="b81f2-110">The return type for the *body-expression* must be `unit`.</span></span> <span data-ttu-id="b81f2-111">Les exemples suivants illustrent différentes utilisations de la `for...to` expression.</span><span class="sxs-lookup"><span data-stu-id="b81f2-111">The following examples show various uses of the `for...to` expression.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5101.fs)]

<span data-ttu-id="b81f2-112">La sortie du code précédent est la suivante.</span><span class="sxs-lookup"><span data-stu-id="b81f2-112">The output of the previous code is as follows.</span></span>

```
1 2 3 4 5 6 7 8 9 10
10 9 8 7 6 5 4 3 2 1
2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18
```

## <a name="see-also"></a><span data-ttu-id="b81f2-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b81f2-113">See Also</span></span>
[<span data-ttu-id="b81f2-114">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="b81f2-114">F# Language Reference</span></span>](index.md)

[<span data-ttu-id="b81f2-115">Boucles : expression `for...in`</span><span class="sxs-lookup"><span data-stu-id="b81f2-115">Loops: `for...in` Expression</span></span>](loops-for-in-expression.md)

[<span data-ttu-id="b81f2-116">Boucles : expression `while...do`</span><span class="sxs-lookup"><span data-stu-id="b81f2-116">Loops: `while...do` Expression</span></span>](loops-while-do-expression.md)
