---
title: IHostSyncManager, interface
ms.date: 03/30/2017
api_name:
- IHostSyncManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSyncManager
helpviewer_keywords:
- IHostSyncManager interface [.NET Framework hosting]
ms.assetid: 2e081a37-6a28-4c93-b7ab-1c96a464637c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 200da8b87b52a29c2b075d1e06929031d3f588b7
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59174224"
---
# <a name="ihostsyncmanager-interface"></a><span data-ttu-id="09337-102">IHostSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="09337-102">IHostSyncManager Interface</span></span>
<span data-ttu-id="09337-103">Fournit des méthodes qui permettent le common language runtime (CLR) pour créer des primitives de synchronisation en appelant l’hôte au lieu d’utiliser les fonctions de synchronisation Win32.</span><span class="sxs-lookup"><span data-stu-id="09337-103">Provides methods that allow the common language runtime (CLR) to create synchronization primitives by calling the host instead of using the Win32 synchronization functions.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="09337-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="09337-104">Methods</span></span>  
  
|<span data-ttu-id="09337-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="09337-105">Method</span></span>|<span data-ttu-id="09337-106">Description</span><span class="sxs-lookup"><span data-stu-id="09337-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="09337-107">CreateAutoEvent, méthode</span><span class="sxs-lookup"><span data-stu-id="09337-107">CreateAutoEvent Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-createautoevent-method.md)|<span data-ttu-id="09337-108">Crée un objet d’événement d’auto-réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="09337-108">Creates an auto-reset event object.</span></span>|  
|[<span data-ttu-id="09337-109">CreateCrst, méthode</span><span class="sxs-lookup"><span data-stu-id="09337-109">CreateCrst Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-createcrst-method.md)|<span data-ttu-id="09337-110">Crée un objet de section critique pour la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="09337-110">Creates a critical section object for synchronization.</span></span>|  
|[<span data-ttu-id="09337-111">CreateCrstWithSpinCount, méthode</span><span class="sxs-lookup"><span data-stu-id="09337-111">CreateCrstWithSpinCount Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-createcrstwithspincount-method.md)|<span data-ttu-id="09337-112">Crée un objet de section critique dont le nombre de sélection numérique pour la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="09337-112">Creates a critical section object with spin count for synchronization.</span></span>|  
|[<span data-ttu-id="09337-113">CreateManualEvent, méthode</span><span class="sxs-lookup"><span data-stu-id="09337-113">CreateManualEvent Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-createmanualevent-method.md)|<span data-ttu-id="09337-114">Crée un objet d’événement de réinitialisation manuelle.</span><span class="sxs-lookup"><span data-stu-id="09337-114">Creates a manual-reset event object.</span></span>|  
|[<span data-ttu-id="09337-115">CreateMonitorEvent, méthode</span><span class="sxs-lookup"><span data-stu-id="09337-115">CreateMonitorEvent Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-createmonitorevent-method.md)|<span data-ttu-id="09337-116">Crée un objet d’événement d’auto-réinitialisation surveillé.</span><span class="sxs-lookup"><span data-stu-id="09337-116">Creates a monitored auto-reset event object.</span></span>|  
|[<span data-ttu-id="09337-117">CreateRWLockReaderEvent, méthode</span><span class="sxs-lookup"><span data-stu-id="09337-117">CreateRWLockReaderEvent Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-createrwlockreaderevent-method.md)|<span data-ttu-id="09337-118">Crée un objet d’événement de réinitialisation manuelle pour l’implémentation d’un verrou de lecteur.</span><span class="sxs-lookup"><span data-stu-id="09337-118">Creates a manual-reset event object for the implementation of a reader lock.</span></span>|  
|[<span data-ttu-id="09337-119">CreateRWLockWriterEvent, méthode</span><span class="sxs-lookup"><span data-stu-id="09337-119">CreateRWLockWriterEvent Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-createrwlockwriterevent-method.md)|<span data-ttu-id="09337-120">Crée un objet d’événement de réinitialisation automatique pour l’implémentation d’un verrou de writer.</span><span class="sxs-lookup"><span data-stu-id="09337-120">Creates an auto-reset event object for the implementation of a writer lock.</span></span>|  
|[<span data-ttu-id="09337-121">CreateSemaphore, méthode</span><span class="sxs-lookup"><span data-stu-id="09337-121">CreateSemaphore Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-createsemaphore-method.md)|<span data-ttu-id="09337-122">Crée un [IHostSemaphore](../../../../docs/framework/unmanaged-api/hosting/ihostsemaphore-interface.md) objet pour le CLR à utiliser comme un sémaphore pour les événements d’attente.</span><span class="sxs-lookup"><span data-stu-id="09337-122">Creates an [IHostSemaphore](../../../../docs/framework/unmanaged-api/hosting/ihostsemaphore-interface.md) object for the CLR to use as a semaphore for wait events.</span></span>|  
|[<span data-ttu-id="09337-123">SetCLRSyncManager, méthode</span><span class="sxs-lookup"><span data-stu-id="09337-123">SetCLRSyncManager Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-setclrsyncmanager-method.md)|<span data-ttu-id="09337-124">Définit le [ICLRSyncManager](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md) instance à associer à l’actuel `IHostSyncManager` instance.</span><span class="sxs-lookup"><span data-stu-id="09337-124">Sets the [ICLRSyncManager](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md) instance to associate with the current `IHostSyncManager` instance.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="09337-125">Notes</span><span class="sxs-lookup"><span data-stu-id="09337-125">Remarks</span></span>  
 <span data-ttu-id="09337-126">Le CLR détecte l’implémentation de l’hôte de `IHostSyncManager` en appelant le [IHostControl::GetHostManager](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-gethostmanager-method.md) méthode avec un `IID` de IID_IHostSyncManager.</span><span class="sxs-lookup"><span data-stu-id="09337-126">The CLR discovers the host's implementation of `IHostSyncManager` by calling the [IHostControl::GetHostManager](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-gethostmanager-method.md) method with an `IID` of IID_IHostSyncManager.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="09337-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09337-127">Requirements</span></span>  
 <span data-ttu-id="09337-128">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="09337-128">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="09337-129">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="09337-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="09337-130">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="09337-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="09337-131">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="09337-131">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="09337-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09337-132">See also</span></span>

- [<span data-ttu-id="09337-133">ICLRSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="09337-133">ICLRSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)
- [<span data-ttu-id="09337-134">Interfaces d'hébergement</span><span class="sxs-lookup"><span data-stu-id="09337-134">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
