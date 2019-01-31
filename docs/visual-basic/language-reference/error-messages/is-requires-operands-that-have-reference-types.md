---
title: "'Is' requiert des opérandes ayant des types référence, mais cet opérande a le type valeur '<typename>'"
ms.date: 07/20/2015
f1_keywords:
- bc30020
- vbc30020
helpviewer_keywords:
- BC30020
ms.assetid: 228afebd-1203-4bd3-8d7a-c5c56f3cedc4
ms.openlocfilehash: fbd0011e76ccecc605b0355025b7ca131e44724e
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55263928"
---
# <a name="is-requires-operands-that-have-reference-types-but-this-operand-has-the-value-type-typename"></a><span data-ttu-id="8d915-102">'Is' requiert des opérandes qui ont des types référence, mais cet opérande a le type valeur '\<nom_type >'</span><span class="sxs-lookup"><span data-stu-id="8d915-102">'Is' requires operands that have reference types, but this operand has the value type '\<typename>'</span></span>
<span data-ttu-id="8d915-103">Le `Is` opérateur de comparaison détermine si deux variables d’objet font référence à la même instance.</span><span class="sxs-lookup"><span data-stu-id="8d915-103">The `Is` comparison operator determines whether two object variables refer to the same instance.</span></span> <span data-ttu-id="8d915-104">Cette comparaison n’est pas définie pour les types valeur.</span><span class="sxs-lookup"><span data-stu-id="8d915-104">This comparison is not defined for value types.</span></span>  
  
 <span data-ttu-id="8d915-105">**ID d’erreur :** BC30020</span><span class="sxs-lookup"><span data-stu-id="8d915-105">**Error ID:** BC30020</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="8d915-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="8d915-106">To correct this error</span></span>  
  
-   <span data-ttu-id="8d915-107">Utilisez l’opérateur de comparaison arithmétique approprié ou `Like` opérateur pour comparer deux types de valeur.</span><span class="sxs-lookup"><span data-stu-id="8d915-107">Use the appropriate arithmetic comparison operator or the `Like` operator to compare two value types.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8d915-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d915-108">See also</span></span>
- [<span data-ttu-id="8d915-109">Is (opérateur)</span><span class="sxs-lookup"><span data-stu-id="8d915-109">Is Operator</span></span>](../../../visual-basic/language-reference/operators/is-operator.md)
- [<span data-ttu-id="8d915-110">Like (opérateur)</span><span class="sxs-lookup"><span data-stu-id="8d915-110">Like Operator</span></span>](../../../visual-basic/language-reference/operators/like-operator.md)
- [<span data-ttu-id="8d915-111">Opérateurs de comparaison</span><span class="sxs-lookup"><span data-stu-id="8d915-111">Comparison Operators</span></span>](../../../visual-basic/language-reference/operators/comparison-operators.md)
