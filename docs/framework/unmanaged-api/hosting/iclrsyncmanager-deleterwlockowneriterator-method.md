---
title: ICLRSyncManager::DeleteRWLockOwnerIterator, méthode
ms.date: 03/30/2017
api_name:
- ICLRSyncManager.DeleteRWLockOwnerIterator
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRSyncManager::DeleteRWLockOwnerIterator
helpviewer_keywords:
- ICLRSyncManager::DeleteRWLockOwnerIterator method [.NET Framework hosting]
- DeleteRWLockOwnerIterator method [.NET Framework hosting]
ms.assetid: fcfd340a-b7d6-44e4-8167-2c05b789d483
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ba0cabfe9e96ace255235f1aa7d2b80452c4d72e
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57482884"
---
# <a name="iclrsyncmanagerdeleterwlockowneriterator-method"></a><span data-ttu-id="c73f8-102">ICLRSyncManager::DeleteRWLockOwnerIterator, méthode</span><span class="sxs-lookup"><span data-stu-id="c73f8-102">ICLRSyncManager::DeleteRWLockOwnerIterator Method</span></span>
<span data-ttu-id="c73f8-103">Demande que le common language runtime (CLR) détruise un itérateur qui a été créé par un appel à [ICLRSyncManager::CreateRWLockOwnerIterator](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-createrwlockowneriterator-method.md).</span><span class="sxs-lookup"><span data-stu-id="c73f8-103">Requests that the common language runtime (CLR) destroy an iterator that was created by a call to [ICLRSyncManager::CreateRWLockOwnerIterator](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-createrwlockowneriterator-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c73f8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c73f8-104">Syntax</span></span>  
  
```  
HRESULT DeleteRWLockOwnerIterator (  
    [in] SIZE_T  Iterator  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c73f8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c73f8-105">Parameters</span></span>  
 `Iterator`  
 <span data-ttu-id="c73f8-106">[in] Itérateur qui a été créé à l’aide d’un appel à `CreateRWLockOwnerIterator`.</span><span class="sxs-lookup"><span data-stu-id="c73f8-106">[in] The iterator that was created by using a call to `CreateRWLockOwnerIterator`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c73f8-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c73f8-107">Return Value</span></span>  
  
|<span data-ttu-id="c73f8-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="c73f8-108">HRESULT</span></span>|<span data-ttu-id="c73f8-109">Description</span><span class="sxs-lookup"><span data-stu-id="c73f8-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="c73f8-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="c73f8-110">S_OK</span></span>|<span data-ttu-id="c73f8-111">`DeleteRWLockOwnerIterator` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="c73f8-111">`DeleteRWLockOwnerIterator` returned successfully.</span></span>|  
|<span data-ttu-id="c73f8-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="c73f8-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="c73f8-113">Le CLR n’a pas été chargé dans un processus, ou est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel.</span><span class="sxs-lookup"><span data-stu-id="c73f8-113">The CLR has not been loaded into a process, or is in a state in which it cannot run managed code or successfully process the call.</span></span>|  
|<span data-ttu-id="c73f8-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="c73f8-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="c73f8-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="c73f8-115">The call timed out.</span></span>|  
|<span data-ttu-id="c73f8-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="c73f8-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="c73f8-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="c73f8-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="c73f8-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="c73f8-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="c73f8-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="c73f8-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="c73f8-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="c73f8-120">E_FAIL</span></span>|<span data-ttu-id="c73f8-121">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c73f8-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="c73f8-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="c73f8-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="c73f8-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="c73f8-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c73f8-124">Notes</span><span class="sxs-lookup"><span data-stu-id="c73f8-124">Remarks</span></span>  
 <span data-ttu-id="c73f8-125">L’hôte peut appeler cette méthode et `CreateRWLockOwnerIterator` pour vous assurer que l’implémentation de threads reste synchronisée.</span><span class="sxs-lookup"><span data-stu-id="c73f8-125">The host can call this method and `CreateRWLockOwnerIterator` to ensure that its threading implementation remains synchronized.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c73f8-126">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c73f8-126">Requirements</span></span>  
 <span data-ttu-id="c73f8-127">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c73f8-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c73f8-128">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="c73f8-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c73f8-129">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c73f8-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c73f8-130">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c73f8-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c73f8-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c73f8-131">See also</span></span>
- [<span data-ttu-id="c73f8-132">ICLRSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="c73f8-132">ICLRSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)
- [<span data-ttu-id="c73f8-133">IHostSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="c73f8-133">IHostSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)
