---
title: '>>=, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '>>=_CSharpKeyword'
helpviewer_keywords:
- right shift assignment operator (>>=) [C#]
- '>>= operator (right-shift assignment) [C#]'
ms.assetid: b593778c-b9b4-440d-8b29-c1ac22cb81c0
ms.openlocfilehash: 8cc341c14ee1b90fde2abb369c187e57b4ce5c00
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55278978"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="aba7e-102">>>=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="aba7e-102">>>= operator (C# Reference)</span></span>

<span data-ttu-id="aba7e-103">Opérateur d’assignation de décalage vers la droite.</span><span class="sxs-lookup"><span data-stu-id="aba7e-103">The right-shift assignment operator.</span></span>

## <a name="remarks"></a><span data-ttu-id="aba7e-104">Notes</span><span class="sxs-lookup"><span data-stu-id="aba7e-104">Remarks</span></span>

<span data-ttu-id="aba7e-105">Une expression sous la forme</span><span class="sxs-lookup"><span data-stu-id="aba7e-105">An expression of the form</span></span>

```csharp
x >>= y
```

<span data-ttu-id="aba7e-106">est évaluée comme étant</span><span class="sxs-lookup"><span data-stu-id="aba7e-106">is evaluated as</span></span>

```csharp
x = x >> y
```

<span data-ttu-id="aba7e-107">sauf que `x` n’est évalué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="aba7e-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="aba7e-108">L’[opérateur >>](right-shift-operator.md) décale `x` vers la droite de la valeur spécifiée par `y`.</span><span class="sxs-lookup"><span data-stu-id="aba7e-108">The [>> operator](right-shift-operator.md) shifts `x` right by an amount specified by `y`.</span></span>

<span data-ttu-id="aba7e-109">L’opérateur >>= ne peut pas être surchargé directement, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur >>](right-shift-operator.md) (voir [operator](../keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="aba7e-109">The >>= operator cannot be overloaded directly, but user-defined types can overload the [>> operator](right-shift-operator.md) (see [operator](../keywords/operator.md)).</span></span>

## <a name="example"></a><span data-ttu-id="aba7e-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="aba7e-110">Example</span></span>

[!code-csharp[csRefOperators#11](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#11)]

## <a name="see-also"></a><span data-ttu-id="aba7e-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aba7e-111">See also</span></span>

- [<span data-ttu-id="aba7e-112">Référence C#</span><span class="sxs-lookup"><span data-stu-id="aba7e-112">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="aba7e-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="aba7e-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="aba7e-114">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="aba7e-114">C# operators</span></span>](index.md)