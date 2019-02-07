---
title: <<, opérateur - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- <<_CSharpKeyword
helpviewer_keywords:
- left shift operator (<<) [C#]
- << operator [C#]
ms.assetid: a654eb56-1ff7-4bf3-9064-b631be0cdccc
ms.openlocfilehash: 0271c97bc624a8946b90508e9ce39d217a128c05
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55261748"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="a5565-102">\<\<, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="a5565-102">\<\< operator (C# Reference)</span></span>

<span data-ttu-id="a5565-103">L’opérateur de décalage vers la gauche (`<<`) décale son premier opérande vers la gauche du nombre de bits spécifié par son deuxième opérande.</span><span class="sxs-lookup"><span data-stu-id="a5565-103">The left-shift operator (`<<`) shifts its first operand left by the number of bits specified by its second operand.</span></span> <span data-ttu-id="a5565-104">Le deuxième opérande doit être de type [int](../keywords/int.md) ou d’un type pour lequel une conversion numérique implicite vers `int` est prédéfinie.</span><span class="sxs-lookup"><span data-stu-id="a5565-104">The type of the second operand must be an [int](../keywords/int.md) or a type that has a predefined implicit numeric conversion to `int`.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5565-105">Notes</span><span class="sxs-lookup"><span data-stu-id="a5565-105">Remarks</span></span>

<span data-ttu-id="a5565-106">Si le premier opérande est de type [int](../keywords/int.md) ou [uint](../keywords/uint.md) (quantité de 32 bits), la valeur du décalage est donnée par les cinq bits de poids faible du second opérande.</span><span class="sxs-lookup"><span data-stu-id="a5565-106">If the first operand is an [int](../keywords/int.md) or [uint](../keywords/uint.md) (32-bit quantity), the shift count is given by the low-order five bits of the second operand.</span></span> <span data-ttu-id="a5565-107">Autrement dit, la valeur réelle du décalage est comprise entre 0 et 31 bits.</span><span class="sxs-lookup"><span data-stu-id="a5565-107">That is, the actual shift count is 0 to 31 bits.</span></span>

<span data-ttu-id="a5565-108">Si le premier opérande est de type [long](../keywords/long.md) ou [ulong](../keywords/ulong.md) (quantité de 64 bits), la valeur du décalage est donnée par les six bits de poids faible du second opérande.</span><span class="sxs-lookup"><span data-stu-id="a5565-108">If the first operand is a [long](../keywords/long.md) or [ulong](../keywords/ulong.md) (64-bit quantity), the shift count is given by the low-order six bits of the second operand.</span></span> <span data-ttu-id="a5565-109">Autrement dit, la valeur réelle du décalage est comprise entre 0 et 63 bits.</span><span class="sxs-lookup"><span data-stu-id="a5565-109">That is, the actual shift count is 0 to 63 bits.</span></span>

<span data-ttu-id="a5565-110">Les bits de poids fort qui ne se trouvent pas dans la plage du type du premier opérande après le décalage sont ignorés, et les bits vides de poids faible sont remplis de zéros.</span><span class="sxs-lookup"><span data-stu-id="a5565-110">Any high-order bits that are not within the range of the type of the first operand after the shift are discarded, and the low-order empty bits are zero-filled.</span></span> <span data-ttu-id="a5565-111">Les opérations de décalage ne provoquent jamais de dépassements de capacité.</span><span class="sxs-lookup"><span data-stu-id="a5565-111">Shift operations never cause overflows.</span></span>

<span data-ttu-id="a5565-112">Les types définis par l’utilisateur peuvent surcharger l’opérateur `<<` (consultez [operator](../keywords/operator.md)) ; le type du premier opérande doit être le type défini par l’utilisateur, et le type du second opérande doit être `int`.</span><span class="sxs-lookup"><span data-stu-id="a5565-112">User-defined types can overload the `<<` operator (see [operator](../keywords/operator.md)); the type of the first operand must be the user-defined type, and the type of the second operand must be `int`.</span></span> <span data-ttu-id="a5565-113">Quand un opérateur binaire est surchargé, l’opérateur d’assignation correspondant, le cas échéant, est aussi implicitement surchargé.</span><span class="sxs-lookup"><span data-stu-id="a5565-113">When a binary operator is overloaded, the corresponding assignment operator, if any, is also implicitly overloaded.</span></span>

## <a name="example"></a><span data-ttu-id="a5565-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="a5565-114">Example</span></span>

[!code-csharp[csRefOperators#14](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#14)]

## <a name="comments"></a><span data-ttu-id="a5565-115">Commentaires</span><span class="sxs-lookup"><span data-stu-id="a5565-115">Comments</span></span>

<span data-ttu-id="a5565-116">Notez que `i<<1` et `i<<33` donnent le même résultat, car 1 et 33 possèdent les cinq mêmes bits de poids faible.</span><span class="sxs-lookup"><span data-stu-id="a5565-116">Note that `i<<1` and `i<<33` give the same result, because 1 and 33 have the same low-order five bits.</span></span>

## <a name="see-also"></a><span data-ttu-id="a5565-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5565-117">See also</span></span>

- [<span data-ttu-id="a5565-118">Référence C#</span><span class="sxs-lookup"><span data-stu-id="a5565-118">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="a5565-119">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="a5565-119">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="a5565-120">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="a5565-120">C# Operators</span></span>](index.md)
