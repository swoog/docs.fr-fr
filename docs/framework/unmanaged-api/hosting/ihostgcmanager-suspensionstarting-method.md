---
title: IHostGCManager::SuspensionStarting, méthode
ms.date: 03/30/2017
api_name:
- IHostGCManager.SuspensionStarting
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostGCManager::SuspensionStarting
helpviewer_keywords:
- SuspensionStarting method, IHostGCManager interface [.NET Framework hosting]
- IHostGCManager::SuspensionStarting method [.NET Framework hosting]
ms.assetid: c381f524-94cf-4fa2-9298-50f847a03431
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6a84da2a337554873e94b47eb51916088edbb5a6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33439031"
---
# <a name="ihostgcmanagersuspensionstarting-method"></a><span data-ttu-id="83691-102">IHostGCManager::SuspensionStarting, méthode</span><span class="sxs-lookup"><span data-stu-id="83691-102">IHostGCManager::SuspensionStarting Method</span></span>
<span data-ttu-id="83691-103">Avertit l’hôte que le common language runtime (CLR) interrompt l’exécution de tâches pour effectuer un garbage collection.</span><span class="sxs-lookup"><span data-stu-id="83691-103">Notifies the host that the common language runtime (CLR) is suspending execution of tasks, to perform a garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="83691-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83691-104">Syntax</span></span>  
  
```  
HRESULT SuspensionStarting ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="83691-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="83691-105">Return Value</span></span>  
  
|<span data-ttu-id="83691-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="83691-106">HRESULT</span></span>|<span data-ttu-id="83691-107">Description</span><span class="sxs-lookup"><span data-stu-id="83691-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="83691-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="83691-108">S_OK</span></span>|<span data-ttu-id="83691-109">`SuspensionStarting` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="83691-109">`SuspensionStarting` returned successfully.</span></span>|  
|<span data-ttu-id="83691-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="83691-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="83691-111">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="83691-111">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="83691-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="83691-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="83691-113">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="83691-113">The call timed out.</span></span>|  
|<span data-ttu-id="83691-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="83691-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="83691-115">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="83691-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="83691-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="83691-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="83691-117">Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="83691-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="83691-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="83691-118">E_FAIL</span></span>|<span data-ttu-id="83691-119">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="83691-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="83691-120">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="83691-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="83691-121">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="83691-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="83691-122">Notes</span><span class="sxs-lookup"><span data-stu-id="83691-122">Remarks</span></span>  
 <span data-ttu-id="83691-123">Le CLR appelle `SuspensionStarting` pour informer l’hôte que le garbage collection est en cours.</span><span class="sxs-lookup"><span data-stu-id="83691-123">The CLR calls `SuspensionStarting` to inform the host that garbage collection is occurring.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="83691-124">Ne replanifiez pas cette tâche.</span><span class="sxs-lookup"><span data-stu-id="83691-124">Do not reschedule this task.</span></span> <span data-ttu-id="83691-125">L’hôte doit replanifier une tâche lorsque [ThreadIsBlockingForSuspension](../../../../docs/framework/unmanaged-api/hosting/ihostgcmanager-threadisblockingforsuspension-method.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="83691-125">The host must reschedule a task when [ThreadIsBlockingForSuspension](../../../../docs/framework/unmanaged-api/hosting/ihostgcmanager-threadisblockingforsuspension-method.md) is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="83691-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="83691-126">Requirements</span></span>  
 <span data-ttu-id="83691-127">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="83691-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="83691-128">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="83691-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="83691-129">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="83691-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="83691-130">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="83691-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="83691-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83691-131">See Also</span></span>  
 [<span data-ttu-id="83691-132">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="83691-132">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)  
 [<span data-ttu-id="83691-133">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="83691-133">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)  
 [<span data-ttu-id="83691-134">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="83691-134">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)  
 [<span data-ttu-id="83691-135">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="83691-135">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)  
 [<span data-ttu-id="83691-136">IHostGCManager, interface</span><span class="sxs-lookup"><span data-stu-id="83691-136">IHostGCManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostgcmanager-interface.md)
