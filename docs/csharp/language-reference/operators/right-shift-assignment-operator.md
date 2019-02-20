---
title: '>>=, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 02/12/2019
f1_keywords:
- '>>=_CSharpKeyword'
helpviewer_keywords:
- right shift assignment operator (>>=) [C#]
- '>>= operator (right-shift assignment) [C#]'
ms.assetid: b593778c-b9b4-440d-8b29-c1ac22cb81c0
ms.openlocfilehash: 51914bb5e9ebffd5d868528b5a8d3072a956cea6
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56220911"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="a6755-102">>>=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="a6755-102">>>= operator (C# Reference)</span></span>

<span data-ttu-id="a6755-103">Opérateur d’assignation de décalage vers la droite.</span><span class="sxs-lookup"><span data-stu-id="a6755-103">The right-shift assignment operator.</span></span>

<span data-ttu-id="a6755-104">Expression utilisant l’opérateur `>>=`, par exemple</span><span class="sxs-lookup"><span data-stu-id="a6755-104">An expression using the `>>=` operator, such as</span></span>

```csharp
x >>= y
```

<span data-ttu-id="a6755-105">est équivalent à</span><span class="sxs-lookup"><span data-stu-id="a6755-105">is equivalent to</span></span>

```csharp
x = x >> y
```

<span data-ttu-id="a6755-106">sauf que `x` n’est évalué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="a6755-106">except that `x` is only evaluated once.</span></span>

<span data-ttu-id="a6755-107">L’opérateur [`>>` ](right-shift-operator.md) décale son premier opérande vers la droite du nombre de bits spécifié par son deuxième opérande.</span><span class="sxs-lookup"><span data-stu-id="a6755-107">The [`>>` operator](right-shift-operator.md) shifts its first operand right by the number of bits defined by its second operand.</span></span>

<span data-ttu-id="a6755-108">L’exemple suivant illustre l’utilisation de l’opérateur `>>=` :</span><span class="sxs-lookup"><span data-stu-id="a6755-108">The following example demonstrates the usage of the `>>=` operator:</span></span>

[!code-csharp-interactive[right shift assignment](~/samples/snippets/csharp/language-reference/operators/ShiftOperatorsExamples.cs#RightShiftAssignment)]

## <a name="operator-overloadability"></a><span data-ttu-id="a6755-109">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="a6755-109">Operator overloadability</span></span>

<span data-ttu-id="a6755-110">Si un type défini par l’utilisateur [surcharge ](../keywords/operator.md) l’[`>>`opérateur](right-shift-operator.md), l’opérateur d’assignation de décalage vers la droite `>>=` est implicitement surchargé.</span><span class="sxs-lookup"><span data-stu-id="a6755-110">If a user-defined type [overloads](../keywords/operator.md) the [`>>` operator](right-shift-operator.md), the right-shift assignment operator `>>=` is implicitly overloaded.</span></span> <span data-ttu-id="a6755-111">Un type défini par l’utilisateur ne peut pas surcharger explicitement l’opérateur d’assignation de décalage vers la droite.</span><span class="sxs-lookup"><span data-stu-id="a6755-111">A user-defined type cannot explicitly overload the right-shift assignment operator.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="a6755-112">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="a6755-112">C# language specification</span></span>

<span data-ttu-id="a6755-113">Pour plus d’informations, consultez la section [Assignation composée](~/_csharplang/spec/expressions.md#compound-assignment) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="a6755-113">For more information, see the [Compound assignment](~/_csharplang/spec/expressions.md#compound-assignment) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a6755-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6755-114">See also</span></span>

- [<span data-ttu-id="a6755-115">Référence C#</span><span class="sxs-lookup"><span data-stu-id="a6755-115">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="a6755-116">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="a6755-116">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="a6755-117">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="a6755-117">C# operators</span></span>](index.md)