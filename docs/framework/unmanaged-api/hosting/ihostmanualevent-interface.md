---
title: IHostManualEvent, interface
ms.date: 03/30/2017
api_name:
- IHostManualEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostManualEvent
helpviewer_keywords:
- IHostManualEvent interface [.NET Framework hosting]
ms.assetid: 300c2661-b7d1-4c39-b080-9ebdef0fd523
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ad580f7cab81323e09a24dc12db39f223be3aeb4
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59208629"
---
# <a name="ihostmanualevent-interface"></a><span data-ttu-id="b1b7d-102">IHostManualEvent, interface</span><span class="sxs-lookup"><span data-stu-id="b1b7d-102">IHostManualEvent Interface</span></span>
<span data-ttu-id="b1b7d-103">Fournit l’implémentation de l’hôte d’une représentation d’un événement de réinitialisation manuelle.</span><span class="sxs-lookup"><span data-stu-id="b1b7d-103">Provides the host's implementation of a representation of a manual reset event.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b1b7d-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b1b7d-104">Methods</span></span>  
  
|<span data-ttu-id="b1b7d-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="b1b7d-105">Method</span></span>|<span data-ttu-id="b1b7d-106">Description</span><span class="sxs-lookup"><span data-stu-id="b1b7d-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b1b7d-107">Reset, méthode</span><span class="sxs-lookup"><span data-stu-id="b1b7d-107">Reset Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-reset-method.md)|<span data-ttu-id="b1b7d-108">Réinitialise l’actuel `IHostManualEvent` instance à un état non signalé.</span><span class="sxs-lookup"><span data-stu-id="b1b7d-108">Resets the current `IHostManualEvent` instance to a non-signaled state.</span></span>|  
|[<span data-ttu-id="b1b7d-109">Set, méthode</span><span class="sxs-lookup"><span data-stu-id="b1b7d-109">Set Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-set-method.md)|<span data-ttu-id="b1b7d-110">Définit l’actuel `IHostManualEvent` instance à un état signalé.</span><span class="sxs-lookup"><span data-stu-id="b1b7d-110">Sets the current `IHostManualEvent` instance to a signaled state.</span></span>|  
|[<span data-ttu-id="b1b7d-111">Wait, méthode</span><span class="sxs-lookup"><span data-stu-id="b1b7d-111">Wait Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-wait-method.md)|<span data-ttu-id="b1b7d-112">Fait en `IHostManualEvent` instance à attendre jusqu'à ce qu’il appartient, ou un certain laps de temps.</span><span class="sxs-lookup"><span data-stu-id="b1b7d-112">Causes the current `IHostManualEvent` instance to wait until it is owned, or a specified amount of time elapses.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b1b7d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1b7d-113">Requirements</span></span>  
 <span data-ttu-id="b1b7d-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b1b7d-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b1b7d-115">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="b1b7d-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b1b7d-116">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b1b7d-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="b1b7d-117">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="b1b7d-117">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="b1b7d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1b7d-118">See also</span></span>

- [<span data-ttu-id="b1b7d-119">ICLRSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="b1b7d-119">ICLRSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)
- [<span data-ttu-id="b1b7d-120">IHostAutoEvent, interface</span><span class="sxs-lookup"><span data-stu-id="b1b7d-120">IHostAutoEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostautoevent-interface.md)
- [<span data-ttu-id="b1b7d-121">IHostSemaphore, interface</span><span class="sxs-lookup"><span data-stu-id="b1b7d-121">IHostSemaphore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsemaphore-interface.md)
- [<span data-ttu-id="b1b7d-122">IHostSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="b1b7d-122">IHostSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)
- [<span data-ttu-id="b1b7d-123">Interfaces d'hébergement</span><span class="sxs-lookup"><span data-stu-id="b1b7d-123">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
