---
title: << =, opérateur (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.<<=
helpviewer_keywords:
- operator <<=
- assignment statements [Visual Basic], compound
- <<= operator [Visual Basic]
- statements [Visual Basic], compound assignment
- operator<<=
- compound assignment statements [Visual Basic]
ms.assetid: 8ad26613-faff-4e2f-89ee-63feee33bfda
ms.openlocfilehash: da2b5ca0b7538d77c3c8d8bc7d45712d656ce63a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61768314"
---
# <a name="-operator-visual-basic"></a>\<\<=, Opérateur (Visual Basic)
Effectue un décalage arithmétique vers la gauche sur la valeur d’une propriété ou une variable et assigne le résultat à la variable ou propriété.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
variableorproperty <<= amount  
```  
  
## <a name="parts"></a>Composants  
 `variableorproperty`  
 Obligatoire. Variable ou propriété d’un type intégral (`SByte`, `Byte`, `Short`, `UShort`, `Integer`, `UInteger`, `Long`, ou `ULong`).  
  
 `amount`  
 Obligatoire. Expression numérique d’un type de données qui s’étend à `Integer`.  
  
## <a name="remarks"></a>Notes  
 L’élément sur le côté gauche de la `<<=` opérateur peut être une simple variable scalaire, une propriété ou un élément d’un tableau. La variable ou la propriété ne peut pas être [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).  
  
 Le `<<=` opérateur effectue d’abord un décalage arithmétique vers la gauche sur la valeur de la variable ou propriété. Puis, l’opérateur assigne le résultat de cette opération à cette variable ou une propriété.  
  
 Les décalages arithmétiques ne sont pas circulaires, ce qui signifie que les bits décalés à une extrémité du résultat ne sont pas réintroduits à l’autre extrémité. Dans un décalage arithmétique vers la gauche, les bits décalés au-delà de la plage du type de données de résultat sont ignorés, et les positions binaires libérées à droite sont définies à zéro.  
  
## <a name="overloading"></a>Surcharge  
 Le [<< opérateur](../../../visual-basic/language-reference/operators/left-shift-operator.md) peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure. La surcharge la `<<` opérateur affecte le comportement de la `<<=` opérateur. Si votre code utilise `<<=` sur une classe ou structure qui surcharge `<<`, assurez-vous que vous comprenez son comportement redéfini. Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le `<<=` opérateur pour décaler le modèle binaire d’une `Integer` variable laissé par la quantité spécifiée et assigner le résultat à la variable.  
  
 [!code-vb[VbVbalrOperators#13](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#13)]  
  
## <a name="see-also"></a>Voir aussi

- [<< (opérateur)](../../../visual-basic/language-reference/operators/left-shift-operator.md)
- [Opérateurs d’assignation](../../../visual-basic/language-reference/operators/assignment-operators.md)
- [Opérateurs de décalage de bits](../../../visual-basic/language-reference/operators/bit-shift-operators.md)
- [Priorité des opérateurs en Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [Opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [Instructions](../../../visual-basic/programming-guide/language-features/statements.md)
