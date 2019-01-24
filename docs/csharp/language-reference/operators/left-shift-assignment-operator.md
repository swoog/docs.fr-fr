---
title: '&lt;&lt;=, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- <<=_CSharpKeyword
helpviewer_keywords:
- <<= operator (left-shift assignment) [C#]
- left shift assignment operator (<<=) [C#]
ms.assetid: 3bc99c78-1edb-4827-86fc-bce6c3048871
ms.openlocfilehash: 4513c4b78dea3e8102c72a43249b4a44ffa2421d
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333250"
---
# <a name="ltlt-operator-c-reference"></a><span data-ttu-id="a8ced-102">&lt;&lt;=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="a8ced-102">&lt;&lt;= operator (C# Reference)</span></span>

<span data-ttu-id="a8ced-103">Opérateur d’assignation de décalage vers la gauche.</span><span class="sxs-lookup"><span data-stu-id="a8ced-103">The left-shift assignment operator.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8ced-104">Notes</span><span class="sxs-lookup"><span data-stu-id="a8ced-104">Remarks</span></span>

<span data-ttu-id="a8ced-105">Une expression sous la forme</span><span class="sxs-lookup"><span data-stu-id="a8ced-105">An expression of the form</span></span>

```csharp
x <<= y
```

<span data-ttu-id="a8ced-106">est évaluée comme étant</span><span class="sxs-lookup"><span data-stu-id="a8ced-106">is evaluated as</span></span>

```csharp
x = x << y
```

<span data-ttu-id="a8ced-107">sauf que `x` n’est évalué qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="a8ced-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="a8ced-108">L’[opérateur << ](left-shift-operator.md) déplace `x` vers la gauche du nombre de bits spécifié par `y`.</span><span class="sxs-lookup"><span data-stu-id="a8ced-108">The [<< operator](left-shift-operator.md) shifts `x` left by the number of bits specified by `y`.</span></span>

<span data-ttu-id="a8ced-109">L’opérateur `<<=` ne peut pas être surchargé directement, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur <<](left-shift-operator.md) (consultez [operator](../keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="a8ced-109">The `<<=` operator cannot be overloaded directly, but user-defined types can overload the [<< operator](left-shift-operator.md) (see [operator](../keywords/operator.md)).</span></span>

## <a name="example"></a><span data-ttu-id="a8ced-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="a8ced-110">Example</span></span>

[!code-csharp[csRefOperators#12](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#12)]

## <a name="see-also"></a><span data-ttu-id="a8ced-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8ced-111">See also</span></span>

- [<span data-ttu-id="a8ced-112">Référence C#</span><span class="sxs-lookup"><span data-stu-id="a8ced-112">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="a8ced-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="a8ced-113">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="a8ced-114">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="a8ced-114">C# Operators</span></span>](index.md)
