---
title: ^, opérateur (référence C#)
ms.date: 07/20/2015
f1_keywords:
- ^_CSharpKeyword
helpviewer_keywords:
- ^ operator [C#]
- bitwise exclusive OR operator [C#]
ms.assetid: b09bc815-570f-4db6-a637-5b4ed99d014a
ms.openlocfilehash: b1333f9d06e2804029550e6364a225558e096431
ms.sourcegitcommit: 412bbc2e43c3b6ca25b358cdf394be97336f0c24
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/25/2018
ms.locfileid: "42925296"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="2d806-102">^, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="2d806-102">^ Operator (C# Reference)</span></span>
<span data-ttu-id="2d806-103">Les opérateurs `^` binaires sont prédéfinis pour les types intégraux et `bool`.</span><span class="sxs-lookup"><span data-stu-id="2d806-103">Binary `^` operators are predefined for the integral types and `bool`.</span></span> <span data-ttu-id="2d806-104">Pour les types intégraux, `^` effectue l’opération de bits OR exclusif sur les opérandes.</span><span class="sxs-lookup"><span data-stu-id="2d806-104">For integral types, `^` computes the bitwise exclusive-OR of its operands.</span></span> <span data-ttu-id="2d806-105">Pour les opérandes `bool`, `^` effectue l’opération OR exclusif logique sur ses opérandes. En conséquence, le résultat est `true` si et seulement si un seul des opérandes correspond à `true`.</span><span class="sxs-lookup"><span data-stu-id="2d806-105">For `bool` operands, `^` computes the logical exclusive-or of its operands; that is, the result is `true` if and only if exactly one of its operands is `true`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2d806-106">Notes</span><span class="sxs-lookup"><span data-stu-id="2d806-106">Remarks</span></span>  
 <span data-ttu-id="2d806-107">Les types définis par l’utilisateur peuvent surcharger l’opérateur `^` (voir [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="2d806-107">User-defined types can overload the `^` operator (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="2d806-108">Les opérations sur les types intégraux sont en général autorisées sur l’énumération.</span><span class="sxs-lookup"><span data-stu-id="2d806-108">Operations on integral types are generally allowed on enumeration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2d806-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="2d806-109">Example</span></span>  
 [!code-csharp[csRefOperators#30](../../../csharp/language-reference/operators/codesnippet/CSharp/xor-operator_1.cs)]  
  
 <span data-ttu-id="2d806-110">Le calcul de `0xf8 ^ 0x3f` dans l’exemple précédent effectue une opération de bits OR exclusif des deux valeurs binaires suivantes, qui correspondent aux valeurs hexadécimales F8 et 3F :</span><span class="sxs-lookup"><span data-stu-id="2d806-110">The computation of `0xf8 ^ 0x3f` in the previous example performs a bitwise exclusive-OR of the following two binary values, which correspond to the hexadecimal values F8 and 3F:</span></span>  
  
 `1111 1000`  
  
 `0011 1111`  
  
 <span data-ttu-id="2d806-111">Le résultat de l’opération OR exclusif est `1100 0111`, qui correspond à C7 en hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="2d806-111">The result of the exclusive-OR is `1100 0111`, which is C7 in hexadecimal.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2d806-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d806-112">See Also</span></span>

- [<span data-ttu-id="2d806-113">Référence C#</span><span class="sxs-lookup"><span data-stu-id="2d806-113">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="2d806-114">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="2d806-114">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="2d806-115">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="2d806-115">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
