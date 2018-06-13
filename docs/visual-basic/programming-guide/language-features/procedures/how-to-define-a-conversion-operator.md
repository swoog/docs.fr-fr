---
title: 'Comment : définir un opérateur de conversion (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], defining
- operators [Visual Basic], defining
- procedures [Visual Basic], operator
- operators [Visual Basic], overloading
- return values [Visual Basic], Operator procedures
- operator overloading
ms.assetid: 54203dfa-c24b-463f-9942-d5153e89e762
ms.openlocfilehash: 24bbe41af67f757cae661a78d482a423ff0ffd85
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33648471"
---
# <a name="how-to-define-a-conversion-operator-visual-basic"></a>Comment : définir un opérateur de conversion (Visual Basic)
Si vous avez défini une classe ou structure, vous pouvez définir un opérateur de conversion de type entre le type de votre classe ou structure et un autre type de données (tel que `Integer`, `Double`, ou `String`).  
  
 Définir la conversion de type comme un [CType, fonction](../../../../visual-basic/language-reference/functions/ctype-function.md) procédure au sein de la classe ou structure. Toutes les procédures de conversion doivent être `Public Shared`, et chacune d’elles doit spécifier [Widening](../../../../visual-basic/language-reference/modifiers/widening.md) ou [Narrowing](../../../../visual-basic/language-reference/modifiers/narrowing.md).  
  
 Définition d’un opérateur sur une classe ou structure est également appelée *surcharge* l’opérateur.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant définit les opérateurs de conversion entre une structure appelée `digit` et un `Byte`.  
  
 [!code-vb[VbVbcnProcedures#27](./codesnippet/VisualBasic/how-to-define-a-conversion-operator_1.vb)]  
  
 Vous pouvez tester la structure `digit` par le code suivant.  
  
 [!code-vb[VbVbcnProcedures#28](./codesnippet/VisualBasic/how-to-define-a-conversion-operator_2.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 [Procédures d’opérateur](./operator-procedures.md)  
 [Guide pratique : définir un opérateur](./how-to-define-an-operator.md)  
 [Guide pratique : appeler une procédure d’opérateur](./how-to-call-an-operator-procedure.md)  
 [Guide pratique : utiliser une classe qui définit des opérateurs](./how-to-use-a-class-that-defines-operators.md)  
 [Operator (instruction)](../../../../visual-basic/language-reference/statements/operator-statement.md)  
 [Structure (instruction)](../../../../visual-basic/language-reference/statements/structure-statement.md)  
 [Guide pratique : déclarer une structure](../../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)  
 [Conversions implicites et explicites](../../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)  
 [Conversions étendues et restrictives](../../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
