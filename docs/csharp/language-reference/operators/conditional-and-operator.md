---
title: '&amp;&amp; Opérateur - Référence C#'
ms.custom: seodec18
ms.date: 11/06/2018
f1_keywords:
- '&&_CSharpKeyword'
helpviewer_keywords:
- '&& operator [C#]'
- logical AND operator [C#]
ms.assetid: 2e4f0a1c-92a3-40f8-8e3b-17b607f20c31
ms.openlocfilehash: 82442f50275f21e0a0748951dc50628a8d7e11bb
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53243584"
---
# <a name="ampamp-operator-c-reference"></a><span data-ttu-id="a880f-102">&amp;&amp;, opérateur (Informations de référence sur C#)</span><span class="sxs-lookup"><span data-stu-id="a880f-102">&amp;&amp; Operator (C# Reference)</span></span>

<span data-ttu-id="a880f-103">L’opérateur logique conditionnel AND `&&`, également appelé opérateur logique AND de « court-circuit », calcule l’opération logique AND de ses opérandes [bool](../keywords/bool.md).</span><span class="sxs-lookup"><span data-stu-id="a880f-103">The conditional logical AND operator `&&`, also known as the "short-circuiting" logical AND operator, computes the logical AND of its [bool](../keywords/bool.md) operands.</span></span> <span data-ttu-id="a880f-104">Le résultat de `x && y` est `true` si `x` et `y` prennent la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="a880f-104">The result of `x && y` is `true` if both `x` and `y` evaluate to `true`.</span></span> <span data-ttu-id="a880f-105">Sinon, le résultat est `false`.</span><span class="sxs-lookup"><span data-stu-id="a880f-105">Otherwise, the result is `false`.</span></span> <span data-ttu-id="a880f-106">Si le premier opérande prend la valeur `false`, le deuxième n’est pas évalué. Le résultat de l’opération est donc `false`.</span><span class="sxs-lookup"><span data-stu-id="a880f-106">If the first operand evaluates to `false`, the second operand is not evaluated and the result of operation is `false`.</span></span> <span data-ttu-id="a880f-107">L’exemple suivant illustre ce comportement :</span><span class="sxs-lookup"><span data-stu-id="a880f-107">The following example demonstrates that behavior:</span></span>

[!code-csharp-interactive[conditional logical AND](~/samples/snippets/csharp/language-reference/operators/ConditionalLogicalOperatorsExamples.cs#And)]

<span data-ttu-id="a880f-108">[L’opérateur logique AND](and-operator.md) `&` calcule également l’opération logique AND de ses opérandes `bool`, mais il évalue toujours les deux opérandes.</span><span class="sxs-lookup"><span data-stu-id="a880f-108">The [logical AND operator](and-operator.md) `&` also computes the logical AND of its `bool` operands, but always evaluates both operands.</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="a880f-109">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="a880f-109">Operator overloadability</span></span>

<span data-ttu-id="a880f-110">Un type défini par l’utilisateur ne peut pas surcharger l’opérateur logique conditionnel AND.</span><span class="sxs-lookup"><span data-stu-id="a880f-110">A user-defined type cannot overload the conditional logical AND operator.</span></span> <span data-ttu-id="a880f-111">Toutefois, si un type défini par l’utilisateur surcharge l’opérateur [logique AND](and-operator.md) et les [opérateurs true et false](../keywords/true-false-operators.md) d’une certaine manière, l’opération `&&` peut être évaluée pour les opérandes de ce type.</span><span class="sxs-lookup"><span data-stu-id="a880f-111">However, if a user-defined type overloads the [logical AND](and-operator.md) and [true and false operators](../keywords/true-false-operators.md) in a certain way, the `&&` operation can be evaluated for the operands of that type.</span></span> <span data-ttu-id="a880f-112">Pour plus d’informations, consultez la section [Opérateurs logiques conditionnels définis par l’utilisateur](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="a880f-112">For more information, see the [User-defined conditional logical operators](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="a880f-113">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="a880f-113">C# language specification</span></span>

<span data-ttu-id="a880f-114">Pour plus d’informations, consultez la section [Opérateurs logiques conditionnels](~/_csharplang/spec/expressions.md#conditional-logical-operators) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="a880f-114">For more information, see the [Conditional logical operators](~/_csharplang/spec/expressions.md#conditional-logical-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a880f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a880f-115">See also</span></span>

- [<span data-ttu-id="a880f-116">Référence C#</span><span class="sxs-lookup"><span data-stu-id="a880f-116">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="a880f-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="a880f-117">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="a880f-118">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="a880f-118">C# Operators</span></span>](index.md)
- [<span data-ttu-id="a880f-119">||, opérateur</span><span class="sxs-lookup"><span data-stu-id="a880f-119">|| operator</span></span>](conditional-or-operator.md)
- [<span data-ttu-id="a880f-120">\!, opérateur</span><span class="sxs-lookup"><span data-stu-id="a880f-120">! operator</span></span>](logical-negation-operator.md)
- [<span data-ttu-id="a880f-121">&, opérateur</span><span class="sxs-lookup"><span data-stu-id="a880f-121">& operator</span></span>](and-operator.md)
