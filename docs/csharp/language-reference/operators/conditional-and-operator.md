---
title: '&amp;&amp;, opérateur (Informations de référence sur C#)'
ms.date: 11/06/2018
f1_keywords:
- '&&_CSharpKeyword'
helpviewer_keywords:
- '&& operator [C#]'
- logical AND operator [C#]
ms.assetid: 2e4f0a1c-92a3-40f8-8e3b-17b607f20c31
ms.openlocfilehash: d0e6d9a5aedc7dc87393e3dea070bf442b3268dc
ms.sourcegitcommit: b5cd9d5d3b75a5537fc9ad8a3f085f0bb1845ee0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "43529233"
---
# <a name="ampamp-operator-c-reference"></a><span data-ttu-id="65db4-102">&amp;&amp;, opérateur (Informations de référence sur C#)</span><span class="sxs-lookup"><span data-stu-id="65db4-102">&amp;&amp; Operator (C# Reference)</span></span>

<span data-ttu-id="65db4-103">L’opérateur logique conditionnel AND `&&`, également appelé opérateur logique AND de « court-circuit », calcule l’opération logique AND de ses opérandes [bool](../keywords/bool.md).</span><span class="sxs-lookup"><span data-stu-id="65db4-103">The conditional logical AND operator `&&`, also known as the "short-circuiting" logical AND operator, computes the logical AND of its [bool](../keywords/bool.md) operands.</span></span> <span data-ttu-id="65db4-104">Le résultat de `x && y` est `true` si `x` et `y` prennent la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="65db4-104">The result of `x && y` is `true` if both `x` and `y` evaluate to `true`.</span></span> <span data-ttu-id="65db4-105">Sinon, le résultat est `false`.</span><span class="sxs-lookup"><span data-stu-id="65db4-105">Otherwise, the result is `false`.</span></span> <span data-ttu-id="65db4-106">Si le premier opérande prend la valeur `false`, le deuxième n’est pas évalué. Le résultat de l’opération est donc `false`.</span><span class="sxs-lookup"><span data-stu-id="65db4-106">If the first operand evaluates to `false`, the second operand is not evaluated and the result of operation is `false`.</span></span> <span data-ttu-id="65db4-107">L’exemple suivant illustre ce comportement :</span><span class="sxs-lookup"><span data-stu-id="65db4-107">The following example demonstrates that behavior:</span></span>

[!code-csharp-interactive[conditional logical AND](~/samples/snippets/csharp/language-reference/operators/ConditionalLogicalOperatorsExamples.cs#And)]

<span data-ttu-id="65db4-108">[L’opérateur logique AND](and-operator.md) `&` calcule également l’opération logique AND de ses opérandes `bool`, mais il évalue toujours les deux opérandes.</span><span class="sxs-lookup"><span data-stu-id="65db4-108">The [logical AND operator](and-operator.md) `&` also computes the logical AND of its `bool` operands, but always evaluates both operands.</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="65db4-109">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="65db4-109">Operator overloadability</span></span>

<span data-ttu-id="65db4-110">Un type défini par l’utilisateur ne peut pas surcharger l’opérateur logique conditionnel AND.</span><span class="sxs-lookup"><span data-stu-id="65db4-110">A user-defined type cannot overload the conditional logical AND operator.</span></span> <span data-ttu-id="65db4-111">Toutefois, si un type défini par l’utilisateur surcharge l’opérateur [logique AND](and-operator.md) et les opérateurs [true](../keywords/true-operator.md) et [false](../keywords/false-operator.md) d’une certaine manière, l’opération `&&` peut être évaluée pour les opérandes de ce type.</span><span class="sxs-lookup"><span data-stu-id="65db4-111">However, if a user-defined type overloads the [logical AND](and-operator.md), [true](../keywords/true-operator.md), and [false](../keywords/false-operator.md) operators in a certain way, the `&&` operation can be evaluated for the operands of that type.</span></span> <span data-ttu-id="65db4-112">Pour plus d’informations, consultez la section [Opérateurs logiques conditionnels définis par l’utilisateur](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="65db4-112">For more information, see the [User-defined conditional logical operators](~/_csharplang/spec/expressions.md#user-defined-conditional-logical-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="65db4-113">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="65db4-113">C# language specification</span></span>

<span data-ttu-id="65db4-114">Pour plus d’informations, consultez la section [Opérateurs logiques conditionnels](~/_csharplang/spec/expressions.md#conditional-logical-operators) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="65db4-114">For more information, see the [Conditional logical operators](~/_csharplang/spec/expressions.md#conditional-logical-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="65db4-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65db4-115">See also</span></span>

- [<span data-ttu-id="65db4-116">Référence C#</span><span class="sxs-lookup"><span data-stu-id="65db4-116">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="65db4-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="65db4-117">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="65db4-118">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="65db4-118">C# Operators</span></span>](index.md)
- [<span data-ttu-id="65db4-119">||, opérateur</span><span class="sxs-lookup"><span data-stu-id="65db4-119">|| operator</span></span>](conditional-or-operator.md)
- [<span data-ttu-id="65db4-120">\!, opérateur</span><span class="sxs-lookup"><span data-stu-id="65db4-120">! operator</span></span>](logical-negation-operator.md)
- [<span data-ttu-id="65db4-121">&, opérateur</span><span class="sxs-lookup"><span data-stu-id="65db4-121">& operator</span></span>](and-operator.md)
