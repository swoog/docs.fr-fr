---
title: IHostTask::Join, méthode
ms.date: 03/30/2017
api_name:
- IHostTask.Join
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTask::Join
helpviewer_keywords:
- IHostTask::Join method [.NET Framework hosting]
- Join method, IHostTask interface [.NET Framework hosting]
ms.assetid: 2cffcc52-19e0-4ced-a440-fc7375078ac9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0320e365daf03703a46eb48aac74e301d47520ed
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33442281"
---
# <a name="ihosttaskjoin-method"></a><span data-ttu-id="bd765-102">IHostTask::Join, méthode</span><span class="sxs-lookup"><span data-stu-id="bd765-102">IHostTask::Join Method</span></span>
<span data-ttu-id="bd765-103">Bloque la tâche appelante jusqu'à ce que la tâche représentée par le [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) fin de l’instance, l’intervalle de temps spécifié est dépassé, ou [IHostTask::Alert](../../../../docs/framework/unmanaged-api/hosting/ihosttask-alert-method.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="bd765-103">Blocks the calling task until the task represented by the current [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) instance completes, the specified time interval elapses, or [IHostTask::Alert](../../../../docs/framework/unmanaged-api/hosting/ihosttask-alert-method.md) is called.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bd765-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd765-104">Syntax</span></span>  
  
```  
HRESULT Join (  
    [in] DWORD milliseconds,  
    [in] DWORD option  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="bd765-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bd765-105">Parameters</span></span>  
 `milliseconds`  
 <span data-ttu-id="bd765-106">[in] L’intervalle de temps, en millisecondes, pour attendre la fin de la tâche.</span><span class="sxs-lookup"><span data-stu-id="bd765-106">[in] The time interval, in milliseconds, to wait for the task to terminate.</span></span> <span data-ttu-id="bd765-107">Si cet intervalle est écoulé avant que la tâche se termine, la tâche appelante se débloque.</span><span class="sxs-lookup"><span data-stu-id="bd765-107">If this interval elapses before the task terminates, the calling task unblocks.</span></span>  
  
 `option`  
 <span data-ttu-id="bd765-108">[in] Parmi les [WAIT_OPTION](../../../../docs/framework/unmanaged-api/hosting/wait-option-enumeration.md) valeurs.</span><span class="sxs-lookup"><span data-stu-id="bd765-108">[in] One of the [WAIT_OPTION](../../../../docs/framework/unmanaged-api/hosting/wait-option-enumeration.md) values.</span></span> <span data-ttu-id="bd765-109">Une valeur WAIT_ALERTABLE indique l’ordinateur hôte pour réactiver la tâche si `Alert` est appelée avant que `milliseconds` s’écoule.</span><span class="sxs-lookup"><span data-stu-id="bd765-109">A value of WAIT_ALERTABLE instructs the host to wake the task if `Alert` is called before `milliseconds` elapses.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="bd765-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="bd765-110">Return Value</span></span>  
  
|<span data-ttu-id="bd765-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="bd765-111">HRESULT</span></span>|<span data-ttu-id="bd765-112">Description</span><span class="sxs-lookup"><span data-stu-id="bd765-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="bd765-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="bd765-113">S_OK</span></span>|<span data-ttu-id="bd765-114">`Join` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="bd765-114">`Join` returned successfully.</span></span>|  
|<span data-ttu-id="bd765-115">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="bd765-115">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="bd765-116">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="bd765-116">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="bd765-117">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="bd765-117">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="bd765-118">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="bd765-118">The call timed out.</span></span>|  
|<span data-ttu-id="bd765-119">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="bd765-119">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="bd765-120">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="bd765-120">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="bd765-121">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="bd765-121">HOST_E_ABANDONED</span></span>|<span data-ttu-id="bd765-122">Un événement a été annulé alors qu’un thread bloqué ou une fibre attendait, ou en cours `IHostTask` instance n’est pas associée à une tâche.</span><span class="sxs-lookup"><span data-stu-id="bd765-122">An event was canceled while a blocked thread or fiber was waiting on it, or the current `IHostTask` instance is not associated with a task.</span></span>|  
|<span data-ttu-id="bd765-123">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="bd765-123">E_FAIL</span></span>|<span data-ttu-id="bd765-124">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="bd765-124">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="bd765-125">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="bd765-125">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="bd765-126">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="bd765-126">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="bd765-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bd765-127">Requirements</span></span>  
 <span data-ttu-id="bd765-128">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bd765-128">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bd765-129">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="bd765-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="bd765-130">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bd765-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bd765-131">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bd765-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bd765-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd765-132">See Also</span></span>  
 [<span data-ttu-id="bd765-133">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="bd765-133">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)  
 [<span data-ttu-id="bd765-134">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="bd765-134">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)  
 [<span data-ttu-id="bd765-135">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="bd765-135">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)  
 [<span data-ttu-id="bd765-136">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="bd765-136">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)  
 [<span data-ttu-id="bd765-137">WAIT_OPTION, énumération</span><span class="sxs-lookup"><span data-stu-id="bd765-137">WAIT_OPTION Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/wait-option-enumeration.md)
