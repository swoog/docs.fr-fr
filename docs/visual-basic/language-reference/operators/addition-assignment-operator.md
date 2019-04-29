---
title: += (opérateur Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.+=
helpviewer_keywords:
- += operator [Visual Basic]
- assignment statements [Visual Basic], compound
- statements [Visual Basic], compound assignment
- += operator [Visual Basic], appending strings
- compound assignment statements [Visual Basic]
ms.assetid: d3e959f4-85d4-4e47-87c4-77b62335a5b3
ms.openlocfilehash: 4b8f36397d0f52866ebe9fa188d6b163364aeffc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61608331"
---
# <a name="-operator-visual-basic"></a>+= (opérateur Visual Basic)
Ajoute la valeur d’une expression numérique à la valeur d’une propriété ou une variable numérique et assigne le résultat à la variable ou propriété. Peut également être utilisé pour concaténer une `String` expression à une `String` variable ou propriété et assigner le résultat à la variable ou propriété.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
variableorproperty += expression  
```  
  
## <a name="parts"></a>Composants  
 `variableorproperty`  
 Obligatoire. Toute numérique ou `String` variable ou propriété.  
  
 `expression`  
 Obligatoire. Toute numérique ou `String` expression.  
  
## <a name="remarks"></a>Notes  
 L’élément sur le côté gauche de la `+=` opérateur peut être une simple variable scalaire, une propriété ou un élément d’un tableau. La variable ou la propriété ne peut pas être [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).  
  
 Le `+=` opérateur ajoute la valeur située à droite vers la variable ou propriété du côté gauche et assigne le résultat à la variable ou la propriété situé à sa gauche. Le `+=` opérateur peut également être utilisé pour concaténer les `String` expression située à droite vers le `String` variable ou une propriété sur la gauche et assigner le résultat à la variable ou propriété du côté gauche.  
  
> [!NOTE]
>  Lorsque vous utilisez le `+=` opérateur, vous ne pourrez pas être en mesure de déterminer si la concaténation d’addition ou la chaîne aura lieu. Utilisez le `&=` opérateur de concaténation pour éliminer toute ambiguïté et pour fournir le code auto-documenté.  
  
 Cet opérateur d’assignation effectue implicitement étendues, mais ne pas les conversions restrictives si l’environnement de compilation applique une sémantique stricte. Pour plus d’informations sur ces conversions, consultez [Widening and Narrowing Conversions](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md). Pour plus d’informations sur les sémantiques strictes et permissives, consultez [Option Strict, instruction](../../../visual-basic/language-reference/statements/option-strict-statement.md).  
  
 Si la sémantique permissive est autorisée, le `+=` opérateur exécute implicitement un ensemble de conversions de chaîne et numériques identiques à ceux effectués par le `+` opérateur. Pour plus d’informations sur ces conversions, consultez [opérateur +](../../../visual-basic/language-reference/operators/addition-operator.md).  
  
## <a name="overloading"></a>Surcharge  
 Le `+` opérateur peut être *surchargé*, ce qui signifie qu’une classe ou structure peut redéfinir son comportement lorsqu’un opérande a le type de cette classe ou structure. La surcharge la `+` opérateur affecte le comportement de la `+=` opérateur. Si votre code utilise `+=` sur une classe ou structure qui surcharge `+`, assurez-vous que vous comprenez son comportement redéfini. Pour plus d'informations, consultez [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le `+=` opérateur pour combiner la valeur d’une variable avec un autre. La première partie utilise `+=` avec des variables numériques pour ajouter une valeur à un autre. La deuxième partie utilise `+=` avec `String` variables pour concaténer une valeur avec un autre. Dans les deux cas, le résultat est assigné à la première variable.  
  
 [!code-vb[VbVbalrOperators#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#7)]  
  
 [!code-vb[VbVbalrOperators#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#8)]  
  
 La valeur de `num1` est maintenant 13 et la valeur de `str1` est désormais « 103 ».  
  
## <a name="see-also"></a>Voir aussi

- [+, opérateur](../../../visual-basic/language-reference/operators/addition-operator.md)
- [Opérateurs d’assignation](../../../visual-basic/language-reference/operators/assignment-operators.md)
- [Opérateurs arithmétiques](../../../visual-basic/language-reference/operators/arithmetic-operators.md)
- [opérateur de concaténation](../../../visual-basic/language-reference/operators/concatenation-operators.md)
- [Priorité des opérateurs en Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [Opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [Instructions](../../../visual-basic/programming-guide/language-features/statements.md)
