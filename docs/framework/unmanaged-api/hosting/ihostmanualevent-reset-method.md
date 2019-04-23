---
title: IHostManualEvent::Reset, méthode
ms.date: 03/30/2017
api_name:
- IHostManualEvent.Reset
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostManualEvent::Reset
helpviewer_keywords:
- Reset method, IHostManualEvent interface [.NET Framework hosting]
- IHostManualEvent::Reset method [.NET Framework hosting]
ms.assetid: 0d101168-b5e3-49ce-90c7-85cf2db83c4c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9b3de70e6bdecba6370174ee825d2dec7c14270e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59148562"
---
# <a name="ihostmanualeventreset-method"></a><span data-ttu-id="6c436-102">IHostManualEvent::Reset, méthode</span><span class="sxs-lookup"><span data-stu-id="6c436-102">IHostManualEvent::Reset Method</span></span>
<span data-ttu-id="6c436-103">Réinitialise l’actuel [IHostManualEvent](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-interface.md) instance à un état non signalé.</span><span class="sxs-lookup"><span data-stu-id="6c436-103">Resets the current [IHostManualEvent](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-interface.md) instance to a non-signaled state.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6c436-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c436-104">Syntax</span></span>  
  
```  
HRESULT Reset ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="6c436-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="6c436-105">Return Value</span></span>  
  
|<span data-ttu-id="6c436-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="6c436-106">HRESULT</span></span>|<span data-ttu-id="6c436-107">Description</span><span class="sxs-lookup"><span data-stu-id="6c436-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="6c436-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="6c436-108">S_OK</span></span>|<span data-ttu-id="6c436-109">`Reset` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="6c436-109">`Reset` returned successfully.</span></span>|  
|<span data-ttu-id="6c436-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="6c436-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="6c436-111">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="6c436-111">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="6c436-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="6c436-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="6c436-113">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="6c436-113">The call timed out.</span></span>|  
|<span data-ttu-id="6c436-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="6c436-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="6c436-115">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="6c436-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="6c436-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="6c436-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="6c436-117">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="6c436-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="6c436-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="6c436-118">E_FAIL</span></span>|<span data-ttu-id="6c436-119">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="6c436-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="6c436-120">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="6c436-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="6c436-121">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="6c436-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="6c436-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c436-122">Requirements</span></span>  
 <span data-ttu-id="6c436-123">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6c436-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6c436-124">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="6c436-124">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="6c436-125">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6c436-125">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6c436-126">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6c436-126">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6c436-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c436-127">See also</span></span>

- [<span data-ttu-id="6c436-128">ICLRSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="6c436-128">ICLRSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)
- [<span data-ttu-id="6c436-129">IHostAutoEvent, interface</span><span class="sxs-lookup"><span data-stu-id="6c436-129">IHostAutoEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostautoevent-interface.md)
- [<span data-ttu-id="6c436-130">IHostManualEvent, interface</span><span class="sxs-lookup"><span data-stu-id="6c436-130">IHostManualEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-interface.md)
- [<span data-ttu-id="6c436-131">IHostSemaphore, interface</span><span class="sxs-lookup"><span data-stu-id="6c436-131">IHostSemaphore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsemaphore-interface.md)
- [<span data-ttu-id="6c436-132">IHostSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="6c436-132">IHostSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)
