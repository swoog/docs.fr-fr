---
title: + Opérateur - Référence C#
ms.custom: seodec18
ms.date: 10/22/2018
f1_keywords:
- +_CSharpKeyword
helpviewer_keywords:
- + operator [C#]
- concatenation operator [C#]
- addition operator [C#]
ms.assetid: 93e56486-bb42-43c1-bd43-60af11e64e67
ms.openlocfilehash: 0f04ba837f9c03107acd0b2174cbd07c14a8c213
ms.sourcegitcommit: 8258515adc6c37ab6278e5a3d102d593246f8672
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/27/2019
ms.locfileid: "58504468"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="0b7fe-102">+, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="0b7fe-102">+ Operator (C# Reference)</span></span>

<span data-ttu-id="0b7fe-103">L’opérateur `+` est pris en charge sous deux formes : un opérateur plus unaire plus ou un opérateur d’addition binaire.</span><span class="sxs-lookup"><span data-stu-id="0b7fe-103">The `+` operator is supported in two forms: a unary plus operator or a binary addition operator.</span></span>

## <a name="unary-plus-operator"></a><span data-ttu-id="0b7fe-104">Opérateur plus unaire</span><span class="sxs-lookup"><span data-stu-id="0b7fe-104">Unary plus operator</span></span>

<span data-ttu-id="0b7fe-105">L’opérateur unaire `+` retourne la valeur de son opérande.</span><span class="sxs-lookup"><span data-stu-id="0b7fe-105">The unary `+` operator returns the value of its operand.</span></span> <span data-ttu-id="0b7fe-106">Il est pris en charge par tous les types numériques.</span><span class="sxs-lookup"><span data-stu-id="0b7fe-106">It's supported by all numeric types.</span></span>

## <a name="numeric-addition"></a><span data-ttu-id="0b7fe-107">Addition numérique</span><span class="sxs-lookup"><span data-stu-id="0b7fe-107">Numeric addition</span></span>

<span data-ttu-id="0b7fe-108">Pour les types numériques, l’opérateur `+` calcule la somme de ses opérandes :</span><span class="sxs-lookup"><span data-stu-id="0b7fe-108">For numeric types, the `+` operator computes the sum of its operands:</span></span>

[!code-csharp-interactive[numeric addition](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#AddNumerics)]

<span data-ttu-id="0b7fe-109">Pour plus d’informations sur les opérateurs arithmétiques, consultez [Opérateurs arithmétiques](arithmetic-operators.md).</span><span class="sxs-lookup"><span data-stu-id="0b7fe-109">For more information about arithmetic operators, see [Arithmetic operators](arithmetic-operators.md).</span></span>

## <a name="string-concatenation"></a><span data-ttu-id="0b7fe-110">Concaténation de chaînes</span><span class="sxs-lookup"><span data-stu-id="0b7fe-110">String concatenation</span></span>

<span data-ttu-id="0b7fe-111">Quand les deux opérandes ou l’un d’entre eux sont de [type chaîne](../keywords/string.md), l’opérateur `+` concatène les représentations sous forme de chaîne de ses opérandes :</span><span class="sxs-lookup"><span data-stu-id="0b7fe-111">When one or both operands are of type [string](../keywords/string.md), the `+` operator concatenates the string representations of its operands:</span></span>

[!code-csharp-interactive[string concatenation](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#AddStrings)]

<span data-ttu-id="0b7fe-112">À partir de C# 6, l’[interpolation de chaîne](../tokens/interpolated.md) fournit un moyen plus pratique de mettre en format les chaînes :</span><span class="sxs-lookup"><span data-stu-id="0b7fe-112">Starting with C# 6, [string interpolation](../tokens/interpolated.md) provides a more convenient way to format strings:</span></span>

[!code-csharp-interactive[string interpolation](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#UseStringInterpolation)]

## <a name="delegate-combination"></a><span data-ttu-id="0b7fe-113">Combinaison de délégués</span><span class="sxs-lookup"><span data-stu-id="0b7fe-113">Delegate combination</span></span>

<span data-ttu-id="0b7fe-114">Pour les types [délégué](../keywords/delegate.md), l’opérateur `+` retourne une nouvelle instance de délégué qui, lorsqu’elle est appelée, appelle le premier opérande puis appelle le second opérande.</span><span class="sxs-lookup"><span data-stu-id="0b7fe-114">For [delegate](../keywords/delegate.md) types, the `+` operator returns a new delegate instance that, when invoked, invokes the first operand and then invokes the second operand.</span></span> <span data-ttu-id="0b7fe-115">Si un des opérandes est `null`, l’opérateur `+` retourne la valeur de l’autre opérande (qui peut également être `null`).</span><span class="sxs-lookup"><span data-stu-id="0b7fe-115">If any of the operands is `null`, the `+` operator returns the value of another operand (which also might be `null`).</span></span> <span data-ttu-id="0b7fe-116">L’exemple suivant montre comment les délégués peuvent être combinés avec l’opérateur `+` :</span><span class="sxs-lookup"><span data-stu-id="0b7fe-116">The following example shows how delegates can be combined with the `+` operator:</span></span>

[!code-csharp-interactive[delegate combination](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#AddDelegates)]

<span data-ttu-id="0b7fe-117">Pour plus d'informations sur les types de délégués, consultez [Délégués](../../programming-guide/delegates/index.md).</span><span class="sxs-lookup"><span data-stu-id="0b7fe-117">For more information about delegate types, see [Delegates](../../programming-guide/delegates/index.md).</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="0b7fe-118">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="0b7fe-118">Operator overloadability</span></span>

<span data-ttu-id="0b7fe-119">Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) les opérateurs unaires et binaires `+`.</span><span class="sxs-lookup"><span data-stu-id="0b7fe-119">User-defined types can [overload](../keywords/operator.md) the unary and binary `+` operators.</span></span> <span data-ttu-id="0b7fe-120">Quand un opérateur binaire `+` est surchargé, l’[opérateur d’assignation d’addition](addition-assignment-operator.md) `+=` est aussi implicitement surchargé.</span><span class="sxs-lookup"><span data-stu-id="0b7fe-120">When a binary `+` operator is overloaded, the [addition assignment operator](addition-assignment-operator.md) `+=` is also implicitly overloaded.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="0b7fe-121">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="0b7fe-121">C# language specification</span></span>

<span data-ttu-id="0b7fe-122">Pour plus d’informations, consultez les sections [Opérateur unaire plus](~/_csharplang/spec/expressions.md#unary-plus-operator) et [Opérateur d’addition](~/_csharplang/spec/expressions.md#addition-operator) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="0b7fe-122">For more information, see the [Unary plus operator](~/_csharplang/spec/expressions.md#unary-plus-operator) and [Addition operator](~/_csharplang/spec/expressions.md#addition-operator) sections of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0b7fe-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b7fe-123">See also</span></span>

- [<span data-ttu-id="0b7fe-124">Référence C#</span><span class="sxs-lookup"><span data-stu-id="0b7fe-124">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="0b7fe-125">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="0b7fe-125">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="0b7fe-126">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="0b7fe-126">C# Operators</span></span>](index.md)
- [<span data-ttu-id="0b7fe-127">Interpolation de chaîne</span><span class="sxs-lookup"><span data-stu-id="0b7fe-127">String interpolation</span></span>](../tokens/interpolated.md)
- [<span data-ttu-id="0b7fe-128">Guide pratique pour concaténer plusieurs chaînes</span><span class="sxs-lookup"><span data-stu-id="0b7fe-128">How to: Concatenate Multiple Strings</span></span>](../../how-to/concatenate-multiple-strings.md)
- [<span data-ttu-id="0b7fe-129">Délégués</span><span class="sxs-lookup"><span data-stu-id="0b7fe-129">Delegates</span></span>](../../programming-guide/delegates/index.md)
- [<span data-ttu-id="0b7fe-130">Checked et unchecked</span><span class="sxs-lookup"><span data-stu-id="0b7fe-130">Checked and unchecked</span></span>](../keywords/checked-and-unchecked.md)
