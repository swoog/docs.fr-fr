---
title: Gestion de l'alimentation dans Windows Forms
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- battery states
- power states
ms.assetid: ad04a801-5682-4d88-92c5-26eb9cdb209a
ms.openlocfilehash: 6bb9b4f30a88ece93b17ff2510087b220d538738
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59979717"
---
# <a name="power-management-in-windows-forms"></a>Gestion de l'alimentation dans Windows Forms
Vos applications Windows Forms peuvent tirer parti des fonctionnalités de gestion d’alimentation dans le système d’exploitation Windows. Vos applications peuvent surveiller l’état d’alimentation d’un ordinateur et prendre des mesures quand un changement d’état se produit. Par exemple, si votre application s’exécute sur un ordinateur portable, vous souhaiterez désactiver certaines fonctionnalités dans votre application lors de la charge de la batterie de l’ordinateur se situe sous un certain niveau.  
  
 Le [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] fournit un <xref:Microsoft.Win32.SystemEvents.PowerModeChanged> événement qui se produit chaque fois qu’une modification à l’état de l’alimentation, tels que lorsqu’un utilisateur interrompt ou redémarre le système d’exploitation, ou lorsque l’état d’alimentation AC ou l’état de la batterie change. Le <xref:System.Windows.Forms.SystemInformation.PowerStatus%2A> propriété de la <xref:System.Windows.Forms.SystemInformation> classe peut être utilisé pour demander l’état actuel, comme indiqué dans l’exemple de code suivant.  
  
 [!code-csharp[PowerMode#1](~/samples/snippets/csharp/VS_Snippets_Winforms/powermode/cs/form1.cs#1)]
 [!code-vb[PowerMode#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/powermode/vb/form1.vb#1)]  
  
 Outre le <xref:System.Windows.Forms.BatteryChargeStatus> énumérations, les <xref:System.Windows.Forms.SystemInformation.PowerStatus%2A> propriété contient également des énumérations permettant de déterminer la capacité de la batterie (<xref:System.Windows.Forms.PowerStatus.BatteryFullLifetime%2A>) et de facturer le pourcentage de batterie (<xref:System.Windows.Forms.PowerStatus.BatteryLifePercent%2A>, <xref:System.Windows.Forms.PowerStatus.BatteryLifeRemaining%2A>).  
  
 Vous pouvez utiliser la <xref:System.Windows.Forms.Application.SetSuspendState%2A> méthode de la <xref:System.Windows.Forms.Application> pour mettre un ordinateur en veille prolongée ou en mode veille. Si le `force` argument a la valeur `false`, le système d’exploitation diffuse un événement à toutes les applications demandant l’autorisation de suspendre. Si le `disableWakeEvent` argument a la valeur `true`, le système d’exploitation désactive tous les événements de mise en éveil.  
  
 L’exemple de code suivant montre comment mettre un ordinateur en veille prolongée.  
  
 [!code-csharp[PowerMode#2](~/samples/snippets/csharp/VS_Snippets_Winforms/powermode/cs/form1.cs#2)]
 [!code-vb[PowerMode#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/powermode/vb/form1.vb#2)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.Win32.SystemEvents.PowerModeChanged>
- <xref:System.Windows.Forms.SystemInformation.PowerStatus%2A>
- <xref:System.Windows.Forms.Application.SetSuspendState%2A>
- <xref:Microsoft.Win32.SystemEvents.SessionSwitch>
