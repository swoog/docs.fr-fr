---
title: IHostTaskManager::BeginDelayAbort, méthode
ms.date: 03/30/2017
api_name:
- IHostTaskManager.BeginDelayAbort
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::BeginDelayAbort
helpviewer_keywords:
- BeginDelayAbort method [.NET Framework hosting]
- IHostTaskManager::BeginDelayAbort method [.NET Framework hosting]
ms.assetid: 75f42a8b-ed68-4718-a030-a179cfba7d72
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 328462343669b3ea6bed2d86514ea348f6ae2b1e
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59197969"
---
# <a name="ihosttaskmanagerbegindelayabort-method"></a><span data-ttu-id="64bae-102">IHostTaskManager::BeginDelayAbort, méthode</span><span class="sxs-lookup"><span data-stu-id="64bae-102">IHostTaskManager::BeginDelayAbort Method</span></span>
<span data-ttu-id="64bae-103">Avertit l’hôte que le code managé entre dans une période dans laquelle la tâche actuelle ne doit pas être abandonnée.</span><span class="sxs-lookup"><span data-stu-id="64bae-103">Notifies the host that managed code is entering a period in which the current task must not be aborted.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="64bae-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64bae-104">Syntax</span></span>  
  
```  
HRESULT BeginDelayAbort ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="64bae-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="64bae-105">Return Value</span></span>  
  
|<span data-ttu-id="64bae-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="64bae-106">HRESULT</span></span>|<span data-ttu-id="64bae-107">Description</span><span class="sxs-lookup"><span data-stu-id="64bae-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="64bae-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="64bae-108">S_OK</span></span>|`BeginDelayAbort` <span data-ttu-id="64bae-109">retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="64bae-109">returned successfully.</span></span>|  
|<span data-ttu-id="64bae-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="64bae-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="64bae-111">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="64bae-111">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="64bae-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="64bae-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="64bae-113">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="64bae-113">The call timed out.</span></span>|  
|<span data-ttu-id="64bae-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="64bae-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="64bae-115">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="64bae-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="64bae-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="64bae-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="64bae-117">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="64bae-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="64bae-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="64bae-118">E_FAIL</span></span>|<span data-ttu-id="64bae-119">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="64bae-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="64bae-120">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="64bae-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="64bae-121">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="64bae-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="64bae-122">E_UNEXPECTED</span><span class="sxs-lookup"><span data-stu-id="64bae-122">E_UNEXPECTED</span></span>|`BeginDelayAbort` <span data-ttu-id="64bae-123">a déjà été appelée, mais l’appel correspondant à [EndDelayAbort](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-enddelayabort-method.md) n’a pas encore été reçus.</span><span class="sxs-lookup"><span data-stu-id="64bae-123">has already been called, but the corresponding call to [EndDelayAbort](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-enddelayabort-method.md) has not yet been received.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="64bae-124">Notes</span><span class="sxs-lookup"><span data-stu-id="64bae-124">Remarks</span></span>  
 <span data-ttu-id="64bae-125">L’hôte ne doit pas abandonner la tâche en cours jusqu'à ce que `EndDelayAbort` est appelée.</span><span class="sxs-lookup"><span data-stu-id="64bae-125">The host must not abort the current task until `EndDelayAbort` is called.</span></span> <span data-ttu-id="64bae-126">Si un autre appel à `BeginDelayAbort` est établie sans appel intermédiaire à `EndDelayAbort`, l’hôte doit retourner E_UNEXPECTED à partir de `BeginDelayAbort`et ne doit effectuer aucune action.</span><span class="sxs-lookup"><span data-stu-id="64bae-126">If another call to `BeginDelayAbort` is made without an intervening call to `EndDelayAbort`, the host should return E_UNEXPECTED from `BeginDelayAbort`, and should take no action.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="64bae-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64bae-127">Requirements</span></span>  
 <span data-ttu-id="64bae-128">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="64bae-128">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="64bae-129">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="64bae-129">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="64bae-130">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="64bae-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="64bae-131">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="64bae-131">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="64bae-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64bae-132">See also</span></span>

- [<span data-ttu-id="64bae-133">ICLRTask, interface</span><span class="sxs-lookup"><span data-stu-id="64bae-133">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [<span data-ttu-id="64bae-134">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="64bae-134">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [<span data-ttu-id="64bae-135">IHostTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="64bae-135">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
