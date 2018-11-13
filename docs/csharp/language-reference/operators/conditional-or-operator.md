---
title: '||, opérateur (référence C#)'
ms.date: 11/06/2018
f1_keywords:
- '||_CSharpKeyword'
helpviewer_keywords:
- logical OR operator [C#]
- conditional-OR operator (||) [C#]
- '|| operator [C#]'
ms.assetid: 7d442d8e-400d-421f-b4d2-034bf82bcbdc
ms.openlocfilehash: a391078372e4ec0a3882bed4515733adedffb547
ms.sourcegitcommit: b5cd9d5d3b75a5537fc9ad8a3f085f0bb1845ee0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "42925538"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="5119c-102">||, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="5119c-102">|| Operator (C# Reference)</span></span>

<span data-ttu-id="5119c-103">L’opérateur logique conditionnel OR `||`, également appelé opérateur logique OR de « court-circuit », calcule l’opération logique OR de ses opérandes [bool](../keywords/bool.md).</span><span class="sxs-lookup"><span data-stu-id="5119c-103">The conditional logical OR operator `||`, also known as the "short-circuiting" logical OR operator, computes the logical OR of its [bool](../keywords/bool.md) operands.</span></span> <span data-ttu-id="5119c-104">Le résultat de `x || y` est `true` si `x` ou `y` prend la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="5119c-104">The result of `x || y` is `true` if either `x` or `y` evaluates to `true`.</span></span> <span data-ttu-id="5119c-105">Sinon, le résultat est `false`.</span><span class="sxs-lookup"><span data-stu-id="5119c-105">Otherwise, the result is `false`.</span></span> <span data-ttu-id="5119c-106">Si le premier opérande prend la valeur `true`, le deuxième n’est pas évalué. Le résultat de l’opération est donc `true`.</span><span class="sxs-lookup"><span data-stu-id="5119c-106">If the first operand evaluates to `true`, the second operand is not evaluated and the result of operation is `true`.</span></span> <span data-ttu-id="5119c-107">L’exemple suivant illustre ce comportement :</span><span class="sxs-lookup"><span data-stu-id="5119c-107">The following example demonstrates that behavior:</span></span>

[!code-csharp-interactive[conditional logical OR](~/samples/snippets/csharp/language-reference/operators/ConditionalLogicalOperatorsExamples.cs#Or)]

<span data-ttu-id="5119c-108">[L’opérateur logique OR](or-operator.md) `|` calcule également l’opération logique OR de ses opérandes `bool`, mais il évalue toujours les deux opérandes.</span><span class="sxs-lookup"><span data-stu-id="5119c-108">The [logical OR operator](or-operator.md) `|` also computes the logical OR of its `bool` operands, but always evaluates both operands.</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="5119c-109">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="5119c-109">Operator overloadability</span></span>

<span data-ttu-id="5119c-110">Un type défini par l’utilisateur ne peut pas surcharger l’opérateur logique conditionnel OR.</span><span class="sxs-lookup"><span data-stu-id="5119c-110">A user-defined type cannot overload the conditional logical OR operator.</span></span> <span data-ttu-id="5119c-111">Toutefois, si un type défini par l’utilisateur surcharge l’opérateur [logique OR](or-operator.md) et les opérateurs [true](../keywords/true-operator.md) et [false](../keywords/false-operator.md) d’une certaine manière, l’opération `||` peut être évaluée pour les opérandes de ce type.</span><span class="sxs-lookup"><span data-stu-id="5119c-111">However, if a user-defined type overloads the [logical OR](or-operator.md), [true](../keywords/true-operator.md), and [false](../keywords/false-operator.md) operators in a certain way, the `||` operation can be evaluated for the operands of that type.</span></span> <span data-ttu-id="5119c-112">Pour plus d’informations, consultez la section [Opérateurs logiques conditionnels définis par l’utilisateur](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="5119c-112">For more information, see the [User-defined conditional logical operators](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="5119c-113">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="5119c-113">C# language specification</span></span>

<span data-ttu-id="5119c-114">Pour plus d’informations, consultez la section [Opérateurs logiques conditionnels](~/_csharplang/spec/expressions.md#conditional-logical-operators) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="5119c-114">For more information, see the [Conditional logical operators](~/_csharplang/spec/expressions.md#conditional-logical-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5119c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5119c-115">See also</span></span>

- [<span data-ttu-id="5119c-116">Référence C#</span><span class="sxs-lookup"><span data-stu-id="5119c-116">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="5119c-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="5119c-117">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="5119c-118">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="5119c-118">C# Operators</span></span>](index.md)
- [<span data-ttu-id="5119c-119">&&, opérateur</span><span class="sxs-lookup"><span data-stu-id="5119c-119">&& operator</span></span>](conditional-and-operator.md)
- [!, opérateur]<span data-ttu-id="5119c-120">(logical-negation-operator.md)</span><span class="sxs-lookup"><span data-stu-id="5119c-120">(logical-negation-operator.md)</span></span>
- [<span data-ttu-id="5119c-121">|, opérateur</span><span class="sxs-lookup"><span data-stu-id="5119c-121">| operator</span></span>](or-operator.md)
