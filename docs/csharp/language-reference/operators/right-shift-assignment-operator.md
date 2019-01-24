---
title: '&gt;&gt;=, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '>>=_CSharpKeyword'
helpviewer_keywords:
- right shift assignment operator (>>=) [C#]
- '>>= operator (right-shift assignment) [C#]'
ms.assetid: b593778c-b9b4-440d-8b29-c1ac22cb81c0
ms.openlocfilehash: 02a9559a5c4086eeed09094c15c3620366ffad8c
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333684"
---
# <a name="gtgt-operator-c-reference"></a><span data-ttu-id="8ed0f-102">&gt;&gt;=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="8ed0f-102">&gt;&gt;= operator (C# Reference)</span></span>

<span data-ttu-id="8ed0f-103">Opérateur d’assignation de décalage vers la droite.</span><span class="sxs-lookup"><span data-stu-id="8ed0f-103">The right-shift assignment operator.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ed0f-104">Notes</span><span class="sxs-lookup"><span data-stu-id="8ed0f-104">Remarks</span></span>

<span data-ttu-id="8ed0f-105">Une expression sous la forme</span><span class="sxs-lookup"><span data-stu-id="8ed0f-105">An expression of the form</span></span>

```csharp
x >>= y
```

<span data-ttu-id="8ed0f-106">est évaluée comme étant</span><span class="sxs-lookup"><span data-stu-id="8ed0f-106">is evaluated as</span></span>

```csharp
x = x >> y
```

<span data-ttu-id="8ed0f-107">sauf que `x` n’est évalué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="8ed0f-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="8ed0f-108">L’[opérateur >>](right-shift-operator.md) décale `x` vers la droite de la valeur spécifiée par `y`.</span><span class="sxs-lookup"><span data-stu-id="8ed0f-108">The [>> operator](right-shift-operator.md) shifts `x` right by an amount specified by `y`.</span></span>

<span data-ttu-id="8ed0f-109">L’opérateur >>= ne peut pas être surchargé directement, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur >>](right-shift-operator.md) (voir [operator](../keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="8ed0f-109">The >>= operator cannot be overloaded directly, but user-defined types can overload the [>> operator](right-shift-operator.md) (see [operator](../keywords/operator.md)).</span></span>

## <a name="example"></a><span data-ttu-id="8ed0f-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="8ed0f-110">Example</span></span>

[!code-csharp[csRefOperators#11](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#11)]

## <a name="see-also"></a><span data-ttu-id="8ed0f-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ed0f-111">See also</span></span>

- [<span data-ttu-id="8ed0f-112">Référence C#</span><span class="sxs-lookup"><span data-stu-id="8ed0f-112">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="8ed0f-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="8ed0f-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="8ed0f-114">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="8ed0f-114">C# operators</span></span>](index.md)