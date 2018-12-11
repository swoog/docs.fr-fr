---
title: 'Boucles : expression while...do (F#)'
description: Voir comment l’instruction while... faire expression est utilisée pour effectuer une exécution itérative (boucle) pendant une condition de test spécifiée a la valeur true.
ms.date: 05/16/2016
ms.openlocfilehash: 43e2098ad6c7f103babc2471aebe987040feb989
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53127275"
---
# <a name="loops-whiledo-expression"></a><span data-ttu-id="9dcea-103">Boucles : expression while...do</span><span class="sxs-lookup"><span data-stu-id="9dcea-103">Loops: while...do Expression</span></span>

<span data-ttu-id="9dcea-104">Le `while...do` expression est utilisée pour effectuer une exécution itérative (boucle) pendant une condition de test spécifiée a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="9dcea-104">The `while...do` expression is used to perform iterative execution (looping) while a specified test condition is true.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dcea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9dcea-105">Syntax</span></span>

```fsharp
while test-expression do
    body-expression
```

## <a name="remarks"></a><span data-ttu-id="9dcea-106">Notes</span><span class="sxs-lookup"><span data-stu-id="9dcea-106">Remarks</span></span>

<span data-ttu-id="9dcea-107">Le *expression de test* est évaluée ; si elle est `true`, le *expression de corps* est exécutée et l’expression de test est de nouveau évaluée.</span><span class="sxs-lookup"><span data-stu-id="9dcea-107">The *test-expression* is evaluated; if it is `true`, the *body-expression* is executed and the test expression is evaluated again.</span></span> <span data-ttu-id="9dcea-108">Le *expression de corps* doit avoir de type `unit`.</span><span class="sxs-lookup"><span data-stu-id="9dcea-108">The *body-expression* must have type `unit`.</span></span> <span data-ttu-id="9dcea-109">Si l’expression de test est `false`, l’itération se termine.</span><span class="sxs-lookup"><span data-stu-id="9dcea-109">If the test expression is `false`, the iteration ends.</span></span>

<span data-ttu-id="9dcea-110">L’exemple suivant illustre l’utilisation de la `while...do` expression.</span><span class="sxs-lookup"><span data-stu-id="9dcea-110">The following example illustrates the use of the `while...do` expression.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet5301.fs)]

<span data-ttu-id="9dcea-111">La sortie du code précédent est un flux de nombres aléatoires compris entre 1 et 20, la dernière qui est 10.</span><span class="sxs-lookup"><span data-stu-id="9dcea-111">The output of the previous code is a stream of random numbers between 1 and 20, the last of which is 10.</span></span>

```
13 19 8 18 16 2 10
Found a 10!
```

> [!NOTE]
> <span data-ttu-id="9dcea-112">Vous pouvez utiliser `while...do` dans les expressions de séquence et autres expressions de calcul, auquel cas une version personnalisée de la `while...do` expression est utilisée.</span><span class="sxs-lookup"><span data-stu-id="9dcea-112">You can use `while...do` in sequence expressions and other computation expressions, in which case a customized version of the `while...do` expression is used.</span></span> <span data-ttu-id="9dcea-113">Pour plus d’informations, consultez [séquences](sequences.md), [flux de travail asynchrones](asynchronous-workflows.md), et [Expressions de calcul](computation-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="9dcea-113">For more information, see [Sequences](sequences.md), [Asynchronous Workflows](asynchronous-workflows.md), and [Computation Expressions](computation-expressions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9dcea-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9dcea-114">See also</span></span>

- [<span data-ttu-id="9dcea-115">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="9dcea-115">F# Language Reference</span></span>](index.md)
- [<span data-ttu-id="9dcea-116">Boucles : `for...in` Expression</span><span class="sxs-lookup"><span data-stu-id="9dcea-116">Loops: `for...in` Expression</span></span>](loops-for-in-expression.md)
- [<span data-ttu-id="9dcea-117">Boucles : `for...to` Expression</span><span class="sxs-lookup"><span data-stu-id="9dcea-117">Loops: `for...to` Expression</span></span>](loops-for-to-expression.md)
