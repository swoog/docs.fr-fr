---
title: IHostThreadPoolManager::SetMinThreads, méthode
ms.date: 03/30/2017
api_name:
- IHostThreadPoolManager.SetMinThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostThreadPoolManager::SetMinThreads
helpviewer_keywords:
- SetMinThreads method, IHostThreadPoolManager interface [.NET Framework hosting]
- IHostThreadPoolManager::SetMinThreads method [.NET Framework hosting]
ms.assetid: 10409db9-9fd2-4e4d-b8cd-cf6fec0afaa2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8f9852034f6d8208bdaa9b424f689adc374bae2d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33443673"
---
# <a name="ihostthreadpoolmanagersetminthreads-method"></a><span data-ttu-id="690a2-102">IHostThreadPoolManager::SetMinThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="690a2-102">IHostThreadPoolManager::SetMinThreads Method</span></span>
<span data-ttu-id="690a2-103">Définit le nombre minimal de threads inactifs que l’hôte doit gérer en anticipation des demandes.</span><span class="sxs-lookup"><span data-stu-id="690a2-103">Sets the minimum number of idle threads that the host must maintain in anticipation of requests.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="690a2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="690a2-104">Syntax</span></span>  
  
```  
HRESULT SetMinThreads (  
    [in] DWORD MinThreads  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="690a2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="690a2-105">Parameters</span></span>  
 `MinThreads`  
 <span data-ttu-id="690a2-106">[in] Le nouveau nombre minimal de threads que l’hôte doit gérer.</span><span class="sxs-lookup"><span data-stu-id="690a2-106">[in] The new minimum number of threads that the host must maintain.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="690a2-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="690a2-107">Return Value</span></span>  
  
|<span data-ttu-id="690a2-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="690a2-108">HRESULT</span></span>|<span data-ttu-id="690a2-109">Description</span><span class="sxs-lookup"><span data-stu-id="690a2-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="690a2-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="690a2-110">S_OK</span></span>|<span data-ttu-id="690a2-111">`SetMinThreads` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="690a2-111">`SetMinThreads` returned successfully.</span></span>|  
|<span data-ttu-id="690a2-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="690a2-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="690a2-113">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="690a2-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="690a2-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="690a2-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="690a2-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="690a2-115">The call timed out.</span></span>|  
|<span data-ttu-id="690a2-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="690a2-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="690a2-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="690a2-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="690a2-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="690a2-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="690a2-119">Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="690a2-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="690a2-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="690a2-120">E_FAIL</span></span>|<span data-ttu-id="690a2-121">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="690a2-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="690a2-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="690a2-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="690a2-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="690a2-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="690a2-124">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="690a2-124">E_NOTIMPL</span></span>|<span data-ttu-id="690a2-125">L’hôte ne fournit pas une implémentation de `SetMinThreads`.</span><span class="sxs-lookup"><span data-stu-id="690a2-125">The host does not provide an implementation of `SetMinThreads`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="690a2-126">Notes</span><span class="sxs-lookup"><span data-stu-id="690a2-126">Remarks</span></span>  
 <span data-ttu-id="690a2-127">Un hôte n’est pas obligé de fournir une implémentation de `SetMinThreads`.</span><span class="sxs-lookup"><span data-stu-id="690a2-127">A host is not required to provide an implementation of `SetMinThreads`.</span></span> <span data-ttu-id="690a2-128">Dans ce cas, elle doit retourner une valeur HRESULT d’E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="690a2-128">In this case, it should return an HRESULT value of E_NOTIMPL.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="690a2-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="690a2-129">Requirements</span></span>  
 <span data-ttu-id="690a2-130">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="690a2-130">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="690a2-131">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="690a2-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="690a2-132">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="690a2-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="690a2-133">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="690a2-133">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="690a2-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="690a2-134">See Also</span></span>  
 <xref:System.Threading.ThreadPool.SetMinThreads%2A>  
 <xref:System.Threading.ThreadPool>  
 [<span data-ttu-id="690a2-135">GetMinThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="690a2-135">GetMinThreads Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-getminthreads-method.md)  
 [<span data-ttu-id="690a2-136">SetMaxThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="690a2-136">SetMaxThreads Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-setmaxthreads-method.md)  
 [<span data-ttu-id="690a2-137">IHostThreadPoolManager, interface</span><span class="sxs-lookup"><span data-stu-id="690a2-137">IHostThreadPoolManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-interface.md)
