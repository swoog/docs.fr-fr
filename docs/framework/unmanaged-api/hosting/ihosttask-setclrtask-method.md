---
title: IHostTask::SetCLRTask, méthode
ms.date: 03/30/2017
api_name:
- IHostTask.SetCLRTask
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTask::SetCLRTask
helpviewer_keywords:
- SetCLRTask method [.NET Framework hosting]
- IHostTask::SetCLRTask method [.NET Framework hosting]
ms.assetid: e9d39c80-41a1-49e7-bb5e-ea3433bfb5d7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b0220a0699e7325c6d81ba3ad4627176640937dd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59131961"
---
# <a name="ihosttasksetclrtask-method"></a><span data-ttu-id="0c018-102">IHostTask::SetCLRTask, méthode</span><span class="sxs-lookup"><span data-stu-id="0c018-102">IHostTask::SetCLRTask Method</span></span>
<span data-ttu-id="0c018-103">Associe un `ICLRTask` instance avec actuel [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) instance.</span><span class="sxs-lookup"><span data-stu-id="0c018-103">Associates an `ICLRTask` instance with the current [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0c018-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c018-104">Syntax</span></span>  
  
```  
HRESULT SetCLRTask (  
    [in] ICLRTask *pCLRTask  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0c018-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c018-105">Parameters</span></span>  
 `pCLRTask`  
 <span data-ttu-id="0c018-106">[in] Un pointeur d’interface vers le `ICLRTask` instance à associer à l’actuel `IHostTask` instance.</span><span class="sxs-lookup"><span data-stu-id="0c018-106">[in] An interface pointer to the `ICLRTask` instance to be associated with the current `IHostTask` instance.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0c018-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0c018-107">Return Value</span></span>  
  
|<span data-ttu-id="0c018-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="0c018-108">HRESULT</span></span>|<span data-ttu-id="0c018-109">Description</span><span class="sxs-lookup"><span data-stu-id="0c018-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="0c018-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c018-110">S_OK</span></span>|<span data-ttu-id="0c018-111">`SetCLRTask` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="0c018-111">`SetCLRTask` returned successfully.</span></span>|  
|<span data-ttu-id="0c018-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="0c018-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="0c018-113">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="0c018-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="0c018-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="0c018-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="0c018-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="0c018-115">The call timed out.</span></span>|  
|<span data-ttu-id="0c018-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="0c018-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="0c018-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="0c018-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="0c018-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="0c018-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="0c018-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="0c018-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="0c018-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0c018-120">E_FAIL</span></span>|<span data-ttu-id="0c018-121">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0c018-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="0c018-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="0c018-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="0c018-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="0c018-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0c018-124">Notes</span><span class="sxs-lookup"><span data-stu-id="0c018-124">Remarks</span></span>  
 <span data-ttu-id="0c018-125">Le CLR appelle `SetCLRTask` pour associer un `ICLRTask` instance avec actuel `IHostTask` instance, ce qui a été créé par un appel à [IHostTaskManager::CreateTask](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-createtask-method.md).</span><span class="sxs-lookup"><span data-stu-id="0c018-125">The CLR calls `SetCLRTask` to associate an `ICLRTask` instance with the current `IHostTask` instance, which was created by a call to [IHostTaskManager::CreateTask](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-createtask-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0c018-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c018-126">Requirements</span></span>  
 <span data-ttu-id="0c018-127">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0c018-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0c018-128">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="0c018-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="0c018-129">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0c018-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0c018-130">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0c018-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0c018-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c018-131">See also</span></span>

- [<span data-ttu-id="0c018-132">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="0c018-132">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="0c018-133">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="0c018-133">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="0c018-134">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="0c018-134">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="0c018-135">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="0c018-135">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
