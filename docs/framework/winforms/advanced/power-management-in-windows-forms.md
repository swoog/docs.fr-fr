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
ms.openlocfilehash: 77d2096239ec70f98ebfc299f1eda75ad4490be9
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57712420"
---
# <a name="power-management-in-windows-forms"></a><span data-ttu-id="1b324-102">Gestion de l'alimentation dans Windows Forms</span><span class="sxs-lookup"><span data-stu-id="1b324-102">Power Management in Windows Forms</span></span>
<span data-ttu-id="1b324-103">Vos applications Windows Forms peuvent tirer parti des fonctionnalités de gestion d’alimentation dans le système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="1b324-103">Your Windows Forms applications can take advantage of the power management features in the Windows operating system.</span></span> <span data-ttu-id="1b324-104">Vos applications peuvent surveiller l’état d’alimentation d’un ordinateur et prendre des mesures quand un changement d’état se produit.</span><span class="sxs-lookup"><span data-stu-id="1b324-104">Your applications can monitor the power status of a computer and take action when a status change occurs.</span></span> <span data-ttu-id="1b324-105">Par exemple, si votre application s’exécute sur un ordinateur portable, vous souhaiterez désactiver certaines fonctionnalités dans votre application lors de la charge de la batterie de l’ordinateur se situe sous un certain niveau.</span><span class="sxs-lookup"><span data-stu-id="1b324-105">For example, if your application is running on a portable computer, you might want to disable certain features in your application when the computer's battery charge falls under a certain level.</span></span>  
  
 <span data-ttu-id="1b324-106">Le [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] fournit un <xref:Microsoft.Win32.SystemEvents.PowerModeChanged> événement qui se produit chaque fois qu’une modification à l’état de l’alimentation, tels que lorsqu’un utilisateur interrompt ou redémarre le système d’exploitation, ou lorsque l’état d’alimentation AC ou l’état de la batterie change.</span><span class="sxs-lookup"><span data-stu-id="1b324-106">The [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] provides a <xref:Microsoft.Win32.SystemEvents.PowerModeChanged> event that occurs whenever there is a change in power status, such as when a user suspends or resumes the operating system, or when the AC power status or battery status changes.</span></span> <span data-ttu-id="1b324-107">Le <xref:System.Windows.Forms.SystemInformation.PowerStatus%2A> propriété de la <xref:System.Windows.Forms.SystemInformation> classe peut être utilisé pour demander l’état actuel, comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="1b324-107">The <xref:System.Windows.Forms.SystemInformation.PowerStatus%2A> property of the <xref:System.Windows.Forms.SystemInformation> class can be used to query for the current status, as shown in the following code example.</span></span>  
  
 [!code-csharp[PowerMode#1](~/samples/snippets/csharp/VS_Snippets_Winforms/powermode/cs/form1.cs#1)]
 [!code-vb[PowerMode#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/powermode/vb/form1.vb#1)]  
  
 <span data-ttu-id="1b324-108">Outre le <xref:System.Windows.Forms.BatteryChargeStatus> énumérations, les <xref:System.Windows.Forms.SystemInformation.PowerStatus%2A> propriété contient également des énumérations permettant de déterminer la capacité de la batterie (<xref:System.Windows.Forms.PowerStatus.BatteryFullLifetime%2A>) et de facturer le pourcentage de batterie (<xref:System.Windows.Forms.PowerStatus.BatteryLifePercent%2A>, <xref:System.Windows.Forms.PowerStatus.BatteryLifeRemaining%2A>).</span><span class="sxs-lookup"><span data-stu-id="1b324-108">Besides the <xref:System.Windows.Forms.BatteryChargeStatus> enumerations, the <xref:System.Windows.Forms.SystemInformation.PowerStatus%2A> property also contains enumerations for determining battery capacity (<xref:System.Windows.Forms.PowerStatus.BatteryFullLifetime%2A>) and battery charge percentage (<xref:System.Windows.Forms.PowerStatus.BatteryLifePercent%2A>, <xref:System.Windows.Forms.PowerStatus.BatteryLifeRemaining%2A>).</span></span>  
  
 <span data-ttu-id="1b324-109">Vous pouvez utiliser la <xref:System.Windows.Forms.Application.SetSuspendState%2A> méthode de la <xref:System.Windows.Forms.Application> pour mettre un ordinateur en veille prolongée ou en mode veille.</span><span class="sxs-lookup"><span data-stu-id="1b324-109">You can use the <xref:System.Windows.Forms.Application.SetSuspendState%2A> method of the <xref:System.Windows.Forms.Application> to put a computer into hibernation or suspend mode.</span></span> <span data-ttu-id="1b324-110">Si le `force` argument a la valeur `false`, le système d’exploitation diffuse un événement à toutes les applications demandant l’autorisation de suspendre.</span><span class="sxs-lookup"><span data-stu-id="1b324-110">If the `force` argument is set to `false`, the operating system will broadcast an event to all applications requesting permission to suspend.</span></span> <span data-ttu-id="1b324-111">Si le `disableWakeEvent` argument a la valeur `true`, le système d’exploitation désactive tous les événements de mise en éveil.</span><span class="sxs-lookup"><span data-stu-id="1b324-111">If the `disableWakeEvent` argument is set to `true`, the operating system disables all wake events.</span></span>  
  
 <span data-ttu-id="1b324-112">L’exemple de code suivant montre comment mettre un ordinateur en veille prolongée.</span><span class="sxs-lookup"><span data-stu-id="1b324-112">The following code example demonstrates how to put a computer into hibernation.</span></span>  
  
 [!code-csharp[PowerMode#2](~/samples/snippets/csharp/VS_Snippets_Winforms/powermode/cs/form1.cs#2)]
 [!code-vb[PowerMode#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/powermode/vb/form1.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="1b324-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b324-113">See also</span></span>
- <xref:Microsoft.Win32.SystemEvents.PowerModeChanged>
- <xref:System.Windows.Forms.SystemInformation.PowerStatus%2A>
- <xref:System.Windows.Forms.Application.SetSuspendState%2A>
- <xref:Microsoft.Win32.SystemEvents.SessionSwitch>
