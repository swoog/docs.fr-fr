---
title: 'Procédure : Placer une valeur dans une propriété (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- property values [Visual Basic]
- Visual Basic code, procedures
- values [Visual Basic], properties
- Visual Basic code, properties
- properties [Visual Basic], values
ms.assetid: c39401e5-b5fc-4439-8f31-ed640f7ce6ed
ms.openlocfilehash: 34348d57db0875d9c2c6192ac754b4f83f515ac4
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56965461"
---
# <a name="how-to-put-a-value-in-a-property-visual-basic"></a>Procédure : Placer une valeur dans une propriété (Visual Basic)
Vous stockez une valeur dans une propriété en plaçant le nom de propriété sur le côté gauche d’une instruction d’assignation.  
  
 La propriété `Set` stocke une valeur, mais vous ne l’appelez pas explicitement par son nom. Vous utilisez la propriété tout comme vous utiliseriez une variable. Visual Basic effectue les appels à des procédures de la propriété.  
  
### <a name="to-store-a-value-in-a-property"></a>Pour stocker une valeur dans une propriété  
  
1.  Utilisez le nom de propriété sur le côté gauche d’une instruction d’assignation.  
  
     L’exemple suivant définit la valeur de Visual Basic `TimeOfDay` propriété à midi, en appelant implicitement sa `Set` procédure.  
  
     [!code-vb[VbVbcnProcedures#11](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#11)]  
  
2.  Si la propriété prend des arguments, faites suivre le nom de propriété entre parenthèses pour encadrer la liste d’arguments. S’il n’y a aucun argument, vous pouvez éventuellement omettre les parenthèses.  
  
3.  Placez les arguments dans la liste d’arguments entre parenthèses, séparées par des virgules. Veillez à que vous fournir les arguments dans le même ordre que la propriété définit les paramètres correspondants.  
  
4.  La valeur générée sur le côté droit de l’instruction d’assignation est stockée dans la propriété.  
  
## <a name="see-also"></a>Voir aussi
- <xref:Microsoft.VisualBasic.DateAndTime.TimeOfDay%2A>
- [Procédures de propriété](./property-procedures.md)
- [Paramètres et arguments d’une procédure](./procedure-parameters-and-arguments.md)
- [Property (instruction)](../../../../visual-basic/language-reference/statements/property-statement.md)
- [Différences entre les propriétés et les Variables en Visual Basic](./differences-between-properties-and-variables.md)
- [Guide pratique pour Créer une propriété](./how-to-create-a-property.md)
- [Guide pratique pour Déclarer une propriété avec des niveaux d’accès mixtes](./how-to-declare-a-property-with-mixed-access-levels.md)
- [Guide pratique pour Appeler une procédure de propriété](./how-to-call-a-property-procedure.md)
- [Guide pratique pour Déclarer et appeler une propriété par défaut en Visual Basic](./how-to-declare-and-call-a-default-property.md)
- [Guide pratique pour Obtenir une valeur d’une propriété](./how-to-get-a-value-from-a-property.md)
