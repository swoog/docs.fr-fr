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
ms.openlocfilehash: 4130dfbe70682e28b6bb15db633ede2790e20aa3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54595550"
---
# <a name="how-to-test-whether-two-objects-are-the-same-visual-basic"></a>Procédure : Tester si deux objets sont du même (Visual Basic)
Si vous avez deux variables qui font référence aux objets, vous pouvez utiliser la `Is` ou `IsNot` opérateur, ou les deux, pour déterminer s’ils font référence à la même instance.  
  
### <a name="to-test-whether-two-objects-are-the-same"></a>Pour tester si deux objets sont identiques  
  
-   Utilisez le [opérateur Is](../../../../visual-basic/language-reference/operators/is-operator.md) ou le [opérateur IsNot](../../../../visual-basic/language-reference/operators/isnot-operator.md) avec les deux variables comme opérandes.  
  
     [!code-vb[VbVbalrOperators#69](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-test-whether-two-objects-are-the-same_1.vb)]  
  
 Vous souhaiterez peut-être prendre une certaine action selon si les deux objets font référence à la même instance. L’exemple précédent compare le contrôle `c` contre le contrôle actif sur le formulaire `f`. Si aucun contrôle n’est active, ou s’il existe et qu’il n’est pas la même instance de contrôle que `c`, puis la `If` instruction échoue et la procédure renvoie sans traitement supplémentaire.  
  
 Si vous utilisez `Is` ou `IsNot` est une question de commodité personnelle. Un peut être plus facile à lire à l’autre dans une expression donnée.  
  
## <a name="see-also"></a>Voir aussi
- [Opérateurs de comparaison en Visual Basic](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/comparison-operators.md)
