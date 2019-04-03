---
title: Opérateurs d’égalité - Informations de référence sur C#
ms.date: 03/28/2019
author: pkulikov
f1_keywords:
- ==_CSharpKeyword
- '!=_CSharpKeyword'
helpviewer_keywords:
- equality operator [C#]
- equals operator [C#]
- == operator [C#]
- inequality operator [C#]
- not equals operator [C#]
- '!= operator [C#]'
ms.openlocfilehash: 98b96f5b4c6d6ea70687a97c849e89573c67c37e
ms.sourcegitcommit: 4a8c2b8d0df44142728b68ebc842575840476f6d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/28/2019
ms.locfileid: "58545890"
---
# <a name="equality-operators-c-reference"></a><span data-ttu-id="786b5-102">Opérateurs d’égalité (Informations de référence sur C#)</span><span class="sxs-lookup"><span data-stu-id="786b5-102">Equality operators (C# Reference)</span></span>

<span data-ttu-id="786b5-103">Les opérateurs [`==` (égalité)](#equality-operator-) et [`!=` (inégalité)](#inequality-operator-) vérifient si leurs opérandes sont égaux ou non.</span><span class="sxs-lookup"><span data-stu-id="786b5-103">The [`==` (equality)](#equality-operator-) and [`!=` (inequality)](#inequality-operator-) operators check if their operands are equal or not.</span></span>

## <a name="equality-operator-"></a><span data-ttu-id="786b5-104">Opérateur d’égalité ==</span><span class="sxs-lookup"><span data-stu-id="786b5-104">Equality operator ==</span></span>

<span data-ttu-id="786b5-105">L’opérateur d’égalité `==` retourne `true` si ses opérandes sont égaux, `false` dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="786b5-105">The equality operator `==` returns `true` if its operands are equal, `false` otherwise.</span></span>

### <a name="value-types-equality"></a><span data-ttu-id="786b5-106">Égalité de types valeur</span><span class="sxs-lookup"><span data-stu-id="786b5-106">Value types equality</span></span>

<span data-ttu-id="786b5-107">Les opérandes des [types valeur intégrés](../keywords/value-types-table.md) sont égaux si leurs valeurs sont égales :</span><span class="sxs-lookup"><span data-stu-id="786b5-107">Operands of the [built-in value types](../keywords/value-types-table.md) are equal if their values are equal:</span></span>

[!code-csharp-interactive[value types equality](~/samples/snippets/csharp/language-reference/operators/EqualityAndNonEqualityExamples.cs#ValueTypesEquality)]

> [!NOTE]
> <span data-ttu-id="786b5-108">Pour les opérateurs d’égalité et de relation `==`, `>`, `<`, `>=` et `<=`, si un des opérandes n’est pas un nombre (<xref:System.Double.NaN?displayProperty=nameWithType> ou <xref:System.Single.NaN?displayProperty=nameWithType>), le résultat de l’opération est `false`.</span><span class="sxs-lookup"><span data-stu-id="786b5-108">For equality and relational operators `==`, `>`, `<`, `>=`, and `<=`, if any of the operands is not a number (<xref:System.Double.NaN?displayProperty=nameWithType> or <xref:System.Single.NaN?displayProperty=nameWithType>), the result of operation is `false`.</span></span> <span data-ttu-id="786b5-109">Cela signifie que la valeur `NaN` n’est ni supérieure à, ni inférieure à, ni égale à n’importe quelle autre valeur `double` (ou `float`), y compris `NaN`.</span><span class="sxs-lookup"><span data-stu-id="786b5-109">That means that the `NaN` value is neither greater than, less than, nor equal to any other `double` (or `float`) value, including `NaN`.</span></span> <span data-ttu-id="786b5-110">Pour plus d’informations et des exemples, consultez l’article de référence <xref:System.Double.NaN?displayProperty=nameWithType> ou <xref:System.Single.NaN?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="786b5-110">For more information and examples, see the <xref:System.Double.NaN?displayProperty=nameWithType> or <xref:System.Single.NaN?displayProperty=nameWithType> reference article.</span></span>

<span data-ttu-id="786b5-111">Deux opérandes du même type [enum](../keywords/enum.md) sont égaux si les valeurs correspondantes du type intégral sous-jacent sont égales.</span><span class="sxs-lookup"><span data-stu-id="786b5-111">Two operands of the same [enum](../keywords/enum.md) type are equal if the corresponding values of the underlying integral type are equal.</span></span>

<span data-ttu-id="786b5-112">Par défaut, les types [struct](../keywords/struct.md) définis par l’utilisateur ne prennent pas en charge l’opérateur `==`.</span><span class="sxs-lookup"><span data-stu-id="786b5-112">User-defined [struct](../keywords/struct.md) types don't support the `==` operator by default.</span></span> <span data-ttu-id="786b5-113">Pour prendre en charge l’opérateur `==`, un struct défini par l’utilisateur doit le [surcharger](#operator-overloadability).</span><span class="sxs-lookup"><span data-stu-id="786b5-113">To support the `==` operator, a user-defined struct must [overload](#operator-overloadability) it.</span></span>

<span data-ttu-id="786b5-114">À compter de C# 7.3, les opérateurs `==` et `!=` sont pris en charge par les [tuples](../../tuples.md) C#.</span><span class="sxs-lookup"><span data-stu-id="786b5-114">Beginning with C# 7.3, the `==` and `!=` operators are supported by C# [tuples](../../tuples.md).</span></span> <span data-ttu-id="786b5-115">Pour plus d’informations, consultez la section [Égalité et tuples](../../tuples.md#equality-and-tuples) de l’article [Types de tuple C#](../../tuples.md).</span><span class="sxs-lookup"><span data-stu-id="786b5-115">For more information, see the [Equality and tuples](../../tuples.md#equality-and-tuples) section of the [C# tuple types](../../tuples.md) article.</span></span>

### <a name="string-equality"></a><span data-ttu-id="786b5-116">Égalité de chaîne</span><span class="sxs-lookup"><span data-stu-id="786b5-116">String equality</span></span>

<span data-ttu-id="786b5-117">Deux opérandes [string](../keywords/string.md) sont égaux lorsque les deux sont `null` ou lorsque les deux instances de chaîne sont de même longueur et ont des caractères identiques dans chaque position de caractère :</span><span class="sxs-lookup"><span data-stu-id="786b5-117">Two [string](../keywords/string.md) operands are equal when both of them are `null` or both string instances are of the same length and have identical characters in each character position:</span></span>

[!code-csharp-interactive[string equality](~/samples/snippets/csharp/language-reference/operators/EqualityAndNonEqualityExamples.cs#StringEquality)]

<span data-ttu-id="786b5-118">Il s’agit d’une comparaison ordinale respectant la casse.</span><span class="sxs-lookup"><span data-stu-id="786b5-118">That is case-sensitive ordinal comparison.</span></span> <span data-ttu-id="786b5-119">Pour plus d’informations sur la comparaison de chaînes, consultez [Comment comparer des chaînes en C#](../../how-to/compare-strings.md).</span><span class="sxs-lookup"><span data-stu-id="786b5-119">For more information about string comparison, see [How to compare strings in C#](../../how-to/compare-strings.md).</span></span>

### <a name="reference-types-equality"></a><span data-ttu-id="786b5-120">Égalité de types référence</span><span class="sxs-lookup"><span data-stu-id="786b5-120">Reference types equality</span></span>

<span data-ttu-id="786b5-121">Deux opérandes de type référence autres que `string` sont égaux lorsqu’ils font référence au même objet :</span><span class="sxs-lookup"><span data-stu-id="786b5-121">Two other than `string` reference type operands are equal when they refer to the same object:</span></span>

[!code-csharp-interactive[reference type equality](~/samples/snippets/csharp/language-reference/operators/EqualityAndNonEqualityExamples.cs#ReferenceTypesEquality)]

<span data-ttu-id="786b5-122">Comme le montre l’exemple, les types référence définis par l’utilisateur prennent en charge l’opérateur `==` par défaut.</span><span class="sxs-lookup"><span data-stu-id="786b5-122">As the example shows, user-defined reference types support the `==` operator by default.</span></span> <span data-ttu-id="786b5-123">Un type référence défini par l’utilisateur peut toutefois surcharger l’opérateur `==`.</span><span class="sxs-lookup"><span data-stu-id="786b5-123">However, a user-defined reference type can overload the `==` operator.</span></span> <span data-ttu-id="786b5-124">Si un type référence surcharge l’opérateur `==`, utilisez la méthode <xref:System.Object.ReferenceEquals%2A?displayProperty=nameWithType> pour vérifier si deux références de ce type font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="786b5-124">If a reference type overloads the `==` operator, use the <xref:System.Object.ReferenceEquals%2A?displayProperty=nameWithType> method to check if two references of that type refer to the same object.</span></span>

## <a name="inequality-operator-"></a><span data-ttu-id="786b5-125">Opérateur d’inégalité !=</span><span class="sxs-lookup"><span data-stu-id="786b5-125">Inequality operator !=</span></span>

<span data-ttu-id="786b5-126">L’opérateur d’inégalité `!=` retourne `true` si ses opérandes ne sont pas égaux, `false` dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="786b5-126">The inequality operator `!=` returns `true` if its operands are not equal, `false` otherwise.</span></span> <span data-ttu-id="786b5-127">Pour les opérandes des [types intégrés](../keywords/built-in-types-table.md), l’expression `x != y` produit le même résultat que l’expression `!(x == y)`.</span><span class="sxs-lookup"><span data-stu-id="786b5-127">For the operands of the [built-in types](../keywords/built-in-types-table.md), the expression `x != y` produces the same result as the expression `!(x == y)`.</span></span> <span data-ttu-id="786b5-128">Pour plus d’informations sur l’égalité des types, consultez la section [Opérateur d’égalité](#equality-operator-).</span><span class="sxs-lookup"><span data-stu-id="786b5-128">For more information about type equality, see the [Equality operator](#equality-operator-) section.</span></span>

<span data-ttu-id="786b5-129">L’exemple suivant illustre l’utilisation de l’opérateur `!=` :</span><span class="sxs-lookup"><span data-stu-id="786b5-129">The following example demonstrates the usage of the `!=` operator:</span></span>

[!code-csharp-interactive[non-equality examples](~/samples/snippets/csharp/language-reference/operators/EqualityAndNonEqualityExamples.cs#NonEquality)]

## <a name="operator-overloadability"></a><span data-ttu-id="786b5-130">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="786b5-130">Operator overloadability</span></span>

<span data-ttu-id="786b5-131">Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) les opérateurs `==` et `!=`.</span><span class="sxs-lookup"><span data-stu-id="786b5-131">User-defined types can [overload](../keywords/operator.md) the `==` and `!=` operators.</span></span> <span data-ttu-id="786b5-132">Si un type surcharge un des deux opérateurs, il doit aussi en surcharger un autre.</span><span class="sxs-lookup"><span data-stu-id="786b5-132">If a type overloads one of the two operators, it must also overload another one.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="786b5-133">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="786b5-133">C# language specification</span></span>

<span data-ttu-id="786b5-134">Pour plus d’informations, consultez la section [Opérateurs relationnels et de test de type](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators) de la [spécification du langage C#](~/_csharplang/spec/introduction.md).</span><span class="sxs-lookup"><span data-stu-id="786b5-134">For more information, see the [Relational and type-testing operators](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators) section of the [C# language specification](~/_csharplang/spec/introduction.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="786b5-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="786b5-135">See also</span></span>

- [<span data-ttu-id="786b5-136">Référence C#</span><span class="sxs-lookup"><span data-stu-id="786b5-136">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="786b5-137">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="786b5-137">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="786b5-138">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="786b5-138">C# Operators</span></span>](index.md)
- <xref:System.IEquatable%601?displayProperty=nameWithType>
- <xref:System.Object.Equals%2A?displayProperty=nameWithType>
- <xref:System.Object.ReferenceEquals%2A?displayProperty=nameWithType>
- [<span data-ttu-id="786b5-139">Comparaisons d’égalité</span><span class="sxs-lookup"><span data-stu-id="786b5-139">Equality comparisons</span></span>](../../programming-guide/statements-expressions-operators/equality-comparisons.md)
