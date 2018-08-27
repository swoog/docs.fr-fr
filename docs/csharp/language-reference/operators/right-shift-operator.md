---
title: '&gt;&gt;, opérateur (Informations de référence sur C#)'
ms.date: 07/20/2015
f1_keywords:
- '>>_CSharpKeyword'
helpviewer_keywords:
- '>> operator [C#]'
- right shift operator (>>) [C#]
ms.assetid: a07f8679-d318-4ef8-b38b-65903efb8056
ms.openlocfilehash: 7a2992befcacfdc1d9bb968b611051e15702cca8
ms.sourcegitcommit: 412bbc2e43c3b6ca25b358cdf394be97336f0c24
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/25/2018
ms.locfileid: "42924822"
---
# <a name="gtgt-operator-c-reference"></a><span data-ttu-id="df5ae-102">&gt;&gt;, opérateur (Informations de référence sur C#)</span><span class="sxs-lookup"><span data-stu-id="df5ae-102">&gt;&gt; Operator (C# Reference)</span></span>
<span data-ttu-id="df5ae-103">L’opérateur de décalage vers la droite (`>>`) décale son premier opérande vers la droite du nombre de bits spécifié par son deuxième opérande.</span><span class="sxs-lookup"><span data-stu-id="df5ae-103">The right-shift operator (`>>`) shifts its first operand right by the number of bits specified by its second operand.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="df5ae-104">Notes</span><span class="sxs-lookup"><span data-stu-id="df5ae-104">Remarks</span></span>  
 <span data-ttu-id="df5ae-105">Si le premier opérande est de type [int](../../../csharp/language-reference/keywords/int.md) ou [uint](../../../csharp/language-reference/keywords/uint.md) (quantité 32 bits), la valeur du décalage est donnée par les cinq bits de poids faible du second opérande (second opérande & 0x1f).</span><span class="sxs-lookup"><span data-stu-id="df5ae-105">If the first operand is an [int](../../../csharp/language-reference/keywords/int.md) or [uint](../../../csharp/language-reference/keywords/uint.md) (32-bit quantity), the shift count is given by the low-order five bits of the second operand (second operand & 0x1f).</span></span>  
  
 <span data-ttu-id="df5ae-106">Si le premier opérande est un [long](../../../csharp/language-reference/keywords/long.md) ou un [ulong](../../../csharp/language-reference/keywords/ulong.md) (quantité 64 bits), la valeur du décalage est donnée par les six bits de poids faible du second opérande (second opérande & 0x3f).</span><span class="sxs-lookup"><span data-stu-id="df5ae-106">If the first operand is a [long](../../../csharp/language-reference/keywords/long.md) or [ulong](../../../csharp/language-reference/keywords/ulong.md) (64-bit quantity), the shift count is given by the low-order six bits of the second operand (second operand & 0x3f).</span></span>  
  
 <span data-ttu-id="df5ae-107">Si le premier opérande est un [int](../../../csharp/language-reference/keywords/int.md) ou un [long](../../../csharp/language-reference/keywords/long.md), le décalage vers la droite est un décalage arithmétique (les bits vierges d’ordre haut prennent la valeur du bit de signe).</span><span class="sxs-lookup"><span data-stu-id="df5ae-107">If the first operand is an [int](../../../csharp/language-reference/keywords/int.md) or [long](../../../csharp/language-reference/keywords/long.md), the right-shift is an arithmetic shift (high-order empty bits are set to the sign bit).</span></span> <span data-ttu-id="df5ae-108">Si le premier opérande est de type [uint](../../../csharp/language-reference/keywords/uint.md) ou [ulong](../../../csharp/language-reference/keywords/ulong.md), le décalage vers la droite est un décalage logique (les bits de poids fort prennent la valeur zéro).</span><span class="sxs-lookup"><span data-stu-id="df5ae-108">If the first operand is of type [uint](../../../csharp/language-reference/keywords/uint.md) or [ulong](../../../csharp/language-reference/keywords/ulong.md), the right-shift is a logical shift (high-order bits are zero-filled).</span></span>  
  
 <span data-ttu-id="df5ae-109">Les types définis par l’utilisateur peuvent surcharger l’opérateur `>>` ; le type du premier opérande doit être le type défini par l’utilisateur, et le type du second opérande doit être [int](../../../csharp/language-reference/keywords/int.md). Pour plus d’informations, consultez [operator](../../../csharp/language-reference/keywords/operator.md).</span><span class="sxs-lookup"><span data-stu-id="df5ae-109">User-defined types can overload the `>>` operator; the type of the first operand must be the user-defined type, and the type of the second operand must be [int](../../../csharp/language-reference/keywords/int.md). For more information, see [operator](../../../csharp/language-reference/keywords/operator.md).</span></span> <span data-ttu-id="df5ae-110">Quand un opérateur binaire est surchargé, l’opérateur d’assignation correspondant, le cas échéant, est aussi implicitement surchargé.</span><span class="sxs-lookup"><span data-stu-id="df5ae-110">When a binary operator is overloaded, the corresponding assignment operator, if any, is also implicitly overloaded.</span></span>  
  
## <a name="example"></a><span data-ttu-id="df5ae-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="df5ae-111">Example</span></span>  
 [!code-csharp[csRefOperators#26](../../../csharp/language-reference/operators/codesnippet/CSharp/right-shift-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="df5ae-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df5ae-112">See Also</span></span>

- [<span data-ttu-id="df5ae-113">Référence C#</span><span class="sxs-lookup"><span data-stu-id="df5ae-113">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="df5ae-114">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="df5ae-114">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="df5ae-115">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="df5ae-115">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
