---
title: 'Expressions Match (F #)'
description: 'Découvrez comment l’expression de correspondance F # fournit le contrôle de branchement basé sur la comparaison d’une expression avec un jeu de modèles.'
author: cartermp
ms.author: phcart
ms.date: 04/19/2018
ms.topic: language-reference
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.openlocfilehash: f843e6fde98eae8a10235dd5cae38ffc10a4fb9f
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="match-expressions"></a><span data-ttu-id="fad05-103">Expressions de correspondance</span><span class="sxs-lookup"><span data-stu-id="fad05-103">Match expressions</span></span>

<span data-ttu-id="fad05-104">Le `match` expression fournit le contrôle de branchement basé sur la comparaison d’une expression avec un jeu de modèles.</span><span class="sxs-lookup"><span data-stu-id="fad05-104">The `match` expression provides branching control that is based on the comparison of an expression with a set of patterns.</span></span>

## <a name="syntax"></a><span data-ttu-id="fad05-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fad05-105">Syntax</span></span>

```fsharp
// Match expression.
match test-expression with
| pattern1 [ when condition ] -> result-expression1
| pattern2 [ when condition ] -> result-expression2
| ...

// Pattern matching function.
function
| pattern1 [ when condition ] -> result-expression1
| pattern2 [ when condition ] -> result-expression2
| ...
```

## <a name="remarks"></a><span data-ttu-id="fad05-106">Notes</span><span class="sxs-lookup"><span data-stu-id="fad05-106">Remarks</span></span>

<span data-ttu-id="fad05-107">Les expressions de critères spéciaux autorisent des branchements complexes basés sur la comparaison d’une expression de test avec un jeu de modèles.</span><span class="sxs-lookup"><span data-stu-id="fad05-107">The pattern matching expressions allow for complex branching based on the comparison of a test expression with a set of patterns.</span></span> <span data-ttu-id="fad05-108">Dans le `match` expression, le *test-expression* est comparé à chaque modèle à son tour, lorsqu’une correspondance est trouvée, correspondant *expression de résultat* est évaluée et la valeur résultante est retourné en tant que la valeur de l’expression de correspondance.</span><span class="sxs-lookup"><span data-stu-id="fad05-108">In the `match` expression, the *test-expression* is compared with each pattern in turn, and when a match is found, the corresponding *result-expression* is evaluated and the resulting value is returned as the value of the match expression.</span></span>

<span data-ttu-id="fad05-109">La fonction présentée dans la syntaxe précédente mise en correspondance est une expression lambda dans le modèle de recherche est effectuée immédiatement sur l’argument.</span><span class="sxs-lookup"><span data-stu-id="fad05-109">The pattern matching function shown in the previous syntax is a lambda expression in which pattern matching is performed immediately on the argument.</span></span> <span data-ttu-id="fad05-110">Les critères spéciaux de fonction présentée dans la syntaxe précédente est équivalente à la suivante.</span><span class="sxs-lookup"><span data-stu-id="fad05-110">The pattern matching function shown in the previous syntax is equivalent to the following.</span></span>

```fsharp
fun arg ->
    match arg with
    | pattern1 [ when condition ] -> result-expression1
    | pattern2 [ when condition ] -> result-expression2
    | ...
```

<span data-ttu-id="fad05-111">Pour plus d’informations sur les expressions lambda, consultez [Expressions Lambda : le `fun` mot clé](functions/lambda-expressions-the-fun-keyword.md).</span><span class="sxs-lookup"><span data-stu-id="fad05-111">For more information about lambda expressions, see [Lambda Expressions: The `fun` Keyword](functions/lambda-expressions-the-fun-keyword.md).</span></span>

<span data-ttu-id="fad05-112">L’ensemble de modèles doit couvrir toutes les correspondances possibles de la variable d’entrée.</span><span class="sxs-lookup"><span data-stu-id="fad05-112">The whole set of patterns should cover all the possible matches of the input variable.</span></span> <span data-ttu-id="fad05-113">Souvent, vous utilisez le modèle de caractère générique (`_`) comme dernier modèle pour faire correspondre les valeurs d’entrée précédemment sans correspondance.</span><span class="sxs-lookup"><span data-stu-id="fad05-113">Frequently, you use the wildcard pattern (`_`) as the last pattern to match any previously unmatched input values.</span></span>

<span data-ttu-id="fad05-114">Le code suivant illustre quelques-unes des façons d’utiliser le `match` expression est utilisée.</span><span class="sxs-lookup"><span data-stu-id="fad05-114">The following code illustrates some of the ways in which the `match` expression is used.</span></span> <span data-ttu-id="fad05-115">Pour une référence et des exemples de tous les modèles qui peuvent être utilisés, consultez [recherche de correspondance](pattern-matching.md).</span><span class="sxs-lookup"><span data-stu-id="fad05-115">For a reference and examples of all the possible patterns that can be used, see [Pattern Matching](pattern-matching.md).</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4601.fs)]

## <a name="guards-on-patterns"></a><span data-ttu-id="fad05-116">Gardes sur des modèles</span><span class="sxs-lookup"><span data-stu-id="fad05-116">Guards on patterns</span></span>

<span data-ttu-id="fad05-117">Vous pouvez utiliser un `when` clause pour spécifier une condition supplémentaire répondant à la variable doit correspondre à un modèle.</span><span class="sxs-lookup"><span data-stu-id="fad05-117">You can use a `when` clause to specify an additional condition that the variable must satisfy to match a pattern.</span></span> <span data-ttu-id="fad05-118">Une telle clause est appelée un *protection*.</span><span class="sxs-lookup"><span data-stu-id="fad05-118">Such a clause is referred to as a *guard*.</span></span> <span data-ttu-id="fad05-119">L’expression qui suit le `when` mot clé n’est pas évaluée, sauf si une correspondance est établie pour le modèle associé à ce garde.</span><span class="sxs-lookup"><span data-stu-id="fad05-119">The expression following the `when` keyword is not evaluated unless a match is made to the pattern associated with that guard.</span></span>

<span data-ttu-id="fad05-120">L’exemple suivant illustre l’utilisation d’un garde pour spécifier une plage numérique pour un modèle de variable.</span><span class="sxs-lookup"><span data-stu-id="fad05-120">The following example illustrates the use of a guard to specify a numeric range for a variable pattern.</span></span> <span data-ttu-id="fad05-121">Notez que plusieurs conditions sont combinées à l’aide d’opérateurs booléens.</span><span class="sxs-lookup"><span data-stu-id="fad05-121">Note that multiple conditions are combined by using Boolean operators.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4602.fs)]

<span data-ttu-id="fad05-122">Notez qu’étant donné que les valeurs autres que des littéraux ne peut pas être utilisés dans le modèle, vous devez utiliser un `when` clause si vous devez comparer une partie de l’entrée à une valeur.</span><span class="sxs-lookup"><span data-stu-id="fad05-122">Note that because values other than literals cannot be used in the pattern, you must use a `when` clause if you have to compare some part of the input against a value.</span></span> <span data-ttu-id="fad05-123">Ceci est illustré dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="fad05-123">This is shown in the following code:</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet4603.fs)]

<span data-ttu-id="fad05-124">Notez que lorsqu’un modèle d’union est couverte par un module de protection, la protection s’applique aux **tous les** des modèles, et pas seulement le dernier.</span><span class="sxs-lookup"><span data-stu-id="fad05-124">Note that when a union pattern is covered by a guard, the guard applies to **all** of the patterns, not just the last one.</span></span> <span data-ttu-id="fad05-125">Par exemple, prenons le code suivant, le module de protection `when a > 12` s’applique aux deux `A a` et `B a`:</span><span class="sxs-lookup"><span data-stu-id="fad05-125">For example, given the following code, the guard `when a > 12` applies to both `A a` and `B a`:</span></span>

```fsharp
type Union =
    | A of int
    | B of int

let foo() =
    let test = A 42
    match test with
    | A a
    | B a when a > 41 -> a // the guard applies to both patterns
    | _ -> 1

foo() // returns 42
```

## <a name="see-also"></a><span data-ttu-id="fad05-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fad05-126">See also</span></span>

[<span data-ttu-id="fad05-127">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="fad05-127">F# Language Reference</span></span>](index.md)  
[<span data-ttu-id="fad05-128">Modèles actifs</span><span class="sxs-lookup"><span data-stu-id="fad05-128">Active Patterns</span></span>](active-patterns.md)  
[<span data-ttu-id="fad05-129">Critères spéciaux</span><span class="sxs-lookup"><span data-stu-id="fad05-129">Pattern Matching</span></span>](pattern-matching.md)  
