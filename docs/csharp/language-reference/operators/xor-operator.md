---
title: ^, opérateur (référence C#)
ms.date: 07/20/2015
f1_keywords:
- ^_CSharpKeyword
helpviewer_keywords:
- ^ operator [C#]
- bitwise exclusive OR operator [C#]
ms.assetid: b09bc815-570f-4db6-a637-5b4ed99d014a
ms.openlocfilehash: 5cc3cd2cfc932646e5b2dd6ec034555b07582379
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33271248"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="d9532-102">^, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="d9532-102">^ Operator (C# Reference)</span></span>
<span data-ttu-id="d9532-103">Les opérateurs `^` binaires sont prédéfinis pour les types intégraux et `bool`.</span><span class="sxs-lookup"><span data-stu-id="d9532-103">Binary `^` operators are predefined for the integral types and `bool`.</span></span> <span data-ttu-id="d9532-104">Pour les types intégraux, `^` effectue l’opération de bits OR exclusif sur les opérandes.</span><span class="sxs-lookup"><span data-stu-id="d9532-104">For integral types, `^` computes the bitwise exclusive-OR of its operands.</span></span> <span data-ttu-id="d9532-105">Pour les opérandes `bool`, `^` effectue l’opération OR exclusif logique sur ses opérandes. En conséquence, le résultat est `true` si et seulement si un seul des opérandes correspond à `true`.</span><span class="sxs-lookup"><span data-stu-id="d9532-105">For `bool` operands, `^` computes the logical exclusive-or of its operands; that is, the result is `true` if and only if exactly one of its operands is `true`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d9532-106">Notes</span><span class="sxs-lookup"><span data-stu-id="d9532-106">Remarks</span></span>  
 <span data-ttu-id="d9532-107">Les types définis par l’utilisateur peuvent surcharger l’opérateur `^` (voir [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="d9532-107">User-defined types can overload the `^` operator (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="d9532-108">Les opérations sur les types intégraux sont en général autorisées sur l’énumération.</span><span class="sxs-lookup"><span data-stu-id="d9532-108">Operations on integral types are generally allowed on enumeration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d9532-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="d9532-109">Example</span></span>  
 [!code-csharp[csRefOperators#30](../../../csharp/language-reference/operators/codesnippet/CSharp/xor-operator_1.cs)]  
  
 <span data-ttu-id="d9532-110">Le calcul de `0xf8 ^ 0x3f` dans l’exemple précédent effectue une opération de bits OR exclusif des deux valeurs binaires suivantes, qui correspondent aux valeurs hexadécimales F8 et 3F :</span><span class="sxs-lookup"><span data-stu-id="d9532-110">The computation of `0xf8 ^ 0x3f` in the previous example performs a bitwise exclusive-OR of the following two binary values, which correspond to the hexadecimal values F8 and 3F:</span></span>  
  
 `1111 1000`  
  
 `0011 1111`  
  
 <span data-ttu-id="d9532-111">Le résultat de l’opération OR exclusif est `1100 0111`, qui correspond à C7 en hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="d9532-111">The result of the exclusive-OR is `1100 0111`, which is C7 in hexadecimal.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d9532-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9532-112">See Also</span></span>  
 [<span data-ttu-id="d9532-113">Référence C#</span><span class="sxs-lookup"><span data-stu-id="d9532-113">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="d9532-114">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="d9532-114">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="d9532-115">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="d9532-115">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
