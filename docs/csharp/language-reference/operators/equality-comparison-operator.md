---
title: ==, opérateur - Référence C#
ms.custom: seodec18
ms.date: 12/14/2018
f1_keywords:
- ==_CSharpKeyword
helpviewer_keywords:
- == operator [C#]
- equality operator [C#]
ms.assetid: 34c6b597-caa2-4855-a7cd-38ecdd11bd07
ms.openlocfilehash: 6d86348eefc87e847267f262141ff49e5d51faae
ms.sourcegitcommit: 3d0c29b878f00caec288dfecb3a5c959de5aa629
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/20/2018
ms.locfileid: "53655957"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="58d8c-102">==, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="58d8c-102">== Operator (C# Reference)</span></span>

<span data-ttu-id="58d8c-103">L’opérateur d’égalité `==` retourne `true` si ses opérandes sont égaux, `false` dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="58d8c-103">The equality operator `==` returns `true` if its operands are equal, `false` otherwise.</span></span>

## <a name="value-types-equality"></a><span data-ttu-id="58d8c-104">Égalité de types valeur</span><span class="sxs-lookup"><span data-stu-id="58d8c-104">Value types equality</span></span>

<span data-ttu-id="58d8c-105">Les opérandes des [types valeur intégrés](../keywords/value-types-table.md) sont égaux si leurs valeurs sont égales :</span><span class="sxs-lookup"><span data-stu-id="58d8c-105">Operands of the [built-in value types](../keywords/value-types-table.md) are equal if their values are equal:</span></span>

[!code-csharp-interactive[value types equality](~/samples/snippets/csharp/language-reference/operators/EqualityAndNonEqualityExamples.cs#ValueTypesEquality)]

> [!NOTE]
> <span data-ttu-id="58d8c-106">Pour les opérateurs de relation `==`, `>`, `<`, `>=` et `<=`, si un des opérandes n’est pas un nombre (<xref:System.Double.NaN?displayProperty=nameWithType> ou <xref:System.Single.NaN?displayProperty=nameWithType>), le résultat de l’opération est `false`.</span><span class="sxs-lookup"><span data-stu-id="58d8c-106">For relational operators `==`, `>`, `<`, `>=`, and `<=`, if any of the operands is not a number (<xref:System.Double.NaN?displayProperty=nameWithType> or <xref:System.Single.NaN?displayProperty=nameWithType>) the result of operation is `false`.</span></span> <span data-ttu-id="58d8c-107">Cela signifie que la valeur `NaN` n’est ni supérieure à, ni inférieure à, ni égale à n’importe quelle autre valeur `double` (ou `float`).</span><span class="sxs-lookup"><span data-stu-id="58d8c-107">That means that the `NaN` value is neither greater than, less than, nor equal to any other `double` (or `float`) value.</span></span> <span data-ttu-id="58d8c-108">Pour plus d’informations et des exemples, consultez l’article de référence <xref:System.Double.NaN?displayProperty=nameWithType> ou <xref:System.Single.NaN?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="58d8c-108">For more information and examples, see the <xref:System.Double.NaN?displayProperty=nameWithType> or <xref:System.Single.NaN?displayProperty=nameWithType> reference article.</span></span>

<span data-ttu-id="58d8c-109">Deux opérandes du même type [enum](../keywords/enum.md) sont égaux si les valeurs correspondantes du type intégral sous-jacent sont égales.</span><span class="sxs-lookup"><span data-stu-id="58d8c-109">Two operands of the same [enum](../keywords/enum.md) type are equal if the corresponding values of the underlying integral type are equal.</span></span>

<span data-ttu-id="58d8c-110">Par défaut, l’opérateur `==` n’est pas défini pour un type [struct](../keywords/struct.md) défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="58d8c-110">By default, the `==` operator is not defined for a user-defined [struct](../keywords/struct.md) type.</span></span> <span data-ttu-id="58d8c-111">Un type défini par l’utilisateur peut [surcharger](#operator-overloadability) l’opérateur `==`.</span><span class="sxs-lookup"><span data-stu-id="58d8c-111">A user-defined type can [overload](#operator-overloadability) the `==` operator.</span></span>

<span data-ttu-id="58d8c-112">À compter de C# 7.3, les opérateurs `==` et [`!=`](not-equal-operator.md) sont pris en charge par les [tuples](../../tuples.md) C#.</span><span class="sxs-lookup"><span data-stu-id="58d8c-112">Beginning with C# 7.3, the `==` and [`!=`](not-equal-operator.md) operators are supported by C# [tuples](../../tuples.md).</span></span> <span data-ttu-id="58d8c-113">Pour plus d’informations, consultez la section [Égalité et tuples](../../tuples.md#equality-and-tuples) de l’article [Types de tuple C#](../../tuples.md).</span><span class="sxs-lookup"><span data-stu-id="58d8c-113">For more information, see the [Equality and tuples](../../tuples.md#equality-and-tuples) section of the [C# tuple types](../../tuples.md) article.</span></span>

## <a name="string-equality"></a><span data-ttu-id="58d8c-114">Égalité de chaîne</span><span class="sxs-lookup"><span data-stu-id="58d8c-114">String equality</span></span>

<span data-ttu-id="58d8c-115">Deux opérandes [string](../keywords/string.md) sont égaux lorsque les deux sont `null` ou lorsque les deux instances de chaîne sont de même longueur et ont des caractères identiques dans chaque position de caractère :</span><span class="sxs-lookup"><span data-stu-id="58d8c-115">Two [string](../keywords/string.md) operands are equal when both of them are `null` or both string instances are of the same length and have identical characters in each character position:</span></span>

[!code-csharp-interactive[string equality](~/samples/snippets/csharp/language-reference/operators/EqualityAndNonEqualityExamples.cs#StringEquality)]

<span data-ttu-id="58d8c-116">Il s’agit d’une comparaison ordinale respectant la casse.</span><span class="sxs-lookup"><span data-stu-id="58d8c-116">That is case-sensitive ordinal comparison.</span></span> <span data-ttu-id="58d8c-117">Pour plus d’informations sur la comparaison de chaînes, consultez [Comment comparer des chaînes en C#](../../how-to/compare-strings.md).</span><span class="sxs-lookup"><span data-stu-id="58d8c-117">For more information about how to compare strings, see [How to compare strings in C#](../../how-to/compare-strings.md).</span></span>

## <a name="reference-types-equality"></a><span data-ttu-id="58d8c-118">Égalité de types référence</span><span class="sxs-lookup"><span data-stu-id="58d8c-118">Reference types equality</span></span>

<span data-ttu-id="58d8c-119">Deux opérandes de type référence autres que `string` sont égaux lorsqu’ils font référence au même objet :</span><span class="sxs-lookup"><span data-stu-id="58d8c-119">Two other than `string` reference type operands are equal when they refer to the same object:</span></span>

[!code-csharp-interactive[reference type equality](~/samples/snippets/csharp/language-reference/operators/EqualityAndNonEqualityExamples.cs#ReferenceTypesEquality)]

<span data-ttu-id="58d8c-120">L’exemple montre que l’opérateur `==` est pris en charge par les types référence définis par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="58d8c-120">The example shows that the `==` operator is supported by user-defined reference types.</span></span> <span data-ttu-id="58d8c-121">Un type référence défini par l’utilisateur peut toutefois surcharger l’opérateur `==`.</span><span class="sxs-lookup"><span data-stu-id="58d8c-121">However, a user-defined reference type can overload the `==` operator.</span></span> <span data-ttu-id="58d8c-122">Si un type référence surcharge l’opérateur `==`, utilisez la méthode <xref:System.Object.ReferenceEquals%2A?displayProperty=nameWithType> pour vérifier si deux références de ce type font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="58d8c-122">If a reference type overloads the `==` operator, use the <xref:System.Object.ReferenceEquals%2A?displayProperty=nameWithType> method to check if two references of that type refer to the same object.</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="58d8c-123">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="58d8c-123">Operator overloadability</span></span>

<span data-ttu-id="58d8c-124">Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) l’opérateur `==`.</span><span class="sxs-lookup"><span data-stu-id="58d8c-124">User-defined types can [overload](../keywords/operator.md) the `==` operator.</span></span> <span data-ttu-id="58d8c-125">Si un type surcharge l’opérateur d’égalité `==`, il doit également surcharger l’[opérateur d’inégalité](not-equal-operator.md) `!=`.</span><span class="sxs-lookup"><span data-stu-id="58d8c-125">If a type overloads the equality operator `==`, it must also overload the [inequality operator](not-equal-operator.md) `!=`.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="58d8c-126">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="58d8c-126">C# language specification</span></span>

<span data-ttu-id="58d8c-127">Pour plus d’informations, consultez la section [Opérateurs relationnels et de test de type](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="58d8c-127">For more information, see the [Relational and type-testing operators](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="58d8c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58d8c-128">See also</span></span>

- [<span data-ttu-id="58d8c-129">Référence C#</span><span class="sxs-lookup"><span data-stu-id="58d8c-129">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="58d8c-130">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="58d8c-130">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="58d8c-131">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="58d8c-131">C# Operators</span></span>](index.md)
- [<span data-ttu-id="58d8c-132">Comparaisons d’égalité</span><span class="sxs-lookup"><span data-stu-id="58d8c-132">Equality comparisons</span></span>](../../programming-guide/statements-expressions-operators/equality-comparisons.md)
