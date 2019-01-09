---
title: '!=, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 12/14/2018
f1_keywords:
- '!=_CSharpKeyword'
helpviewer_keywords:
- inequality operator (!=) [C#]
- not equals operator (!=) [C#]
- '!= operator [C#]'
ms.assetid: eeff7a4e-ad6f-462d-9f8d-49e9b91c6c97
ms.openlocfilehash: 939b5664dba4345e62a43fb2f8d4d5379659d6aa
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53610175"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="684af-102">!=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="684af-102">!= Operator (C# Reference)</span></span>

<span data-ttu-id="684af-103">L’opérateur d’inégalité `!=` retourne `true` si ses opérandes ne sont pas égaux, `false` dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="684af-103">The inequality operator `!=` returns `true` if its operands are not equal, `false` otherwise.</span></span> <span data-ttu-id="684af-104">Pour les opérandes des [types intégrés](../keywords/built-in-types-table.md), l’expression `x != y` produit le même résultat que l’expression `!(x == y)`.</span><span class="sxs-lookup"><span data-stu-id="684af-104">For the operands of the [built-in types](../keywords/built-in-types-table.md), the expression `x != y` produces the same result as the expression `!(x == y)`.</span></span> <span data-ttu-id="684af-105">Pour plus d’informations, consultez l’article [Opérateur ==](equality-comparison-operator.md).</span><span class="sxs-lookup"><span data-stu-id="684af-105">For more information, see the [== Operator](equality-comparison-operator.md) article.</span></span>

<span data-ttu-id="684af-106">L’exemple suivant illustre l’utilisation de l’opérateur `!=` :</span><span class="sxs-lookup"><span data-stu-id="684af-106">The following example demonstrates the usage of the `!=` operator:</span></span>

[!code-csharp-interactive[non-equality examples](~/samples/snippets/csharp/language-reference/operators/EqualityAndNonEqualityExamples.cs#NonEquality)]

## <a name="operator-overloadability"></a><span data-ttu-id="684af-107">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="684af-107">Operator overloadability</span></span>

<span data-ttu-id="684af-108">Les types définis par l’utilisateur peuvent [surcharger](../keywords/operator.md) l’opérateur `!=`.</span><span class="sxs-lookup"><span data-stu-id="684af-108">User-defined types can [overload](../keywords/operator.md) the `!=` operator.</span></span> <span data-ttu-id="684af-109">Si un type surcharge l’opérateur d’inégalité `!=`, il doit également surcharger l’[opérateur d’égalité](equality-comparison-operator.md) `==`.</span><span class="sxs-lookup"><span data-stu-id="684af-109">If a type overloads the inequality operator `!=`, it must also overload the [equality operator](equality-comparison-operator.md) `==`.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="684af-110">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="684af-110">C# language specification</span></span>

<span data-ttu-id="684af-111">Pour plus d’informations, consultez la section [Opérateurs relationnels et de test de type](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="684af-111">For more information, see the [Relational and type-testing operators](~/_csharplang/spec/expressions.md#relational-and-type-testing-operators) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="684af-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="684af-112">See also</span></span>

- [<span data-ttu-id="684af-113">Référence C#</span><span class="sxs-lookup"><span data-stu-id="684af-113">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="684af-114">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="684af-114">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="684af-115">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="684af-115">C# Operators</span></span>](index.md)
- [<span data-ttu-id="684af-116">Comparaisons d’égalité</span><span class="sxs-lookup"><span data-stu-id="684af-116">Equality comparisons</span></span>](../../programming-guide/statements-expressions-operators/equality-comparisons.md)
