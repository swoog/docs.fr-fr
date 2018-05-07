---
title: 'Comment : appeler une procédure qui ne retourne pas de valeur (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- procedure calls [Visual Basic], returning values
- Visual Basic code, procedures
- procedures [Visual Basic], calling
ms.assetid: 259b49a3-a3c1-4254-ba8c-73cdc4127703
ms.openlocfilehash: cf136f1486645d6e8e4b5856c0b1baf9e99f6c50
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-call-a-procedure-that-does-not-return-a-value-visual-basic"></a>Comment : appeler une procédure qui ne retourne pas de valeur (Visual Basic)
A `Sub` procédure ne retourne pas de valeur au code appelant. Vous appelez explicitement avec une instruction d’appel autonome. Vous ne pouvez pas l’appeler en utilisant simplement son nom dans une expression.  
  
### <a name="to-call-a-sub-procedure"></a>Pour appeler une procédure Sub  
  
1.  Spécifiez le nom de la `Sub` procédure.  
  
2.  Suivez le nom de la procédure avec des parenthèses pour encadrer la liste d’arguments. S’il n’y a pas d’arguments, vous pouvez éventuellement omettre les parenthèses. Toutefois, à l’aide de parenthèses rend votre code plus facile à lire.  
  
3.  Placez les arguments dans la liste d’arguments entre parenthèses, séparées par des virgules. Assurez-vous de fournir les arguments dans le même ordre que les `Sub` procédure définit les paramètres correspondants.  
  
     L’exemple suivant appelle Visual Basic <xref:Microsoft.VisualBasic.Interaction.AppActivate%2A> fonction pour activer une fenêtre d’application. <xref:Microsoft.VisualBasic.Interaction.AppActivate%2A> accepte le titre de la fenêtre comme unique argument. Il ne retourne pas une valeur au code appelant. Si un processus Notepad n’est pas en cours d’exécution, l’exemple lève une <xref:System.ArgumentException>. Le `Shell` procédure suppose que les applications se trouvent dans les chemins d’accès spécifiés.  
  
     [!code-vb[VbVbalrCatRef#11](./codesnippet/VisualBasic/how-to-call-a-procedure-that-does-not-return-a-value_1.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:Microsoft.VisualBasic.Interaction.Shell%2A>  
 <xref:System.ArgumentException>  
 [Procédures](./index.md)  
 [Procédures Sub](./sub-procedures.md)  
 [Paramètres et arguments d’une procédure](./procedure-parameters-and-arguments.md)  
 [Sub (instruction)](../../../../visual-basic/language-reference/statements/sub-statement.md)  
 [Guide pratique : créer une procédure](./how-to-create-a-procedure.md)  
 [Guide pratique : appeler une procédure qui retourne une valeur](./how-to-call-a-procedure-that-returns-a-value.md)  
 [Comment : appeler un gestionnaire d’événements en Visual Basic](./how-to-call-an-event-handler.md)
