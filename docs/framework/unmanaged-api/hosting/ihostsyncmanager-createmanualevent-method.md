---
title: IHostSyncManager::CreateManualEvent, méthode
ms.date: 03/30/2017
api_name:
- IHostSyncManager.CreateManualEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSyncManager::CreateManualEvent
helpviewer_keywords:
- CreateManualEvent method [.NET Framework hosting]
- IHostSyncManager::CreateManualEvent method [.NET Framework hosting]
ms.assetid: 68661fbd-09cf-46dc-890b-e694f8a3880a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ecf53606dd12b517d9ec31ab25f98452d35bdf98
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33443442"
---
# <a name="ihostsyncmanagercreatemanualevent-method"></a><span data-ttu-id="6ae1b-102">IHostSyncManager::CreateManualEvent, méthode</span><span class="sxs-lookup"><span data-stu-id="6ae1b-102">IHostSyncManager::CreateManualEvent Method</span></span>
<span data-ttu-id="6ae1b-103">Crée un objet d’événement de réinitialisation manuelle.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-103">Creates a manual-reset event object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6ae1b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ae1b-104">Syntax</span></span>  
  
```  
HRESULT CreateManualEvent (  
    [in]  BOOL bInitialState,  
    [out] IHostManualEvent **ppEvent  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6ae1b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ae1b-105">Parameters</span></span>  
 `bInitialState`  
 <span data-ttu-id="6ae1b-106">[in] `true`, si l’objet est signalé ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-106">[in] `true`, if the object is signaled; otherwise, `false`.</span></span>  
  
 `ppEvent`  
 <span data-ttu-id="6ae1b-107">[out] Un pointeur vers l’adresse d’un [IHostManualEvent](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-interface.md) de l’instance, ou null si l’événement n’a pas pu être créé.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-107">[out] A pointer to the address of an [IHostManualEvent](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-interface.md) instance, or null if the event could not be created.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6ae1b-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="6ae1b-108">Return Value</span></span>  
  
|<span data-ttu-id="6ae1b-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="6ae1b-109">HRESULT</span></span>|<span data-ttu-id="6ae1b-110">Description</span><span class="sxs-lookup"><span data-stu-id="6ae1b-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="6ae1b-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="6ae1b-111">S_OK</span></span>|<span data-ttu-id="6ae1b-112">`CreateManualEvent` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-112">`CreateManualEvent` returned successfully.</span></span>|  
|<span data-ttu-id="6ae1b-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="6ae1b-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="6ae1b-114">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="6ae1b-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="6ae1b-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="6ae1b-116">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-116">The call timed out.</span></span>|  
|<span data-ttu-id="6ae1b-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="6ae1b-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="6ae1b-118">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="6ae1b-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="6ae1b-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="6ae1b-120">Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="6ae1b-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="6ae1b-121">E_FAIL</span></span>|<span data-ttu-id="6ae1b-122">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="6ae1b-123">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="6ae1b-124">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="6ae1b-125">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="6ae1b-125">E_OUTOFMEMORY</span></span>|<span data-ttu-id="6ae1b-126">Pas assez de mémoire n’était disponible pour créer l’objet de l’événement demandé.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-126">Not enough memory was available to create the requested event object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6ae1b-127">Notes</span><span class="sxs-lookup"><span data-stu-id="6ae1b-127">Remarks</span></span>  
 <span data-ttu-id="6ae1b-128">`CreateManualEvent` Crée un `IHostManualEvent`, un objet d’événement de réinitialisation manuelle qui nécessite un appel à la [IHostManualEvent::Reset](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-reset-method.md) méthode lui affecter un état non signalé.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-128">`CreateManualEvent` creates an `IHostManualEvent`, a manual-reset event object that requires a call to the [IHostManualEvent::Reset](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-reset-method.md) method to set it to a non-signaled state.</span></span> <span data-ttu-id="6ae1b-129">`CreateManualEvent` reflète Win32 `CreateEvent` fonction avec la valeur `true` spécifié pour le `bManualReset` paramètre.</span><span class="sxs-lookup"><span data-stu-id="6ae1b-129">`CreateManualEvent` mirrors the Win32 `CreateEvent` function with a value of `true` specified for the `bManualReset` parameter.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6ae1b-130">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6ae1b-130">Requirements</span></span>  
 <span data-ttu-id="6ae1b-131">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6ae1b-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6ae1b-132">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="6ae1b-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6ae1b-133">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6ae1b-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6ae1b-134">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6ae1b-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6ae1b-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ae1b-135">See Also</span></span>  
 [<span data-ttu-id="6ae1b-136">ICLRSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="6ae1b-136">ICLRSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)  
 [<span data-ttu-id="6ae1b-137">IHostManualEvent, interface</span><span class="sxs-lookup"><span data-stu-id="6ae1b-137">IHostManualEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-interface.md)  
 [<span data-ttu-id="6ae1b-138">IHostSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="6ae1b-138">IHostSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)
