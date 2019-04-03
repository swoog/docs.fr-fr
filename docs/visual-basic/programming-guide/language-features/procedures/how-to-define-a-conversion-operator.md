---
title: 'Procédure : Définir un opérateur de Conversion (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], defining
- operators [Visual Basic], defining
- procedures [Visual Basic], operator
- operators [Visual Basic], overloading
- return values [Visual Basic], Operator procedures
- operator overloading
ms.assetid: 54203dfa-c24b-463f-9942-d5153e89e762
ms.openlocfilehash: cf7bfdd09c7f3429f9c730a7aec34b24af3f2e9f
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58829224"
---
# <a name="how-to-define-a-conversion-operator-visual-basic"></a>Procédure : Définir un opérateur de Conversion (Visual Basic)
Si vous avez défini une classe ou structure, vous pouvez définir un opérateur de conversion de type entre le type de votre classe ou une structure et un autre type de données (tel que `Integer`, `Double`, ou `String`).  
  
 Définir la conversion de type comme un [CType Function](../../../../visual-basic/language-reference/functions/ctype-function.md) procédure au sein de la classe ou structure. Toutes les procédures de conversion doivent être `Public Shared`, et chacune d’elles doit spécifier [Widening](../../../../visual-basic/language-reference/modifiers/widening.md) ou [Narrowing](../../../../visual-basic/language-reference/modifiers/narrowing.md).  
  
 Définition d’un opérateur sur une classe ou structure est également appelée *surcharge* l’opérateur.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant définit les opérateurs de conversion entre une structure appelée `digit` et un `Byte`.  
  
 [!code-vb[VbVbcnProcedures#27](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#27)]  
  
 Vous pouvez tester la structure `digit` par le code suivant.  
  
 [!code-vb[VbVbcnProcedures#28](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#28)]  
  
## <a name="see-also"></a>Voir aussi

- [Procédures d’opérateur](./operator-procedures.md)
- [Guide pratique pour Définir un opérateur](./how-to-define-an-operator.md)
- [Guide pratique pour Appeler une procédure d’opérateur](./how-to-call-an-operator-procedure.md)
- [Guide pratique pour Utiliser une classe qui définit des opérateurs](./how-to-use-a-class-that-defines-operators.md)
- [Operator (instruction)](../../../../visual-basic/language-reference/statements/operator-statement.md)
- [Structure (instruction)](../../../../visual-basic/language-reference/statements/structure-statement.md)
- [Guide pratique pour déclarer une structure](../../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)
- [Conversions implicites et explicites](../../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)
- [Conversions étendues et restrictives](../../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
