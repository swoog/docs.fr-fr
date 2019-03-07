---
title: IHostTaskManager::LeaveRuntime, méthode
ms.date: 03/30/2017
api_name:
- IHostTaskManager.LeaveRuntime
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::LeaveRuntime
helpviewer_keywords:
- IHostTaskManager::LeaveRuntime method [.NET Framework hosting]
- LeaveRuntime method [.NET Framework hosting]
ms.assetid: 43689cc4-e48e-46e5-a22d-bafd768b8759
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2059657a6f4543ee29d795ecae7b93b72876fdf4
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57474629"
---
# <a name="ihosttaskmanagerleaveruntime-method"></a><span data-ttu-id="d7ada-102">IHostTaskManager::LeaveRuntime, méthode</span><span class="sxs-lookup"><span data-stu-id="d7ada-102">IHostTaskManager::LeaveRuntime Method</span></span>
<span data-ttu-id="d7ada-103">Avertit l’hôte que la tâche en cours d’exécution est sur le point de quitter le common language runtime (CLR) et entrez le code non managé.</span><span class="sxs-lookup"><span data-stu-id="d7ada-103">Notifies the host that the currently executing task is about to leave the common language runtime (CLR) and enter unmanaged code.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="d7ada-104">Un appel correspondant à [IHostTaskManager::EnterRuntime](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-enterruntime-method.md) avertit l’hôte que la tâche en cours d’exécution du code managé.</span><span class="sxs-lookup"><span data-stu-id="d7ada-104">A corresponding call to [IHostTaskManager::EnterRuntime](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-enterruntime-method.md) notifies the host that the currently executing task is reentering managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d7ada-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7ada-105">Syntax</span></span>  
  
```  
HRESULT LeaveRuntime (  
    [in] SIZE_T target  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d7ada-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7ada-106">Parameters</span></span>  
 `target`  
 <span data-ttu-id="d7ada-107">[in] L’adresse dans le fichier exécutable portable mappé de la fonction non managée à appeler.</span><span class="sxs-lookup"><span data-stu-id="d7ada-107">[in] The address within the mapped portable executable file of the unmanaged function to be called.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d7ada-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d7ada-108">Return Value</span></span>  
  
|<span data-ttu-id="d7ada-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="d7ada-109">HRESULT</span></span>|<span data-ttu-id="d7ada-110">Description</span><span class="sxs-lookup"><span data-stu-id="d7ada-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="d7ada-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="d7ada-111">S_OK</span></span>|<span data-ttu-id="d7ada-112">`LeaveRuntime` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="d7ada-112">`LeaveRuntime` returned successfully.</span></span>|  
|<span data-ttu-id="d7ada-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="d7ada-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="d7ada-114">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="d7ada-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="d7ada-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="d7ada-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="d7ada-116">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="d7ada-116">The call timed out.</span></span>|  
|<span data-ttu-id="d7ada-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="d7ada-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="d7ada-118">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="d7ada-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="d7ada-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="d7ada-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="d7ada-120">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="d7ada-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="d7ada-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="d7ada-121">E_FAIL</span></span>|<span data-ttu-id="d7ada-122">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d7ada-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="d7ada-123">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="d7ada-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="d7ada-124">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="d7ada-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="d7ada-125">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="d7ada-125">E_OUTOFMEMORY</span></span>|<span data-ttu-id="d7ada-126">Mémoire est insuffisante pour terminer l’allocation demandée.</span><span class="sxs-lookup"><span data-stu-id="d7ada-126">Not enough memory is available to complete the requested allocation.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d7ada-127">Notes</span><span class="sxs-lookup"><span data-stu-id="d7ada-127">Remarks</span></span>  
 <span data-ttu-id="d7ada-128">Séquences d’appel vers et à partir de code non managé peuvent être imbriquées.</span><span class="sxs-lookup"><span data-stu-id="d7ada-128">Call sequences to and from unmanaged code can be nested.</span></span> <span data-ttu-id="d7ada-129">Par exemple, la liste ci-dessous décrit une situation hypothétique dans laquelle la séquence d’appels à `LeaveRuntime`, [IHostTaskManager::ReverseEnterRuntime](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-reverseenterruntime-method.md), [IHostTaskManager::ReverseLeaveRuntime](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-reverseleaveruntime-method.md), et `IHostTaskManager::EnterRuntime` permet à l’hôte identifier des couches imbriquées.</span><span class="sxs-lookup"><span data-stu-id="d7ada-129">For example, the list below describes a hypothetical situation in which the sequence of calls to `LeaveRuntime`, [IHostTaskManager::ReverseEnterRuntime](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-reverseenterruntime-method.md), [IHostTaskManager::ReverseLeaveRuntime](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-reverseleaveruntime-method.md), and `IHostTaskManager::EnterRuntime` allows the host to identify the nested layers.</span></span>  
  
|<span data-ttu-id="d7ada-130">Action</span><span class="sxs-lookup"><span data-stu-id="d7ada-130">Action</span></span>|<span data-ttu-id="d7ada-131">Appel de méthode correspondant</span><span class="sxs-lookup"><span data-stu-id="d7ada-131">Corresponding Method Call</span></span>|  
|------------|-------------------------------|  
|<span data-ttu-id="d7ada-132">Un managé Visual Basic exécutable appelle une fonction non managée écrite en C à l’aide de plateforme appeler.</span><span class="sxs-lookup"><span data-stu-id="d7ada-132">A managed Visual Basic executable calls an unmanaged function written in C by using platform invoke.</span></span>|`IHostTaskManager::LeaveRuntime`|  
|<span data-ttu-id="d7ada-133">La fonction C non managée appelle une méthode dans une DLL managée écrite C#.</span><span class="sxs-lookup"><span data-stu-id="d7ada-133">The unmanaged C function calls a method in a managed DLL written in C#.</span></span>|`IHostTaskManager::ReverseEnterRuntime`|  
|<span data-ttu-id="d7ada-134">Managé C# fonction appelle une autre fonction non managée écrite en C, également à l’aide de la plateforme appellent.</span><span class="sxs-lookup"><span data-stu-id="d7ada-134">The managed C# function calls another unmanaged function written in C, also using platform invoke.</span></span>|`IHostTaskManager::LeaveRuntime`|  
|<span data-ttu-id="d7ada-135">La deuxième fonction non managée retourne l’exécution à le C# (fonction).</span><span class="sxs-lookup"><span data-stu-id="d7ada-135">The second unmanaged function returns execution to the C# function.</span></span>|`IHostTaskManager::EnterRuntime`|  
|<span data-ttu-id="d7ada-136">Le C# fonction retourne l’exécution à la première fonction non managée.</span><span class="sxs-lookup"><span data-stu-id="d7ada-136">The C# function returns execution to the first unmanaged function.</span></span>|`IHostTaskManager::ReverseLeaveRuntime`|  
|<span data-ttu-id="d7ada-137">La première fonction non managée retourne l’exécution au programme Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d7ada-137">The first unmanaged function returns execution to the Visual Basic program.</span></span>|`IHostTaskManager::EnterRuntime`|  
  
## <a name="requirements"></a><span data-ttu-id="d7ada-138">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d7ada-138">Requirements</span></span>  
 <span data-ttu-id="d7ada-139">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d7ada-139">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d7ada-140">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="d7ada-140">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="d7ada-141">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d7ada-141">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d7ada-142">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d7ada-142">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d7ada-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7ada-143">See also</span></span>
- [<span data-ttu-id="d7ada-144">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="d7ada-144">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="d7ada-145">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="d7ada-145">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="d7ada-146">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="d7ada-146">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="d7ada-147">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="d7ada-147">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
