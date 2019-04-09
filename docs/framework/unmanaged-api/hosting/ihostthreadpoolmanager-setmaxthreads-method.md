---
title: IHostThreadPoolManager::SetMaxThreads, méthode
ms.date: 03/30/2017
api_name:
- IHostThreadPoolManager.SetMaxThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostThreadPoolManager::SetMaxThreads
helpviewer_keywords:
- IHostThreadPoolManager::SetMaxThreads method [.NET Framework hosting]
- SetMaxThreads method, IHostThreadPoolManager interface [.NET Framework hosting]
ms.assetid: 77cfd347-95c2-4425-b807-4ecc2a8d4578
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0df8d11bba870dfec880401064ec3f78f5f04e1f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59081474"
---
# <a name="ihostthreadpoolmanagersetmaxthreads-method"></a><span data-ttu-id="f5458-102">IHostThreadPoolManager::SetMaxThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="f5458-102">IHostThreadPoolManager::SetMaxThreads Method</span></span>
<span data-ttu-id="f5458-103">Définit le nombre maximal de threads que l’hôte peut gérer dans le pool de threads.</span><span class="sxs-lookup"><span data-stu-id="f5458-103">Sets the maximum number of threads that the host can maintain in the thread pool.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f5458-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5458-104">Syntax</span></span>  
  
```  
HRESULT SetMaxThreads (  
    [in] DWORD MaxThreads  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f5458-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5458-105">Parameters</span></span>  
 `MaxThreads`  
 <span data-ttu-id="f5458-106">Nombre maximal de threads de travail dans le pool de threads.</span><span class="sxs-lookup"><span data-stu-id="f5458-106">The maximum number of worker threads in the thread pool.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f5458-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f5458-107">Return Value</span></span>  
  
|<span data-ttu-id="f5458-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f5458-108">HRESULT</span></span>|<span data-ttu-id="f5458-109">Description</span><span class="sxs-lookup"><span data-stu-id="f5458-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f5458-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="f5458-110">S_OK</span></span>|`SetMaxThreads` <span data-ttu-id="f5458-111">retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="f5458-111">returned successfully.</span></span>|  
|<span data-ttu-id="f5458-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="f5458-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="f5458-113">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="f5458-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="f5458-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f5458-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="f5458-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="f5458-115">The call timed out.</span></span>|  
|<span data-ttu-id="f5458-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="f5458-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="f5458-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="f5458-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="f5458-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="f5458-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="f5458-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="f5458-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="f5458-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f5458-120">E_FAIL</span></span>|<span data-ttu-id="f5458-121">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f5458-121">An unknown, catastrophic failure occurred.</span></span> <span data-ttu-id="f5458-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="f5458-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="f5458-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="f5458-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="f5458-124">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="f5458-124">E_NOTIMPL</span></span>|<span data-ttu-id="f5458-125">L’hôte ne fournit pas une implémentation de `SetMaxThreads`.</span><span class="sxs-lookup"><span data-stu-id="f5458-125">The host does not provide an implementation of `SetMaxThreads`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f5458-126">Notes</span><span class="sxs-lookup"><span data-stu-id="f5458-126">Remarks</span></span>  
 <span data-ttu-id="f5458-127">Un hôte n’est pas requis pour permettre au CLR configurer la taille du pool de threads.</span><span class="sxs-lookup"><span data-stu-id="f5458-127">A host is not required to allow the CLR to configure the size of the thread pool.</span></span> <span data-ttu-id="f5458-128">Certains hôtes peuvent vouloir le contrôle exclusif sur le pool de threads, pour des raisons telles que l’implémentation, de performances ou d’évolutivité.</span><span class="sxs-lookup"><span data-stu-id="f5458-128">Some hosts might want exclusive control over the thread pool, for reasons such as implementation, performance, or scalability.</span></span> <span data-ttu-id="f5458-129">Dans ce cas, un hôte doit retourner une valeur HRESULT d’E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="f5458-129">In this case, a host should return an HRESULT value of E_NOTIMPL.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f5458-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5458-130">Requirements</span></span>  
 <span data-ttu-id="f5458-131">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f5458-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f5458-132">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="f5458-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f5458-133">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f5458-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="f5458-134">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="f5458-134">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="f5458-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5458-135">See also</span></span>

- <xref:System.Threading.ThreadPool.SetMaxThreads%2A>
- <xref:System.Threading.ThreadPool>
- [<span data-ttu-id="f5458-136">GetMaxThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="f5458-136">GetMaxThreads Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-getmaxthreads-method.md)
- [<span data-ttu-id="f5458-137">SetMinThreads, méthode</span><span class="sxs-lookup"><span data-stu-id="f5458-137">SetMinThreads Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-setminthreads-method.md)
- [<span data-ttu-id="f5458-138">IHostThreadPoolManager, interface</span><span class="sxs-lookup"><span data-stu-id="f5458-138">IHostThreadPoolManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-interface.md)
