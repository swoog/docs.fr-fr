---
title: 'Comment : placer une valeur dans une propriété (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- property values [Visual Basic]
- Visual Basic code, procedures
- values [Visual Basic], properties
- Visual Basic code, properties
- properties [Visual Basic], values
ms.assetid: c39401e5-b5fc-4439-8f31-ed640f7ce6ed
ms.openlocfilehash: 29e68ca2b9436921c81346eb1def2417157aae9c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-put-a-value-in-a-property-visual-basic"></a>Comment : placer une valeur dans une propriété (Visual Basic)
Vous stockez une valeur dans une propriété en plaçant le nom de propriété sur le côté gauche d’une instruction d’assignation.  
  
 La propriété `Set` stocke une valeur, mais vous ne l’appelez pas explicitement par son nom. Vous utilisez la propriété comme vous utiliseriez une variable. Visual Basic effectue les appels aux procédures de la propriété.  
  
### <a name="to-store-a-value-in-a-property"></a>Pour stocker une valeur dans une propriété  
  
1.  Utilisez le nom de propriété sur le côté gauche d’une instruction d’assignation.  
  
     L’exemple suivant définit la valeur de Visual Basic `TimeOfDay` propriété à midi, en appelant implicitement sa `Set` procédure.  
  
     [!code-vb[VbVbcnProcedures#11](./codesnippet/VisualBasic/how-to-put-a-value-in-a-property_1.vb)]  
  
2.  Si la propriété accepte des arguments, faites suivre le nom de propriété avec des parenthèses pour encadrer la liste d’arguments. S’il n’y a pas d’arguments, vous pouvez éventuellement omettre les parenthèses.  
  
3.  Placez les arguments dans la liste d’arguments entre parenthèses, séparées par des virgules. Assurez-vous de que fournir les arguments dans le même ordre que la propriété définit les paramètres correspondants.  
  
4.  La valeur générée sur le côté droit de l’instruction d’assignation est stockée dans la propriété.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:Microsoft.VisualBasic.DateAndTime.TimeOfDay%2A>  
 [Procédures de propriété](./property-procedures.md)  
 [Paramètres et arguments d’une procédure](./procedure-parameters-and-arguments.md)  
 [Property (instruction)](../../../../visual-basic/language-reference/statements/property-statement.md)  
 [Différences entre les propriétés et les Variables en Visual Basic](./differences-between-properties-and-variables.md)  
 [Guide pratique : créer une propriété](./how-to-create-a-property.md)  
 [Guide pratique : déclarer une propriété avec des niveaux d’accès mixtes](./how-to-declare-a-property-with-mixed-access-levels.md)  
 [Guide pratique : appeler une procédure de propriété](./how-to-call-a-property-procedure.md)  
 [Comment : déclarer et appeler une propriété par défaut en Visual Basic](./how-to-declare-and-call-a-default-property.md)  
 [Guide pratique : obtenir une valeur d’une propriété](./how-to-get-a-value-from-a-property.md)
