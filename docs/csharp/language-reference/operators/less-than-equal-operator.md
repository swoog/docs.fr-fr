---
title: '&lt;=, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 12/18/2018
f1_keywords:
- <=_CSharpKeyword
helpviewer_keywords:
- less than or equal to operator (<=) [C#]
- <= operator [C#]
ms.assetid: bb0caec9-d253-4105-b8bc-5252233251e4
ms.openlocfilehash: 30f42de68667756a8233fef4241bfd74ed4eff2a
ms.sourcegitcommit: 3d0c29b878f00caec288dfecb3a5c959de5aa629
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/20/2018
ms.locfileid: "53656087"
---
# <a name="lt-operator-c-reference"></a><span data-ttu-id="b266c-102">&lt;=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="b266c-102">&lt;= Operator (C# Reference)</span></span>

<span data-ttu-id="b266c-103">L’opérateur de relation « inférieur ou égal à » `<=` retourne `true` si son premier opérande est inférieur ou égal à son second opérande, `false` dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b266c-103">The "less than or equal" relational operator `<=` returns `true` if its first operand is less than or equal to its second operand, `false` otherwise.</span></span> <span data-ttu-id="b266c-104">Tous les types numériques et d’énumération prennent en charge l’opérateur `<=`.</span><span class="sxs-lookup"><span data-stu-id="b266c-104">All numeric and enumeration types support the `<=` operator.</span></span> <span data-ttu-id="b266c-105">Pour les opérandes du même type [enum](../keywords/enum.md), les valeurs correspondantes du type intégral sous-jacent sont comparées.</span><span class="sxs-lookup"><span data-stu-id="b266c-105">For operands of the same [enum](../keywords/enum.md) type, the corresponding values of the underlying integral type are compared.</span></span>

> [!NOTE]
> <span data-ttu-id="b266c-106">Pour les opérateurs de relation `==`, `>`, `<`, `>=` et `<=`, si un des opérandes n’est pas un nombre (<xref:System.Double.NaN?displayProperty=nameWithType> ou <xref:System.Single.NaN?displayProperty=nameWithType>), le résultat de l’opération est `false`.</span><span class="sxs-lookup"><span data-stu-id="b266c-106">For relational operators `==`, `>`, `<`, `>=`, and `<=`, if any of the operands is not a number (<xref:System.Double.NaN?displayProperty=nameWithType> or <xref:System.Single.NaN?displayProperty=nameWithType>) the result of operation is `false`.</span></span> <span data-ttu-id="b266c-107">Cela signifie que la valeur `NaN` n’est ni supérieure à, ni inférieure à, ni égale à n’importe quelle autre valeur `double` (ou `float`).</span><span class="sxs-lookup"><span data-stu-id="b266c-107">That means that the `NaN` value is neither greater than, less than, nor equal to any other `double` (or `float`) value.</span></span> <span data-ttu-id="b266c-108">Pour plus d’informations et des exemples, consultez l’article de référence <xref:System.Double.NaN?displayProperty=nameWithType> ou <xref:System.Single.NaN?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="b266c-108">For more information and examples, see the <xref:System.Double.NaN?displayProperty=nameWithType> or <xref:System.Single.NaN?displayProperty=nameWithType> reference article.</span></span>

<span data-ttu-id="b266c-109">L’exemple suivant illustre l’utilisation de l’opérateur `<=` :</span><span class="sxs-lookup"><span data-stu-id="b266c-109">The following example demonstrates the usage of the `<=` operator:</span></span>

[!code-csharp-interactive[less than or equal example](~/samples/snippets/csharp/language-reference/operators/GreaterAndLessOperatorsExamples.cs#LessOrEqual)]

## <a name="operator-overloadability"></a><span data-ttu-id="b266c-110">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="b266c-110">Operator overloadability</span></span>

<span data-ttu-id="b266c-111">Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) l’opérateur `<=`.</span><span class="sxs-lookup"><span data-stu-id="b266c-111">User-defined types can [overload](../keywords/operator.md) the `<=` operator.</span></span> <span data-ttu-id="b266c-112">Si un type surcharge l’opérateur « inférieur ou égal à » `<=`, il doit également surcharger l’[opérateur « supérieur ou égal à »](greater-than-equal-operator.md) `>=`.</span><span class="sxs-lookup"><span data-stu-id="b266c-112">If a type overloads the "less than or equal" operator `<=`, it must also overload the ["greater than or equal" operator](greater-than-equal-operator.md) `>=`.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="b266c-113">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="b266c-113">C# language specification</span></span>

<span data-ttu-id="b266c-114">Pour plus d’informations, consultez la section [Opérateurs relationnels et de test de type](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="b266c-114">For more information, see the [Relational and type-testing operators](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b266c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b266c-115">See also</span></span>

- [<span data-ttu-id="b266c-116">Référence C#</span><span class="sxs-lookup"><span data-stu-id="b266c-116">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="b266c-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="b266c-117">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="b266c-118">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="b266c-118">C# Operators</span></span>](index.md)
- [<span data-ttu-id="b266c-119"><, opérateur</span><span class="sxs-lookup"><span data-stu-id="b266c-119">< Operator</span></span>](less-than-operator.md)
- [<span data-ttu-id="b266c-120">==, opérateur</span><span class="sxs-lookup"><span data-stu-id="b266c-120">== Operator</span></span>](equality-comparison-operator.md)
- <xref:System.IComparable%601?displayProperty=nameWithType>
