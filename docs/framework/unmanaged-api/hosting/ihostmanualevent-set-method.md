---
title: IHostManualEvent::Set, méthode
ms.date: 03/30/2017
api_name:
- IHostManualEvent.Set
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostManualEvent::Set
helpviewer_keywords:
- Set method, IHostManualEvent interface [.NET Framework hosting]
- IHostManualEvent::Set method [.NET Framework hosting]
ms.assetid: e930c174-f71d-4faa-bb59-f0fb3df4d77b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 674745636033f42eb8fb67babf6f5a3f013491c0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61993211"
---
# <a name="ihostmanualeventset-method"></a><span data-ttu-id="a36fd-102">IHostManualEvent::Set, méthode</span><span class="sxs-lookup"><span data-stu-id="a36fd-102">IHostManualEvent::Set Method</span></span>
<span data-ttu-id="a36fd-103">Définit l’actuel [IHostManualEvent](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-interface.md) instance à un état signalé.</span><span class="sxs-lookup"><span data-stu-id="a36fd-103">Sets the current [IHostManualEvent](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-interface.md) instance to a signaled state.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a36fd-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a36fd-104">Syntax</span></span>  
  
```  
HRESULT Set ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="a36fd-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a36fd-105">Return Value</span></span>  
  
|<span data-ttu-id="a36fd-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="a36fd-106">HRESULT</span></span>|<span data-ttu-id="a36fd-107">Description</span><span class="sxs-lookup"><span data-stu-id="a36fd-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="a36fd-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="a36fd-108">S_OK</span></span>|<span data-ttu-id="a36fd-109">`Set` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="a36fd-109">`Set` returned successfully.</span></span>|  
|<span data-ttu-id="a36fd-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="a36fd-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="a36fd-111">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="a36fd-111">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="a36fd-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="a36fd-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="a36fd-113">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="a36fd-113">The call timed out.</span></span>|  
|<span data-ttu-id="a36fd-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="a36fd-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="a36fd-115">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="a36fd-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="a36fd-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="a36fd-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="a36fd-117">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="a36fd-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="a36fd-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="a36fd-118">E_FAIL</span></span>|<span data-ttu-id="a36fd-119">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="a36fd-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="a36fd-120">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="a36fd-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="a36fd-121">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="a36fd-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a36fd-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a36fd-122">Requirements</span></span>  
 <span data-ttu-id="a36fd-123">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a36fd-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a36fd-124">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a36fd-124">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a36fd-125">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a36fd-125">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a36fd-126">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a36fd-126">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a36fd-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a36fd-127">See also</span></span>

- [<span data-ttu-id="a36fd-128">ICLRSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="a36fd-128">ICLRSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)
- [<span data-ttu-id="a36fd-129">IHostAutoEvent, interface</span><span class="sxs-lookup"><span data-stu-id="a36fd-129">IHostAutoEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostautoevent-interface.md)
- [<span data-ttu-id="a36fd-130">IHostManualEvent, interface</span><span class="sxs-lookup"><span data-stu-id="a36fd-130">IHostManualEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-interface.md)
- [<span data-ttu-id="a36fd-131">IHostSemaphore, interface</span><span class="sxs-lookup"><span data-stu-id="a36fd-131">IHostSemaphore Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsemaphore-interface.md)
- [<span data-ttu-id="a36fd-132">IHostSyncManager, interface</span><span class="sxs-lookup"><span data-stu-id="a36fd-132">IHostSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)
