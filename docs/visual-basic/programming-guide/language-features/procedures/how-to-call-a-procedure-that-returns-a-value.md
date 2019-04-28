---
title: 'Procédure : Appeler une procédure qui retourne une valeur (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- procedure calls [Visual Basic], returning values
- Visual Basic code, procedures
- procedures [Visual Basic], calling
- procedures [Visual Basic], returning a value
ms.assetid: a445127b-0f5f-465a-98fb-3e514b93d115
ms.openlocfilehash: 6f45f01489ee84b6addb1f7c7c8dc584332f38dd
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61864180"
---
# <a name="how-to-call-a-procedure-that-returns-a-value-visual-basic"></a>Procédure : Appeler une procédure qui retourne une valeur (Visual Basic)
Un `Function` procédure retourne une valeur au code appelant. Vous appelez en incluant son nom et ses arguments soit situé à droite d’une instruction d’assignation ou dans une expression.  
  
### <a name="to-call-a-function-procedure-within-an-expression"></a>Pour appeler une procédure de fonction dans une expression  
  
1. Utiliser le `Function` la même façon que vous utiliseriez une variable de nom de la procédure. Vous pouvez utiliser un `Function` partout où vous pouvez utiliser une variable ou une constante dans une expression d’appel de procédure.  
  
2. Faites suivre le nom de procédure avec des parenthèses pour encadrer la liste d’arguments. S’il n’y a aucun argument, vous pouvez éventuellement omettre les parenthèses. Toutefois, à l’aide de parenthèses rend votre code plus facile à lire.  
  
3. Placez les arguments dans la liste d’arguments entre parenthèses, séparées par des virgules. Veillez à vous fournir les arguments dans le même ordre que les `Function` procédure définit les paramètres correspondants.  
  
     Vous pouvez également transmettre un ou plusieurs arguments par nom. Pour plus d’informations, consultez [en passant les Arguments par Position et par nom](./passing-arguments-by-position-and-by-name.md).  
  
4. La valeur retournée par la procédure participe à l’expression comme la valeur d’une variable ou constante le ferait.  
  
### <a name="to-call-a-function-procedure-in-an-assignment-statement"></a>Pour appeler une procédure de fonction dans une instruction d’assignation  
  
1. Utilisez le `Function` nom de procédure suivant égaux (`=`) connectez-vous à l’instruction d’assignation.  
  
2. Faites suivre le nom de procédure avec des parenthèses pour encadrer la liste d’arguments. S’il n’y a aucun argument, vous pouvez éventuellement omettre les parenthèses. Toutefois, à l’aide de parenthèses rend votre code plus facile à lire.  
  
3. Placez les arguments dans la liste d’arguments entre parenthèses, séparées par des virgules. Veillez à vous fournir les arguments dans le même ordre que les `Function` procédure définit les paramètres correspondants, sauf si vous les transmettez par nom.  
  
4. La valeur retournée par la procédure est stockée dans la variable ou la propriété sur le côté gauche de l’instruction d’assignation.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant appelle le Visual Basic <xref:Microsoft.VisualBasic.Interaction.Environ%2A> pour récupérer la valeur de variable d’environnement de système d’exploitation. La première ligne appelle `Environ` au sein d’une expression et la deuxième ligne l’appelle dans une instruction d’assignation. `Environ` prend le nom de variable comme unique argument. Elle retourne la valeur de la variable au code appelant.  
  
 [!code-vb[VbVbcnProcedures#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#7)]  
  
## <a name="see-also"></a>Voir aussi

- [Procédures Function](./function-procedures.md)
- [Paramètres et arguments d’une procédure](./procedure-parameters-and-arguments.md)
- [Function (instruction)](../../../../visual-basic/language-reference/statements/function-statement.md)
- [Guide pratique pour Créer une procédure qui retourne une valeur](./how-to-create-a-procedure-that-returns-a-value.md)
- [Guide pratique pour Retourner une valeur à partir d’une procédure](./how-to-return-a-value-from-a-procedure.md)
- [Guide pratique pour Appeler une procédure qui ne retourne pas de valeur](./how-to-call-a-procedure-that-does-not-return-a-value.md)
