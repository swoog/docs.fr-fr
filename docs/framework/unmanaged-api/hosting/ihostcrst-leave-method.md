---
title: IHostCrst::Leave, méthode
ms.date: 03/30/2017
api_name:
- IHostCrst.Leave
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostCrst::Leave
helpviewer_keywords:
- IHostCrst::Leave method [.NET Framework hosting]
- Leave method [.NET Framework hosting]
ms.assetid: dfc51d9e-b36d-4dba-9ea1-4f63fa0601ae
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2d60cdee0a5357f7e117dc902b073049f3bbaea9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61984384"
---
# <a name="ihostcrstleave-method"></a><span data-ttu-id="cc7e1-102">IHostCrst::Leave, méthode</span><span class="sxs-lookup"><span data-stu-id="cc7e1-102">IHostCrst::Leave Method</span></span>
<span data-ttu-id="cc7e1-103">Quitte la section critique qui est représentée par l’instance actuelle de [IHostCrst](../../../../docs/framework/unmanaged-api/hosting/ihostcrst-interface.md).</span><span class="sxs-lookup"><span data-stu-id="cc7e1-103">Leaves the critical section that is represented by the current instance of [IHostCrst](../../../../docs/framework/unmanaged-api/hosting/ihostcrst-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cc7e1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc7e1-104">Syntax</span></span>  
  
```  
HRESULT Leave ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="cc7e1-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="cc7e1-105">Return Value</span></span>  
  
|<span data-ttu-id="cc7e1-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="cc7e1-106">HRESULT</span></span>|<span data-ttu-id="cc7e1-107">Description</span><span class="sxs-lookup"><span data-stu-id="cc7e1-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="cc7e1-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="cc7e1-108">S_OK</span></span>|<span data-ttu-id="cc7e1-109">`Leave` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="cc7e1-109">`Leave` returned successfully.</span></span>|  
|<span data-ttu-id="cc7e1-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="cc7e1-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="cc7e1-111">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="cc7e1-111">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="cc7e1-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="cc7e1-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="cc7e1-113">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="cc7e1-113">The call timed out.</span></span>|  
|<span data-ttu-id="cc7e1-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="cc7e1-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="cc7e1-115">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="cc7e1-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="cc7e1-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="cc7e1-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="cc7e1-117">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="cc7e1-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="cc7e1-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="cc7e1-118">E_FAIL</span></span>|<span data-ttu-id="cc7e1-119">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="cc7e1-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="cc7e1-120">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="cc7e1-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="cc7e1-121">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="cc7e1-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cc7e1-122">Notes</span><span class="sxs-lookup"><span data-stu-id="cc7e1-122">Remarks</span></span>  
 <span data-ttu-id="cc7e1-123">`Leave` permet au CLR de communiquer directement avec threading implémentation, à l’hôte lieu d’utiliser Win32 correspondante `LeaveCriticalSection` (fonction).</span><span class="sxs-lookup"><span data-stu-id="cc7e1-123">`Leave` allows the CLR to communicate directly with the host's threading implementation, rather than using the corresponding Win32 `LeaveCriticalSection` function.</span></span> <span data-ttu-id="cc7e1-124">Un thread qui assume la propriété de la section critique représentée par le `IHostCrst` instance doit appeler `Leave` une fois que chaque fois qu’il entre dans cette section critique.</span><span class="sxs-lookup"><span data-stu-id="cc7e1-124">A thread that takes ownership of the critical section represented by the current `IHostCrst` instance must call `Leave` once for each time it enters that critical section.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cc7e1-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc7e1-125">Requirements</span></span>  
 <span data-ttu-id="cc7e1-126">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cc7e1-126">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cc7e1-127">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="cc7e1-127">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="cc7e1-128">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cc7e1-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="cc7e1-129">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cc7e1-129">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cc7e1-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc7e1-130">See also</span></span>

- [<span data-ttu-id="cc7e1-131">ICLRSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="cc7e1-131">ICLRSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)
- [<span data-ttu-id="cc7e1-132">IHostCrst, interface</span><span class="sxs-lookup"><span data-stu-id="cc7e1-132">IHostCrst Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostcrst-interface.md)
- [<span data-ttu-id="cc7e1-133">IHostSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="cc7e1-133">IHostSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)
