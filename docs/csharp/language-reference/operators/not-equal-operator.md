---
title: '!=, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '!=_CSharpKeyword'
helpviewer_keywords:
- inequality operator (!=) [C#]
- not equals operator (!=) [C#]
- '!= operator [C#]'
ms.assetid: eeff7a4e-ad6f-462d-9f8d-49e9b91c6c97
ms.openlocfilehash: 15f1b5930117e608644a58343fb855562f36b21c
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53237816"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="69ad4-102">!=, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="69ad4-102">!= Operator (C# Reference)</span></span>
<span data-ttu-id="69ad4-103">L’opérateur d’inégalité (`!=`) retourne la valeur false si ses opérandes sont égaux et la valeur true dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="69ad4-103">The inequality operator (`!=`) returns false if its operands are equal, true otherwise.</span></span> <span data-ttu-id="69ad4-104">Les opérateurs d’inégalité sont prédéfinis pour tous les types, dont string et object.</span><span class="sxs-lookup"><span data-stu-id="69ad4-104">Inequality operators are predefined for all types, including string and object.</span></span> <span data-ttu-id="69ad4-105">Les types définis par l’utilisateur peuvent surcharger l’opérateur `!=`.</span><span class="sxs-lookup"><span data-stu-id="69ad4-105">User-defined types can overload the `!=` operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="69ad4-106">Notes</span><span class="sxs-lookup"><span data-stu-id="69ad4-106">Remarks</span></span>  
 <span data-ttu-id="69ad4-107">Pour les types valeur prédéfinis, l’opérateur d’inégalité (`!=`) retourne la valeur true si les valeurs de ses opérandes sont différentes et la valeur false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="69ad4-107">For predefined value types, the inequality operator (`!=`) returns true if the values of its operands are different, false otherwise.</span></span> <span data-ttu-id="69ad4-108">Pour les types référence autres que `string`, `!=` retourne la valeur true si ses deux opérandes font référence à des objets différents.</span><span class="sxs-lookup"><span data-stu-id="69ad4-108">For reference types other than `string`, `!=` returns true if its two operands refer to different objects.</span></span> <span data-ttu-id="69ad4-109">Pour le type `string`, `!=` compare les valeurs des chaînes.</span><span class="sxs-lookup"><span data-stu-id="69ad4-109">For the `string` type, `!=` compares the values of the strings.</span></span>  
  
 <span data-ttu-id="69ad4-110">Les types valeur définis par l’utilisateur peuvent surcharger l’opérateur `!=` (consultez [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="69ad4-110">User-defined value types can overload the `!=` operator (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="69ad4-111">Il en va de même pour les types référence définis par l’utilisateur, même si par défaut `!=` se comporte comme indiqué ci-dessus pour les types référence prédéfinis et définis par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="69ad4-111">So can user-defined reference types, although by default `!=` behaves as described above for both predefined and user-defined reference types.</span></span> <span data-ttu-id="69ad4-112">Si `!=` est surchargé, [==](../../../csharp/language-reference/operators/equality-comparison-operator.md) doit aussi l’être.</span><span class="sxs-lookup"><span data-stu-id="69ad4-112">If `!=` is overloaded, [==](../../../csharp/language-reference/operators/equality-comparison-operator.md) must also be overloaded.</span></span> <span data-ttu-id="69ad4-113">Les opérations sur les types intégraux sont en général autorisées sur l’énumération.</span><span class="sxs-lookup"><span data-stu-id="69ad4-113">Operations on integral types are generally allowed on enumeration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="69ad4-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="69ad4-114">Example</span></span>  
 [!code-csharp[csRefOperators#33](../../../csharp/language-reference/operators/codesnippet/CSharp/not-equal-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="69ad4-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69ad4-115">See Also</span></span>

- [<span data-ttu-id="69ad4-116">Référence C#</span><span class="sxs-lookup"><span data-stu-id="69ad4-116">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="69ad4-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="69ad4-117">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="69ad4-118">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="69ad4-118">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
