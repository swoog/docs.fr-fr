---
title: Comparaisons de valeurs (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], comparing values
- Visual Basic code, operators
- Visual Basic code, expressions
- comparison operators [Visual Basic], comparing expressions
- numeric expressions
- operators [Visual Basic], comparison
- expressions [Visual Basic], comparing
ms.assetid: 60da0c76-9458-4afc-97e9-44a7939c064c
ms.openlocfilehash: 23733741a79506730187d5735a20f3848e43da1d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54724812"
---
# <a name="value-comparisons-visual-basic"></a>Comparaisons de valeurs (Visual Basic)
Opérateurs de comparaison peuvent être utilisés pour construire des expressions qui comparent les valeurs de variables numériques. Ces expressions retournent un `Boolean` valeur selon que la comparaison est true ou false. Voici quelques exemples de ce type d’expression.  
  
 `45 > 26`  
  
 `26 > 45`  
  
 La première expression prend la valeur `True`, car 45 est supérieur à 26. Le deuxième exemple prend la valeur `False`, car 26 n’est pas supérieure à 45.  
  
 Vous pouvez également comparer des expressions numériques de cette façon. Les expressions que vous comparez peuvent être des expressions complexes, comme dans l’exemple suivant.  
  
 `x / 45 * (y +17) >= System.Math.Sqrt(z) / (p - (x * 16))`  
  
 L’expression précédente complexe inclut des littéraux, des variables et des appels de fonction. Les expressions des deux côtés de l’opérateur de comparaison sont évaluées et les valeurs résultantes sont ensuite comparés à l’aide de la `>=` opérateur de comparaison. Si la valeur de l’expression sur le côté gauche est supérieure ou égal à la valeur de l’expression de droite, l’ensemble de l’expression prend la valeur `True`; sinon, il renvoie la valeur `False`.  
  
 Les expressions qui comparent des valeurs sont couramment utilisées dans `If...Then` constructions, comme dans l’exemple suivant.  
  
 [!code-vb[VbVbalrOperators#84](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/value-comparisons_1.vb)]  
  
 Le `=` signe est un opérateur de comparaison ainsi que d’un opérateur d’assignation. Lorsqu’il est utilisé comme un opérateur de comparaison, il évalue si la valeur sur la gauche est égale à la valeur à droite, comme indiqué dans l’exemple suivant.  
  
 [!code-vb[VbVbalrOperators#85](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/value-comparisons_2.vb)]  
  
 Vous pouvez également utiliser une expression de comparaison n’importe où un `Boolean` valeur est nécessaire, comme dans un `If`, `While`, `Loop`, ou `ElseIf` instruction, ou lors de l’assignation ou du passage d’une valeur à une `Boolean` variable. Dans l’exemple suivant, la valeur retournée par l’expression de comparaison est assignée à un `Boolean` variable.  
  
 [!code-vb[VbVbalrOperators#86](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/value-comparisons_3.vb)]  
  
## <a name="see-also"></a>Voir aussi
- [Expressions booléennes](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/boolean-expressions.md)
- [Opérateurs et expressions](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/index.md)
- [Opérateurs de comparaison en Visual Basic](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/comparison-operators.md)
- [Guide pratique pour Calculer des valeurs numériques](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/how-to-calculate-numeric-values.md)
- [Priorité des opérateurs en Visual Basic](../../../../visual-basic/language-reference/operators/operator-precedence.md)
