---
title: Guide pratique pour démarrer une application et envoyer des séquences de touches (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- keystrokes, sending
- Shell command example [Visual Basic]
- processes, starting and sending keystrokes
- SendKeys.SendWait examples
ms.assetid: f1303184-fce4-44fb-88b4-aac5f42d5d77
ms.openlocfilehash: 716c88153ad01c7b225f31948c8aaaa2694dc512
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33582146"
---
# <a name="how-to-start-an-application-and-send-it-keystrokes-visual-basic"></a>Guide pratique pour démarrer une application et envoyer des séquences de touches (Visual Basic)
Cet exemple utilise la fonction `Shell` pour démarrer l’application Calculatrice, puis multiplie deux nombres en envoyant des séquences de touches à l’aide de la méthode `My.Computer.Keyboard.SendKeys`.  
  
## <a name="example"></a>Exemple  
 [!code-vb[VbVbalrMyComputer#25](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/how-to-start-an-application-and-send-it-keystrokes_1.vb)]  
  
## <a name="robust-programming"></a>Programmation fiable  
 Une exception <xref:System.ArgumentException> est levée si aucune application avec l’identificateur de processus demandé n’est trouvée.  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 L’appel à la fonction `Shell` nécessite une confiance totale (classe <xref:System.Security.SecurityException>).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:Microsoft.VisualBasic.Devices.Keyboard.SendKeys%2A>  
 <xref:Microsoft.VisualBasic.Interaction.Shell%2A>  
 <xref:Microsoft.VisualBasic.Interaction.AppActivate%2A>
