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
---
# <a name="how-to-test-whether-two-objects-are-the-same-visual-basic"></a>Comment : déterminer si deux objets sont identiques (Visual Basic)
Si vous avez deux variables qui font référence aux objets, vous pouvez utiliser la `Is` ou `IsNot` (opérateur), ou les deux, pour déterminer si elles font référence à la même instance.  
  
### <a name="to-test-whether-two-objects-are-the-same"></a>Pour tester si deux objets sont identiques  
  
-   Utilisez le [est un opérateur](../../../../visual-basic/language-reference/operators/is-operator.md) ou [opérateur IsNot](../../../../visual-basic/language-reference/operators/isnot-operator.md) avec les deux variables comme opérandes.  
  
     [!code-vb[VbVbalrOperators#69](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-test-whether-two-objects-are-the-same_1.vb)]  
  
 Vous pouvez souhaiter prendre une certaine action selon si les deux objets font référence à la même instance. L’exemple précédent compare le contrôle `c` le contrôle actif du formulaire `f`. S’il n’existe aucun contrôle actif, ou s’il existe et qu’il n’est pas la même instance de contrôle que `c`, puis la `If` instruction échoue et la procédure est retournée sans traitement supplémentaire.  
  
 Si vous utilisez `Is` ou `IsNot` est une question de commodité personnelle. Un peut être plus facile à lire à l’autre dans une expression donnée.  
  
## <a name="see-also"></a>Voir aussi  
 [Opérateurs de comparaison en Visual Basic](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/comparison-operators.md)
