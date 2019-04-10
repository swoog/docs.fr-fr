---
title: 'Procédure : Passer des procédures à une autre procédure en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- AddressOf operator [Visual Basic]
- delegates [Visual Basic], passing procedures
ms.assetid: 5adbba15-5a1d-413f-ab3e-3ff6cc0a4669
ms.openlocfilehash: 312c0e0f100e85256ad4ca856ccf7f35dbaa36dc
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59305245"
---
# <a name="how-to-pass-procedures-to-another-procedure-in-visual-basic"></a>Procédure : Passer des procédures à une autre procédure en Visual Basic
Cet exemple montre comment utiliser des délégués pour passer d’une procédure à une autre procédure.  
  
 Un délégué est un type que vous pouvez utiliser comme tout autre type dans Visual Basic. Le `AddressOf` opérateur retourne un objet délégué lorsqu’il est appliqué à un nom de procédure.  
  
 Cet exemple comporte une procédure avec un paramètre de délégué qui peut prendre une référence à une autre procédure, obtenue avec la `AddressOf` opérateur.  
  
### <a name="create-the-delegate-and-matching-procedures"></a>Créer le délégué et les procédures correspondantes  
  
1. Créez un délégué nommé `MathOperator`.  
  
     [!code-vb[VbVbalrDelegates#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDelegates/VB/Class1.vb#1)]  
  
2. Créez une procédure nommée `AddNumbers` avec des paramètres et la valeur de retour qui correspondent à celles de `MathOperator`, de sorte que les signatures correspondent.  
  
     [!code-vb[VbVbalrDelegates#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDelegates/VB/Class1.vb#2)]  
  
3. Créez une procédure nommée `SubtractNumbers` avec une signature qui correspond à `MathOperator`.  
  
     [!code-vb[VbVbalrDelegates#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDelegates/VB/Class1.vb#3)]  
  
4. Créez une procédure nommée `DelegateTest` qui prend un délégué en tant que paramètre.  
  
     Cette procédure peut accepter une référence à `AddNumbers` ou `SubtractNumbers`, car leurs signatures correspondent à la `MathOperator` signature.  
  
     [!code-vb[VbVbalrDelegates#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDelegates/VB/Class1.vb#4)]  
  
5. Créez une procédure nommée `Test` qui appelle `DelegateTest` une autre fois avec le délégué pour `AddNumbers` en tant que paramètre, puis à nouveau avec le délégué pour `SubtractNumbers` en tant que paramètre.  
  
     [!code-vb[VbVbalrDelegates#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrDelegates/VB/Class1.vb#5)]  
  
     Lorsque `Test` est appelée, elle affiche d’abord le résultat de `AddNumbers` agissant sur `5` et `3`, qui est 8. Puis le résultat de `SubtractNumbers` agissant sur `9` et `3` s’affiche, qui est 6.  
  
## <a name="see-also"></a>Voir aussi

- [Délégués](../../../../visual-basic/programming-guide/language-features/delegates/index.md)
- [AddressOf, opérateur](../../../../visual-basic/language-reference/operators/addressof-operator.md)
- [Delegate, instruction](../../../../visual-basic/language-reference/statements/delegate-statement.md)
- [Procédure : appeler une méthode déléguée](../../../../visual-basic/programming-guide/language-features/delegates/how-to-invoke-a-delegate-method.md)
