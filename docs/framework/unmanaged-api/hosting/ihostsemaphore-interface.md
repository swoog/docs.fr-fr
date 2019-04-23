---
title: IHostSemaphore, interface
ms.date: 03/30/2017
api_name:
- IHostSemaphore
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSemaphore
helpviewer_keywords:
- IHostSemaphore interface [.NET Framework hosting]
ms.assetid: c0765321-656c-441e-bab5-58176292be1e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2d7d4a295832a958fb6a8fe2e6c43a09135500d3
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59182284"
---
# <a name="ihostsemaphore-interface"></a><span data-ttu-id="1f5f6-102">IHostSemaphore, interface</span><span class="sxs-lookup"><span data-stu-id="1f5f6-102">IHostSemaphore Interface</span></span>
<span data-ttu-id="1f5f6-103">Représente l’implémentation de l’hôte d’un sémaphore pour le thread.</span><span class="sxs-lookup"><span data-stu-id="1f5f6-103">Represents the host's implementation of a semaphore for threading.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="1f5f6-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1f5f6-104">Methods</span></span>  
  
|<span data-ttu-id="1f5f6-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="1f5f6-105">Method</span></span>|<span data-ttu-id="1f5f6-106">Description</span><span class="sxs-lookup"><span data-stu-id="1f5f6-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="1f5f6-107">ReleaseSemaphore, méthode</span><span class="sxs-lookup"><span data-stu-id="1f5f6-107">ReleaseSemaphore Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsemaphore-releasesemaphore-method.md)|<span data-ttu-id="1f5f6-108">Augmente le nombre de cours `IHostSemaphore` instance de la quantité spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1f5f6-108">Increases the count of the current `IHostSemaphore` instance by the specified amount.</span></span>|  
|[<span data-ttu-id="1f5f6-109">Wait, méthode</span><span class="sxs-lookup"><span data-stu-id="1f5f6-109">Wait Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsemaphore-wait-method.md)|<span data-ttu-id="1f5f6-110">Fait en `IHostSemaphore` instance attendre jusqu'à ce qu’il appartient ou la quantité de temps s’écoule spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1f5f6-110">Causes the current `IHostSemaphore` instance to wait until it is owned or the specified amount of time elapses.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="1f5f6-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f5f6-111">Requirements</span></span>  
 <span data-ttu-id="1f5f6-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1f5f6-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1f5f6-113">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="1f5f6-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="1f5f6-114">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1f5f6-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1f5f6-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1f5f6-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1f5f6-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f5f6-116">See also</span></span>

- [<span data-ttu-id="1f5f6-117">ICLRSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="1f5f6-117">ICLRSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)
- [<span data-ttu-id="1f5f6-118">IHostAutoEvent, interface</span><span class="sxs-lookup"><span data-stu-id="1f5f6-118">IHostAutoEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostautoevent-interface.md)
- [<span data-ttu-id="1f5f6-119">IHostManualEvent, interface</span><span class="sxs-lookup"><span data-stu-id="1f5f6-119">IHostManualEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-interface.md)
- [<span data-ttu-id="1f5f6-120">IHostSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="1f5f6-120">IHostSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)
- [<span data-ttu-id="1f5f6-121">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="1f5f6-121">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
