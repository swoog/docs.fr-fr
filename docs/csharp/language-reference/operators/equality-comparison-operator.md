---
title: ==, opérateur (référence C#)
ms.date: 07/20/2015
f1_keywords:
- ==_CSharpKeyword
helpviewer_keywords:
- == operator [C#]
- equality operator [C#]
ms.assetid: 34c6b597-caa2-4855-a7cd-38ecdd11bd07
ms.openlocfilehash: d9d7dcf3b38939e681fb51d6c674151cee78b3d0
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43779160"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="06822-102">==, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="06822-102">== Operator (C# Reference)</span></span>
<span data-ttu-id="06822-103">Pour les types valeur prédéfinis, l’opérateur d’égalité (`==`) retourne true si les valeurs des opérandes sont égales et `false` dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="06822-103">For predefined value types, the equality operator (`==`) returns true if the values of its operands are equal, `false` otherwise.</span></span> <span data-ttu-id="06822-104">Pour les types référence autres que [string](../../../csharp/language-reference/keywords/string.md), `==` retourne `true` si ses deux opérandes font référence au même objet.</span><span class="sxs-lookup"><span data-stu-id="06822-104">For reference types other than [string](../../../csharp/language-reference/keywords/string.md), `==` returns `true` if its two operands refer to the same object.</span></span> <span data-ttu-id="06822-105">Pour le type `string`, `==` compare les valeurs des chaînes.</span><span class="sxs-lookup"><span data-stu-id="06822-105">For the `string` type, `==` compares the values of the strings.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="06822-106">Notes</span><span class="sxs-lookup"><span data-stu-id="06822-106">Remarks</span></span>  
 <span data-ttu-id="06822-107">Les types valeur définis par l’utilisateur peuvent surcharger l’opérateur `==` (consultez [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="06822-107">User-defined value types can overload the `==` operator (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="06822-108">Il en va de même pour les types référence définis par l’utilisateur, même si par défaut `==` se comporte comme indiqué ci-dessus pour les types référence prédéfinis et définis par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="06822-108">So can user-defined reference types, although by default `==` behaves as described above for both predefined and user-defined reference types.</span></span> <span data-ttu-id="06822-109">Si `==` est surchargé, [!=](../../../csharp/language-reference/operators/not-equal-operator.md) doit l’être aussi.</span><span class="sxs-lookup"><span data-stu-id="06822-109">If `==` is overloaded, [!=](../../../csharp/language-reference/operators/not-equal-operator.md) must also be overloaded.</span></span> <span data-ttu-id="06822-110">Les opérations sur les types intégraux sont en général autorisées sur l’énumération.</span><span class="sxs-lookup"><span data-stu-id="06822-110">Operations on integral types are generally allowed on enumeration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="06822-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="06822-111">Example</span></span>  
 [!code-csharp[csRefOperators#36](../../../csharp/language-reference/operators/codesnippet/CSharp/equality-comparison-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="06822-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06822-112">See Also</span></span>

- [<span data-ttu-id="06822-113">Référence C#</span><span class="sxs-lookup"><span data-stu-id="06822-113">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="06822-114">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="06822-114">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="06822-115">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="06822-115">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
