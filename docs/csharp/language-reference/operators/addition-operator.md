---
title: + , opérateur (Informations de référence sur C#)
ms.date: 10/22/2018
f1_keywords:
- +_CSharpKeyword
helpviewer_keywords:
- + operator [C#]
- concatenation operator [C#]
- addition operator [C#]
ms.assetid: 93e56486-bb42-43c1-bd43-60af11e64e67
ms.openlocfilehash: ae2774d96bc50afa271fffdea445e640e68c3647
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50192295"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="3ebab-102">+, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="3ebab-102">+ Operator (C# Reference)</span></span>

<span data-ttu-id="3ebab-103">L’opérateur `+` est pris en charge sous deux formes : un opérateur plus unaire plus ou un opérateur d’addition binaire.</span><span class="sxs-lookup"><span data-stu-id="3ebab-103">The `+` operator is supported in two forms: a unary plus operator or a binary addition operator.</span></span>

<span data-ttu-id="3ebab-104">Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) les opérateurs unaires et binaires `+`.</span><span class="sxs-lookup"><span data-stu-id="3ebab-104">User-defined types can [overload](../keywords/operator.md) the unary and binary `+` operators.</span></span> <span data-ttu-id="3ebab-105">Quand un opérateur binaire `+` est surchargé, l’[opérateur d’assignation d’addition](addition-assignment-operator.md) `+=` est aussi implicitement surchargé.</span><span class="sxs-lookup"><span data-stu-id="3ebab-105">When a binary `+` operator is overloaded, the [addition assignment operator](addition-assignment-operator.md) `+=` is also implicitly overloaded.</span></span>

## <a name="unary-plus-operator"></a><span data-ttu-id="3ebab-106">Opérateur plus unaire</span><span class="sxs-lookup"><span data-stu-id="3ebab-106">Unary plus operator</span></span>

<span data-ttu-id="3ebab-107">L’opérateur unaire `+` retourne la valeur de son opérande.</span><span class="sxs-lookup"><span data-stu-id="3ebab-107">The unary `+` operator returns the value of its operand.</span></span> <span data-ttu-id="3ebab-108">Il est pris en charge par tous les types numériques.</span><span class="sxs-lookup"><span data-stu-id="3ebab-108">It's supported by all numeric types.</span></span>

## <a name="numeric-addition"></a><span data-ttu-id="3ebab-109">Addition numérique</span><span class="sxs-lookup"><span data-stu-id="3ebab-109">Numeric addition</span></span>

<span data-ttu-id="3ebab-110">Pour les types numériques, l’opérateur `+` calcule la somme de ses opérandes :</span><span class="sxs-lookup"><span data-stu-id="3ebab-110">For numeric types, the `+` operator computes the sum of its operands:</span></span>

[!code-csharp-interactive[numeric addition](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#AddNumerics)]

## <a name="string-concatenation"></a><span data-ttu-id="3ebab-111">Concaténation de chaînes</span><span class="sxs-lookup"><span data-stu-id="3ebab-111">String concatenation</span></span>

<span data-ttu-id="3ebab-112">Quand les deux opérandes ou l’un d’entre eux sont de [type chaîne](../keywords/string.md), l’opérateur `+` concatène les représentations sous forme de chaîne de ses opérandes :</span><span class="sxs-lookup"><span data-stu-id="3ebab-112">When one or both operands are of type [string](../keywords/string.md), the `+` operator concatenates the string representations of its operands:</span></span>

[!code-csharp-interactive[string concatenation](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#AddStrings)]

<span data-ttu-id="3ebab-113">À partir de C# 6, l’[interpolation de chaîne](../tokens/interpolated.md) fournit un moyen plus pratique de mettre en format les chaînes :</span><span class="sxs-lookup"><span data-stu-id="3ebab-113">Starting with C# 6, [string interpolation](../tokens/interpolated.md) provides a more convenient way to format strings:</span></span>

[!code-csharp-interactive[string interpolation](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#UseStringInterpolation)]

## <a name="delegate-combination"></a><span data-ttu-id="3ebab-114">Combinaison de délégués</span><span class="sxs-lookup"><span data-stu-id="3ebab-114">Delegate combination</span></span>

<span data-ttu-id="3ebab-115">Pour les types [délégué](../keywords/delegate.md), l’opérateur `+` retourne une nouvelle instance de délégué qui, lorsqu’elle est appelée, appelle le premier opérande puis appelle le second opérande.</span><span class="sxs-lookup"><span data-stu-id="3ebab-115">For [delegate](../keywords/delegate.md) types, the `+` operator returns a new delegate instance that, when invoked, invokes the first operand and then invokes the second operand.</span></span> <span data-ttu-id="3ebab-116">Si un des opérandes est `null`, l’opérateur `+` retourne la valeur de l’autre opérande (qui peut également être `null`).</span><span class="sxs-lookup"><span data-stu-id="3ebab-116">If any of the operands is `null`, the `+` operator returns the value of another operand (which also might be `null`).</span></span> <span data-ttu-id="3ebab-117">L’exemple suivant montre comment les délégués peuvent être combinés avec l’opérateur `+` :</span><span class="sxs-lookup"><span data-stu-id="3ebab-117">The following example shows how delegates can be combined with the `+` operator:</span></span>

[!code-csharp-interactive[delegate combination](~/samples/snippets/csharp/language-reference/operators/AdditionExamples.cs#AddDelegates)]

<span data-ttu-id="3ebab-118">Pour plus d'informations sur les types de délégués, consultez [Délégués](../../programming-guide/delegates/index.md).</span><span class="sxs-lookup"><span data-stu-id="3ebab-118">For more information about delegate types, see [Delegates](../../programming-guide/delegates/index.md).</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="3ebab-119">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="3ebab-119">C# language specification</span></span>

<span data-ttu-id="3ebab-120">Pour plus d’informations, consultez les sections [Opérateur unaire plus](~/_csharplang/spec/expressions.md#unary-plus-operator) et [Opérateur d’addition](~/_csharplang/spec/expressions.md#addition-operator) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="3ebab-120">For more information, see the [Unary plus operator](~/_csharplang/spec/expressions.md#unary-plus-operator) and [Addition operator](~/_csharplang/spec/expressions.md#addition-operator) sections of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3ebab-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ebab-121">See also</span></span>

- [<span data-ttu-id="3ebab-122">Référence C#</span><span class="sxs-lookup"><span data-stu-id="3ebab-122">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="3ebab-123">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="3ebab-123">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="3ebab-124">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="3ebab-124">C# Operators</span></span>](index.md)
- [<span data-ttu-id="3ebab-125">Interpolation de chaîne</span><span class="sxs-lookup"><span data-stu-id="3ebab-125">String interpolation</span></span>](../tokens/interpolated.md)
- [<span data-ttu-id="3ebab-126">Comment : concaténer plusieurs chaînes</span><span class="sxs-lookup"><span data-stu-id="3ebab-126">How to: Concatenate Multiple Strings</span></span>](../../how-to/concatenate-multiple-strings.md)
- [<span data-ttu-id="3ebab-127">Délégués</span><span class="sxs-lookup"><span data-stu-id="3ebab-127">Delegates</span></span>](../../programming-guide/delegates/index.md)
- [<span data-ttu-id="3ebab-128">Checked et unchecked</span><span class="sxs-lookup"><span data-stu-id="3ebab-128">Checked and unchecked</span></span>](../keywords/checked-and-unchecked.md)
