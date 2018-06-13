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
ms.openlocfilehash: 103deb5ec46ba8c1d385c5339bc52a0c220c4c93
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33439766"
---
# <a name="ihostsemaphore-interface"></a><span data-ttu-id="42ed2-102">IHostSemaphore, interface</span><span class="sxs-lookup"><span data-stu-id="42ed2-102">IHostSemaphore Interface</span></span>
<span data-ttu-id="42ed2-103">Représente l’implémentation de l’hôte d’un sémaphore pour le thread.</span><span class="sxs-lookup"><span data-stu-id="42ed2-103">Represents the host's implementation of a semaphore for threading.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="42ed2-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="42ed2-104">Methods</span></span>  
  
|<span data-ttu-id="42ed2-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="42ed2-105">Method</span></span>|<span data-ttu-id="42ed2-106">Description</span><span class="sxs-lookup"><span data-stu-id="42ed2-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="42ed2-107">ReleaseSemaphore, méthode</span><span class="sxs-lookup"><span data-stu-id="42ed2-107">ReleaseSemaphore Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsemaphore-releasesemaphore-method.md)|<span data-ttu-id="42ed2-108">Incrémente le nombre d’actuel `IHostSemaphore` instance de la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="42ed2-108">Increases the count of the current `IHostSemaphore` instance by the specified amount.</span></span>|  
|[<span data-ttu-id="42ed2-109">Wait, méthode</span><span class="sxs-lookup"><span data-stu-id="42ed2-109">Wait Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsemaphore-wait-method.md)|<span data-ttu-id="42ed2-110">Fait en `IHostSemaphore` instance attendre qu’elle appartient ou la quantité de temps spécifiée.</span><span class="sxs-lookup"><span data-stu-id="42ed2-110">Causes the current `IHostSemaphore` instance to wait until it is owned or the specified amount of time elapses.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="42ed2-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="42ed2-111">Requirements</span></span>  
 <span data-ttu-id="42ed2-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="42ed2-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="42ed2-113">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="42ed2-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="42ed2-114">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="42ed2-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="42ed2-115">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="42ed2-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="42ed2-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42ed2-116">See Also</span></span>  
 [<span data-ttu-id="42ed2-117">ICLRSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="42ed2-117">ICLRSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)  
 [<span data-ttu-id="42ed2-118">IHostAutoEvent, interface</span><span class="sxs-lookup"><span data-stu-id="42ed2-118">IHostAutoEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostautoevent-interface.md)  
 [<span data-ttu-id="42ed2-119">IHostManualEvent, interface</span><span class="sxs-lookup"><span data-stu-id="42ed2-119">IHostManualEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-interface.md)  
 [<span data-ttu-id="42ed2-120">IHostSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="42ed2-120">IHostSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)  
 [<span data-ttu-id="42ed2-121">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="42ed2-121">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
