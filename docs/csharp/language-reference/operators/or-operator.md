---
title: '|, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '|_CSharpKeyword'
helpviewer_keywords:
- bitwise OR operator [C#]
- '| operator [C#]'
- binary operator (|) [C#]
ms.assetid: 82d6bb78-54c8-40bf-b679-531180ddaf70
ms.openlocfilehash: 185ea3aabff4794ec08cca541773dbec3574ab4b
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333510"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="69491-102">|, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="69491-102">| operator (C# Reference)</span></span>

<span data-ttu-id="69491-103">Les opérateurs `|` binaires sont prédéfinis pour les types intégraux et `bool`.</span><span class="sxs-lookup"><span data-stu-id="69491-103">Binary `|` operators are predefined for the integral types and `bool`.</span></span> <span data-ttu-id="69491-104">Pour les types intégraux, `|` calcule l’opération OR au niveau du bit de ses opérandes.</span><span class="sxs-lookup"><span data-stu-id="69491-104">For integral types, `|` computes the bitwise OR of its operands.</span></span> <span data-ttu-id="69491-105">Pour les opérandes `bool`, `|` calcule l’opération OR logique de ses opérandes ; autrement dit, le résultat est `false` si et seulement si ses deux opérandes ont la valeur `false`.</span><span class="sxs-lookup"><span data-stu-id="69491-105">For `bool` operands, `|` computes the logical OR of its operands; that is, the result is `false` if and only if both its operands are `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="69491-106">Notes</span><span class="sxs-lookup"><span data-stu-id="69491-106">Remarks</span></span>

<span data-ttu-id="69491-107">L’opérateur `|` binaire évalue les deux opérandes, quelle que soit la valeur du premier, à la différence de [l’opérateur OR conditionnel](conditional-or-operator.md) `||`.</span><span class="sxs-lookup"><span data-stu-id="69491-107">The binary `|` operator evaluates both operands regardless of the first one's value, in contrast to the [conditional-OR operator](conditional-or-operator.md) `||`.</span></span>

<span data-ttu-id="69491-108">Les types définis par l’utilisateur peuvent surcharger l’opérateur `|` (voir [operator](../keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="69491-108">User-defined types can overload the `|` operator (see [operator](../keywords/operator.md)).</span></span>

## <a name="example"></a><span data-ttu-id="69491-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="69491-109">Example</span></span>

 [!code-csharp[csRefOperators#31](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#31)]

## <a name="see-also"></a><span data-ttu-id="69491-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69491-110">See also</span></span>

- [<span data-ttu-id="69491-111">Référence C#</span><span class="sxs-lookup"><span data-stu-id="69491-111">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="69491-112">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="69491-112">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="69491-113">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="69491-113">C# operators</span></span>](index.md)