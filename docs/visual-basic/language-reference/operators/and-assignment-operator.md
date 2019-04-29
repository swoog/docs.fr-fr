---
title: '&amp;=, Opérateur (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- vb.&=
helpviewer_keywords:
- operator &=
- assignment statements [Visual Basic], compound
- statements [Visual Basic], compound assignment
- '&= operator [Visual Basic]'
- compound assignment statements [Visual Basic]
ms.assetid: 0cf262fc-1a05-419a-a503-60013f111c8a
ms.openlocfilehash: a79e779d8fcf549daeabc494e0a55deee30b5d22
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61608435"
---
# <a name="amp-operator-visual-basic"></a>&amp;=, Opérateur (Visual Basic)
Concatène une `String` expression à une `String` variable ou propriété et assigne le résultat à la variable ou propriété.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
variableorproperty &= expression  
```  
  
## <a name="parts"></a>Composants  
 `variableorproperty`  
 Obligatoire. N’importe quel `String` variable ou propriété.  
  
 `expression`  
 Obligatoire. Toute expression `String` .  
  
## <a name="remarks"></a>Notes  
 L’élément sur le côté gauche de la `&=` opérateur peut être une simple variable scalaire, une propriété ou un élément d’un tableau. La variable ou la propriété ne peut pas être [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md). Le `&=` opérateur concatène le `String` expression située à droite vers le `String` variable ou propriété du côté gauche et assigne le résultat à la variable ou la propriété situé à sa gauche.  
  
## <a name="overloading"></a>Surcharge  
 Le [& opérateur](../../../visual-basic/language-reference/operators/concatenation-operator.md) peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure. La surcharge la `&` opérateur affecte le comportement de la `&=` opérateur. Si votre code utilise `&=` sur une classe ou structure qui surcharge `&`, assurez-vous que vous comprenez son comportement redéfini. Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le `&=` pour concaténer deux `String` variables et assigner le résultat à la première variable.  
  
 [!code-vb[VbVbalrOperators#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#3)]  
  
## <a name="see-also"></a>Voir aussi

- [& (opérateur)](../../../visual-basic/language-reference/operators/concatenation-operator.md)
- [+= (opérateur)](../../../visual-basic/language-reference/operators/addition-assignment-operator.md)
- [Opérateurs d’assignation](../../../visual-basic/language-reference/operators/assignment-operators.md)
- [opérateur de concaténation](../../../visual-basic/language-reference/operators/concatenation-operators.md)
- [Priorité des opérateurs en Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [Opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [Instructions](../../../visual-basic/programming-guide/language-features/statements.md)
