---
title: '*=, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 02/26/2019
f1_keywords:
- '*=_CSharpKeyword'
helpviewer_keywords:
- '*= operator [C#]'
- binary multiplication assignment operator (*=) [C#]
ms.assetid: 2e472155-59db-4dbf-bb94-bcccfa1a794d
ms.openlocfilehash: 70461f79e714e44354fe4137e5360769fa048d3e
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56967384"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="47320-102">\*=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="47320-102">\*= Operator (C# Reference)</span></span>

<span data-ttu-id="47320-103">Opérateur d’assignation de multiplication.</span><span class="sxs-lookup"><span data-stu-id="47320-103">The multiplication assignment operator.</span></span>

<span data-ttu-id="47320-104">Expression utilisant l’opérateur `*=`, par exemple</span><span class="sxs-lookup"><span data-stu-id="47320-104">An expression using the `*=` operator, such as</span></span>

```csharp
x *= y
```

<span data-ttu-id="47320-105">est équivalent à</span><span class="sxs-lookup"><span data-stu-id="47320-105">is equivalent to</span></span>

```csharp
x = x * y
```

<span data-ttu-id="47320-106">sauf que `x` n’est évalué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="47320-106">except that `x` is only evaluated once.</span></span>

<span data-ttu-id="47320-107">Pour les types numériques, [l’opérateur \*](multiplication-operator.md) calcule le produit de ses opérandes.</span><span class="sxs-lookup"><span data-stu-id="47320-107">For numeric types, the [\* operator](multiplication-operator.md) computes the product of its operands.</span></span>

<span data-ttu-id="47320-108">L’exemple suivant illustre l’utilisation de l’opérateur `*=` :</span><span class="sxs-lookup"><span data-stu-id="47320-108">The following example demonstrates the usage of the `*=` operator:</span></span>

[!code-csharp-interactive[multiply and assign](~/samples/snippets/csharp/language-reference/operators/MultiplicationExamples.cs#MultiplyAndAssign)]

## <a name="operator-overloadability"></a><span data-ttu-id="47320-109">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="47320-109">Operator overloadability</span></span>

<span data-ttu-id="47320-110">Si un type défini par l’utilisateur [surcharge](../keywords/operator.md) [l’opérateur de multiplication](multiplication-operator.md) `*`, l’opérateur d’assignation de multiplication `*=` est implicitement surchargé.</span><span class="sxs-lookup"><span data-stu-id="47320-110">If a user-defined type [overloads](../keywords/operator.md) the [multiplication operator](multiplication-operator.md) `*`, the multiplication assignment operator `*=` is implicitly overloaded.</span></span> <span data-ttu-id="47320-111">Un type défini par l’utilisateur ne peut pas surcharger explicitement l’opérateur d’assignation de multiplication.</span><span class="sxs-lookup"><span data-stu-id="47320-111">A user-defined type cannot explicitly overload the multiplication assignment operator.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="47320-112">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="47320-112">C# language specification</span></span>

<span data-ttu-id="47320-113">Pour plus d’informations, consultez la section [Assignation composée](~/_csharplang/spec/expressions.md#compound-assignment) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="47320-113">For more information, see the [Compound assignment](~/_csharplang/spec/expressions.md#compound-assignment) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="47320-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47320-114">See also</span></span>

- [<span data-ttu-id="47320-115">Référence C#</span><span class="sxs-lookup"><span data-stu-id="47320-115">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="47320-116">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="47320-116">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="47320-117">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="47320-117">C# Operators</span></span>](index.md)
