---
title: '&amp;, opérateur (référence C#)'
ms.date: 04/04/2018
f1_keywords:
- '&_CSharpKeyword'
helpviewer_keywords:
- bitwise AND operator [C#]
- ampersand operator (&) [C#]
- '& operator [C#]'
- AND operator (&) [C#]
ms.assetid: afa346d5-90ec-4b1f-a2c8-3881f018741d
ms.openlocfilehash: 59813b4bc5781776c9f9741c3e49e660c684bff9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33267878"
---
# <a name="amp-operator-c-reference"></a><span data-ttu-id="b6f2e-102">&amp;, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="b6f2e-102">&amp; Operator (C# Reference)</span></span>
<span data-ttu-id="b6f2e-103">L’opérateur `&` peut être utilisé comme opérateur unaire ou opérateur binaire.</span><span class="sxs-lookup"><span data-stu-id="b6f2e-103">The `&` operator can function as either a unary or a binary operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b6f2e-104">Notes</span><span class="sxs-lookup"><span data-stu-id="b6f2e-104">Remarks</span></span>  
 <span data-ttu-id="b6f2e-105">L’opérateur `&` unaire retourne l’adresse de son opérande (requiert un contexte [unsafe](../../../csharp/language-reference/keywords/unsafe.md)).</span><span class="sxs-lookup"><span data-stu-id="b6f2e-105">The unary `&` operator returns the address of its operand (requires [unsafe](../../../csharp/language-reference/keywords/unsafe.md) context).</span></span>  
  
 <span data-ttu-id="b6f2e-106">Les opérateurs `&` binaires sont prédéfinis pour les types intégraux et `bool`.</span><span class="sxs-lookup"><span data-stu-id="b6f2e-106">Binary `&` operators are predefined for the integral types and `bool`.</span></span> <span data-ttu-id="b6f2e-107">Pour les types intégraux, & calcule l’opération logique AND au niveau du bit de ses opérandes.</span><span class="sxs-lookup"><span data-stu-id="b6f2e-107">For integral types, & computes the logical bitwise AND of its operands.</span></span> <span data-ttu-id="b6f2e-108">Pour les opérandes `bool`, & calcule l’opération logique AND de ses opérandes ; autrement dit, le résultat est `true` uniquement si ses deux opérandes ont la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="b6f2e-108">For `bool` operands, & computes the logical AND of its operands; that is, the result is `true` if and only if both its operands are `true`.</span></span>  
  
 <span data-ttu-id="b6f2e-109">L’opérateur `&` binaire évalue les deux opérateurs, quelle que soit la valeur du premier, à la différence de [l’opérateur AND conditionnel](../../../csharp/language-reference/operators/conditional-and-operator.md) `&&`.</span><span class="sxs-lookup"><span data-stu-id="b6f2e-109">The binary `&` operator evaluates both operators regardless of the first one's value, in contrast to the [conditional AND operator](../../../csharp/language-reference/operators/conditional-and-operator.md) `&&`.</span></span> <span data-ttu-id="b6f2e-110">Exemple :</span><span class="sxs-lookup"><span data-stu-id="b6f2e-110">For example:</span></span>  
  
 [!code-csharp[csRefOperators#37](../../../csharp/language-reference/operators/codesnippet/CSharp/and-operator_1.cs)]  
  
 <span data-ttu-id="b6f2e-111">Les types définis par l’utilisateur peuvent surcharger l’opérateur `&` binaire (voir [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="b6f2e-111">User-defined types can overload the binary `&` operator (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="b6f2e-112">Les opérations sur les types intégraux sont en général autorisées sur l’énumération.</span><span class="sxs-lookup"><span data-stu-id="b6f2e-112">Operations on integral types are generally allowed on enumeration.</span></span> <span data-ttu-id="b6f2e-113">Quand un opérateur binaire est surchargé, l’opérateur d’assignation correspondant, le cas échéant, est aussi implicitement surchargé.</span><span class="sxs-lookup"><span data-stu-id="b6f2e-113">When a binary operator is overloaded, the corresponding assignment operator, if any, is also implicitly overloaded.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b6f2e-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="b6f2e-114">Example</span></span>  
 [!code-csharp[csRefOperators#38](../../../csharp/language-reference/operators/codesnippet/CSharp/and-operator_2.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="b6f2e-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6f2e-115">See Also</span></span>  
 [<span data-ttu-id="b6f2e-116">Référence C#</span><span class="sxs-lookup"><span data-stu-id="b6f2e-116">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="b6f2e-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="b6f2e-117">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="b6f2e-118">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="b6f2e-118">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
