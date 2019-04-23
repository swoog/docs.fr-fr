---
title: IHostIoCompletionManager::SetCLRIoCompletionManager, méthode
ms.date: 03/30/2017
api_name:
- IHostIoCompletionManager.SetCLRIoCompletionManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostIoCompletionManager::SetCLRIoCompletionManager
helpviewer_keywords:
- IHostIoCompletionManager::SetCLRIoCompletionManager method [.NET Framework hosting]
- SetCLRIoCompletionManager method [.NET Framework hosting]
ms.assetid: 4254bb01-3a14-4f34-a3be-60ff1f5072b5
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cd48664c78e3f5772cdfa655ebbc7cfa716f4950
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59107196"
---
# <a name="ihostiocompletionmanagersetclriocompletionmanager-method"></a><span data-ttu-id="162d3-102">IHostIoCompletionManager::SetCLRIoCompletionManager, méthode</span><span class="sxs-lookup"><span data-stu-id="162d3-102">IHostIoCompletionManager::SetCLRIoCompletionManager Method</span></span>
<span data-ttu-id="162d3-103">Fournit à l’hôte avec un pointeur d’interface vers le [ICLRIoCompletionManager](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-interface.md) instance implémentée par le common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="162d3-103">Provides the host with an interface pointer to the [ICLRIoCompletionManager](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-interface.md) instance implemented by the common language runtime (CLR).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="162d3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="162d3-104">Syntax</span></span>  
  
```  
HRESULT SetCLRIoCompletionManager (  
    [in] ICLRIoCompletionManager *pManager  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="162d3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="162d3-105">Parameters</span></span>  
 `pManager`  
 <span data-ttu-id="162d3-106">[in] Un pointeur d’interface vers un `ICLRIoCompletionManager` instance fournie par le CLR.</span><span class="sxs-lookup"><span data-stu-id="162d3-106">[in] An interface pointer to an `ICLRIoCompletionManager` instance provided by the CLR.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="162d3-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="162d3-107">Return Value</span></span>  
  
|<span data-ttu-id="162d3-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="162d3-108">HRESULT</span></span>|<span data-ttu-id="162d3-109">Description</span><span class="sxs-lookup"><span data-stu-id="162d3-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="162d3-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="162d3-110">S_OK</span></span>|<span data-ttu-id="162d3-111">`SetCLRIoCompletionManager` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="162d3-111">`SetCLRIoCompletionManager` returned successfully.</span></span>|  
|<span data-ttu-id="162d3-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="162d3-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="162d3-113">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="162d3-113">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="162d3-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="162d3-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="162d3-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="162d3-115">The call timed out.</span></span>|  
|<span data-ttu-id="162d3-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="162d3-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="162d3-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="162d3-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="162d3-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="162d3-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="162d3-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="162d3-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="162d3-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="162d3-120">E_FAIL</span></span>|<span data-ttu-id="162d3-121">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="162d3-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="162d3-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="162d3-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="162d3-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="162d3-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="162d3-124">Notes</span><span class="sxs-lookup"><span data-stu-id="162d3-124">Remarks</span></span>  
 <span data-ttu-id="162d3-125">Une fois que le CLR a appelé `SetCLRIoCompletionManager`, l’hôte doit appeler [ICLRIoCompletionManager::OnComplete](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-oncomplete-method.md) pour informer le CLR lorsqu’une demande d’e/s a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="162d3-125">After the CLR has called `SetCLRIoCompletionManager`, the host must call [ICLRIoCompletionManager::OnComplete](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-oncomplete-method.md) to notify the CLR when an I/O request has been completed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="162d3-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="162d3-126">Requirements</span></span>  
 <span data-ttu-id="162d3-127">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="162d3-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="162d3-128">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="162d3-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="162d3-129">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="162d3-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="162d3-130">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="162d3-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="162d3-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="162d3-131">See also</span></span>

- [<span data-ttu-id="162d3-132">ICLRIoCompletionManager, interface</span><span class="sxs-lookup"><span data-stu-id="162d3-132">ICLRIoCompletionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-interface.md)
- [<span data-ttu-id="162d3-133">IHostIoCompletionManager, interface</span><span class="sxs-lookup"><span data-stu-id="162d3-133">IHostIoCompletionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-interface.md)
