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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59212152"
---
# <a name="iclrmemorynotificationcallback-interface"></a><span data-ttu-id="464b5-102">ICLRMemoryNotificationCallback, interface</span><span class="sxs-lookup"><span data-stu-id="464b5-102">ICLRMemoryNotificationCallback Interface</span></span>
<span data-ttu-id="464b5-103">Permet à l’hôte de signaler des conditions de sollicitation de la mémoire à l’aide d’une approche similaire à celle de Win32 `CreateMemoryResourceNotification` (fonction).</span><span class="sxs-lookup"><span data-stu-id="464b5-103">Allows the host to report memory pressure conditions using an approach similar to that of the Win32 `CreateMemoryResourceNotification` function.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="464b5-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="464b5-104">Methods</span></span>  
  
|<span data-ttu-id="464b5-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="464b5-105">Method</span></span>|<span data-ttu-id="464b5-106">Description</span><span class="sxs-lookup"><span data-stu-id="464b5-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="464b5-107">OnMemoryNotification, méthode</span><span class="sxs-lookup"><span data-stu-id="464b5-107">OnMemoryNotification Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrmemorynotificationcallback-onmemorynotification-method.md)|<span data-ttu-id="464b5-108">Notifie le common language runtime (CLR) de la charge de mémoire sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="464b5-108">Notifies the common language runtime (CLR) of the memory load on the computer.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="464b5-109">Notes</span><span class="sxs-lookup"><span data-stu-id="464b5-109">Remarks</span></span>  
 <span data-ttu-id="464b5-110">L’hôte utilise le `ICLRMemoryNotificationCallback` interface pour demander que le CLR libère des ressources mémoire.</span><span class="sxs-lookup"><span data-stu-id="464b5-110">The host uses the `ICLRMemoryNotificationCallback` interface to request that the CLR free memory resources.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="464b5-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="464b5-111">Requirements</span></span>  
 <span data-ttu-id="464b5-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="464b5-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="464b5-113">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="464b5-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="464b5-114">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="464b5-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="464b5-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="464b5-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="464b5-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="464b5-116">See also</span></span>

- [<span data-ttu-id="464b5-117">IHostMemoryManager, interface</span><span class="sxs-lookup"><span data-stu-id="464b5-117">IHostMemoryManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md)
- [<span data-ttu-id="464b5-118">Interfaces d'hébergement</span><span class="sxs-lookup"><span data-stu-id="464b5-118">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
