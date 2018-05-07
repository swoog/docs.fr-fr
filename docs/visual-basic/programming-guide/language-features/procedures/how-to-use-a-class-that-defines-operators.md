---
title: 'Comment : utiliser une classe qui définit des opérateurs (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- operator procedures [Visual Basic], calling
- procedures [Visual Basic], operator
- procedures [Visual Basic], calling
- examples [Visual Basic], CType
- syntax [Visual Basic], Operator procedures
- operators [Visual Basic], overloading
- return values [Visual Basic], Operator procedures
- operator overloading
ms.assetid: 7ccce94a-6ca0-47d1-9f3f-13385d34f5d5
ms.openlocfilehash: 7e1d5698c1e83f0adf1be67245e0726aecaabdac
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-use-a-class-that-defines-operators-visual-basic"></a>Comment : utiliser une classe qui définit des opérateurs (Visual Basic)
Si vous utilisez une classe ou structure qui définit ses propres opérateurs, vous pouvez accéder à ces opérateurs à partir de Visual Basic.  
  
 Définition d’un opérateur sur une classe ou structure est également appelée *surcharge* l’opérateur.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant accède à la structure SQL <xref:System.Data.SqlTypes.SqlString>, qui définit les opérateurs de conversion ([CType, fonction](../../../../visual-basic/language-reference/functions/ctype-function.md)) dans les deux sens entre une chaîne SQL et une chaîne de Visual Basic. Utilisez `CType(` *expression de chaîne SQL*, `String)` pour convertir une chaîne SQL en une chaîne de Visual Basic, et `CType(` *expression de chaîne Visual Basic*, <xref:System.Data.SqlTypes.SqlString> `)` à convertir dans l’autre direction.  
  
 [!code-vb[VbVbcnProcedures#30](./codesnippet/VisualBasic/how-to-use-a-class-that-defines-operators_1.vb)]  
  
 [!code-vb[VbVbcnProcedures#31](./codesnippet/VisualBasic/how-to-use-a-class-that-defines-operators_2.vb)]  
  
 Le <xref:System.Data.SqlTypes.SqlString> structure définit un opérateur de conversion ([CType, fonction](../../../../visual-basic/language-reference/functions/ctype-function.md)) à partir de `String` à <xref:System.Data.SqlTypes.SqlString> et l’autre à partir de <xref:System.Data.SqlTypes.SqlString> à `String`. L’instruction qui assigne `title` à `jobTitle` utilise le premier opérateur et la <xref:Microsoft.VisualBasic.Interaction.MsgBox%2A> appel de fonction utilise le second.  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Assurez-vous que la classe ou structure que vous utilisez définit l’opérateur que vous souhaitez utiliser. Ne supposez pas que la classe ou structure a défini chaque opérateur disponible pour la surcharge. Pour obtenir la liste des opérateurs disponibles, consultez [Operator, instruction](../../../../visual-basic/language-reference/statements/operator-statement.md).  
  
 Inclure les `Imports` instruction pour la chaîne SQL au début de votre fichier source (dans ce cas <xref:System.Data.SqlTypes>).  
  
 Votre projet doit avoir des références à System.Data et System.XML.  
  
## <a name="see-also"></a>Voir aussi  
 [Procédures d’opérateur](./operator-procedures.md)  
 [Guide pratique : définir un opérateur](./how-to-define-an-operator.md)  
 [Guide pratique : définir un opérateur de conversion](./how-to-define-a-conversion-operator.md)  
 [Guide pratique : appeler une procédure d’opérateur](./how-to-call-an-operator-procedure.md)  
 [Widening](../../../../visual-basic/language-reference/modifiers/widening.md)  
 [Narrowing](../../../../visual-basic/language-reference/modifiers/narrowing.md)  
 [Structure (instruction)](../../../../visual-basic/language-reference/statements/structure-statement.md)  
 [Guide pratique : déclarer une structure](../../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)  
 [Conversions implicites et explicites](../../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)  
 [Conversions étendues et restrictives](../../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
