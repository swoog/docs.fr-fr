---
title: 'Procédure : Tester si deux objets sont du même (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], reference
- Is operator [Visual Basic], comparing objects
- reference variables [Visual Basic]
- variables [Visual Basic], referring to same object
- objects [Visual Basic], variables referring to same
- Visual Basic code, operators
ms.assetid: f760e828-8704-4256-bc2d-c22a4c93b524
ms.openlocfilehash: dbb268175d197e7b931af45a98f3a273c593e5a3
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58819107"
---
# <a name="how-to-test-whether-two-objects-are-the-same-visual-basic"></a><span data-ttu-id="8666f-102">Procédure : Tester si deux objets sont du même (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="8666f-102">How to: Test Whether Two Objects Are the Same (Visual Basic)</span></span>
<span data-ttu-id="8666f-103">Si vous avez deux variables qui font référence aux objets, vous pouvez utiliser la `Is` ou `IsNot` opérateur, ou les deux, pour déterminer s’ils font référence à la même instance.</span><span class="sxs-lookup"><span data-stu-id="8666f-103">If you have two variables that refer to objects, you can use either the `Is` or `IsNot` operator, or both, to determine whether they refer to the same instance.</span></span>  
  
### <a name="to-test-whether-two-objects-are-the-same"></a><span data-ttu-id="8666f-104">Pour tester si deux objets sont identiques</span><span class="sxs-lookup"><span data-stu-id="8666f-104">To test whether two objects are the same</span></span>  
  
-   <span data-ttu-id="8666f-105">Utilisez le [opérateur Is](../../../../visual-basic/language-reference/operators/is-operator.md) ou le [opérateur IsNot](../../../../visual-basic/language-reference/operators/isnot-operator.md) avec les deux variables comme opérandes.</span><span class="sxs-lookup"><span data-stu-id="8666f-105">Use the [Is Operator](../../../../visual-basic/language-reference/operators/is-operator.md) or the [IsNot Operator](../../../../visual-basic/language-reference/operators/isnot-operator.md) with the two variables as operands.</span></span>  
  
     [!code-vb[VbVbalrOperators#69](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#69)]  
  
 <span data-ttu-id="8666f-106">Vous souhaiterez peut-être prendre une certaine action selon si les deux objets font référence à la même instance.</span><span class="sxs-lookup"><span data-stu-id="8666f-106">You might want to take a certain action depending on whether two objects refer to the same instance.</span></span> <span data-ttu-id="8666f-107">L’exemple précédent compare le contrôle `c` contre le contrôle actif sur le formulaire `f`.</span><span class="sxs-lookup"><span data-stu-id="8666f-107">The preceding example compares control `c` against the active control on form `f`.</span></span> <span data-ttu-id="8666f-108">Si aucun contrôle n’est active, ou s’il existe et qu’il n’est pas la même instance de contrôle que `c`, puis la `If` instruction échoue et la procédure renvoie sans traitement supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="8666f-108">If there is no active control, or if there is one but it is not the same control instance as `c`, then the `If` statement fails and the procedure returns without further processing.</span></span>  
  
 <span data-ttu-id="8666f-109">Si vous utilisez `Is` ou `IsNot` est une question de commodité personnelle.</span><span class="sxs-lookup"><span data-stu-id="8666f-109">Whether you use `Is` or `IsNot` is a matter of personal convenience to you.</span></span> <span data-ttu-id="8666f-110">Un peut être plus facile à lire à l’autre dans une expression donnée.</span><span class="sxs-lookup"><span data-stu-id="8666f-110">One might be easier to read than the other in a given expression.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8666f-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8666f-111">See also</span></span>

- [<span data-ttu-id="8666f-112">Opérateurs de comparaison en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="8666f-112">Comparison Operators in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/comparison-operators.md)
