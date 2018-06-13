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
# <a name="how-to-start-an-application-and-send-it-keystrokes-visual-basic"></a><span data-ttu-id="8f400-102">Guide pratique pour démarrer une application et envoyer des séquences de touches (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="8f400-102">How to: Start an Application and Send it Keystrokes (Visual Basic)</span></span>
<span data-ttu-id="8f400-103">Cet exemple utilise la fonction `Shell` pour démarrer l’application Calculatrice, puis multiplie deux nombres en envoyant des séquences de touches à l’aide de la méthode `My.Computer.Keyboard.SendKeys`.</span><span class="sxs-lookup"><span data-stu-id="8f400-103">This example uses the `Shell` function to start the calculator application and then multiplies two numbers by sending keystrokes using the `My.Computer.Keyboard.SendKeys` method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8f400-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="8f400-104">Example</span></span>  
 [!code-vb[VbVbalrMyComputer#25](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/how-to-start-an-application-and-send-it-keystrokes_1.vb)]  
  
## <a name="robust-programming"></a><span data-ttu-id="8f400-105">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="8f400-105">Robust Programming</span></span>  
 <span data-ttu-id="8f400-106">Une exception <xref:System.ArgumentException> est levée si aucune application avec l’identificateur de processus demandé n’est trouvée.</span><span class="sxs-lookup"><span data-stu-id="8f400-106">A <xref:System.ArgumentException> exception is raised if an application with the requested process identifier cannot be found.</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="8f400-107">Sécurité .NET Framework</span><span class="sxs-lookup"><span data-stu-id="8f400-107">.NET Framework Security</span></span>  
 <span data-ttu-id="8f400-108">L’appel à la fonction `Shell` nécessite une confiance totale (classe <xref:System.Security.SecurityException>).</span><span class="sxs-lookup"><span data-stu-id="8f400-108">The call to the `Shell` function requires full trust (<xref:System.Security.SecurityException> class).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8f400-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f400-109">See Also</span></span>  
 <xref:Microsoft.VisualBasic.Devices.Keyboard.SendKeys%2A>  
 <xref:Microsoft.VisualBasic.Interaction.Shell%2A>  
 <xref:Microsoft.VisualBasic.Interaction.AppActivate%2A>
