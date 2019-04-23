---
title: 'Résolution des problèmes : impossibilité d’installer une application de service'
ms.date: 03/30/2017
helpviewer_keywords:
- troubleshooting service applications
- services, troubleshooting
- services, debugging
- Windows NT services, troubleshooting
- troubleshooting NT services
- Windows Service applications, troubleshooting
ms.assetid: 45c48e2e-b97d-44bc-8896-14f328e0ce33
author: ghogen
ms.openlocfilehash: f75a2f33ecde408d2d8e2f2343197ba56c4b8c21
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59143817"
---
# <a name="troubleshooting-service-application-wont-install"></a><span data-ttu-id="f8763-102">Résolution des problèmes : impossibilité d’installer une application de service</span><span class="sxs-lookup"><span data-stu-id="f8763-102">Troubleshooting: Service Application Won't Install</span></span>
<span data-ttu-id="f8763-103">Si votre application de service ne s’installe pas correctement, vérifiez que la propriété <xref:System.ServiceProcess.ServiceBase.ServiceName%2A> de la classe de service est définie avec la même valeur que celle indiquée dans le programme d’installation de ce service.</span><span class="sxs-lookup"><span data-stu-id="f8763-103">If your service application will not install correctly, check to make sure that the <xref:System.ServiceProcess.ServiceBase.ServiceName%2A> property for the service class is set to the same value as is shown in the installer for that service.</span></span> <span data-ttu-id="f8763-104">Pour que votre service s’installe correctement, la valeur doit être la même dans les deux instances.</span><span class="sxs-lookup"><span data-stu-id="f8763-104">The value must be the same in both instances in order for your service to install correctly.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f8763-105">Vous pouvez également passer en revue les journaux d’installation pour récupérer des commentaires sur le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="f8763-105">You can also look at the installation logs to get feedback on the installation process.</span></span>  
  
 <span data-ttu-id="f8763-106">Déterminez également si un autre service portant le même nom est déjà installé.</span><span class="sxs-lookup"><span data-stu-id="f8763-106">You should also check to determine whether you have another service with the same name already installed.</span></span> <span data-ttu-id="f8763-107">Pour que l’installation réussisse, les noms de service doivent être uniques.</span><span class="sxs-lookup"><span data-stu-id="f8763-107">Service names must be unique for installation to succeed.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f8763-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8763-108">See also</span></span>

- [<span data-ttu-id="f8763-109">Introduction aux applications de service Windows</span><span class="sxs-lookup"><span data-stu-id="f8763-109">Introduction to Windows Service Applications</span></span>](../../../docs/framework/windows-services/introduction-to-windows-service-applications.md)
