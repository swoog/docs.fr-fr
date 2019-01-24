---
title: '*=, opérateur (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- vb.*=
helpviewer_keywords:
- operator *=
- assignment statements [Visual Basic], compound
- statements [Visual Basic], compound assignment
- '*= operator [Visual Basic]'
- compound assignment statements [Visual Basic]
ms.assetid: 96c86509-6eb8-4682-8226-3852e049376f
ms.openlocfilehash: 3aa1d563b9657d4e80425b8c2d29e069ca2ef06a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54601881"
---
# <a name="-operator-visual-basic"></a>*=, opérateur (Visual Basic)
Multiplie la valeur d’une variable ou une propriété par la valeur d’une expression et assigne le résultat à la variable ou propriété.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
variableorproperty *= expression  
```  
  
## <a name="parts"></a>Composants  
 `variableorproperty`  
 Obligatoire. Toute variable ou propriété numérique.  
  
 `expression`  
 Obligatoire. Toute expression numérique.  
  
## <a name="remarks"></a>Notes  
 L’élément sur le côté gauche de la `*=` opérateur peut être une simple variable scalaire, une propriété ou un élément d’un tableau. La variable ou la propriété ne peut pas être [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).  
  
 Le `*=` opérateur multiplie d’abord la valeur de l’expression (sur le côté droit de l’opérateur) par la valeur de la variable ou la propriété (sur le côté gauche de l’opérateur). L’opérateur assigne ensuite le résultat de cette opération à la variable ou la propriété.  
  
## <a name="overloading"></a>Surcharge  
 Le [* opérateur](../../../visual-basic/language-reference/operators/multiplication-operator.md) peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure. La surcharge la `*` opérateur affecte le comportement de la `*=` opérateur. Si votre code utilise `*=` sur une classe ou structure qui surcharge `*`, assurez-vous que vous comprenez son comportement redéfini. Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le `*=` opérateur pour multiplier une `Integer` variable par une autre et assigner le résultat à la première variable.  
  
 [!code-vb[VbVbalrOperators#5](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/multiplication-assignment-operator_1.vb)]  
  
## <a name="see-also"></a>Voir aussi
- [* (opérateur)](../../../visual-basic/language-reference/operators/multiplication-operator.md)
- [Opérateurs d’assignation](../../../visual-basic/language-reference/operators/assignment-operators.md)
- [Opérateurs arithmétiques](../../../visual-basic/language-reference/operators/arithmetic-operators.md)
- [Priorité des opérateurs en Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [Opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [Instructions](../../../visual-basic/programming-guide/language-features/statements.md)
