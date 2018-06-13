---
title: IHostThreadPoolManager::GetMaxThreads, méthode
ms.date: 03/30/2017
api_name:
- IHostThreadPoolManager.GetMaxThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostThreadPoolManager::GetMaxThreads
helpviewer_keywords:
- IHostThreadPoolManager::GetMaxThreads method [.NET Framework hosting]
- GetMaxThreads method, IHostThreadPoolManager interface [.NET Framework hosting]
ms.assetid: db268876-6178-4a81-aca3-318ee7f96001
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fa6e0e2447cc3ff6766bb33bb603388f37ec3ce0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33443765"
---
# <a name="ihostthreadpoolmanagergetmaxthreads-method"></a><span data-ttu-id="f3e6f-102">IHostThreadPoolManager::GetMaxThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="f3e6f-102">IHostThreadPoolManager::GetMaxThreads Method</span></span>
<span data-ttu-id="f3e6f-103">Obtient le nombre maximal de threads que l’hôte conserve simultanément dans le pool de threads.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-103">Gets the maximum number of threads that the host maintains concurrently in the thread pool.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f3e6f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3e6f-104">Syntax</span></span>  
  
```  
HRESULT GetMaxThreads (  
    [out] DWORD *pdwMaxWorkerThreads  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f3e6f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3e6f-105">Parameters</span></span>  
 `pdwMaxWorkerThreads`  
 <span data-ttu-id="f3e6f-106">[out] Pointeur vers le nombre maximal de threads que l’hôte gère dans le pool de threads.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-106">[out] A pointer to the maximum number of threads that the host maintains in the thread pool.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f3e6f-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f3e6f-107">Return Value</span></span>  
  
|<span data-ttu-id="f3e6f-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f3e6f-108">HRESULT</span></span>|<span data-ttu-id="f3e6f-109">Description</span><span class="sxs-lookup"><span data-stu-id="f3e6f-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f3e6f-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3e6f-110">S_OK</span></span>|<span data-ttu-id="f3e6f-111">`GetMaxThreads` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-111">`GetMaxThreads` returned successfully.</span></span>|  
|<span data-ttu-id="f3e6f-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="f3e6f-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="f3e6f-113">Le common language runtime (CLR (n’a pas été chargé dans un processus, ou le CLR est dans un état dans lequel elle ne peut pas exécuter le code managé ou un processus l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-113">The common language runtime (CLR( has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="f3e6f-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f3e6f-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="f3e6f-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-115">The call timed out.</span></span>|  
|<span data-ttu-id="f3e6f-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="f3e6f-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="f3e6f-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="f3e6f-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="f3e6f-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="f3e6f-119">Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="f3e6f-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f3e6f-120">E_FAIL</span></span>|<span data-ttu-id="f3e6f-121">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="f3e6f-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="f3e6f-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="f3e6f-124">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="f3e6f-124">E_NOTIMPL</span></span>|<span data-ttu-id="f3e6f-125">L’hôte ne fournit pas une implémentation de `GetMaxThreads`.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-125">The host does not provide an implementation of `GetMaxThreads`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f3e6f-126">Notes</span><span class="sxs-lookup"><span data-stu-id="f3e6f-126">Remarks</span></span>  
 <span data-ttu-id="f3e6f-127">Le CLR appelle `GetMaxThreads` pour déterminer le nombre total de threads dans le pool de threads.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-127">The CLR calls `GetMaxThreads` to determine the total number of threads in the thread pool.</span></span> <span data-ttu-id="f3e6f-128">Le [GetAvailableThreads](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-getavailablethreads-method.md) méthode obtient le nombre de threads qui ne traitent pas actuellement des éléments de travail.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-128">The [GetAvailableThreads](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-getavailablethreads-method.md) method gets the number of threads that are not currently processing work items.</span></span> <span data-ttu-id="f3e6f-129">Toutes les demandes supérieures à la valeur retournée de la `pdwMaxWorkerThreads` paramètre restent en file d’attente jusqu'à ce que les threads deviennent disponibles.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-129">All requests above the returned value of the `pdwMaxWorkerThreads` parameter remain queued until threads become available.</span></span>  
  
 <span data-ttu-id="f3e6f-130">Si l’hôte ne fournit pas une implémentation de `GetMaxThreads`, elle doit retourner une valeur HRESULT d’E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-130">If the host does not provide an implementation of `GetMaxThreads`, it should return an HRESULT value of E_NOTIMPL.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f3e6f-131">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f3e6f-131">Requirements</span></span>  
 <span data-ttu-id="f3e6f-132">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f3e6f-132">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f3e6f-133">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="f3e6f-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f3e6f-134">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f3e6f-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f3e6f-135">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f3e6f-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f3e6f-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3e6f-136">See Also</span></span>  
 <xref:System.Threading.ThreadPool.GetMaxThreads%2A>  
 <xref:System.Threading.ThreadPool>  
 [<span data-ttu-id="f3e6f-137">GetMinThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="f3e6f-137">GetMinThreads Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-getminthreads-method.md)  
 [<span data-ttu-id="f3e6f-138">SetMaxThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="f3e6f-138">SetMaxThreads Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-setmaxthreads-method.md)  
 [<span data-ttu-id="f3e6f-139">IHostThreadPoolManager, interface</span><span class="sxs-lookup"><span data-stu-id="f3e6f-139">IHostThreadPoolManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-interface.md)
