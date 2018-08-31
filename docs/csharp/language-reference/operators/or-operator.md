---
title: '|, opérateur (référence C#)'
ms.date: 07/20/2015
f1_keywords:
- '|_CSharpKeyword'
helpviewer_keywords:
- bitwise OR operator [C#]
- '| operator [C#]'
- binary operator (|) [C#]
ms.assetid: 82d6bb78-54c8-40bf-b679-531180ddaf70
ms.openlocfilehash: d95fe29aa7ffab9938e8edc57999445268fe41a8
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "43001228"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="366b0-102">|, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="366b0-102">| Operator (C# Reference)</span></span>
<span data-ttu-id="366b0-103">Les opérateurs `|` binaires sont prédéfinis pour les types intégraux et `bool`.</span><span class="sxs-lookup"><span data-stu-id="366b0-103">Binary `|` operators are predefined for the integral types and `bool`.</span></span> <span data-ttu-id="366b0-104">Pour les types intégraux, `|` calcule l’opération OR au niveau du bit de ses opérandes.</span><span class="sxs-lookup"><span data-stu-id="366b0-104">For integral types, `|` computes the bitwise OR of its operands.</span></span> <span data-ttu-id="366b0-105">Pour les opérandes `bool`, `|` calcule l’opération OR logique de ses opérandes ; autrement dit, le résultat est `false` si et seulement si ses deux opérandes ont la valeur `false`.</span><span class="sxs-lookup"><span data-stu-id="366b0-105">For `bool` operands, `|` computes the logical OR of its operands; that is, the result is `false` if and only if both its operands are `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="366b0-106">Notes</span><span class="sxs-lookup"><span data-stu-id="366b0-106">Remarks</span></span>  
 <span data-ttu-id="366b0-107">L’opérateur `|` binaire évalue les deux operandes, quelle que soit la valeur du premier, à la différence de l’[opérateur OR conditionnel]     (conditional-or-operator.md) `||`.</span><span class="sxs-lookup"><span data-stu-id="366b0-107">The binary `|` operator evaluates both operands regardless of the first one's value, in contrast to the [conditional-OR operator]     (conditional-or-operator.md) `||`.</span></span>
 
 <span data-ttu-id="366b0-108">Les types définis par l’utilisateur peuvent surcharger l’opérateur `|` (voir [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="366b0-108">User-defined types can overload the `|` operator (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="366b0-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="366b0-109">Example</span></span>  
 [!code-csharp[csRefOperators#31](../../../csharp/language-reference/operators/codesnippet/CSharp/or-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="366b0-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="366b0-110">See Also</span></span>

- [<span data-ttu-id="366b0-111">Référence C#</span><span class="sxs-lookup"><span data-stu-id="366b0-111">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="366b0-112">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="366b0-112">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="366b0-113">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="366b0-113">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
