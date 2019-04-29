---
title: IHostThreadPoolManager::GetMinThreads, méthode
ms.date: 03/30/2017
api_name:
- IHostThreadPoolManager.GetMinThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostThreadPoolManager::GetMinThreads
helpviewer_keywords:
- IHostThreadPoolManager::GetMinThreads method [.NET Framework hosting]
- GetMinThreads method, IHostThreadPoolManager interface [.NET Framework hosting]
ms.assetid: dc07232b-b2e4-4dab-87e2-3c955974ab48
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f1230a72d06677b4d36d10a8a31d63638c1fcd41
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61796545"
---
# <a name="ihostthreadpoolmanagergetminthreads-method"></a><span data-ttu-id="83036-102">IHostThreadPoolManager::GetMinThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="83036-102">IHostThreadPoolManager::GetMinThreads Method</span></span>
<span data-ttu-id="83036-103">Obtient le nombre minimal de threads inactifs que l’hôte conserve dans le pool de threads par anticipation des demandes.</span><span class="sxs-lookup"><span data-stu-id="83036-103">Gets the minimum number of idle threads that the host maintains in the thread pool in anticipation of requests.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="83036-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83036-104">Syntax</span></span>  
  
```  
HRESULT GetMinThreads (  
    [out] DWORD *MinThreads  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="83036-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83036-105">Parameters</span></span>  
 `MinThreads`  
 <span data-ttu-id="83036-106">[out] Pointeur vers le nombre minimal de threads de travail inactifs que l’hôte gère actuellement.</span><span class="sxs-lookup"><span data-stu-id="83036-106">[out] A pointer to the minimum number of idle worker threads that the host currently maintains.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="83036-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="83036-107">Return Value</span></span>  
  
|<span data-ttu-id="83036-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="83036-108">HRESULT</span></span>|<span data-ttu-id="83036-109">Description</span><span class="sxs-lookup"><span data-stu-id="83036-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="83036-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="83036-110">S_OK</span></span>|<span data-ttu-id="83036-111">`GetMinThreads` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="83036-111">`GetMinThreads` returned successfully.</span></span>|  
|<span data-ttu-id="83036-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="83036-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="83036-113">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="83036-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="83036-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="83036-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="83036-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="83036-115">The call timed out.</span></span>|  
|<span data-ttu-id="83036-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="83036-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="83036-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="83036-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="83036-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="83036-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="83036-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="83036-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="83036-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="83036-120">E_FAIL</span></span>|<span data-ttu-id="83036-121">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="83036-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="83036-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="83036-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="83036-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="83036-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="83036-124">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="83036-124">E_NOTIMPL</span></span>|<span data-ttu-id="83036-125">L’hôte ne fournit pas une implémentation de `GetMinThreads`.</span><span class="sxs-lookup"><span data-stu-id="83036-125">The host does not provide an implementation of `GetMinThreads`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="83036-126">Notes</span><span class="sxs-lookup"><span data-stu-id="83036-126">Remarks</span></span>  
 <span data-ttu-id="83036-127">L’hôte n’est pas obligé de fournir une implémentation de `GetMinThreads`.</span><span class="sxs-lookup"><span data-stu-id="83036-127">The host is not required to provide an implementation of `GetMinThreads`.</span></span> <span data-ttu-id="83036-128">Dans ce cas, il doit retourner une valeur HRESULT d’E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="83036-128">In this case, it should return an HRESULT value of E_NOTIMPL.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="83036-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83036-129">Requirements</span></span>  
 <span data-ttu-id="83036-130">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="83036-130">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="83036-131">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="83036-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="83036-132">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="83036-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="83036-133">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="83036-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="83036-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83036-134">See also</span></span>

- <xref:System.Threading.ThreadPool.GetMinThreads%2A>
- <xref:System.Threading.ThreadPool>
- [<span data-ttu-id="83036-135">GetMaxThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="83036-135">GetMaxThreads Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-getmaxthreads-method.md)
- [<span data-ttu-id="83036-136">SetMinThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="83036-136">SetMinThreads Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-setminthreads-method.md)
- [<span data-ttu-id="83036-137">IHostThreadPoolManager, interface</span><span class="sxs-lookup"><span data-stu-id="83036-137">IHostThreadPoolManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-interface.md)
