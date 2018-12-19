---
title: '%=, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 09/04/2018
f1_keywords:
- '%=_CSharpKeyword'
helpviewer_keywords:
- remainder assignment operator (%=) [C#]
- '%= assignment operator (remainder assignment) [C#]'
ms.assetid: 47e5f068-1d97-4010-bd3b-e21b5d3a77f5
ms.openlocfilehash: d0732f9578b64c894ecc1d3bb15cee11a8d5b6a3
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53245559"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="bbaa9-102">%=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="bbaa9-102">%= Operator (C# Reference)</span></span>

<span data-ttu-id="bbaa9-103">Opérateur d’assignation de reste.</span><span class="sxs-lookup"><span data-stu-id="bbaa9-103">The remainder assignment operator.</span></span>

<span data-ttu-id="bbaa9-104">Expression utilisant l’opérateur `%=`, par exemple</span><span class="sxs-lookup"><span data-stu-id="bbaa9-104">An expression using the `%=` operator, such as</span></span>  

```csharp
x %= y
```  

<span data-ttu-id="bbaa9-105">est équivalent à</span><span class="sxs-lookup"><span data-stu-id="bbaa9-105">is equivalent to</span></span>  

```csharp
x = x % y
```  

<span data-ttu-id="bbaa9-106">sauf que `x` n’est évalué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="bbaa9-106">except that `x` is only evaluated once.</span></span>
  
<span data-ttu-id="bbaa9-107">[L’opérateur de reste](remainder-operator.md) `%` calcule le reste après division de ses opérandes.</span><span class="sxs-lookup"><span data-stu-id="bbaa9-107">The [remainder operator](remainder-operator.md) `%` computes the remainder after division of its operands.</span></span> <span data-ttu-id="bbaa9-108">Il est pris en charge par tous les types numériques.</span><span class="sxs-lookup"><span data-stu-id="bbaa9-108">It's supported by all numeric types.</span></span>

<span data-ttu-id="bbaa9-109">Si un type défini par l’utilisateur [surcharge](../keywords/operator.md) l’[opérateur de reste](remainder-operator.md) `%`, l’opérateur d’assignation de reste `%=` est implicitement surchargé.</span><span class="sxs-lookup"><span data-stu-id="bbaa9-109">If a user-defined type [overloads](../keywords/operator.md) the [remainder operator](remainder-operator.md) `%`, the remainder assignment operator `%=` is implicitly overloaded.</span></span>
  
<span data-ttu-id="bbaa9-110">L’exemple suivant illustre l’utilisation de l’opérateur `%=` :</span><span class="sxs-lookup"><span data-stu-id="bbaa9-110">The following example demonstrates the usage of the `%=` operator:</span></span>

[!code-csharp-interactive[%= example](~/samples/snippets/csharp/language-reference/operators/RemainderExamples.cs#3)]

## <a name="see-also"></a><span data-ttu-id="bbaa9-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbaa9-111">See also</span></span>

- [<span data-ttu-id="bbaa9-112">Référence C#</span><span class="sxs-lookup"><span data-stu-id="bbaa9-112">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="bbaa9-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="bbaa9-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="bbaa9-114">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="bbaa9-114">C# Operators</span></span>](index.md)
