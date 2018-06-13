---
title: 'Exceptions : expression try...finally (F#)'
description: "Découvrez comment F # ' try... finally' expression vous permet d’exécuter du code de nettoyage même si un bloc de code lève une exception."
ms.date: 05/16/2016
ms.openlocfilehash: a5fdec7b3986fc9a85c34b08d20dc31947c92b2e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33563491"
---
# <a name="exceptions-the-tryfinally-expression"></a><span data-ttu-id="67527-103">Exceptions : expression try...finally</span><span class="sxs-lookup"><span data-stu-id="67527-103">Exceptions: The try...finally Expression</span></span>

<span data-ttu-id="67527-104">Le `try...finally` expression vous permet d’exécuter du code de nettoyage même si un bloc de code lève une exception.</span><span class="sxs-lookup"><span data-stu-id="67527-104">The `try...finally` expression enables you to execute clean-up code even if a block of code throws an exception.</span></span>


## <a name="syntax"></a><span data-ttu-id="67527-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67527-105">Syntax</span></span>

```fsharp
try
    expression1
finally
    expression2
```

## <a name="remarks"></a><span data-ttu-id="67527-106">Notes</span><span class="sxs-lookup"><span data-stu-id="67527-106">Remarks</span></span>
<span data-ttu-id="67527-107">Le `try...finally` expression peut être utilisée pour exécuter le code dans *expression2* dans la syntaxe précédente, indépendamment de si une exception est générée pendant l’exécution de *expression1*.</span><span class="sxs-lookup"><span data-stu-id="67527-107">The `try...finally` expression can be used to execute the code in *expression2* in the preceding syntax regardless of whether an exception is generated during the execution of *expression1*.</span></span>

<span data-ttu-id="67527-108">Le type de *expression2* ne contribue pas à la valeur de l’expression entière ; le type retourné lorsqu’une exception ne se produit pas est la dernière valeur dans *expression1*.</span><span class="sxs-lookup"><span data-stu-id="67527-108">The type of *expression2* does not contribute to the value of the whole expression; the type returned when an exception does not occur is the last value in *expression1*.</span></span> <span data-ttu-id="67527-109">Lorsqu’une exception se produit, aucune valeur n’est retournée et le flux de contrôle est transféré vers le Gestionnaire d’exceptions correspondant suivant dans la pile des appels.</span><span class="sxs-lookup"><span data-stu-id="67527-109">When an exception does occur, no value is returned and the flow of control transfers to the next matching exception handler up the call stack.</span></span> <span data-ttu-id="67527-110">Si aucun gestionnaire d’exceptions n’est trouvée, le programme se termine.</span><span class="sxs-lookup"><span data-stu-id="67527-110">If no exception handler is found, the program terminates.</span></span> <span data-ttu-id="67527-111">Avant que le code dans un gestionnaire correspondant est exécuté ou que le programme se termine, le code dans le `finally` branche est exécutée.</span><span class="sxs-lookup"><span data-stu-id="67527-111">Before the code in a matching handler is executed or the program terminates, the code in the `finally` branch is executed.</span></span>

<span data-ttu-id="67527-112">Le code suivant illustre l’utilisation de la `try...finally` expression.</span><span class="sxs-lookup"><span data-stu-id="67527-112">The following code demonstrates the use of the `try...finally` expression.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet5701.fs)]

<span data-ttu-id="67527-113">La sortie dans la console est la suivante.</span><span class="sxs-lookup"><span data-stu-id="67527-113">The output to the console is as follows.</span></span>

```
Closing stream
Exception handled.
```

<span data-ttu-id="67527-114">Comme vous pouvez le voir à partir de la sortie, le flux a été fermé avant que l’exception externe a été gérée et le fichier `test.txt` contient le texte `test1`, ce qui signifie que les mémoires tampons ont été vidés et écrites sur le disque même si l’exception transférés contrôle au gestionnaire d’exceptions externe.</span><span class="sxs-lookup"><span data-stu-id="67527-114">As you can see from the output, the stream was closed before the outer exception was handled, and the file `test.txt` contains the text `test1`, which indicates that the buffers were flushed and written to disk even though the exception transferred control to the outer exception handler.</span></span>

<span data-ttu-id="67527-115">Notez que la `try...with` est une construction distincte à partir de la `try...finally` construire.</span><span class="sxs-lookup"><span data-stu-id="67527-115">Note that the `try...with` construct is a separate construct from the `try...finally` construct.</span></span> <span data-ttu-id="67527-116">Par conséquent, si votre code requiert à la fois un `with` bloc et un `finally` bloc, vous devez imbriquer les deux constructions, comme dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="67527-116">Therefore, if your code requires both a `with` block and a `finally` block, you have to nest the two constructs, as in the following code example.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet5702.fs)]

<span data-ttu-id="67527-117">Dans le contexte d’expressions de calcul, y compris les expressions de séquence et flux de travail asynchrones, **try... finally** expressions peuvent avoir une implémentation personnalisée.</span><span class="sxs-lookup"><span data-stu-id="67527-117">In the context of computation expressions, including sequence expressions and asynchronous workflows, **try...finally** expressions can have a custom implementation.</span></span> <span data-ttu-id="67527-118">Pour plus d’informations, consultez [Expressions de calcul](../computation-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="67527-118">For more information, see [Computation Expressions](../computation-expressions.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="67527-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67527-119">See Also</span></span>
[<span data-ttu-id="67527-120">Gestion des exceptions</span><span class="sxs-lookup"><span data-stu-id="67527-120">Exception Handling</span></span>](index.md)

[<span data-ttu-id="67527-121">Exceptions : expression `try...with`</span><span class="sxs-lookup"><span data-stu-id="67527-121">Exceptions: The `try...with` Expression</span></span>](the-try-with-expression.md)
