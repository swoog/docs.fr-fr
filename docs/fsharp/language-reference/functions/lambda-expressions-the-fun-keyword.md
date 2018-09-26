---
title: 'Expressions lambda : mot clé fun (F#)'
description: 'Découvrez comment utiliser le mot clé F # « fun » pour définir une expression lambda, qui est une fonction anonyme.'
ms.date: 05/16/2016
ms.openlocfilehash: a37757f6b7328cd348bbf13f058a6dbc881769cf
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47231019"
---
# <a name="lambda-expressions-the-fun-keyword-f"></a><span data-ttu-id="3764a-103">Expressions lambda : mot clé fun (F#)</span><span class="sxs-lookup"><span data-stu-id="3764a-103">Lambda Expressions: The fun Keyword (F#)</span></span>

<span data-ttu-id="3764a-104">Le `fun` mot clé est utilisé pour définir une expression lambda, autrement dit, une fonction anonyme.</span><span class="sxs-lookup"><span data-stu-id="3764a-104">The `fun` keyword is used to define a lambda expression, that is, an anonymous function.</span></span>

## <a name="syntax"></a><span data-ttu-id="3764a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3764a-105">Syntax</span></span>

```fsharp
fun parameter-list -> expression
```

## <a name="remarks"></a><span data-ttu-id="3764a-106">Notes</span><span class="sxs-lookup"><span data-stu-id="3764a-106">Remarks</span></span>

<span data-ttu-id="3764a-107">Le *liste de paramètres* se compose généralement de noms et, éventuellement, de types de paramètres.</span><span class="sxs-lookup"><span data-stu-id="3764a-107">The *parameter-list* typically consists of names and, optionally, types of parameters.</span></span> <span data-ttu-id="3764a-108">En règle générale, le *liste de paramètres* peuvent être composées de n’importe quel modèle F #.</span><span class="sxs-lookup"><span data-stu-id="3764a-108">More generally, the *parameter-list* can be composed of any F# patterns.</span></span> <span data-ttu-id="3764a-109">Pour obtenir une liste complète des modèles possibles, consultez [critères spéciaux](../pattern-matching.md).</span><span class="sxs-lookup"><span data-stu-id="3764a-109">For a full list of possible patterns, see [Pattern Matching](../pattern-matching.md).</span></span> <span data-ttu-id="3764a-110">Listes de paramètres valides comprennent les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="3764a-110">Lists of valid parameters include the following examples.</span></span>

```fsharp
// Lambda expressions with parameter lists.
fun a b c -> ...
fun (a: int) b c -> ...
fun (a : int) (b : string) (c:float) -> ...

// A lambda expression with a tuple pattern.
fun (a, b) -> …

// A lambda expression with a list pattern.
fun head :: tail -> …
```

<span data-ttu-id="3764a-111">Le *expression* est le corps de la fonction, la dernière expression qui génère une valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="3764a-111">The *expression* is the body of the function, the last expression of which generates a return value.</span></span> <span data-ttu-id="3764a-112">Exemples d’expressions lambda valides sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="3764a-112">Examples of valid lambda expressions include the following:</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet301.fs)]

## <a name="using-lambda-expressions"></a><span data-ttu-id="3764a-113">Utilisation d’expressions lambda</span><span class="sxs-lookup"><span data-stu-id="3764a-113">Using Lambda Expressions</span></span>

<span data-ttu-id="3764a-114">Expressions lambda sont particulièrement utiles lorsque vous souhaitez effectuer des opérations sur une liste ou une autre collection et souhaitez éviter le travail supplémentaire de la définition d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="3764a-114">Lambda expressions are especially useful when you want to perform operations on a list or other collection and want to avoid the extra work of defining a function.</span></span> <span data-ttu-id="3764a-115">De nombreuses fonctions de bibliothèque F # prennent des valeurs de fonction en tant qu’arguments, et il peut être particulièrement pratique d’utiliser une expression lambda dans ces cas.</span><span class="sxs-lookup"><span data-stu-id="3764a-115">Many F# library functions take function values as arguments, and it can be especially convenient to use a lambda expression in those cases.</span></span> <span data-ttu-id="3764a-116">Le code suivant applique une expression lambda aux éléments d’une liste.</span><span class="sxs-lookup"><span data-stu-id="3764a-116">The following code applies a lambda expression to elements of a list.</span></span> <span data-ttu-id="3764a-117">Dans ce cas, la fonction anonyme ajoute 1 à chaque élément d’une liste.</span><span class="sxs-lookup"><span data-stu-id="3764a-117">In this case, the anonymous function adds 1 to every element of a list.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet302.fs)]

## <a name="see-also"></a><span data-ttu-id="3764a-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3764a-118">See also</span></span>

- [<span data-ttu-id="3764a-119">Fonctions</span><span class="sxs-lookup"><span data-stu-id="3764a-119">Functions</span></span>](index.md)
