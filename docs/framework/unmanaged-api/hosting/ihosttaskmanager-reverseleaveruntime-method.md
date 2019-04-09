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
ms.openlocfilehash: 4cd3012d966c777749eb800b8986974a4e8d401f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59154165"
---
# <a name="ihosttaskmanagerreverseleaveruntime-method"></a><span data-ttu-id="d22b5-102">IHostTaskManager::ReverseLeaveRuntime, méthode</span><span class="sxs-lookup"><span data-stu-id="d22b5-102">IHostTaskManager::ReverseLeaveRuntime Method</span></span>
<span data-ttu-id="d22b5-103">Avertit l’hôte que le contrôle est en laissant le common language runtime (CLR) et une fonction non managée qui a été, à son tour, appelée à partir du code managé.</span><span class="sxs-lookup"><span data-stu-id="d22b5-103">Notifies the host that control is leaving the common language runtime (CLR) and entering an unmanaged function that was, in turn, called from managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d22b5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d22b5-104">Syntax</span></span>  
  
```  
HRESULT ReverseLeaveRuntime ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="d22b5-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d22b5-105">Return Value</span></span>  
  
|<span data-ttu-id="d22b5-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="d22b5-106">HRESULT</span></span>|<span data-ttu-id="d22b5-107">Description</span><span class="sxs-lookup"><span data-stu-id="d22b5-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="d22b5-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="d22b5-108">S_OK</span></span>|`ReverseLeaveRuntime` <span data-ttu-id="d22b5-109">retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="d22b5-109">returned successfully.</span></span>|  
|<span data-ttu-id="d22b5-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="d22b5-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="d22b5-111">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="d22b5-111">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="d22b5-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="d22b5-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="d22b5-113">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="d22b5-113">The call timed out.</span></span>|  
|<span data-ttu-id="d22b5-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="d22b5-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="d22b5-115">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="d22b5-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="d22b5-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="d22b5-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="d22b5-117">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="d22b5-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="d22b5-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="d22b5-118">E_FAIL</span></span>|<span data-ttu-id="d22b5-119">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d22b5-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="d22b5-120">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="d22b5-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="d22b5-121">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="d22b5-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="d22b5-122">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="d22b5-122">E_OUTOFMEMORY</span></span>|<span data-ttu-id="d22b5-123">Mémoire est insuffisante pour terminer l’allocation de la ressource demandée.</span><span class="sxs-lookup"><span data-stu-id="d22b5-123">Not enough memory is available to complete the requested resource allocation.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d22b5-124">Notes</span><span class="sxs-lookup"><span data-stu-id="d22b5-124">Remarks</span></span>  
 <span data-ttu-id="d22b5-125">Le CLR appelle `ReverseLeaveRuntime` pour informer l’hôte que la tâche en cours d’exécution retourne le contrôle à une fonction non managée qui a été, à son tour, appelée à partir de code géré via la plateforme appeler.</span><span class="sxs-lookup"><span data-stu-id="d22b5-125">The CLR calls `ReverseLeaveRuntime` to inform the host that the currently executing task is returning control to an unmanaged function that was, in turn, called from managed code through platform invoke.</span></span> <span data-ttu-id="d22b5-126">Chaque appel à `ReverseLeaveRuntime` correspond à un appel correspondant à [ReverseEnterRuntime](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-reverseenterruntime-method.md).</span><span class="sxs-lookup"><span data-stu-id="d22b5-126">Each call to `ReverseLeaveRuntime` matches a corresponding call to [ReverseEnterRuntime](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-reverseenterruntime-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d22b5-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d22b5-127">Requirements</span></span>  
 <span data-ttu-id="d22b5-128">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d22b5-128">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d22b5-129">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="d22b5-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="d22b5-130">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d22b5-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="d22b5-131">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="d22b5-131">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="d22b5-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d22b5-132">See also</span></span>

- [<span data-ttu-id="d22b5-133">CallNeedsHostHook, méthode</span><span class="sxs-lookup"><span data-stu-id="d22b5-133">CallNeedsHostHook Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-callneedshosthook-method.md)
- [<span data-ttu-id="d22b5-134">EnterRuntime, méthode</span><span class="sxs-lookup"><span data-stu-id="d22b5-134">EnterRuntime Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-enterruntime-method.md)
- [<span data-ttu-id="d22b5-135">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="d22b5-135">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="d22b5-136">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="d22b5-136">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="d22b5-137">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="d22b5-137">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="d22b5-138">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="d22b5-138">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
- [<span data-ttu-id="d22b5-139">LeaveRuntime, méthode</span><span class="sxs-lookup"><span data-stu-id="d22b5-139">LeaveRuntime Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-leaveruntime-method.md)
- [<span data-ttu-id="d22b5-140">Présentation détaillée de l'appel de code non managé</span><span class="sxs-lookup"><span data-stu-id="d22b5-140">A Closer Look at Platform Invoke</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/0h9e9t7d(v=vs.100))
