---
title: IHostCrst::SetSpinCount, méthode
ms.date: 03/30/2017
api_name:
- IHostCrst.SetSpinCount
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostCrst::SetSpinCount
helpviewer_keywords:
- IHostCrst::SetSpinCount method [.NET Framework hosting]
- SetSpinCount method [.NET Framework hosting]
ms.assetid: 863fc8ce-9b8a-477e-8dd8-75c8544bb43a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ddae8f64eca348afa337b986ac81d59c37e51701
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54504299"
---
# <a name="ihostcrstsetspincount-method"></a><span data-ttu-id="f6920-102">IHostCrst::SetSpinCount, méthode</span><span class="sxs-lookup"><span data-stu-id="f6920-102">IHostCrst::SetSpinCount Method</span></span>
<span data-ttu-id="f6920-103">Définit le nombre de rotations actif [IHostCrst](../../../../docs/framework/unmanaged-api/hosting/ihostcrst-interface.md) instance.</span><span class="sxs-lookup"><span data-stu-id="f6920-103">Sets the spin count for the current [IHostCrst](../../../../docs/framework/unmanaged-api/hosting/ihostcrst-interface.md) instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f6920-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6920-104">Syntax</span></span>  
  
```  
HRESULT SetSpinCount (  
    [in] DWORD dwSpinCount  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f6920-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f6920-105">Parameters</span></span>  
 `dwSpinCount`  
 <span data-ttu-id="f6920-106">[in] Le nouveau décompte de sélection numérique pour actuel `IHostCrst` instance.</span><span class="sxs-lookup"><span data-stu-id="f6920-106">[in] The new spin count for the current `IHostCrst` instance.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f6920-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f6920-107">Return Value</span></span>  
  
|<span data-ttu-id="f6920-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f6920-108">HRESULT</span></span>|<span data-ttu-id="f6920-109">Description</span><span class="sxs-lookup"><span data-stu-id="f6920-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f6920-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="f6920-110">S_OK</span></span>|<span data-ttu-id="f6920-111">`SetSpinCount` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="f6920-111">`SetSpinCount` returned successfully.</span></span>|  
|<span data-ttu-id="f6920-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="f6920-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="f6920-113">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="f6920-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="f6920-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f6920-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="f6920-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="f6920-115">The call timed out.</span></span>|  
|<span data-ttu-id="f6920-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="f6920-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="f6920-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="f6920-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="f6920-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="f6920-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="f6920-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="f6920-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="f6920-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f6920-120">E_FAIL</span></span>|<span data-ttu-id="f6920-121">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f6920-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="f6920-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="f6920-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="f6920-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="f6920-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f6920-124">Notes</span><span class="sxs-lookup"><span data-stu-id="f6920-124">Remarks</span></span>  
 <span data-ttu-id="f6920-125">Sur les systèmes multiprocesseurs, si la section critique représentée par l’actuel `IHostCrst` instance n’est pas disponible, un thread appelant tourne `dwSpinCount` fois avant d’appeler [IHostSemaphore::Wait](../../../../docs/framework/unmanaged-api/hosting/ihostsemaphore-wait-method.md) sur un sémaphore associé avec la section critique.</span><span class="sxs-lookup"><span data-stu-id="f6920-125">On multi-processor systems, if the critical section represented by the current `IHostCrst` instance is unavailable, a calling thread spins `dwSpinCount` times before calling [IHostSemaphore::Wait](../../../../docs/framework/unmanaged-api/hosting/ihostsemaphore-wait-method.md) on a semaphore associated with the critical section.</span></span> <span data-ttu-id="f6920-126">Si la section critique se libère pendant l’opération de sélection numérique, le thread appelant évite l’opération d’attente.</span><span class="sxs-lookup"><span data-stu-id="f6920-126">If the critical section becomes free during the spin operation, the calling thread avoids the wait operation.</span></span>  
  
 <span data-ttu-id="f6920-127">L’utilisation de `dwSpinCount` est identique à l’utilisation du paramètre du même nom dans Win32 `InitializeCriticalSectionAndSpinCount` (fonction).</span><span class="sxs-lookup"><span data-stu-id="f6920-127">The usage of `dwSpinCount` is identical to the usage of the parameter of the same name in the Win32 `InitializeCriticalSectionAndSpinCount` function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f6920-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f6920-128">Requirements</span></span>  
 <span data-ttu-id="f6920-129">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f6920-129">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f6920-130">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="f6920-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f6920-131">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f6920-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f6920-132">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f6920-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f6920-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6920-133">See also</span></span>
- [<span data-ttu-id="f6920-134">ICLRSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="f6920-134">ICLRSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)
- [<span data-ttu-id="f6920-135">IHostCrst, interface</span><span class="sxs-lookup"><span data-stu-id="f6920-135">IHostCrst Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostcrst-interface.md)
- [<span data-ttu-id="f6920-136">IHostSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="f6920-136">IHostSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)
