---
title: 'Résolution des problèmes : débogage des services Windows'
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
manager: douge
ms.openlocfilehash: 77a0c19c2da2d1886beaf396650fa024fc1243a6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33510135"
---
# <a name="troubleshooting-debugging-windows-services"></a><span data-ttu-id="0baff-102">Résolution des problèmes : débogage des services Windows</span><span class="sxs-lookup"><span data-stu-id="0baff-102">Troubleshooting: Debugging Windows Services</span></span>
<span data-ttu-id="0baff-103">Quand vous déboguez une application de service Windows, votre service et le **Gestionnaire des services Windows** interagissent.</span><span class="sxs-lookup"><span data-stu-id="0baff-103">When you debug a Windows service application, your service and the **Windows Service Manager** interact.</span></span> <span data-ttu-id="0baff-104">Le **Gestionnaire des services** démarre votre service en appelant la méthode <xref:System.ServiceProcess.ServiceBase.OnStart%2A>, puis attend 30 secondes que la méthode <xref:System.ServiceProcess.ServiceBase.OnStart%2A> retourne une valeur.</span><span class="sxs-lookup"><span data-stu-id="0baff-104">The **Service Manager** starts your service by calling the <xref:System.ServiceProcess.ServiceBase.OnStart%2A> method, and then waits 30 seconds for the <xref:System.ServiceProcess.ServiceBase.OnStart%2A> method to return.</span></span> <span data-ttu-id="0baff-105">Si la méthode ne retourne aucune valeur au terme de ce délai, le gestionnaire affiche une erreur indiquant que le service ne peut pas être démarré.</span><span class="sxs-lookup"><span data-stu-id="0baff-105">If the method does not return in this time, the manager shows an error that the service cannot be started.</span></span>  
  
 <span data-ttu-id="0baff-106">Quand vous déboguez la méthode <xref:System.ServiceProcess.ServiceBase.OnStart%2A> comme décrit dans [Guide pratique pour déboguer des applications de service Windows](../../../docs/framework/windows-services/how-to-debug-windows-service-applications.md), tenez compte de ce délai de 30 secondes.</span><span class="sxs-lookup"><span data-stu-id="0baff-106">When you debug the <xref:System.ServiceProcess.ServiceBase.OnStart%2A> method as described in [How to: Debug Windows Service Applications](../../../docs/framework/windows-services/how-to-debug-windows-service-applications.md), you must be aware of this 30-second period.</span></span> <span data-ttu-id="0baff-107">Si vous placez un point d’arrêt dans la méthode <xref:System.ServiceProcess.ServiceBase.OnStart%2A> et que vous n’effectuez aucun pas à pas détaillé dans un délai de 30 secondes, le gestionnaire ne démarre pas le service.</span><span class="sxs-lookup"><span data-stu-id="0baff-107">If you place a breakpoint in the <xref:System.ServiceProcess.ServiceBase.OnStart%2A> method and do not step through it in 30 seconds, the manager will not start the service.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0baff-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0baff-108">See Also</span></span>  
 [<span data-ttu-id="0baff-109">Guide pratique pour déboguer les applications de service Windows</span><span class="sxs-lookup"><span data-stu-id="0baff-109">How to: Debug Windows Service Applications</span></span>](../../../docs/framework/windows-services/how-to-debug-windows-service-applications.md)  
 [<span data-ttu-id="0baff-110">Introduction aux applications de service Windows</span><span class="sxs-lookup"><span data-stu-id="0baff-110">Introduction to Windows Service Applications</span></span>](../../../docs/framework/windows-services/introduction-to-windows-service-applications.md)
