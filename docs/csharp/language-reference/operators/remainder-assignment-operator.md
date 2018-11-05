---
title: '%=, opérateur (référence C#)'
ms.date: 09/04/2018
f1_keywords:
- '%=_CSharpKeyword'
helpviewer_keywords:
- remainder assignment operator (%=) [C#]
- '%= assignment operator (remainder assignment) [C#]'
ms.assetid: 47e5f068-1d97-4010-bd3b-e21b5d3a77f5
ms.openlocfilehash: ab3a6a8d5cbfeb4d527ca1f9c233ddfaba3d35ff
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188714"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="b6101-102">%=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="b6101-102">%= Operator (C# Reference)</span></span>

<span data-ttu-id="b6101-103">Opérateur d’assignation de reste.</span><span class="sxs-lookup"><span data-stu-id="b6101-103">The remainder assignment operator.</span></span>

<span data-ttu-id="b6101-104">Expression utilisant l’opérateur `%=`, par exemple</span><span class="sxs-lookup"><span data-stu-id="b6101-104">An expression using the `%=` operator, such as</span></span>  

```csharp
x %= y
```  

<span data-ttu-id="b6101-105">est équivalent à</span><span class="sxs-lookup"><span data-stu-id="b6101-105">is equivalent to</span></span>  

```csharp
x = x % y
```  

<span data-ttu-id="b6101-106">sauf que `x` n’est évalué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="b6101-106">except that `x` is only evaluated once.</span></span>
  
<span data-ttu-id="b6101-107">[L’opérateur de reste](remainder-operator.md) `%` calcule le reste après division de ses opérandes.</span><span class="sxs-lookup"><span data-stu-id="b6101-107">The [remainder operator](remainder-operator.md) `%` computes the remainder after division of its operands.</span></span> <span data-ttu-id="b6101-108">Il est pris en charge par tous les types numériques.</span><span class="sxs-lookup"><span data-stu-id="b6101-108">It's supported by all numeric types.</span></span>

<span data-ttu-id="b6101-109">Si un type défini par l’utilisateur [surcharge](../keywords/operator.md) l’[opérateur de reste](remainder-operator.md) `%`, l’opérateur d’assignation de reste `%=` est implicitement surchargé.</span><span class="sxs-lookup"><span data-stu-id="b6101-109">If a user-defined type [overloads](../keywords/operator.md) the [remainder operator](remainder-operator.md) `%`, the remainder assignment operator `%=` is implicitly overloaded.</span></span>
  
<span data-ttu-id="b6101-110">L’exemple suivant illustre l’utilisation de l’opérateur `%=` :</span><span class="sxs-lookup"><span data-stu-id="b6101-110">The following example demonstrates the usage of the `%=` operator:</span></span>

[!code-csharp-interactive[%= example](~/samples/snippets/csharp/language-reference/operators/RemainderExamples.cs#3)]

## <a name="see-also"></a><span data-ttu-id="b6101-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6101-111">See also</span></span>

- [<span data-ttu-id="b6101-112">Référence C#</span><span class="sxs-lookup"><span data-stu-id="b6101-112">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="b6101-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="b6101-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="b6101-114">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="b6101-114">C# Operators</span></span>](index.md)
