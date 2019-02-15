---
title: IHostTaskManager::ReverseLeaveRuntime, méthode
ms.date: 03/30/2017
api_name:
- IHostTaskManager.ReverseLeaveRuntime
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::ReverseLeaveRuntime
helpviewer_keywords:
- IHostTaskManager::ReverseLeaveRuntime method [.NET Framework hosting]
- ReverseLeaveRuntime method [.NET Framework hosting]
ms.assetid: 4837d398-16a1-4e32-902c-022cd1aad3ca
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0a7abcda5ecf56602e884e4d66e1c6900f17b4c6
ms.sourcegitcommit: bef803e2025642df39f2f1e046767d89031e0304
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56305881"
---
# <a name="ihosttaskmanagerreverseleaveruntime-method"></a><span data-ttu-id="b6ff8-102">IHostTaskManager::ReverseLeaveRuntime, méthode</span><span class="sxs-lookup"><span data-stu-id="b6ff8-102">IHostTaskManager::ReverseLeaveRuntime Method</span></span>
<span data-ttu-id="b6ff8-103">Avertit l’hôte que le contrôle est en laissant le common language runtime (CLR) et une fonction non managée qui a été, à son tour, appelée à partir du code managé.</span><span class="sxs-lookup"><span data-stu-id="b6ff8-103">Notifies the host that control is leaving the common language runtime (CLR) and entering an unmanaged function that was, in turn, called from managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b6ff8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6ff8-104">Syntax</span></span>  
  
```  
HRESULT ReverseLeaveRuntime ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="b6ff8-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b6ff8-105">Return Value</span></span>  
  
|<span data-ttu-id="b6ff8-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="b6ff8-106">HRESULT</span></span>|<span data-ttu-id="b6ff8-107">Description</span><span class="sxs-lookup"><span data-stu-id="b6ff8-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="b6ff8-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="b6ff8-108">S_OK</span></span>|<span data-ttu-id="b6ff8-109">`ReverseLeaveRuntime` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="b6ff8-109">`ReverseLeaveRuntime` returned successfully.</span></span>|  
|<span data-ttu-id="b6ff8-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="b6ff8-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="b6ff8-111">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="b6ff8-111">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="b6ff8-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b6ff8-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="b6ff8-113">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="b6ff8-113">The call timed out.</span></span>|  
|<span data-ttu-id="b6ff8-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="b6ff8-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="b6ff8-115">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="b6ff8-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="b6ff8-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="b6ff8-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="b6ff8-117">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="b6ff8-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="b6ff8-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="b6ff8-118">E_FAIL</span></span>|<span data-ttu-id="b6ff8-119">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="b6ff8-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="b6ff8-120">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="b6ff8-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="b6ff8-121">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="b6ff8-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="b6ff8-122">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="b6ff8-122">E_OUTOFMEMORY</span></span>|<span data-ttu-id="b6ff8-123">Mémoire est insuffisante pour terminer l’allocation de la ressource demandée.</span><span class="sxs-lookup"><span data-stu-id="b6ff8-123">Not enough memory is available to complete the requested resource allocation.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b6ff8-124">Notes</span><span class="sxs-lookup"><span data-stu-id="b6ff8-124">Remarks</span></span>  
 <span data-ttu-id="b6ff8-125">Le CLR appelle `ReverseLeaveRuntime` pour informer l’hôte que la tâche en cours d’exécution retourne le contrôle à une fonction non managée qui a été, à son tour, appelée à partir de code géré via la plateforme appeler.</span><span class="sxs-lookup"><span data-stu-id="b6ff8-125">The CLR calls `ReverseLeaveRuntime` to inform the host that the currently executing task is returning control to an unmanaged function that was, in turn, called from managed code through platform invoke.</span></span> <span data-ttu-id="b6ff8-126">Chaque appel à `ReverseLeaveRuntime` correspond à un appel correspondant à [ReverseEnterRuntime](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-reverseenterruntime-method.md).</span><span class="sxs-lookup"><span data-stu-id="b6ff8-126">Each call to `ReverseLeaveRuntime` matches a corresponding call to [ReverseEnterRuntime](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-reverseenterruntime-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b6ff8-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b6ff8-127">Requirements</span></span>  
 <span data-ttu-id="b6ff8-128">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b6ff8-128">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b6ff8-129">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="b6ff8-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b6ff8-130">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b6ff8-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b6ff8-131">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b6ff8-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b6ff8-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6ff8-132">See also</span></span>
- [<span data-ttu-id="b6ff8-133">CallNeedsHostHook, méthode</span><span class="sxs-lookup"><span data-stu-id="b6ff8-133">CallNeedsHostHook Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-callneedshosthook-method.md)
- [<span data-ttu-id="b6ff8-134">EnterRuntime, méthode</span><span class="sxs-lookup"><span data-stu-id="b6ff8-134">EnterRuntime Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-enterruntime-method.md)
- [<span data-ttu-id="b6ff8-135">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="b6ff8-135">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="b6ff8-136">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="b6ff8-136">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="b6ff8-137">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="b6ff8-137">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="b6ff8-138">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="b6ff8-138">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
- [<span data-ttu-id="b6ff8-139">LeaveRuntime, méthode</span><span class="sxs-lookup"><span data-stu-id="b6ff8-139">LeaveRuntime Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-leaveruntime-method.md)
- <span data-ttu-id="b6ff8-140">[Présentation détaillée de l’appel de code non managé](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/0h9e9t7d(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="b6ff8-140">[A Closer Look at Platform Invoke](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/0h9e9t7d(v=vs.100))</span></span>
