---
title: IHostAutoEvent::Wait, méthode
ms.date: 03/30/2017
api_name:
- IHostAutoEvent.Wait
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostAutoEvent::Wait
helpviewer_keywords:
- Wait method, IHostAutoEvent interface [.NET Framework hosting]
- IHostAutoEvent::Wait method [.NET Framework hosting]
ms.assetid: 535d51c5-9112-401b-8c36-85f35d7ee609
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8559c4c0a1f301c72b48350eff5037faefde5704
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54678658"
---
# <a name="ihostautoeventwait-method"></a><span data-ttu-id="a3805-102">IHostAutoEvent::Wait, méthode</span><span class="sxs-lookup"><span data-stu-id="a3805-102">IHostAutoEvent::Wait Method</span></span>
<span data-ttu-id="a3805-103">Fait en [IHostAutoEvent](../../../../docs/framework/unmanaged-api/hosting/ihostautoevent-interface.md) instance attendre jusqu'à ce qu’il appartient ou un certain laps de temps.</span><span class="sxs-lookup"><span data-stu-id="a3805-103">Causes the current [IHostAutoEvent](../../../../docs/framework/unmanaged-api/hosting/ihostautoevent-interface.md) instance to wait until it is owned or a specified amount of time elapses.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a3805-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3805-104">Syntax</span></span>  
  
```  
HRESULT Wait (  
    [in] DWORD dwMilliseconds,  
    [in] DWORD option  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a3805-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3805-105">Parameters</span></span>  
 `dwMilliseconds`  
 <span data-ttu-id="a3805-106">[in] Le nombre de millisecondes actuel `IHostAutoEvent` instance doit attendre avant de retourner, si aucun thread ou Fibre prend possession.</span><span class="sxs-lookup"><span data-stu-id="a3805-106">[in] The number of milliseconds the current `IHostAutoEvent` instance should wait before returning, if no thread or fiber takes ownership.</span></span>  
  
 `option`  
 <span data-ttu-id="a3805-107">[in] Parmi les [WAIT_OPTION](../../../../docs/framework/unmanaged-api/hosting/wait-option-enumeration.md) valeurs, qui spécifient l’action de l’hôte doit effectuer si cette opération bloque.</span><span class="sxs-lookup"><span data-stu-id="a3805-107">[in] One of the [WAIT_OPTION](../../../../docs/framework/unmanaged-api/hosting/wait-option-enumeration.md) values, specifying the action the host should take if this operation blocks.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a3805-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a3805-108">Return Value</span></span>  
  
|<span data-ttu-id="a3805-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="a3805-109">HRESULT</span></span>|<span data-ttu-id="a3805-110">Description</span><span class="sxs-lookup"><span data-stu-id="a3805-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="a3805-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="a3805-111">S_OK</span></span>|<span data-ttu-id="a3805-112">`Wait` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="a3805-112">`Wait` returned successfully.</span></span>|  
|<span data-ttu-id="a3805-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="a3805-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="a3805-114">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="a3805-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="a3805-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a3805-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="a3805-116">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="a3805-116">The call timed out.</span></span>|  
|<span data-ttu-id="a3805-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="a3805-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="a3805-118">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="a3805-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="a3805-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="a3805-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="a3805-120">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="a3805-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="a3805-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="a3805-121">E_FAIL</span></span>|<span data-ttu-id="a3805-122">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="a3805-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="a3805-123">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="a3805-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="a3805-124">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="a3805-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="a3805-125">HOST_E_DEADLOCK</span><span class="sxs-lookup"><span data-stu-id="a3805-125">HOST_E_DEADLOCK</span></span>|<span data-ttu-id="a3805-126">L’hôte a détecté un interblocage pendant l’intervalle d’attente et a choisi l’événement représenté par l’actuel `IHostAutoEvent` instance comme victime du blocage.</span><span class="sxs-lookup"><span data-stu-id="a3805-126">The host detected a deadlock during the wait interval, and chose the event represented by the current `IHostAutoEvent` instance as the deadlock victim.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a3805-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a3805-127">Requirements</span></span>  
 <span data-ttu-id="a3805-128">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a3805-128">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a3805-129">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a3805-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a3805-130">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a3805-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a3805-131">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a3805-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a3805-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3805-132">See also</span></span>
- [<span data-ttu-id="a3805-133">ICLRSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="a3805-133">ICLRSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)
- [<span data-ttu-id="a3805-134">IHostAutoEvent, interface</span><span class="sxs-lookup"><span data-stu-id="a3805-134">IHostAutoEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostautoevent-interface.md)
- [<span data-ttu-id="a3805-135">IHostManualEvent, interface</span><span class="sxs-lookup"><span data-stu-id="a3805-135">IHostManualEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-interface.md)
- [<span data-ttu-id="a3805-136">IHostSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="a3805-136">IHostSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)
