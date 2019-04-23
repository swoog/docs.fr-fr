---
title: ICLRSyncManager::GetRWLockOwnerNext, méthode
ms.date: 03/30/2017
api_name:
- ICLRSyncManager.GetRWLockOwnerNext
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRSyncManager::GetRWLockOwnerNext
helpviewer_keywords:
- ICLRSyncManager::GetRWLockOwnerNext method [.NET Framework hosting]
- GetRWLockOwnerNext method [.NET Framework hosting]
ms.assetid: 0e025b6a-280e-40a2-a2d0-b15f58777b81
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d3efe80c0442e765274b309e39a79cc867676043
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59169648"
---
# <a name="iclrsyncmanagergetrwlockownernext-method"></a><span data-ttu-id="8acb0-102">ICLRSyncManager::GetRWLockOwnerNext, méthode</span><span class="sxs-lookup"><span data-stu-id="8acb0-102">ICLRSyncManager::GetRWLockOwnerNext Method</span></span>
<span data-ttu-id="8acb0-103">Obtient le prochain [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) instance est bloquée sur le verrou de lecteur-writer actuel.</span><span class="sxs-lookup"><span data-stu-id="8acb0-103">Gets the next [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) instance that is blocked on the current reader-writer lock.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8acb0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8acb0-104">Syntax</span></span>  
  
```  
HRESULT GetRWLockOwnerNext (  
    [in] SIZE_T       Iterator,  
    [out] IHostTask  *ppOwnerHostTask  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8acb0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8acb0-105">Parameters</span></span>  
 `Iterator`  
 <span data-ttu-id="8acb0-106">[in] Itérateur qui a été créé à l’aide d’un appel à [CreateRWLockOwnerIterator](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-createrwlockowneriterator-method.md).</span><span class="sxs-lookup"><span data-stu-id="8acb0-106">[in] The iterator that was created by using a call to [CreateRWLockOwnerIterator](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-createrwlockowneriterator-method.md).</span></span>  
  
 `ppOwnerHostTask`  
 <span data-ttu-id="8acb0-107">[out] Un pointeur vers la prochaine `IHostTask` qui attend le verrou, ou null si aucune tâche n’attend.</span><span class="sxs-lookup"><span data-stu-id="8acb0-107">[out] A pointer to the next `IHostTask` that is waiting on the lock, or null if no task is waiting.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8acb0-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8acb0-108">Return Value</span></span>  
  
|<span data-ttu-id="8acb0-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="8acb0-109">HRESULT</span></span>|<span data-ttu-id="8acb0-110">Description</span><span class="sxs-lookup"><span data-stu-id="8acb0-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="8acb0-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="8acb0-111">S_OK</span></span>|<span data-ttu-id="8acb0-112">`GetRWLockOwnerNext` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="8acb0-112">`GetRWLockOwnerNext` returned successfully.</span></span>|  
|<span data-ttu-id="8acb0-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="8acb0-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="8acb0-114">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="8acb0-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="8acb0-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="8acb0-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="8acb0-116">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="8acb0-116">The call timed out.</span></span>|  
|<span data-ttu-id="8acb0-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="8acb0-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="8acb0-118">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="8acb0-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="8acb0-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="8acb0-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="8acb0-120">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="8acb0-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="8acb0-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="8acb0-121">E_FAIL</span></span>|<span data-ttu-id="8acb0-122">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8acb0-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="8acb0-123">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="8acb0-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="8acb0-124">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="8acb0-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8acb0-125">Notes</span><span class="sxs-lookup"><span data-stu-id="8acb0-125">Remarks</span></span>  
 <span data-ttu-id="8acb0-126">Si `ppOwnerHostTask` a la valeur null, l’itération est terminée et l’hôte doit appeler la [DeleteRWLockOwnerIterator](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-deleterwlockowneriterator-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="8acb0-126">If `ppOwnerHostTask` is set to null, the iteration has terminated, and the host should call the [DeleteRWLockOwnerIterator](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-deleterwlockowneriterator-method.md) method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8acb0-127">Le CLR appelle `AddRef` sur le `IHostTask` auquel `ppOwnerHostTask` points pour empêcher cette tâche de quitter alors que l’hôte conserve le pointeur.</span><span class="sxs-lookup"><span data-stu-id="8acb0-127">The CLR calls `AddRef` on the `IHostTask` to which `ppOwnerHostTask` points to prevent this task from exiting while the host holds the pointer.</span></span> <span data-ttu-id="8acb0-128">L’hôte doit appeler `Release` pour décrémenter le décompte de références lorsqu’il est terminé.</span><span class="sxs-lookup"><span data-stu-id="8acb0-128">The host must call `Release` to decrement the reference count when it is finished.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8acb0-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8acb0-129">Requirements</span></span>  
 <span data-ttu-id="8acb0-130">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8acb0-130">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8acb0-131">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="8acb0-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="8acb0-132">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8acb0-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8acb0-133">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8acb0-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8acb0-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8acb0-134">See also</span></span>

- [<span data-ttu-id="8acb0-135">ICLRSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="8acb0-135">ICLRSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)
- [<span data-ttu-id="8acb0-136">IHostSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="8acb0-136">IHostSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)
