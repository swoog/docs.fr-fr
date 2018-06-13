---
title: IHostGCManager::ThreadIsBlockingForSuspension, méthode
ms.date: 03/30/2017
api_name:
- IHostGCManager.ThreadIsBlockingForSuspension
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostGCManager::ThreadIsBlockingForSuspension
helpviewer_keywords:
- IHostGCManager::ThreadIsBlockingForSuspension method [.NET Framework hosting]
- ThreadIsBlockingForSuspension method [.NET Framework hosting]
ms.assetid: 2657d45d-26d2-4d0a-8473-32b652e3321d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 85921156860f52eb2a898e6be356e191c2a4f02d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33439268"
---
# <a name="ihostgcmanagerthreadisblockingforsuspension-method"></a><span data-ttu-id="189bc-102">IHostGCManager::ThreadIsBlockingForSuspension, méthode</span><span class="sxs-lookup"><span data-stu-id="189bc-102">IHostGCManager::ThreadIsBlockingForSuspension Method</span></span>
<span data-ttu-id="189bc-103">Avertit l’hôte que le thread à partir de laquelle l’appel de méthode a été effectué sur le point de bloquer pour un garbage collection.</span><span class="sxs-lookup"><span data-stu-id="189bc-103">Notifies the host that the thread from which the method call was made is about to block for a garbage collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="189bc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="189bc-104">Syntax</span></span>  
  
```  
HRESULT ThreadIsBlockingForSuspension ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="189bc-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="189bc-105">Return Value</span></span>  
  
|<span data-ttu-id="189bc-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="189bc-106">HRESULT</span></span>|<span data-ttu-id="189bc-107">Description</span><span class="sxs-lookup"><span data-stu-id="189bc-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="189bc-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="189bc-108">S_OK</span></span>|<span data-ttu-id="189bc-109">`ThreadIsBlockingForSuspension` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="189bc-109">`ThreadIsBlockingForSuspension` returned successfully.</span></span>|  
|<span data-ttu-id="189bc-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="189bc-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="189bc-111">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="189bc-111">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="189bc-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="189bc-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="189bc-113">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="189bc-113">The call timed out.</span></span>|  
|<span data-ttu-id="189bc-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="189bc-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="189bc-115">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="189bc-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="189bc-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="189bc-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="189bc-117">Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="189bc-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="189bc-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="189bc-118">E_FAIL</span></span>|<span data-ttu-id="189bc-119">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="189bc-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="189bc-120">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="189bc-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="189bc-121">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="189bc-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="189bc-122">Notes</span><span class="sxs-lookup"><span data-stu-id="189bc-122">Remarks</span></span>  
 <span data-ttu-id="189bc-123">Le CLR appelle généralement la `ThreadIsBlockForSuspension` méthode en vue d’un garbage collection, pour permettre à l’hôte de replanifier le thread pour les tâches non managées.</span><span class="sxs-lookup"><span data-stu-id="189bc-123">The CLR typically calls the `ThreadIsBlockForSuspension` method in preparation for a garbage collection, to give the host an opportunity to reschedule the thread for unmanaged tasks.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="189bc-124">L’hôte peut replanifier des tâches uniquement après un appel à `ThreadIsBlockingForSuspension`.</span><span class="sxs-lookup"><span data-stu-id="189bc-124">The host can reschedule tasks only after a call to `ThreadIsBlockingForSuspension`.</span></span> <span data-ttu-id="189bc-125">Après le runtime appelle [SuspensionStarting](../../../../docs/framework/unmanaged-api/hosting/ihostgcmanager-suspensionstarting-method.md), l’hôte ne doit pas replanifier une tâche.</span><span class="sxs-lookup"><span data-stu-id="189bc-125">After the runtime calls [SuspensionStarting](../../../../docs/framework/unmanaged-api/hosting/ihostgcmanager-suspensionstarting-method.md), the host must not reschedule a task.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="189bc-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="189bc-126">Requirements</span></span>  
 <span data-ttu-id="189bc-127">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="189bc-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="189bc-128">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="189bc-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="189bc-129">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="189bc-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="189bc-130">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="189bc-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="189bc-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="189bc-131">See Also</span></span>  
 [<span data-ttu-id="189bc-132">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="189bc-132">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)  
 [<span data-ttu-id="189bc-133">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="189bc-133">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)  
 [<span data-ttu-id="189bc-134">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="189bc-134">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)  
 [<span data-ttu-id="189bc-135">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="189bc-135">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)  
 [<span data-ttu-id="189bc-136">IHostGCManager, interface</span><span class="sxs-lookup"><span data-stu-id="189bc-136">IHostGCManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostgcmanager-interface.md)
