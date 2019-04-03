---
title: ^=, opérateur (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.^=
helpviewer_keywords:
- assignment statements [Visual Basic], compound
- statements [Visual Basic], compound assignment
- ^= operator [Visual Basic]
- compound assignment statements [Visual Basic]
ms.assetid: 397da132-2d96-4a85-a7bc-f7c730a608c9
ms.openlocfilehash: fe5d7b3dcb55192167512e0934e09cff7dfddb6d
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58819648"
---
# <a name="-operator-visual-basic"></a>^=, opérateur (Visual Basic)
Élève la valeur d’une variable ou une propriété à la puissance d’une expression et assigne le résultat à la variable ou propriété.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
variableorproperty ^= expression  
```  
  
## <a name="parts"></a>Composants  
 `variableorproperty`  
 Obligatoire. Toute variable ou propriété numérique.  
  
 `expression`  
 Obligatoire. Toute expression numérique.  
  
## <a name="remarks"></a>Notes  
 L’élément sur le côté gauche de la `^=` opérateur peut être une simple variable scalaire, une propriété ou un élément d’un tableau. La variable ou la propriété ne peut pas être [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).  
  
 Le `^=` opérateur déclenche tout d’abord la valeur de la variable ou une propriété (sur le côté gauche de l’opérateur) à la puissance de la valeur de l’expression (sur le côté droit de l’opérateur). Puis, l’opérateur assigne le résultat de cette opération à la variable ou propriété.  
  
 Visual Basic exécute toujours l’élévation à la puissance dans le [Type de données Double](../../../visual-basic/language-reference/data-types/double-data-type.md). Opérandes de tous types sont convertis en `Double`, et le résultat est toujours `Double`.  
  
 La valeur de `expression` peut être fractionnaire, négative ou les deux.  
  
## <a name="overloading"></a>Surcharge  
 Le [^ opérateur](../../../visual-basic/language-reference/operators/exponentiation-operator.md) peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure. La surcharge la `^` opérateur affecte le comportement de la `^=` opérateur. Si votre code utilise `^=` sur une classe ou structure qui surcharge `^`, assurez-vous que vous comprenez son comportement redéfini. Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le `^=` opérateur pour déclencher la valeur d’un `Integer` variable à la puissance d’une deuxième variable et assigner le résultat à la première variable.  
  
 [!code-vb[VbVbalrOperators#21](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#21)]  
  
## <a name="see-also"></a>Voir aussi

- [^ (opérateur)](../../../visual-basic/language-reference/operators/exponentiation-operator.md)
- [Opérateurs d’assignation](../../../visual-basic/language-reference/operators/assignment-operators.md)
- [Opérateurs arithmétiques](../../../visual-basic/language-reference/operators/arithmetic-operators.md)
- [Priorité des opérateurs en Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [Opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [Instructions](../../../visual-basic/programming-guide/language-features/statements.md)
