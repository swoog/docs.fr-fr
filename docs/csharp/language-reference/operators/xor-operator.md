---
title: ^, opérateur - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- ^_CSharpKeyword
helpviewer_keywords:
- ^ operator [C#]
- bitwise exclusive OR operator [C#]
ms.assetid: b09bc815-570f-4db6-a637-5b4ed99d014a
ms.openlocfilehash: f6f09f197502af1bc38bcdef97dd1db0ad9c7c08
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53236945"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="383c4-102">^, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="383c4-102">^ Operator (C# Reference)</span></span>
<span data-ttu-id="383c4-103">Les opérateurs `^` binaires sont prédéfinis pour les types intégraux et `bool`.</span><span class="sxs-lookup"><span data-stu-id="383c4-103">Binary `^` operators are predefined for the integral types and `bool`.</span></span> <span data-ttu-id="383c4-104">Pour les types intégraux, `^` effectue l’opération de bits OR exclusif sur les opérandes.</span><span class="sxs-lookup"><span data-stu-id="383c4-104">For integral types, `^` computes the bitwise exclusive-OR of its operands.</span></span> <span data-ttu-id="383c4-105">Pour les opérandes `bool`, `^` effectue l’opération OR exclusif logique sur ses opérandes. En conséquence, le résultat est `true` si et seulement si un seul des opérandes correspond à `true`.</span><span class="sxs-lookup"><span data-stu-id="383c4-105">For `bool` operands, `^` computes the logical exclusive-or of its operands; that is, the result is `true` if and only if exactly one of its operands is `true`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="383c4-106">Notes</span><span class="sxs-lookup"><span data-stu-id="383c4-106">Remarks</span></span>  
 <span data-ttu-id="383c4-107">Les types définis par l’utilisateur peuvent surcharger l’opérateur `^` (voir [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="383c4-107">User-defined types can overload the `^` operator (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="383c4-108">Les opérations sur les types intégraux sont en général autorisées sur l’énumération.</span><span class="sxs-lookup"><span data-stu-id="383c4-108">Operations on integral types are generally allowed on enumeration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="383c4-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="383c4-109">Example</span></span>  
 [!code-csharp[csRefOperators#30](../../../csharp/language-reference/operators/codesnippet/CSharp/xor-operator_1.cs)]  
  
 <span data-ttu-id="383c4-110">Le calcul de `0xf8 ^ 0x3f` dans l’exemple précédent effectue une opération de bits OR exclusif des deux valeurs binaires suivantes, qui correspondent aux valeurs hexadécimales F8 et 3F :</span><span class="sxs-lookup"><span data-stu-id="383c4-110">The computation of `0xf8 ^ 0x3f` in the previous example performs a bitwise exclusive-OR of the following two binary values, which correspond to the hexadecimal values F8 and 3F:</span></span>  
  
 `1111 1000`  
  
 `0011 1111`  
  
 <span data-ttu-id="383c4-111">Le résultat de l’opération OR exclusif est `1100 0111`, qui correspond à C7 en hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="383c4-111">The result of the exclusive-OR is `1100 0111`, which is C7 in hexadecimal.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="383c4-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="383c4-112">See Also</span></span>

- [<span data-ttu-id="383c4-113">Référence C#</span><span class="sxs-lookup"><span data-stu-id="383c4-113">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="383c4-114">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="383c4-114">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="383c4-115">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="383c4-115">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
