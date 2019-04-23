---
title: IHostTaskManager::EndDelayAbort, méthode
ms.date: 03/30/2017
api_name:
- IHostTaskManager.EndDelayAbort
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::EndDelayAbort
helpviewer_keywords:
- EndDelayAbort method [.NET Framework hosting]
- IHostTaskManager::EndDelayAbort method [.NET Framework hosting]
ms.assetid: 6e02facb-2504-4356-9af5-0cee1f8436a7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 10d12e5cab41f016ddee78089dc1df1f5c942ecd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59194446"
---
# <a name="ihosttaskmanagerenddelayabort-method"></a><span data-ttu-id="bcdfc-102">IHostTaskManager::EndDelayAbort, méthode</span><span class="sxs-lookup"><span data-stu-id="bcdfc-102">IHostTaskManager::EndDelayAbort Method</span></span>
<span data-ttu-id="bcdfc-103">Avertit l’hôte que le code managé sort de la période dans laquelle la tâche actuelle ne doit pas être abandonnée, à la suite d’un appel précédent à [IHostTaskManager::BeginDelayAbort](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-begindelayabort-method.md).</span><span class="sxs-lookup"><span data-stu-id="bcdfc-103">Notifies the host that managed code is exiting the period in which the current task must not be aborted, following an earlier call to [IHostTaskManager::BeginDelayAbort](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-begindelayabort-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bcdfc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bcdfc-104">Syntax</span></span>  
  
```  
HRESULT EndDelayAbort ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="bcdfc-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="bcdfc-105">Return Value</span></span>  
  
|<span data-ttu-id="bcdfc-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="bcdfc-106">HRESULT</span></span>|<span data-ttu-id="bcdfc-107">Description</span><span class="sxs-lookup"><span data-stu-id="bcdfc-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="bcdfc-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="bcdfc-108">S_OK</span></span>|<span data-ttu-id="bcdfc-109">`EndDelayAbort` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="bcdfc-109">`EndDelayAbort` returned successfully.</span></span>|  
|<span data-ttu-id="bcdfc-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="bcdfc-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="bcdfc-111">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="bcdfc-111">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="bcdfc-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="bcdfc-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="bcdfc-113">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="bcdfc-113">The call timed out.</span></span>|  
|<span data-ttu-id="bcdfc-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="bcdfc-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="bcdfc-115">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="bcdfc-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="bcdfc-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="bcdfc-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="bcdfc-117">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="bcdfc-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="bcdfc-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="bcdfc-118">E_FAIL</span></span>|<span data-ttu-id="bcdfc-119">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="bcdfc-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="bcdfc-120">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="bcdfc-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="bcdfc-121">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="bcdfc-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="bcdfc-122">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="bcdfc-122">E_UNEXPECTED</span></span>|<span data-ttu-id="bcdfc-123">`EndDelayAbort` a été appelée sans appel correspondant à `BeginDelayAbort`.</span><span class="sxs-lookup"><span data-stu-id="bcdfc-123">`EndDelayAbort` was called without a corresponding call to `BeginDelayAbort`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bcdfc-124">Notes</span><span class="sxs-lookup"><span data-stu-id="bcdfc-124">Remarks</span></span>  
 <span data-ttu-id="bcdfc-125">Le CLR effectue un appel correspondant à `BeginDelayAbort` sur la tâche en cours avant d’appeler `EndDelayAbort`.</span><span class="sxs-lookup"><span data-stu-id="bcdfc-125">The CLR makes a corresponding call to `BeginDelayAbort` on the current task before calling `EndDelayAbort`.</span></span> <span data-ttu-id="bcdfc-126">En l’absence d’un tel appel correspondant, implémentation de l’hôte de [IHostTaskManager](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md) doit retourner E_UNEXPECTED à partir de `EndDelayAbort`et ne doit effectuer aucune action.</span><span class="sxs-lookup"><span data-stu-id="bcdfc-126">In the absence of such a corresponding call, the host's implementation of [IHostTaskManager](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md) should return E_UNEXPECTED from `EndDelayAbort`, and should take no action.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bcdfc-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcdfc-127">Requirements</span></span>  
 <span data-ttu-id="bcdfc-128">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bcdfc-128">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bcdfc-129">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="bcdfc-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="bcdfc-130">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bcdfc-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bcdfc-131">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bcdfc-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bcdfc-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcdfc-132">See also</span></span>

- <xref:System.Threading>
- [<span data-ttu-id="bcdfc-133">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="bcdfc-133">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="bcdfc-134">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="bcdfc-134">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="bcdfc-135">IHostTask, interface</span><span class="sxs-lookup"><span data-stu-id="bcdfc-135">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [<span data-ttu-id="bcdfc-136">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="bcdfc-136">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
