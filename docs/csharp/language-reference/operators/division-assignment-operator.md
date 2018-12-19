---
title: /=, opérateur - Référence C#
ms.custom: seodec18
ms.date: 12/13/2018
f1_keywords:
- /=_CSharpKeyword
helpviewer_keywords:
- division assignment operator (/=) [C#]
- /= (division assignment operator) [C#]
ms.assetid: 50fc02b0-ee9c-4c3e-b58d-d591282caf1c
ms.openlocfilehash: ed4dd6c0c944b77543aae4de8d51534b4df4f4ef
ms.sourcegitcommit: d6e419f9d9cd7e8f21ebf5acde6d016c16332579
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2018
ms.locfileid: "53286518"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="055f1-102">/=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="055f1-102">/= Operator (C# Reference)</span></span>

<span data-ttu-id="055f1-103">Opérateur d’assignation de division.</span><span class="sxs-lookup"><span data-stu-id="055f1-103">The division assignment operator.</span></span>

<span data-ttu-id="055f1-104">Expression utilisant l’opérateur `/=`, par exemple</span><span class="sxs-lookup"><span data-stu-id="055f1-104">An expression using the `/=` operator, such as</span></span>

```csharp
x /= y
```

<span data-ttu-id="055f1-105">est équivalent à</span><span class="sxs-lookup"><span data-stu-id="055f1-105">is equivalent to</span></span>

```csharp
x = x / y
```

<span data-ttu-id="055f1-106">sauf que `x` n’est évalué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="055f1-106">except that `x` is only evaluated once.</span></span>

<span data-ttu-id="055f1-107">[L’opérateur de division](division-operator.md) `/` divise son premier opérande par son deuxième opérande.</span><span class="sxs-lookup"><span data-stu-id="055f1-107">The [division operator](division-operator.md) `/` divides its first operand by its second operand.</span></span> <span data-ttu-id="055f1-108">Il est pris en charge par tous les types numériques.</span><span class="sxs-lookup"><span data-stu-id="055f1-108">It's supported by all numeric types.</span></span>

<span data-ttu-id="055f1-109">L’exemple suivant illustre l’utilisation de l’opérateur `/=` :</span><span class="sxs-lookup"><span data-stu-id="055f1-109">The following example demonstrates the usage of the `/=` operator:</span></span>

[!code-csharp-interactive[divide and assign](~/samples/snippets/csharp/language-reference/operators/DivisionExamples.cs#DivisionAssignment)]

## <a name="operator-overloadability"></a><span data-ttu-id="055f1-110">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="055f1-110">Operator overloadability</span></span>

<span data-ttu-id="055f1-111">Si un type défini par l’utilisateur [surcharge](../keywords/operator.md) [l’opérateur de division](division-operator.md) `/`, l’opérateur d’assignation de division `/=` est implicitement surchargé.</span><span class="sxs-lookup"><span data-stu-id="055f1-111">If a user-defined type [overloads](../keywords/operator.md) the [division operator](division-operator.md) `/`, the division assignment operator `/=` is implicitly overloaded.</span></span> <span data-ttu-id="055f1-112">Un type défini par l’utilisateur ne peut pas surcharger explicitement l’opérateur d’assignation de division.</span><span class="sxs-lookup"><span data-stu-id="055f1-112">A user-defined type cannot explicitly overload the division assignment operator.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="055f1-113">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="055f1-113">C# language specification</span></span>

<span data-ttu-id="055f1-114">Pour plus d’informations, consultez la section [Assignation composée](~/_csharplang/spec/expressions.md#compound-assignment) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="055f1-114">For more information, see the [Compound assignment](~/_csharplang/spec/expressions.md#compound-assignment) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="055f1-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="055f1-115">See also</span></span>

- [<span data-ttu-id="055f1-116">Référence C#</span><span class="sxs-lookup"><span data-stu-id="055f1-116">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="055f1-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="055f1-117">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="055f1-118">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="055f1-118">C# Operators</span></span>](index.md)
