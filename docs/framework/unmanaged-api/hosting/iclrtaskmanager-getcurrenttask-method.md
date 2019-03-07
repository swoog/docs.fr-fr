---
title: ICLRTaskManager::GetCurrentTask, méthode
ms.date: 03/30/2017
api_name:
- ICLRTaskManager.GetCurrentTask
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTaskManager::GetCurrentTask
helpviewer_keywords:
- GetCurrentTask method, ICLRTaskManager interface [.NET Framework hosting]
- ICLRTaskManager::GetCurrentTask method [.NET Framework hosting]
ms.assetid: c0b82a9f-edc6-4878-9c81-48de53c02142
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c2efc8e0b47e68e53858bc949e6f0d0ca1352c7e
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57501581"
---
# <a name="iclrtaskmanagergetcurrenttask-method"></a><span data-ttu-id="a90b2-102">ICLRTaskManager::GetCurrentTask, méthode</span><span class="sxs-lookup"><span data-stu-id="a90b2-102">ICLRTaskManager::GetCurrentTask Method</span></span>
<span data-ttu-id="a90b2-103">Obtient le [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) instance en cours d’exécution sur le thread de système d’exploitation d'où provenance l’appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="a90b2-103">Gets the [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) instance that is currently running on the operating system thread from which the method call originated.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a90b2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a90b2-104">Syntax</span></span>  
  
```  
HRESULT GetCurrentTask (  
    [out] ICLRTask **ppTask  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a90b2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a90b2-105">Parameters</span></span>  
 `ppTask`  
 <span data-ttu-id="a90b2-106">[out] Un pointeur vers l’adresse d’un `ICLRTask` instance en cours d’exécution sur le thread de système d’exploitation à partir duquel provient l’appel, ou null si aucune tâche n’est en cours d’exécution sur ce thread.</span><span class="sxs-lookup"><span data-stu-id="a90b2-106">[out] A pointer to the address of an `ICLRTask` instance that is currently executing on the operating system thread from which the call originated, or null if no task is currently executing on this thread.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a90b2-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a90b2-107">Return Value</span></span>  
  
|<span data-ttu-id="a90b2-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="a90b2-108">HRESULT</span></span>|<span data-ttu-id="a90b2-109">Description</span><span class="sxs-lookup"><span data-stu-id="a90b2-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="a90b2-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="a90b2-110">S_OK</span></span>|<span data-ttu-id="a90b2-111">La méthode a été retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="a90b2-111">The method returned successfully.</span></span>|  
|<span data-ttu-id="a90b2-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="a90b2-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="a90b2-113">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="a90b2-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="a90b2-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a90b2-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="a90b2-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="a90b2-115">The call timed out.</span></span>|  
|<span data-ttu-id="a90b2-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="a90b2-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="a90b2-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="a90b2-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="a90b2-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="a90b2-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="a90b2-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="a90b2-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="a90b2-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="a90b2-120">E_FAIL</span></span>|<span data-ttu-id="a90b2-121">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="a90b2-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="a90b2-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="a90b2-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="a90b2-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="a90b2-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a90b2-124">Notes</span><span class="sxs-lookup"><span data-stu-id="a90b2-124">Remarks</span></span>  
 <span data-ttu-id="a90b2-125">Le `ICLRTask` de l’instance qui le `ppTask` paramètre pointe représente la tâche en cours d’exécution pour le CLR.</span><span class="sxs-lookup"><span data-stu-id="a90b2-125">The `ICLRTask` instance that the `ppTask` parameter points to represents the currently executing task for the CLR.</span></span> <span data-ttu-id="a90b2-126">Le `ICLRTask` instance est associée à un correspondant [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) instance qui représente la tâche pour l’hôte.</span><span class="sxs-lookup"><span data-stu-id="a90b2-126">The `ICLRTask` instance is associated with a corresponding [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) instance that represents the task for the host.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a90b2-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a90b2-127">Requirements</span></span>  
 <span data-ttu-id="a90b2-128">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a90b2-128">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a90b2-129">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a90b2-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a90b2-130">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a90b2-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a90b2-131">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a90b2-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a90b2-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a90b2-132">See also</span></span>
- [<span data-ttu-id="a90b2-133">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="a90b2-133">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="a90b2-134">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="a90b2-134">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="a90b2-135">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="a90b2-135">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="a90b2-136">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="a90b2-136">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
