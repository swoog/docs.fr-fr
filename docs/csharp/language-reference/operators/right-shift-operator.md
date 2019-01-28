---
title: '&gt;&gt;, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '>>_CSharpKeyword'
helpviewer_keywords:
- '>> operator [C#]'
- right shift operator (>>) [C#]
ms.assetid: a07f8679-d318-4ef8-b38b-65903efb8056
ms.openlocfilehash: f7cacd740966f0716e125887568a39abf0d9e454
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54725426"
---
# <a name="gtgt-operator-c-reference"></a><span data-ttu-id="52c68-102">&gt;&gt;, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="52c68-102">&gt;&gt; operator (C# Reference)</span></span>

<span data-ttu-id="52c68-103">L’opérateur de décalage vers la droite (`>>`) décale son premier opérande vers la droite du nombre de bits spécifié par son deuxième opérande.</span><span class="sxs-lookup"><span data-stu-id="52c68-103">The right-shift operator (`>>`) shifts its first operand right by the number of bits specified by its second operand.</span></span>

## <a name="remarks"></a><span data-ttu-id="52c68-104">Notes</span><span class="sxs-lookup"><span data-stu-id="52c68-104">Remarks</span></span>

<span data-ttu-id="52c68-105">Si le premier opérande est de type [int](../keywords/int.md) ou [uint](../keywords/uint.md) (quantité 32 bits), la valeur du décalage est donnée par les cinq bits de poids faible du second opérande (second opérande & 0x1f).</span><span class="sxs-lookup"><span data-stu-id="52c68-105">If the first operand is an [int](../keywords/int.md) or [uint](../keywords/uint.md) (32-bit quantity), the shift count is given by the low-order five bits of the second operand (second operand & 0x1f).</span></span>

<span data-ttu-id="52c68-106">Si le premier opérande est un [long](../keywords/long.md) ou un [ulong](../keywords/ulong.md) (quantité 64 bits), la valeur du décalage est donnée par les six bits de poids faible du second opérande (second opérande & 0x3f).</span><span class="sxs-lookup"><span data-stu-id="52c68-106">If the first operand is a [long](../keywords/long.md) or [ulong](../keywords/ulong.md) (64-bit quantity), the shift count is given by the low-order six bits of the second operand (second operand & 0x3f).</span></span>

<span data-ttu-id="52c68-107">Si le premier opérande est un [int](../keywords/int.md) ou un [long](../keywords/long.md), le décalage vers la droite est un décalage arithmétique (les bits vierges d’ordre haut prennent la valeur du bit de signe).</span><span class="sxs-lookup"><span data-stu-id="52c68-107">If the first operand is an [int](../keywords/int.md) or [long](../keywords/long.md), the right-shift is an arithmetic shift (high-order empty bits are set to the sign bit).</span></span> <span data-ttu-id="52c68-108">Si le premier opérande est de type [uint](../keywords/uint.md) ou [ulong](../keywords/ulong.md), le décalage vers la droite est un décalage logique (les bits de poids fort prennent la valeur zéro).</span><span class="sxs-lookup"><span data-stu-id="52c68-108">If the first operand is of type [uint](../keywords/uint.md) or [ulong](../keywords/ulong.md), the right-shift is a logical shift (high-order bits are zero-filled).</span></span>

<span data-ttu-id="52c68-109">Les types définis par l’utilisateur peuvent surcharger l’opérateur `>>` ; le type du premier opérande doit être le type défini par l’utilisateur, et le type du second opérande doit être [int](../keywords/int.md). Pour plus d’informations, consultez [operator](../keywords/operator.md).</span><span class="sxs-lookup"><span data-stu-id="52c68-109">User-defined types can overload the `>>` operator; the type of the first operand must be the user-defined type, and the type of the second operand must be [int](../keywords/int.md). For more information, see [operator](../keywords/operator.md).</span></span> <span data-ttu-id="52c68-110">Quand un opérateur binaire est surchargé, l’opérateur d’assignation correspondant, le cas échéant, est aussi implicitement surchargé.</span><span class="sxs-lookup"><span data-stu-id="52c68-110">When a binary operator is overloaded, the corresponding assignment operator, if any, is also implicitly overloaded.</span></span>

## <a name="example"></a><span data-ttu-id="52c68-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="52c68-111">Example</span></span>

[!code-csharp[csRefOperators#26](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#26)]

## <a name="see-also"></a><span data-ttu-id="52c68-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52c68-112">See also</span></span>

- [<span data-ttu-id="52c68-113">Référence C#</span><span class="sxs-lookup"><span data-stu-id="52c68-113">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="52c68-114">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="52c68-114">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="52c68-115">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="52c68-115">C# operators</span></span>](index.md)