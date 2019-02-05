---
title: 'Procédure : Définir un opérateur (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], defining
- Visual Basic code, procedures
- operators [Visual Basic], defining
- procedures [Visual Basic], operator
- Visual Basic code, operators
- syntax [Visual Basic], Operator procedures
- operators [Visual Basic], overloading
- operator procedures [Visual Basic], about operator procedures
- return values [Visual Basic], Operator procedures
- operator overloading
ms.assetid: d4b0e253-092a-4e6e-9fe2-01f562140a29
ms.openlocfilehash: 6ced9e2ab71ccb00c9ce3495e38d895a7104fdde
ms.sourcegitcommit: facefcacd7ae2e5645e463bc841df213c505ffd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2019
ms.locfileid: "55738654"
---
# <a name="how-to-define-an-operator-visual-basic"></a>Procédure : Définir un opérateur (Visual Basic)
Si vous avez défini une classe ou structure, vous pouvez définir le comportement d’un opérateur standard (tel que `*`, `<>`, ou `And`) lorsqu’au moins des opérandes est du type de votre classe ou structure.  
  
 Définissez l’opérateur standard comme une procédure d’opérateur dans la classe ou structure. Toutes les procédures d’opérateur doivent être `Public` `Shared`.  
  
 Définition d’un opérateur sur une classe ou structure est également appelée *surcharge* l’opérateur.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant définit la `+` opérateur pour une structure appelée `height`. La structure utilise des hauteurs mesurées en mètres et de centimètres. Un *pouce* est 2,54 centimètres et l’autre *foot* est de 12 pouces. Pour garantir des valeurs normalisées (pouces < 12.0), le constructeur effectue *modulo* 12 arithmétique. Le `+` opérateur utilise le constructeur pour générer des valeurs normalisées.  
  
 [!code-vb[VbVbcnProcedures#25](./codesnippet/VisualBasic/how-to-define-an-operator_1.vb)]  
  
 Vous pouvez tester la structure `height` par le code suivant.  
  
 [!code-vb[VbVbcnProcedures#26](./codesnippet/VisualBasic/how-to-define-an-operator_2.vb)]  
  
  
## <a name="see-also"></a>Voir aussi
- [Procédures d’opérateur](./operator-procedures.md)
- [Guide pratique pour Définir un opérateur de Conversion](./how-to-define-a-conversion-operator.md)
- [Guide pratique pour Appeler une procédure d’opérateur](./how-to-call-an-operator-procedure.md)
- [Guide pratique pour Utiliser une classe qui définit des opérateurs](./how-to-use-a-class-that-defines-operators.md)
- [Operator (instruction)](../../../../visual-basic/language-reference/statements/operator-statement.md)
- [Structure (instruction)](../../../../visual-basic/language-reference/statements/structure-statement.md)
- [Guide pratique pour déclarer une structure](../../../../visual-basic/programming-guide/language-features/data-types/how-to-declare-a-structure.md)
- [Mod (opérateur)](../../../../visual-basic/language-reference/operators/mod-operator.md)
