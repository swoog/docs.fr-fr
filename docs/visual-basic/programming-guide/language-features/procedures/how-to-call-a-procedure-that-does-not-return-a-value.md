---
title: 'Procédure : Appeler une procédure qui ne retourne pas une valeur (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- procedure calls [Visual Basic], returning values
- Visual Basic code, procedures
- procedures [Visual Basic], calling
ms.assetid: 259b49a3-a3c1-4254-ba8c-73cdc4127703
ms.openlocfilehash: 6e3ce2a184ca5411a6a016929a16bf3d67e669ca
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59335470"
---
# <a name="how-to-call-a-procedure-that-does-not-return-a-value-visual-basic"></a>Procédure : Appeler une procédure qui ne retourne pas une valeur (Visual Basic)
Un `Sub` procédure ne retourne pas de valeur au code appelant. Vous l’appelez explicitement avec une instruction d’appel autonome. Vous ne pouvez pas l’appeler en utilisant simplement son nom dans une expression.  
  
### <a name="to-call-a-sub-procedure"></a>Pour appeler une procédure Sub  
  
1. Spécifiez le nom de la `Sub` procédure.  
  
2. Faites suivre le nom de procédure avec des parenthèses pour encadrer la liste d’arguments. S’il n’y a aucun argument, vous pouvez éventuellement omettre les parenthèses. Toutefois, à l’aide de parenthèses rend votre code plus facile à lire.  
  
3. Placez les arguments dans la liste d’arguments entre parenthèses, séparées par des virgules. Veillez à vous fournir les arguments dans le même ordre que les `Sub` procédure définit les paramètres correspondants.  
  
     L’exemple suivant appelle le Visual Basic <xref:Microsoft.VisualBasic.Interaction.AppActivate%2A> fonction pour activer une fenêtre d’application. <xref:Microsoft.VisualBasic.Interaction.AppActivate%2A> accepte le titre de fenêtre comme unique argument. Il ne retourne pas une valeur au code appelant. Si un processus Notepad n’est pas en cours d’exécution, l’exemple lève une <xref:System.ArgumentException>. Le `Shell` procédure suppose que les applications sont dans les chemins d’accès spécifiés.  
  
     [!code-vb[VbVbalrCatRef#11](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrCatRef/VB/Class1.vb#11)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.Interaction.Shell%2A>
- <xref:System.ArgumentException>
- [Procédures](./index.md)
- [Procédures Sub](./sub-procedures.md)
- [Paramètres et arguments d’une procédure](./procedure-parameters-and-arguments.md)
- [Sub, instruction](../../../../visual-basic/language-reference/statements/sub-statement.md)
- [Procédure : créer une procédure](./how-to-create-a-procedure.md)
- [Procédure : appeler une procédure qui retourne une valeur](./how-to-call-a-procedure-that-returns-a-value.md)
- [Procédure : Appeler un gestionnaire d’événements en Visual Basic](./how-to-call-an-event-handler.md)
