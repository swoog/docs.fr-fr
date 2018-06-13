---
title: ICLRSyncManager::GetMonitorOwner, méthode
ms.date: 03/30/2017
api_name:
- ICLRSyncManager.GetMonitorOwner
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRSyncManager::GetMonitorOwner
helpviewer_keywords:
- ICLRSyncManager::GetMonitorOwner method [.NET Framework hosting]
- GetMonitorOwner method [.NET Framework hosting]
ms.assetid: 840983a4-396d-47b4-86a0-d35f9b437cdb
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5668d75c831710b4f077c325b40352a518ee2c96
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33434302"
---
# <a name="iclrsyncmanagergetmonitorowner-method"></a><span data-ttu-id="59249-102">ICLRSyncManager::GetMonitorOwner, méthode</span><span class="sxs-lookup"><span data-stu-id="59249-102">ICLRSyncManager::GetMonitorOwner Method</span></span>
<span data-ttu-id="59249-103">Obtient le [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) instance qui possède l’analyseur identifié par le cookie spécifié.</span><span class="sxs-lookup"><span data-stu-id="59249-103">Gets the [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) instance that owns the monitor identified by the specified cookie.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="59249-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59249-104">Syntax</span></span>  
  
```  
HRESULT GetMonitorOwner (  
    [in]  SIZE_T     cookie,  
    [out] IHostTask *ppOwnerHostTask  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="59249-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59249-105">Parameters</span></span>  
 `cookie`  
 <span data-ttu-id="59249-106">[in] Le cookie associé à l’analyse.</span><span class="sxs-lookup"><span data-stu-id="59249-106">[in] The cookie associated with the monitor.</span></span>  
  
 `ppOwnerHostTask`  
 <span data-ttu-id="59249-107">[out] Un pointeur vers le `IHostTask` qui possède actuellement l’analyseur, ou null si aucune tâche n’est propriétaire.</span><span class="sxs-lookup"><span data-stu-id="59249-107">[out] A pointer to the `IHostTask` that currently owns the monitor, or null if no task has ownership.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="59249-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="59249-108">Return Value</span></span>  
  
|<span data-ttu-id="59249-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="59249-109">HRESULT</span></span>|<span data-ttu-id="59249-110">Description</span><span class="sxs-lookup"><span data-stu-id="59249-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="59249-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="59249-111">S_OK</span></span>|<span data-ttu-id="59249-112">`GetMonitorOwner` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="59249-112">`GetMonitorOwner` returned successfully.</span></span>|  
|<span data-ttu-id="59249-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="59249-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="59249-114">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="59249-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="59249-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="59249-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="59249-116">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="59249-116">The call timed out.</span></span>|  
|<span data-ttu-id="59249-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="59249-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="59249-118">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="59249-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="59249-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="59249-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="59249-120">Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="59249-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="59249-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="59249-121">E_FAIL</span></span>|<span data-ttu-id="59249-122">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="59249-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="59249-123">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="59249-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="59249-124">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="59249-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="59249-125">Notes</span><span class="sxs-lookup"><span data-stu-id="59249-125">Remarks</span></span>  
 <span data-ttu-id="59249-126">L’hôte appelle généralement `GetMonitorOwner` dans le cadre d’un mécanisme de détection de blocage.</span><span class="sxs-lookup"><span data-stu-id="59249-126">The host typically calls `GetMonitorOwner` as part of a deadlock-detection mechanism.</span></span> <span data-ttu-id="59249-127">Le cookie est associé à un analyseur lorsqu’il est créé à l’aide d’un appel à [IHostSyncManager::CreateMonitorEvent](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-createmonitorevent-method.md).</span><span class="sxs-lookup"><span data-stu-id="59249-127">The cookie is associated with a monitor when it is created by using a call to [IHostSyncManager::CreateMonitorEvent](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-createmonitorevent-method.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="59249-128">Un appel pour libérer l’événement sous-jacent de l’analyseur peut se bloquer, mais pas blocage — si un appel à cette méthode est actuellement en vigueur sur le cookie associé à ce moniteur.</span><span class="sxs-lookup"><span data-stu-id="59249-128">A call to release the event underlying the monitor might block—but will not deadlock—if a call to this method is currently in effect on the cookie associated with that monitor.</span></span> <span data-ttu-id="59249-129">Autres tâches peuvent également se bloquer si elles tentent d’acquérir ce moniteur.</span><span class="sxs-lookup"><span data-stu-id="59249-129">Other tasks might also block if they attempt to acquire this monitor.</span></span>  
  
 <span data-ttu-id="59249-130">`GetMonitorOwner` Retourne toujours immédiatement et peut être appelée à tout moment après un appel à `CreateMonitorEvent`.</span><span class="sxs-lookup"><span data-stu-id="59249-130">`GetMonitorOwner` always returns immediately and can be called any time after a call to `CreateMonitorEvent`.</span></span> <span data-ttu-id="59249-131">L’ordinateur hôte n’a pas besoin d’attendre une tâche est en attente sur l’événement.</span><span class="sxs-lookup"><span data-stu-id="59249-131">The host does not need to wait until a task is waiting on the event.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="59249-132">Spécifications</span><span class="sxs-lookup"><span data-stu-id="59249-132">Requirements</span></span>  
 <span data-ttu-id="59249-133">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="59249-133">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="59249-134">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="59249-134">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="59249-135">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="59249-135">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="59249-136">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="59249-136">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="59249-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59249-137">See Also</span></span>  
 [<span data-ttu-id="59249-138">ICLRSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="59249-138">ICLRSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)  
 [<span data-ttu-id="59249-139">IHostSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="59249-139">IHostSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)
