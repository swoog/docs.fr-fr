---
title: IHostTaskManager::SwitchToTask, méthode
ms.date: 03/30/2017
api_name:
- IHostTaskManager.SwitchToTask
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::SwitchToTask
helpviewer_keywords:
- IHostTaskManager::SwitchToTask method [.NET Framework hosting]
- SwitchToTask method [.NET Framework hosting]
ms.assetid: 35d0c27e-4b14-49ce-810d-7ab2120177e8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7e2d5c299814202d0a3a8ff1da577fdfd17801e4
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57471999"
---
# <a name="ihosttaskmanagerswitchtotask-method"></a><span data-ttu-id="1c9b7-102">IHostTaskManager::SwitchToTask, méthode</span><span class="sxs-lookup"><span data-stu-id="1c9b7-102">IHostTaskManager::SwitchToTask Method</span></span>
<span data-ttu-id="1c9b7-103">Avertit l’hôte qu’il doit éliminer la tâche actuelle.</span><span class="sxs-lookup"><span data-stu-id="1c9b7-103">Notifies the host that it should switch out the current task.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1c9b7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c9b7-104">Syntax</span></span>  
  
```  
HRESULT SwitchToTask (  
    [in] DWORD option  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1c9b7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c9b7-105">Parameters</span></span>  
 `option`  
 <span data-ttu-id="1c9b7-106">[in] Parmi les [WAIT_OPTION](../../../../docs/framework/unmanaged-api/hosting/wait-option-enumeration.md) valeurs d’énumération indiquant l’action de l’hôte doit effectuer si l’opération demandée se bloque.</span><span class="sxs-lookup"><span data-stu-id="1c9b7-106">[in] One of the [WAIT_OPTION](../../../../docs/framework/unmanaged-api/hosting/wait-option-enumeration.md) enumeration values, indicating the action the host should take if the requested operation blocks.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1c9b7-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="1c9b7-107">Return Value</span></span>  
  
|<span data-ttu-id="1c9b7-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="1c9b7-108">HRESULT</span></span>|<span data-ttu-id="1c9b7-109">Description</span><span class="sxs-lookup"><span data-stu-id="1c9b7-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="1c9b7-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="1c9b7-110">S_OK</span></span>|<span data-ttu-id="1c9b7-111">`SwitchToTask` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="1c9b7-111">`SwitchToTask` returned successfully.</span></span>|  
|<span data-ttu-id="1c9b7-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="1c9b7-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="1c9b7-113">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="1c9b7-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="1c9b7-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="1c9b7-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="1c9b7-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="1c9b7-115">The call timed out.</span></span>|  
|<span data-ttu-id="1c9b7-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="1c9b7-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="1c9b7-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="1c9b7-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="1c9b7-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="1c9b7-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="1c9b7-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="1c9b7-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="1c9b7-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="1c9b7-120">E_FAIL</span></span>|<span data-ttu-id="1c9b7-121">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="1c9b7-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="1c9b7-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="1c9b7-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="1c9b7-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="1c9b7-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1c9b7-124">Notes</span><span class="sxs-lookup"><span data-stu-id="1c9b7-124">Remarks</span></span>  
 <span data-ttu-id="1c9b7-125">L’hôte peut basculer dans une autre tâche en tant que souhaité ou nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1c9b7-125">The host can switch in another task as desired or needed.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="1c9b7-126">`SwitchToTask` ne spécifie pas de tâche que l’hôte doit basculer ; Il spécifie uniquement la tâche sur lequel il doit basculer à partir de.</span><span class="sxs-lookup"><span data-stu-id="1c9b7-126">`SwitchToTask` does not specify which task the host should switch to; it specifies only the task that it should switch from.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1c9b7-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1c9b7-127">Requirements</span></span>  
 <span data-ttu-id="1c9b7-128">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1c9b7-128">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1c9b7-129">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="1c9b7-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="1c9b7-130">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1c9b7-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1c9b7-131">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1c9b7-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1c9b7-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c9b7-132">See also</span></span>
- [<span data-ttu-id="1c9b7-133">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="1c9b7-133">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="1c9b7-134">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="1c9b7-134">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="1c9b7-135">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="1c9b7-135">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="1c9b7-136">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="1c9b7-136">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
