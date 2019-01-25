---
title: 'Procédure : Appeler une procédure d’opérateur (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- operator procedures [Visual Basic], calling
- procedures [Visual Basic], operator
- procedure calls [Visual Basic], operator overloading
- syntax [Visual Basic], Operator procedures
- operators [Visual Basic], overloading
- return values [Visual Basic], Operator procedures
- overloaded operators [Visual Basic], calling
- operator overloading
ms.assetid: 0dce42cc-f0b0-4c14-9f62-018b21f33497
ms.openlocfilehash: fc658dd7ef001c8d3ef7761bd2a7889f70e9e4a3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54667581"
---
# <a name="how-to-call-an-operator-procedure-visual-basic"></a>Procédure : Appeler une procédure d’opérateur (Visual Basic)
Vous appelez une procédure d’opérateur en utilisant le symbole d’opérateur dans une expression. Dans le cas d’un opérateur de conversion, vous appelez le [CType Function](../../../../visual-basic/language-reference/functions/ctype-function.md) pour convertir une valeur à partir d’un type de données à un autre.  
  
 Vous n’appelez pas explicitement de procédures d’opérateur. Vous utilisez l’opérateur, ou la `CType` fonction dans une instruction d’assignation ou une expression, la même façon que vous utilisez normalement un opérateur. Visual Basic effectue l’appel à la procédure d’opérateur.  
  
 Définition d’un opérateur sur une classe ou structure est également appelée *surcharge* l’opérateur.  
  
### <a name="to-call-an-operator-procedure"></a>Pour appeler une procédure d’opérateur  
  
1.  Utilisez le symbole d’opérateur dans une expression de la façon habituelle.  
  
2.  N’oubliez pas que les types de données des opérandes sont appropriés pour l’opérateur et dans le bon ordre.  
  
3.  L’opérateur contribue à la valeur de l’expression comme prévu.  
  
### <a name="to-call-a-conversion-operator-procedure"></a>Pour appeler une procédure d’opérateur de conversion  
  
1.  Utilisez `CType` à l’intérieur d’une expression.  
  
2.  N’oubliez pas que les types de données des opérandes sont appropriés pour la conversion et dans le bon ordre.  
  
3.  `CType` appelle la procédure d’opérateur de conversion et retourne la valeur convertie.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée deux <xref:System.TimeSpan> structures, les additionne et stocke le résultat dans une troisième <xref:System.TimeSpan> structure. Le <xref:System.TimeSpan> structure définit des procédures d’opérateur pour surcharger plusieurs opérateurs standards.  
  
 [!code-vb[VbVbcnProcedures#29](./codesnippet/VisualBasic/how-to-call-an-operator-procedure_1.vb)]  
  
 Étant donné que <xref:System.TimeSpan> surcharges de la norme `+` opérateur, l’exemple précédent appelle une procédure d’opérateur lorsqu’il calcule la valeur de `combinedSpan`.  
  
 Pour obtenir un exemple d’appel de procédure d’opérateur de conversation, consultez [Comment : Utiliser une classe qui définit des opérateurs](./how-to-use-a-class-that-defines-operators.md).  
  
## <a name="compiling-the-code"></a>Compilation du code  
 N’oubliez pas de la classe ou structure que vous utilisez définit l’opérateur que vous souhaitez utiliser.  
  
## <a name="see-also"></a>Voir aussi
- [Procédures d’opérateur](./operator-procedures.md)
- [Guide pratique pour Définir un opérateur](./how-to-define-an-operator.md)
- [Guide pratique pour Définir un opérateur de Conversion](./how-to-define-a-conversion-operator.md)
- [Operator (instruction)](../../../../visual-basic/language-reference/statements/operator-statement.md)
- [Widening](../../../../visual-basic/language-reference/modifiers/widening.md)
- [Narrowing](../../../../visual-basic/language-reference/modifiers/narrowing.md)
- [Structure (instruction)](../../../../visual-basic/language-reference/statements/structure-statement.md)
- [Guide pratique pour déclarer une structure](../../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)
- [Conversions implicites et explicites](../../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)
- [Conversions étendues et restrictives](../../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
