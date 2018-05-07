---
title: "Comment : déclarer une propriété avec des niveaux d'accès mixtes (Visual Basic)"
ms.date: 07/20/2015
helpviewer_keywords:
- access levels [Visual Basic], properties
- procedures [Visual Basic], defining
- Visual Basic code, procedures
- mixed access levels
- Visual Basic code, properties
- properties [Visual Basic], access levels
- Property statement [Visual Basic], declaring mixed access levels
ms.assetid: fdbb2d97-279a-4956-b26c-cbdfbc34915a
ms.openlocfilehash: 8d25086fe6f8b5f5300006466ef49782cb065edf
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-declare-a-property-with-mixed-access-levels-visual-basic"></a>Comment : déclarer une propriété avec des niveaux d'accès mixtes (Visual Basic)
Si vous souhaitez que le `Get` et `Set` procédures d’une propriété d’avoir différents niveaux d’accès, vous pouvez utiliser le niveau le plus permissif dans le `Property` instruction et le niveau le plus restrictif, que ce soit le `Get` ou `Set` instruction. Vous utilisez des niveaux d’accès mixtes sur une propriété lorsque vous souhaitez que certaines parties du code pour être en mesure d’obtenir la valeur de propriété et que d’autres parties du code pour être en mesure de modifier la valeur.  
  
 Pour plus d’informations sur les niveaux d’accès, consultez [niveaux en Visual Basic d’accès](../../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).  
  
### <a name="to-declare-a-property-with-mixed-access-levels"></a>Pour déclarer une propriété avec des niveaux d’accès mixtes  
  
1.  Déclarez la propriété de façon normale et spécifier le niveau d’accès moins restrictif (tel que `Public`) dans le `Property` instruction.  
  
2.  Déclarez le `Get` ou le `Set` procédure en spécifiant le niveau d’accès plus restrictif (tels que `Friend`).  
  
3.  Ne spécifiez pas un niveau d’accès sur les autres procédures de propriété. Il suppose que le niveau d’accès déclaré dans la `Property` instruction. Vous pouvez restreindre l’accès sur un seul des procédures de propriété.  
  
     [!code-vb[VbVbcnProcedures#10](./codesnippet/VisualBasic/how-to-declare-a-property-with-mixed-access-levels_1.vb)]  
  
     Dans l’exemple précédent, le `Get` procédure a le même `Protected` accès en tant que la propriété elle-même, alors que le `Set` procédure a `Private` accès. Une classe dérivée de `employee` peut lire le `salary` valeur, mais uniquement la `employee` classe peut le définir.  
  
## <a name="see-also"></a>Voir aussi  
 [Procédures](./index.md)  
 [Procédures de propriété](./property-procedures.md)  
 [Paramètres et arguments d’une procédure](./procedure-parameters-and-arguments.md)  
 [Property (instruction)](../../../../visual-basic/language-reference/statements/property-statement.md)  
 [Différences entre les propriétés et les Variables en Visual Basic](./differences-between-properties-and-variables.md)  
 [Guide pratique : créer une propriété](./how-to-create-a-property.md)  
 [Guide pratique : appeler une procédure de propriété](./how-to-call-a-property-procedure.md)  
 [Comment : déclarer et appeler une propriété par défaut en Visual Basic](./how-to-declare-and-call-a-default-property.md)  
 [Guide pratique : placer une valeur dans une propriété](./how-to-put-a-value-in-a-property.md)  
 [Guide pratique : obtenir une valeur d’une propriété](./how-to-get-a-value-from-a-property.md)
