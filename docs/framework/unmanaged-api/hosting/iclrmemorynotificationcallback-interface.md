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
ms.openlocfilehash: 2c5cf7e17989f3c083c7c4e52fa8cfc09c00bc7d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33431517"
---
# <a name="iclrmemorynotificationcallback-interface"></a><span data-ttu-id="a8a3e-102">ICLRMemoryNotificationCallback, interface</span><span class="sxs-lookup"><span data-stu-id="a8a3e-102">ICLRMemoryNotificationCallback Interface</span></span>
<span data-ttu-id="a8a3e-103">Permet à l’hôte de signaler des conditions de sollicitation de la mémoire à l’aide d’une approche similaire à celle de Win32 `CreateMemoryResourceNotification` (fonction).</span><span class="sxs-lookup"><span data-stu-id="a8a3e-103">Allows the host to report memory pressure conditions using an approach similar to that of the Win32 `CreateMemoryResourceNotification` function.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a8a3e-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a8a3e-104">Methods</span></span>  
  
|<span data-ttu-id="a8a3e-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="a8a3e-105">Method</span></span>|<span data-ttu-id="a8a3e-106">Description</span><span class="sxs-lookup"><span data-stu-id="a8a3e-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a8a3e-107">OnMemoryNotification, méthode</span><span class="sxs-lookup"><span data-stu-id="a8a3e-107">OnMemoryNotification Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrmemorynotificationcallback-onmemorynotification-method.md)|<span data-ttu-id="a8a3e-108">Notifie le common language runtime (CLR) de la charge de mémoire sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a8a3e-108">Notifies the common language runtime (CLR) of the memory load on the computer.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a8a3e-109">Notes</span><span class="sxs-lookup"><span data-stu-id="a8a3e-109">Remarks</span></span>  
 <span data-ttu-id="a8a3e-110">L’hôte utilise le `ICLRMemoryNotificationCallback` interface pour demander que le CLR libère des ressources mémoire.</span><span class="sxs-lookup"><span data-stu-id="a8a3e-110">The host uses the `ICLRMemoryNotificationCallback` interface to request that the CLR free memory resources.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a8a3e-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a8a3e-111">Requirements</span></span>  
 <span data-ttu-id="a8a3e-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a8a3e-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a8a3e-113">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a8a3e-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a8a3e-114">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a8a3e-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a8a3e-115">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a8a3e-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a8a3e-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8a3e-116">See Also</span></span>  
 [<span data-ttu-id="a8a3e-117">IHostMemoryManager, interface</span><span class="sxs-lookup"><span data-stu-id="a8a3e-117">IHostMemoryManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md)  
 [<span data-ttu-id="a8a3e-118">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="a8a3e-118">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
