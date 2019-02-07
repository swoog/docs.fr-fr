---
title: <, opérateur - Référence C#
ms.custom: seodec18
ms.date: 12/18/2018
f1_keywords:
- <_CSharpKeyword
helpviewer_keywords:
- less than operator (<) [C#]
- < operator [C#]
ms.assetid: 38cb91e6-79a6-48ec-9c1e-7b71fd8d2b41
ms.openlocfilehash: ab21e32b7609bc0c8753b42ccf8b6091bf3ad57b
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55286635"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="29091-102">\<, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="29091-102">\< Operator (C# Reference)</span></span>

<span data-ttu-id="29091-103">L’opérateur de relation « inférieur à » `<` retourne `true` si son premier opérande est inférieur à son second opérande, `false` dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="29091-103">The "less than" relational operator `<` returns `true` if its first operand is less than its second operand, `false` otherwise.</span></span> <span data-ttu-id="29091-104">Tous les types numériques et d’énumération prennent en charge l’opérateur `<`.</span><span class="sxs-lookup"><span data-stu-id="29091-104">All numeric and enumeration types support the `<` operator.</span></span> <span data-ttu-id="29091-105">Pour les opérandes du même type [enum](../keywords/enum.md), les valeurs correspondantes du type intégral sous-jacent sont comparées.</span><span class="sxs-lookup"><span data-stu-id="29091-105">For operands of the same [enum](../keywords/enum.md) type, the corresponding values of the underlying integral type are compared.</span></span>

> [!NOTE]
> <span data-ttu-id="29091-106">Pour les opérateurs de relation `==`, `>`, `<`, `>=` et `<=`, si un des opérandes n’est pas un nombre (<xref:System.Double.NaN?displayProperty=nameWithType> ou <xref:System.Single.NaN?displayProperty=nameWithType>), le résultat de l’opération est `false`.</span><span class="sxs-lookup"><span data-stu-id="29091-106">For relational operators `==`, `>`, `<`, `>=`, and `<=`, if any of the operands is not a number (<xref:System.Double.NaN?displayProperty=nameWithType> or <xref:System.Single.NaN?displayProperty=nameWithType>) the result of operation is `false`.</span></span> <span data-ttu-id="29091-107">Cela signifie que la valeur `NaN` n’est ni supérieure à, ni inférieure à, ni égale à n’importe quelle autre valeur `double` (ou `float`).</span><span class="sxs-lookup"><span data-stu-id="29091-107">That means that the `NaN` value is neither greater than, less than, nor equal to any other `double` (or `float`) value.</span></span> <span data-ttu-id="29091-108">Pour plus d’informations et des exemples, consultez l’article de référence <xref:System.Double.NaN?displayProperty=nameWithType> ou <xref:System.Single.NaN?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="29091-108">For more information and examples, see the <xref:System.Double.NaN?displayProperty=nameWithType> or <xref:System.Single.NaN?displayProperty=nameWithType> reference article.</span></span>

<span data-ttu-id="29091-109">L’exemple suivant illustre l’utilisation de l’opérateur `<` :</span><span class="sxs-lookup"><span data-stu-id="29091-109">The following example demonstrates the usage of the `<` operator:</span></span>

[!code-csharp-interactive[less than example](~/samples/snippets/csharp/language-reference/operators/GreaterAndLessOperatorsExamples.cs#Less)]

## <a name="operator-overloadability"></a><span data-ttu-id="29091-110">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="29091-110">Operator overloadability</span></span>

<span data-ttu-id="29091-111">Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) l’opérateur `<`.</span><span class="sxs-lookup"><span data-stu-id="29091-111">User-defined types can [overload](../keywords/operator.md) the `<` operator.</span></span> <span data-ttu-id="29091-112">Si un type surcharge l’opérateur « inférieur à » `<`, il doit également surcharger l’[opérateur « supérieur à »](greater-than-operator.md) `>`.</span><span class="sxs-lookup"><span data-stu-id="29091-112">If a type overloads the "less than" operator `<`, it must also overload the ["greater than" operator](greater-than-operator.md) `>`.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="29091-113">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="29091-113">C# language specification</span></span>

<span data-ttu-id="29091-114">Pour plus d’informations, consultez la section [Opérateurs relationnels et de test de type](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="29091-114">For more information, see the [Relational and type-testing operators](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="29091-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29091-115">See also</span></span>

- [<span data-ttu-id="29091-116">Référence C#</span><span class="sxs-lookup"><span data-stu-id="29091-116">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="29091-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="29091-117">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="29091-118">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="29091-118">C# Operators</span></span>](index.md)
- [<span data-ttu-id="29091-119"><=, opérateur</span><span class="sxs-lookup"><span data-stu-id="29091-119"><= Operator</span></span>](less-than-equal-operator.md)
- <xref:System.IComparable%601?displayProperty=nameWithType>
