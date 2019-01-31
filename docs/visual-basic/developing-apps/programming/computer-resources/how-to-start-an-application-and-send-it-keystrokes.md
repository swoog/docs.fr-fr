---
title: 'Procédure : démarrer une application et lui envoyer des séquences de touches (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- keystrokes, sending
- Shell command example [Visual Basic]
- processes, starting and sending keystrokes
- SendKeys.SendWait examples
ms.assetid: f1303184-fce4-44fb-88b4-aac5f42d5d77
ms.openlocfilehash: 36d6110a9e0ccf20718e95e6d7601e21e8d8f22c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54688387"
---
# <a name="how-to-start-an-application-and-send-it-keystrokes-visual-basic"></a>Procédure : démarrer une application et lui envoyer des séquences de touches (Visual Basic)
Cet exemple utilise la fonction `Shell` pour démarrer l’application Calculatrice, puis multiplie deux nombres en envoyant des séquences de touches à l’aide de la méthode `My.Computer.Keyboard.SendKeys`.  
  
## <a name="example"></a>Exemple  
 [!code-vb[VbVbalrMyComputer#25](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/how-to-start-an-application-and-send-it-keystrokes_1.vb)]  
  
## <a name="robust-programming"></a>Programmation fiable  
 Une exception <xref:System.ArgumentException> est levée si aucune application avec l’identificateur de processus demandé n’est trouvée.  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 L’appel à la fonction `Shell` nécessite une confiance totale (classe <xref:System.Security.SecurityException>).  
  
## <a name="see-also"></a>Voir aussi
- <xref:Microsoft.VisualBasic.Devices.Keyboard.SendKeys%2A>
- <xref:Microsoft.VisualBasic.Interaction.Shell%2A>
- <xref:Microsoft.VisualBasic.Interaction.AppActivate%2A>
