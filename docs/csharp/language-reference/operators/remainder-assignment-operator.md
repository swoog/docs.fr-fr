---
title: '%=, opérateur (référence C#)'
ms.date: 09/04/2018
f1_keywords:
- '%=_CSharpKeyword'
helpviewer_keywords:
- remainder assignment operator (%=) [C#]
- '%= assignment operator (remainder assignment) [C#]'
ms.assetid: 47e5f068-1d97-4010-bd3b-e21b5d3a77f5
ms.openlocfilehash: c475517666bdadaa457dbb4188808b3a96fcdf0e
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44085638"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="17340-102">%=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="17340-102">%= Operator (C# Reference)</span></span>

<span data-ttu-id="17340-103">Opérateur d’assignation de reste.</span><span class="sxs-lookup"><span data-stu-id="17340-103">The remainder assignment operator.</span></span>

<span data-ttu-id="17340-104">Expression utilisant l’opérateur `%=`, par exemple</span><span class="sxs-lookup"><span data-stu-id="17340-104">An expression using the `%=` operator, such as</span></span>  

```csharp
x %= y
```  

<span data-ttu-id="17340-105">est équivalent à</span><span class="sxs-lookup"><span data-stu-id="17340-105">is equivalent to</span></span>  

```csharp
x = x % y
```  

<span data-ttu-id="17340-106">sauf que `x` n’est évalué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="17340-106">except that `x` is only evaluated once.</span></span>
  
<span data-ttu-id="17340-107">L’[opérateur de reste](remainder-operator.md)`%` est pris en charge par tous les types numériques. Il calcule le reste après la division de ses opérandes.</span><span class="sxs-lookup"><span data-stu-id="17340-107">The [remainder operator](remainder-operator.md) `%` is supported by all numeric types and computes the remainder after division of its operands.</span></span>

<span data-ttu-id="17340-108">Si un type défini par l’utilisateur [surcharge](../keywords/operator.md) l’[opérateur de reste](remainder-operator.md) `%`, l’opérateur d’assignation de reste `%=` est implicitement surchargé.</span><span class="sxs-lookup"><span data-stu-id="17340-108">If a user-defined type [overloads](../keywords/operator.md) the [remainder operator](remainder-operator.md) `%`, the remainder assignment operator `%=` is implicitly overloaded.</span></span>
  
<span data-ttu-id="17340-109">L’exemple suivant illustre l’utilisation de l’opérateur `%=` :</span><span class="sxs-lookup"><span data-stu-id="17340-109">The following example demonstrates the usage of the `%=` operator:</span></span>

[!code-csharp-interactive[%= example](~/samples/snippets/csharp/language-reference/operators/RemainderExamples.cs#3)]

## <a name="see-also"></a><span data-ttu-id="17340-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17340-110">See also</span></span>

- [<span data-ttu-id="17340-111">Référence C#</span><span class="sxs-lookup"><span data-stu-id="17340-111">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="17340-112">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="17340-112">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="17340-113">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="17340-113">C# Operators</span></span>](index.md)
