---
title: 'Comment : déterminer si deux objets sont identiques (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], reference
- Is operator [Visual Basic], comparing objects
- reference variables [Visual Basic]
- variables [Visual Basic], referring to same object
- objects [Visual Basic], variables referring to same
- Visual Basic code, operators
ms.assetid: f760e828-8704-4256-bc2d-c22a4c93b524
ms.openlocfilehash: 005c91e6f4ec556a7e1bf255b47c8276a5d3d185
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33647603"
---
# <a name="how-to-test-whether-two-objects-are-the-same-visual-basic"></a><span data-ttu-id="a0948-102">Comment : déterminer si deux objets sont identiques (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a0948-102">How to: Test Whether Two Objects Are the Same (Visual Basic)</span></span>
<span data-ttu-id="a0948-103">Si vous avez deux variables qui font référence aux objets, vous pouvez utiliser la `Is` ou `IsNot` (opérateur), ou les deux, pour déterminer si elles font référence à la même instance.</span><span class="sxs-lookup"><span data-stu-id="a0948-103">If you have two variables that refer to objects, you can use either the `Is` or `IsNot` operator, or both, to determine whether they refer to the same instance.</span></span>  
  
### <a name="to-test-whether-two-objects-are-the-same"></a><span data-ttu-id="a0948-104">Pour tester si deux objets sont identiques</span><span class="sxs-lookup"><span data-stu-id="a0948-104">To test whether two objects are the same</span></span>  
  
-   <span data-ttu-id="a0948-105">Utilisez le [est un opérateur](../../../../visual-basic/language-reference/operators/is-operator.md) ou [opérateur IsNot](../../../../visual-basic/language-reference/operators/isnot-operator.md) avec les deux variables comme opérandes.</span><span class="sxs-lookup"><span data-stu-id="a0948-105">Use the [Is Operator](../../../../visual-basic/language-reference/operators/is-operator.md) or the [IsNot Operator](../../../../visual-basic/language-reference/operators/isnot-operator.md) with the two variables as operands.</span></span>  
  
     [!code-vb[VbVbalrOperators#69](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-test-whether-two-objects-are-the-same_1.vb)]  
  
 <span data-ttu-id="a0948-106">Vous pouvez souhaiter prendre une certaine action selon si les deux objets font référence à la même instance.</span><span class="sxs-lookup"><span data-stu-id="a0948-106">You might want to take a certain action depending on whether two objects refer to the same instance.</span></span> <span data-ttu-id="a0948-107">L’exemple précédent compare le contrôle `c` le contrôle actif du formulaire `f`.</span><span class="sxs-lookup"><span data-stu-id="a0948-107">The preceding example compares control `c` against the active control on form `f`.</span></span> <span data-ttu-id="a0948-108">S’il n’existe aucun contrôle actif, ou s’il existe et qu’il n’est pas la même instance de contrôle que `c`, puis la `If` instruction échoue et la procédure est retournée sans traitement supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="a0948-108">If there is no active control, or if there is one but it is not the same control instance as `c`, then the `If` statement fails and the procedure returns without further processing.</span></span>  
  
 <span data-ttu-id="a0948-109">Si vous utilisez `Is` ou `IsNot` est une question de commodité personnelle.</span><span class="sxs-lookup"><span data-stu-id="a0948-109">Whether you use `Is` or `IsNot` is a matter of personal convenience to you.</span></span> <span data-ttu-id="a0948-110">Un peut être plus facile à lire à l’autre dans une expression donnée.</span><span class="sxs-lookup"><span data-stu-id="a0948-110">One might be easier to read than the other in a given expression.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a0948-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0948-111">See Also</span></span>  
 [<span data-ttu-id="a0948-112">Opérateurs de comparaison en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="a0948-112">Comparison Operators in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/comparison-operators.md)
