---
title: '|=, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '|=_CSharpKeyword'
helpviewer_keywords:
- OR assignment operator (|=) [C#]
- '|= operator (OR assignment) [C#]'
ms.assetid: 8315b8cf-dd15-402f-92f0-c7db931696ca
ms.openlocfilehash: f4f7806c8679af400a371decd0c367929b3fb81d
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333263"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="e8541-102">|=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="e8541-102">|= operator (C# Reference)</span></span>

<span data-ttu-id="e8541-103">Opérateur d’assignation OR.</span><span class="sxs-lookup"><span data-stu-id="e8541-103">The OR assignment operator.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8541-104">Notes</span><span class="sxs-lookup"><span data-stu-id="e8541-104">Remarks</span></span>

<span data-ttu-id="e8541-105">Une expression qui utilise l’opérateur d’assignation `|=`, telle que</span><span class="sxs-lookup"><span data-stu-id="e8541-105">An expression using the `|=` assignment operator, such as</span></span>

```csharp
x |= y
```

<span data-ttu-id="e8541-106">est équivalent à</span><span class="sxs-lookup"><span data-stu-id="e8541-106">is equivalent to</span></span>

```csharp
x = x | y
```

<span data-ttu-id="e8541-107">sauf que `x` n’est évalué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="e8541-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="e8541-108">L’[opérateur &#124](or-operator.md) effectue une opération OR logique au niveau du bit sur les opérandes intégraux et une opération OR logique sur les opérandes de type bool.</span><span class="sxs-lookup"><span data-stu-id="e8541-108">The [&#124; operator](or-operator.md) performs a bitwise logical OR operation on integral operands and logical OR on bool operands.</span></span>

<span data-ttu-id="e8541-109">L’opérateur `|=` ne peut pas être surchargé directement, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur &#124;](or-operator.md) (consultez [operator](../keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="e8541-109">The `|=` operator cannot be overloaded directly, but user-defined types can overload the [&#124; operator](or-operator.md) (see [operator](../keywords/operator.md)).</span></span>

## <a name="example"></a><span data-ttu-id="e8541-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="e8541-110">Example</span></span>

[!code-csharp[csRefOperators#10](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#10)]

## <a name="see-also"></a><span data-ttu-id="e8541-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8541-111">See also</span></span>

- [<span data-ttu-id="e8541-112">Référence C#</span><span class="sxs-lookup"><span data-stu-id="e8541-112">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="e8541-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="e8541-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="e8541-114">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="e8541-114">C# operators</span></span>](index.md)