---
title: ICLRMemoryNotificationCallback, interface
ms.date: 03/30/2017
api_name:
- ICLRMemoryNotificationCallback
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMemoryNotificationCallback
helpviewer_keywords:
- ICLRMemoryNotificationCallback interface [.NET Framework hosting]
ms.assetid: 873639e2-4837-4568-83b3-4493e67e4174
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c98ece9d60571034f3298f15897b10c4d8fb06f4
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59212152"
---
# <a name="iclrmemorynotificationcallback-interface"></a><span data-ttu-id="af01b-102">ICLRMemoryNotificationCallback, interface</span><span class="sxs-lookup"><span data-stu-id="af01b-102">ICLRMemoryNotificationCallback Interface</span></span>
<span data-ttu-id="af01b-103">Permet à l’hôte de signaler des conditions de sollicitation de la mémoire à l’aide d’une approche similaire à celle de Win32 `CreateMemoryResourceNotification` (fonction).</span><span class="sxs-lookup"><span data-stu-id="af01b-103">Allows the host to report memory pressure conditions using an approach similar to that of the Win32 `CreateMemoryResourceNotification` function.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="af01b-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="af01b-104">Methods</span></span>  
  
|<span data-ttu-id="af01b-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="af01b-105">Method</span></span>|<span data-ttu-id="af01b-106">Description</span><span class="sxs-lookup"><span data-stu-id="af01b-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="af01b-107">OnMemoryNotification, méthode</span><span class="sxs-lookup"><span data-stu-id="af01b-107">OnMemoryNotification Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrmemorynotificationcallback-onmemorynotification-method.md)|<span data-ttu-id="af01b-108">Notifie le common language runtime (CLR) de la charge de mémoire sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="af01b-108">Notifies the common language runtime (CLR) of the memory load on the computer.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="af01b-109">Notes</span><span class="sxs-lookup"><span data-stu-id="af01b-109">Remarks</span></span>  
 <span data-ttu-id="af01b-110">L’hôte utilise le `ICLRMemoryNotificationCallback` interface pour demander que le CLR libère des ressources mémoire.</span><span class="sxs-lookup"><span data-stu-id="af01b-110">The host uses the `ICLRMemoryNotificationCallback` interface to request that the CLR free memory resources.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="af01b-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af01b-111">Requirements</span></span>  
 <span data-ttu-id="af01b-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="af01b-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="af01b-113">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="af01b-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="af01b-114">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="af01b-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="af01b-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="af01b-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="af01b-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af01b-116">See also</span></span>

- [<span data-ttu-id="af01b-117">IHostMemoryManager, interface</span><span class="sxs-lookup"><span data-stu-id="af01b-117">IHostMemoryManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md)
- [<span data-ttu-id="af01b-118">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="af01b-118">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
