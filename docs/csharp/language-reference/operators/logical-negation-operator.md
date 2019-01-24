---
title: '! opérateur - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '!_CSharpKeyword'
helpviewer_keywords:
- '! operator [C#]'
- logical negation operator (!) [C#]
- NOT operator [C#]
ms.assetid: f5ae133f-8f64-4560-b34f-cd9cd5eed4ad
ms.openlocfilehash: 6b6d1796032f536aac0be49d4f101c1380b4e98f
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333224"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="8f8bf-103">!</span><span class="sxs-lookup"><span data-stu-id="8f8bf-103">!</span></span> <span data-ttu-id="8f8bf-104">operator (référence C#)</span><span class="sxs-lookup"><span data-stu-id="8f8bf-104">operator (C# Reference)</span></span>

<span data-ttu-id="8f8bf-105">L’opérateur de négation logique (`!`) est un opérateur unaire qui nie son opérande.</span><span class="sxs-lookup"><span data-stu-id="8f8bf-105">The logical negation operator (`!`) is a unary operator that negates its operand.</span></span> <span data-ttu-id="8f8bf-106">Il est défini pour `bool` et retourne `true` si et seulement si son opérande a la valeur `false`.</span><span class="sxs-lookup"><span data-stu-id="8f8bf-106">It is defined for `bool` and returns `true` if and only if its operand is `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f8bf-107">Notes</span><span class="sxs-lookup"><span data-stu-id="8f8bf-107">Remarks</span></span>

<span data-ttu-id="8f8bf-108">Les types définis par l’utilisateur peuvent surcharger l’opérateur `!` (voir [operator](../keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="8f8bf-108">User-defined types can overload the `!` operator (see [operator](../keywords/operator.md)).</span></span>

## <a name="example"></a><span data-ttu-id="8f8bf-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="8f8bf-109">Example</span></span>

[!code-csharp[csRefOperators#7](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#7)]

## <a name="see-also"></a><span data-ttu-id="8f8bf-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f8bf-110">See also</span></span>

- [<span data-ttu-id="8f8bf-111">Référence C#</span><span class="sxs-lookup"><span data-stu-id="8f8bf-111">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="8f8bf-112">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="8f8bf-112">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="8f8bf-113">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="8f8bf-113">C# Operators</span></span>](index.md)