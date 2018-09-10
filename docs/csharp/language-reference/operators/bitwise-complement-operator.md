---
title: ~, opérateur (référence C#)
ms.date: 07/20/2015
f1_keywords:
- ~_CSharpKeyword
helpviewer_keywords:
- tilde (~) one's complement operator [C#]
- ~ operator [C#]
- ~ [C#], bitwise complement operator
- bitwise complement operator [C#]
ms.assetid: 11bc078a-50e2-4d7e-9896-67ef669dc602
ms.openlocfilehash: 8af25217f9e7e66796192783a0b8e3415604dc90
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43510109"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="64259-102">~, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="64259-102">~ Operator (C# Reference)</span></span>
<span data-ttu-id="64259-103">L’opérateur `~` effectue une opération de complément de bits sur son opérande, qui a pour effet d’inverser chaque bit.</span><span class="sxs-lookup"><span data-stu-id="64259-103">The `~` operator performs a bitwise complement operation on its operand, which has the effect of reversing each bit.</span></span> <span data-ttu-id="64259-104">Les opérateurs de complément de bits sont prédéfinis pour [int](../../../csharp/language-reference/keywords/int.md), [uint](../../../csharp/language-reference/keywords/uint.md), [long](../../../csharp/language-reference/keywords/long.md) et [ulong](../../../csharp/language-reference/keywords/ulong.md).</span><span class="sxs-lookup"><span data-stu-id="64259-104">Bitwise complement operators are predefined for [int](../../../csharp/language-reference/keywords/int.md), [uint](../../../csharp/language-reference/keywords/uint.md), [long](../../../csharp/language-reference/keywords/long.md), and [ulong](../../../csharp/language-reference/keywords/ulong.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="64259-105">Le symbole `~` est également utilisé pour déclarer des finaliseurs.</span><span class="sxs-lookup"><span data-stu-id="64259-105">The `~` symbol also is used to declare finalizers.</span></span> <span data-ttu-id="64259-106">Pour plus d’informations, consultez [Finaliseurs](../../../csharp/programming-guide/classes-and-structs/destructors.md).</span><span class="sxs-lookup"><span data-stu-id="64259-106">For more information, see [Finalizers](../../../csharp/programming-guide/classes-and-structs/destructors.md).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="64259-107">Notes</span><span class="sxs-lookup"><span data-stu-id="64259-107">Remarks</span></span>  
 <span data-ttu-id="64259-108">Les types définis par l’utilisateur peuvent surcharger l’opérateur `~`.</span><span class="sxs-lookup"><span data-stu-id="64259-108">User-defined types can overload the `~` operator.</span></span> <span data-ttu-id="64259-109">Pour plus d’informations, consultez [operator](../../../csharp/language-reference/keywords/operator.md).</span><span class="sxs-lookup"><span data-stu-id="64259-109">For more information, see [operator](../../../csharp/language-reference/keywords/operator.md).</span></span> <span data-ttu-id="64259-110">Les opérations sur les types intégraux sont en général autorisées sur l’énumération.</span><span class="sxs-lookup"><span data-stu-id="64259-110">Operations on integral types are generally allowed on enumeration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="64259-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="64259-111">Example</span></span>  
 [!code-csharp[csRefOperators#25](../../../csharp/language-reference/operators/codesnippet/CSharp/bitwise-complement-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="64259-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64259-112">See Also</span></span>

- [<span data-ttu-id="64259-113">Référence C#</span><span class="sxs-lookup"><span data-stu-id="64259-113">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="64259-114">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="64259-114">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="64259-115">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="64259-115">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)  
- [<span data-ttu-id="64259-116">Finaliseurs</span><span class="sxs-lookup"><span data-stu-id="64259-116">Finalizers</span></span>](../../../csharp/programming-guide/classes-and-structs/destructors.md)
