---
title: -=, opérateur (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.-=
helpviewer_keywords:
- -= operator [Visual Basic]
- assignment statements [Visual Basic], compound
- statements [Visual Basic], compound assignment
- operator -=
- compound assignment statements [Visual Basic]
ms.assetid: 5ead0c37-ae50-48f7-8435-8e341d81cae1
ms.openlocfilehash: c3495c4e45fe5e1d497578ee3ee6afe874e90eed
ms.sourcegitcommit: 41c0637e894fbcd0713d46d6ef1866f08dc321a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/01/2019
ms.locfileid: "57203043"
---
# <a name="--operator-visual-basic"></a>-=, opérateur (Visual Basic)
Soustrait la valeur d’une expression de la valeur d’une propriété ou une variable et assigne le résultat à la variable ou propriété.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
variableorproperty -= expression  
```  
  
## <a name="parts"></a>Composants  
 `variableorproperty`  
 Obligatoire. Toute variable ou propriété numérique.  
  
 `expression`  
 Obligatoire. Toute expression numérique.  
  
## <a name="remarks"></a>Notes  
 L’élément sur le côté gauche de la `-=` opérateur peut être une simple variable scalaire, une propriété ou un élément d’un tableau. La variable ou la propriété ne peut pas être [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).  
  
 Le `-=` opérateur soustrait tout d’abord la valeur de l’expression (sur le côté droit de l’opérateur) à partir de la valeur de la variable ou une propriété (sur le côté gauche de l’opérateur). L’opérateur assigne ensuite le résultat de cette opération à la variable ou la propriété.  
  
## <a name="overloading"></a>Surcharge  
 Le [-, opérateur (Visual Basic)](../../../visual-basic/language-reference/operators/subtraction-operator.md) peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure. La surcharge la `-` opérateur affecte le comportement de la `-=` opérateur. Si votre code utilise `-=` sur une classe ou structure qui surcharge `-`, assurez-vous que vous comprenez son comportement redéfini. Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le `-=` opérateur pour soustraire une `Integer` variable d’une autre et assigner le résultat à la dernière variable.  
  
 [!code-vb[VbVbalrOperators#11](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#11)]  
  
## <a name="see-also"></a>Voir aussi
- [-, Opérateur (Visual Basic)](../../../visual-basic/language-reference/operators/subtraction-operator.md)
- [Opérateurs d’assignation](../../../visual-basic/language-reference/operators/assignment-operators.md)
- [Opérateurs arithmétiques](../../../visual-basic/language-reference/operators/arithmetic-operators.md)
- [Priorité des opérateurs en Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [Opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [Instructions](../../../visual-basic/programming-guide/language-features/statements.md)
