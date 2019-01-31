---
title: 'Résolution des problèmes : débogage de services Windows'
ms.date: 03/30/2017
helpviewer_keywords:
- debugging Windows Service applications
- debugging [Visual Studio], Windows services
- troubleshooting service applications
- services, troubleshooting
- troubleshooting debugging, Windows Services
- Windows Service applications, debugging
- services, debugging
- Windows Service applications, troubleshooting
ms.assetid: cf859d4c-f04c-4cb7-81e3-bc7de8bea190
author: ghogen
ms.openlocfilehash: cdffb3a8ce9c5119a0a17a8bc7e6ca78276423f4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54745673"
---
# <a name="troubleshooting-debugging-windows-services"></a><span data-ttu-id="07be7-102">Résolution des problèmes : débogage de services Windows</span><span class="sxs-lookup"><span data-stu-id="07be7-102">Troubleshooting: Debugging Windows Services</span></span>
<span data-ttu-id="07be7-103">Quand vous déboguez une application de service Windows, votre service et le **Gestionnaire des services Windows** interagissent.</span><span class="sxs-lookup"><span data-stu-id="07be7-103">When you debug a Windows service application, your service and the **Windows Service Manager** interact.</span></span> <span data-ttu-id="07be7-104">Le **Gestionnaire des services** démarre votre service en appelant la méthode <xref:System.ServiceProcess.ServiceBase.OnStart%2A>, puis attend 30 secondes que la méthode <xref:System.ServiceProcess.ServiceBase.OnStart%2A> retourne une valeur.</span><span class="sxs-lookup"><span data-stu-id="07be7-104">The **Service Manager** starts your service by calling the <xref:System.ServiceProcess.ServiceBase.OnStart%2A> method, and then waits 30 seconds for the <xref:System.ServiceProcess.ServiceBase.OnStart%2A> method to return.</span></span> <span data-ttu-id="07be7-105">Si la méthode ne retourne aucune valeur au terme de ce délai, le gestionnaire affiche une erreur indiquant que le service ne peut pas être démarré.</span><span class="sxs-lookup"><span data-stu-id="07be7-105">If the method does not return in this time, the manager shows an error that the service cannot be started.</span></span>  
  
 <span data-ttu-id="07be7-106">Quand vous déboguez la méthode <xref:System.ServiceProcess.ServiceBase.OnStart%2A> comme décrit dans [Guide pratique pour déboguer des applications de service Windows](../../../docs/framework/windows-services/how-to-debug-windows-service-applications.md), tenez compte de ce délai de 30 secondes.</span><span class="sxs-lookup"><span data-stu-id="07be7-106">When you debug the <xref:System.ServiceProcess.ServiceBase.OnStart%2A> method as described in [How to: Debug Windows Service Applications](../../../docs/framework/windows-services/how-to-debug-windows-service-applications.md), you must be aware of this 30-second period.</span></span> <span data-ttu-id="07be7-107">Si vous placez un point d’arrêt dans la méthode <xref:System.ServiceProcess.ServiceBase.OnStart%2A> et que vous n’effectuez aucun pas à pas détaillé dans un délai de 30 secondes, le gestionnaire ne démarre pas le service.</span><span class="sxs-lookup"><span data-stu-id="07be7-107">If you place a breakpoint in the <xref:System.ServiceProcess.ServiceBase.OnStart%2A> method and do not step through it in 30 seconds, the manager will not start the service.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="07be7-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07be7-108">See also</span></span>
- [<span data-ttu-id="07be7-109">Guide pratique pour déboguer les applications de service Windows</span><span class="sxs-lookup"><span data-stu-id="07be7-109">How to: Debug Windows Service Applications</span></span>](../../../docs/framework/windows-services/how-to-debug-windows-service-applications.md)
- [<span data-ttu-id="07be7-110">Introduction aux applications de service Windows</span><span class="sxs-lookup"><span data-stu-id="07be7-110">Introduction to Windows Service Applications</span></span>](../../../docs/framework/windows-services/introduction-to-windows-service-applications.md)
