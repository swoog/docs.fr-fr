---
title: ICLROnEventManager::RegisterActionOnEvent, méthode
ms.date: 03/30/2017
api_name:
- ICLROnEventManager.RegisterActionOnEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLROnEventManager::RegisterActionOnEvent
helpviewer_keywords:
- ICLROnEventManager::RegisterActionOnEvent method [.NET Framework hosting]
- RegisterActionOnEvent method [.NET Framework hosting]
ms.assetid: b944cf49-918d-4c4e-993b-77d097a52550
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c85c70acbdf7e5da1286f11d9962ca16f0d0ed72
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54569126"
---
# <a name="iclroneventmanagerregisteractiononevent-method"></a><span data-ttu-id="a52db-102">ICLROnEventManager::RegisterActionOnEvent, méthode</span><span class="sxs-lookup"><span data-stu-id="a52db-102">ICLROnEventManager::RegisterActionOnEvent Method</span></span>
<span data-ttu-id="a52db-103">Enregistre un pointeur de rappel pour l’événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="a52db-103">Registers a callback pointer for the specified event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a52db-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a52db-104">Syntax</span></span>  
  
```  
HRESULT RegisterActionOnEvent (  
    [in] EClrEvent event,  
    [in] IActionOnCLREvent *pAction  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a52db-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a52db-105">Parameters</span></span>  
 `event`  
 <span data-ttu-id="a52db-106">[in] Parmi les [EClrEvent](../../../../docs/framework/unmanaged-api/hosting/eclrevent-enumeration.md) valeurs indiquant l’événement pour lequel enregistrer le pointeur de rappel décrit par `pAction`.</span><span class="sxs-lookup"><span data-stu-id="a52db-106">[in] One of the [EClrEvent](../../../../docs/framework/unmanaged-api/hosting/eclrevent-enumeration.md) values, indicating the event for which to register the callback pointer described by `pAction`.</span></span>  
  
 `pAction`  
 <span data-ttu-id="a52db-107">[in] Un pointeur vers un [IActionOnCLREvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-interface.md) objet qui est appelé lorsque l’événement inscrit se déclenche.</span><span class="sxs-lookup"><span data-stu-id="a52db-107">[in] A pointer to an [IActionOnCLREvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-interface.md) object that is called when the registered event fires.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a52db-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a52db-108">Return Value</span></span>  
  
|<span data-ttu-id="a52db-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="a52db-109">HRESULT</span></span>|<span data-ttu-id="a52db-110">Description</span><span class="sxs-lookup"><span data-stu-id="a52db-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="a52db-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="a52db-111">S_OK</span></span>|<span data-ttu-id="a52db-112">`RegisterActionOnEvent` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="a52db-112">`RegisterActionOnEvent` returned successfully.</span></span>|  
|<span data-ttu-id="a52db-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="a52db-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="a52db-114">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="a52db-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="a52db-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a52db-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="a52db-116">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="a52db-116">The call timed out.</span></span>|  
|<span data-ttu-id="a52db-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="a52db-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="a52db-118">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="a52db-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="a52db-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="a52db-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="a52db-120">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="a52db-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="a52db-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="a52db-121">E_FAIL</span></span>|<span data-ttu-id="a52db-122">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="a52db-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="a52db-123">Une fois une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="a52db-123">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="a52db-124">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="a52db-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a52db-125">Notes</span><span class="sxs-lookup"><span data-stu-id="a52db-125">Remarks</span></span>  
 <span data-ttu-id="a52db-126">L’hôte peut enregistrer des rappels pour une ou les deux de deux types d’événements décrits par `EClrEvent`.</span><span class="sxs-lookup"><span data-stu-id="a52db-126">The host can register callbacks for either or both of the two event types described by `EClrEvent`.</span></span> <span data-ttu-id="a52db-127">L’hôte obtient le `ICLROnEventManager` interface en appelant le [ICLRControl::GetCLRManager](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-getclrmanager-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="a52db-127">The host gets the `ICLROnEventManager` interface by calling the [ICLRControl::GetCLRManager](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-getclrmanager-method.md) method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a52db-128">Les événements qui `RegisterActionOnEvent` peuvent être déclenchés plusieurs fois et à partir de threads différents pour signaler le déchargement ou la désactivation du CLR.</span><span class="sxs-lookup"><span data-stu-id="a52db-128">The events that `RegisterActionOnEvent` registers can be fired more than once and from different threads to signal an unload or the disabling of the CLR.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a52db-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a52db-129">Requirements</span></span>  
 <span data-ttu-id="a52db-130">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a52db-130">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a52db-131">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a52db-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a52db-132">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a52db-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a52db-133">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a52db-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a52db-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a52db-134">See also</span></span>
- [<span data-ttu-id="a52db-135">EClrEvent, énumération</span><span class="sxs-lookup"><span data-stu-id="a52db-135">EClrEvent Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclrevent-enumeration.md)
- [<span data-ttu-id="a52db-136">IActionOnCLREvent, interface</span><span class="sxs-lookup"><span data-stu-id="a52db-136">IActionOnCLREvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-interface.md)
- [<span data-ttu-id="a52db-137">ICLRControl, interface</span><span class="sxs-lookup"><span data-stu-id="a52db-137">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)
- [<span data-ttu-id="a52db-138">ICLROnEventManager, interface</span><span class="sxs-lookup"><span data-stu-id="a52db-138">ICLROnEventManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-interface.md)
