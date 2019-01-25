---
title: '&#39;Est&#39; requiert des opérandes qui ont des types référence, mais cet opérande a le type de valeur &#39; &lt;typename&gt;&#39;'
ms.date: 07/20/2015
f1_keywords:
- bc30020
- vbc30020
helpviewer_keywords:
- BC30020
ms.assetid: 228afebd-1203-4bd3-8d7a-c5c56f3cedc4
ms.openlocfilehash: 0b3f80e98087e455ec730dea8c57478528e9259c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54722918"
---
# <a name="39is39-requires-operands-that-have-reference-types-but-this-operand-has-the-value-type-39lttypenamegt39"></a><span data-ttu-id="03c83-102">&#39;Est&#39; requiert des opérandes qui ont des types référence, mais cet opérande a le type de valeur &#39; &lt;typename&gt;&#39;</span><span class="sxs-lookup"><span data-stu-id="03c83-102">&#39;Is&#39; requires operands that have reference types, but this operand has the value type &#39;&lt;typename&gt;&#39;</span></span>
<span data-ttu-id="03c83-103">Le `Is` opérateur de comparaison détermine si deux variables d’objet font référence à la même instance.</span><span class="sxs-lookup"><span data-stu-id="03c83-103">The `Is` comparison operator determines whether two object variables refer to the same instance.</span></span> <span data-ttu-id="03c83-104">Cette comparaison n’est pas définie pour les types valeur.</span><span class="sxs-lookup"><span data-stu-id="03c83-104">This comparison is not defined for value types.</span></span>  
  
 <span data-ttu-id="03c83-105">**ID d’erreur :** BC30020</span><span class="sxs-lookup"><span data-stu-id="03c83-105">**Error ID:** BC30020</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="03c83-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="03c83-106">To correct this error</span></span>  
  
-   <span data-ttu-id="03c83-107">Utilisez l’opérateur de comparaison arithmétique approprié ou `Like` opérateur pour comparer deux types de valeur.</span><span class="sxs-lookup"><span data-stu-id="03c83-107">Use the appropriate arithmetic comparison operator or the `Like` operator to compare two value types.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="03c83-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03c83-108">See also</span></span>
- [<span data-ttu-id="03c83-109">Is (opérateur)</span><span class="sxs-lookup"><span data-stu-id="03c83-109">Is Operator</span></span>](../../../visual-basic/language-reference/operators/is-operator.md)
- [<span data-ttu-id="03c83-110">Like (opérateur)</span><span class="sxs-lookup"><span data-stu-id="03c83-110">Like Operator</span></span>](../../../visual-basic/language-reference/operators/like-operator.md)
- [<span data-ttu-id="03c83-111">Opérateurs de comparaison</span><span class="sxs-lookup"><span data-stu-id="03c83-111">Comparison Operators</span></span>](../../../visual-basic/language-reference/operators/comparison-operators.md)
