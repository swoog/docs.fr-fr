---
title: IHostIoCompletionManager::GetAvailableThreads, méthode
ms.date: 03/30/2017
api_name:
- IHostIoCompletionManager.GetAvailableThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostIoCompletionManager::GetAvailableThreads
helpviewer_keywords:
- GetAvailableThreads method, IHostIoCompletionManager interface [.NET Framework hosting]
- IHostIoCompletionManager::GetAvailableThreads method [.NET Framework hosting]
ms.assetid: bab363d1-b859-47a4-9884-5661c611cce7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1e96a12bbf9c4fdc8a0bc79661070eb7fec1a593
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59123968"
---
# <a name="ihostiocompletionmanagergetavailablethreads-method"></a><span data-ttu-id="f2061-102">IHostIoCompletionManager::GetAvailableThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="f2061-102">IHostIoCompletionManager::GetAvailableThreads Method</span></span>
<span data-ttu-id="f2061-103">Obtient le nombre de threads de terminaison d’e/s, du nombre total de threads gérés par l’hôte, qui ne traitent pas actuellement des demandes.</span><span class="sxs-lookup"><span data-stu-id="f2061-103">Gets the number of I/O completion threads, of the total number of threads managed by the host, that are not currently servicing requests.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f2061-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2061-104">Syntax</span></span>  
  
```  
HRESULT GetAvailableThreads (  
    [out] DWORD *pdwAvailableIoCompletionThreads  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f2061-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2061-105">Parameters</span></span>  
 `pdwAvailableIoCompletionThreads`  
 <span data-ttu-id="f2061-106">[out] Pointeur vers le nombre de threads d’achèvement d’e/s gérés par l’hôte qui sont actuellement disponibles pour les demandes de service.</span><span class="sxs-lookup"><span data-stu-id="f2061-106">[out] A pointer to the number of I/O completion threads managed by the host that are currently available to service requests.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f2061-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f2061-107">Return Value</span></span>  
  
|<span data-ttu-id="f2061-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f2061-108">HRESULT</span></span>|<span data-ttu-id="f2061-109">Description</span><span class="sxs-lookup"><span data-stu-id="f2061-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f2061-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="f2061-110">S_OK</span></span>|<span data-ttu-id="f2061-111">`GetAvailableThreads` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="f2061-111">`GetAvailableThreads` returned successfully.</span></span>|  
|<span data-ttu-id="f2061-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="f2061-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="f2061-113">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="f2061-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="f2061-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f2061-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="f2061-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="f2061-115">The call timed out.</span></span>|  
|<span data-ttu-id="f2061-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="f2061-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="f2061-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="f2061-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="f2061-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="f2061-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="f2061-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="f2061-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="f2061-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f2061-120">E_FAIL</span></span>|<span data-ttu-id="f2061-121">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f2061-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="f2061-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="f2061-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="f2061-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="f2061-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="f2061-124">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="f2061-124">E_NOTIMPL</span></span>|<span data-ttu-id="f2061-125">L’hôte ne fournit pas une implémentation de `GetAvailableThreads`.</span><span class="sxs-lookup"><span data-stu-id="f2061-125">The host does not provide an implementation of `GetAvailableThreads`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f2061-126">Notes</span><span class="sxs-lookup"><span data-stu-id="f2061-126">Remarks</span></span>  
 <span data-ttu-id="f2061-127">Un hôte peut souhaiter le contrôle exclusif sur la taille du pool de threads d’achèvement d’e/s, pour des raisons telles que l’implémentation, de performances ou d’évolutivité.</span><span class="sxs-lookup"><span data-stu-id="f2061-127">A host might want exclusive control over the size of the I/O completion thread pool, for reasons such as implementation, performance, or scalability.</span></span> <span data-ttu-id="f2061-128">Par conséquent, l’hôte n’est pas nécessaire d’implémenter `GetAvailableThreads`.</span><span class="sxs-lookup"><span data-stu-id="f2061-128">Therefore, the host is not required to implement `GetAvailableThreads`.</span></span> <span data-ttu-id="f2061-129">Dans ce cas, l’hôte doit retourner E_NOTIMPL à partir de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="f2061-129">In this case, the host should return E_NOTIMPL from this method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f2061-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2061-130">Requirements</span></span>  
 <span data-ttu-id="f2061-131">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f2061-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f2061-132">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="f2061-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f2061-133">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f2061-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f2061-134">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f2061-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f2061-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2061-135">See also</span></span>

- [<span data-ttu-id="f2061-136">ICLRIoCompletionManager, interface</span><span class="sxs-lookup"><span data-stu-id="f2061-136">ICLRIoCompletionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-interface.md)
- [<span data-ttu-id="f2061-137">IHostIoCompletionManager, interface</span><span class="sxs-lookup"><span data-stu-id="f2061-137">IHostIoCompletionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-interface.md)
