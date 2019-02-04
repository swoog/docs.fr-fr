---
title: '>=, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 12/18/2018
f1_keywords:
- '>=_CSharpKeyword'
helpviewer_keywords:
- greater than or equal to operator (>=) [C#]
- '>= operator [C#]'
ms.assetid: 0db4dcaf-56a3-4884-a7ad-35f64978a58d
ms.openlocfilehash: 821369734e64648714bf89efb0c02d12d4d816e3
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55256551"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="c83a4-102">>=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="c83a4-102">>= Operator (C# Reference)</span></span>

<span data-ttu-id="c83a4-103">L’opérateur de relation « supérieur ou égal à » `>=` retourne `true` si son premier opérande est supérieur ou égal à son second opérande, `false` dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c83a4-103">The "greater than or equal" relational operator `>=` returns `true` if its first operand is greater than or equal to its second operand, `false` otherwise.</span></span> <span data-ttu-id="c83a4-104">Tous les types numériques et d’énumération prennent en charge l’opérateur `>=`.</span><span class="sxs-lookup"><span data-stu-id="c83a4-104">All numeric and  enumeration types support the `>=` operator.</span></span> <span data-ttu-id="c83a4-105">Pour les opérandes du même type [enum](../keywords/enum.md), les valeurs correspondantes du type intégral sous-jacent sont comparées.</span><span class="sxs-lookup"><span data-stu-id="c83a4-105">For operands of the same [enum](../keywords/enum.md) type, the corresponding values of the underlying integral type are compared.</span></span>

> [!NOTE]
> <span data-ttu-id="c83a4-106">Pour les opérateurs de relation `==`, `>`, `<`, `>=` et `<=`, si un des opérandes n’est pas un nombre (<xref:System.Double.NaN?displayProperty=nameWithType> ou <xref:System.Single.NaN?displayProperty=nameWithType>), le résultat de l’opération est `false`.</span><span class="sxs-lookup"><span data-stu-id="c83a4-106">For relational operators `==`, `>`, `<`, `>=`, and `<=`, if any of the operands is not a number (<xref:System.Double.NaN?displayProperty=nameWithType> or <xref:System.Single.NaN?displayProperty=nameWithType>) the result of operation is `false`.</span></span> <span data-ttu-id="c83a4-107">Cela signifie que la valeur `NaN` n’est ni supérieure à, ni inférieure à, ni égale à n’importe quelle autre valeur `double` (ou `float`).</span><span class="sxs-lookup"><span data-stu-id="c83a4-107">That means that the `NaN` value is neither greater than, less than, nor equal to any other `double` (or `float`) value.</span></span> <span data-ttu-id="c83a4-108">Pour plus d’informations et des exemples, consultez l’article de référence <xref:System.Double.NaN?displayProperty=nameWithType> ou <xref:System.Single.NaN?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="c83a4-108">For more information and examples, see the <xref:System.Double.NaN?displayProperty=nameWithType> or <xref:System.Single.NaN?displayProperty=nameWithType> reference article.</span></span>

<span data-ttu-id="c83a4-109">L’exemple suivant illustre l’utilisation de l’opérateur `>=` :</span><span class="sxs-lookup"><span data-stu-id="c83a4-109">The following example demonstrates the usage of the `>=` operator:</span></span>

[!code-csharp-interactive[greater than or equal example](~/samples/snippets/csharp/language-reference/operators/GreaterAndLessOperatorsExamples.cs#GreaterOrEqual)]

## <a name="operator-overloadability"></a><span data-ttu-id="c83a4-110">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="c83a4-110">Operator overloadability</span></span>

<span data-ttu-id="c83a4-111">Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) l’opérateur `>=`.</span><span class="sxs-lookup"><span data-stu-id="c83a4-111">User-defined types can [overload](../keywords/operator.md) the `>=` operator.</span></span> <span data-ttu-id="c83a4-112">Si un type surcharge l’opérateur « supérieur ou égal à » `>=`, il doit également surcharger l’[opérateur « inférieur ou égal à »](less-than-equal-operator.md) `<=`.</span><span class="sxs-lookup"><span data-stu-id="c83a4-112">If a type overloads the "greater than or equal" operator `>=`, it must also overload the ["less than or equal" operator](less-than-equal-operator.md) `<=`.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="c83a4-113">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="c83a4-113">C# language specification</span></span>

<span data-ttu-id="c83a4-114">Pour plus d’informations, consultez la section [Opérateurs relationnels et de test de type](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="c83a4-114">For more information, see the [Relational and type-testing operators](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c83a4-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c83a4-115">See also</span></span>

- [<span data-ttu-id="c83a4-116">Référence C#</span><span class="sxs-lookup"><span data-stu-id="c83a4-116">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="c83a4-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="c83a4-117">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="c83a4-118">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="c83a4-118">C# Operators</span></span>](index.md)
- [<span data-ttu-id="c83a4-119">>, opérateur</span><span class="sxs-lookup"><span data-stu-id="c83a4-119">> Operator</span></span>](greater-than-operator.md)
- [<span data-ttu-id="c83a4-120">==, opérateur</span><span class="sxs-lookup"><span data-stu-id="c83a4-120">== Operator</span></span>](equality-comparison-operator.md)
- <xref:System.IComparable%601?displayProperty=nameWithType>
