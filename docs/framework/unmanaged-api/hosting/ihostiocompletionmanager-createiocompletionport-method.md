---
title: IHostIoCompletionManager::CreateIoCompletionPort, méthode
ms.date: 03/30/2017
api_name:
- IHostIoCompletionManager.CreateIoCompletionPort
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostIoCompletionManager::CreateIoCompletionPort
helpviewer_keywords:
- IHostIoCompletionManager::CreateIoCompletionPort method [.NET Framework hosting]
- CreateIoCompletionPort method [.NET Framework hosting]
ms.assetid: 907a2b43-68db-44a7-acac-89e792e7bb3c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 52e1dd05a87eaf06b5352d7c8d63c402a65d95ab
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33439073"
---
# <a name="ihostiocompletionmanagercreateiocompletionport-method"></a><span data-ttu-id="e7f6a-102">IHostIoCompletionManager::CreateIoCompletionPort, méthode</span><span class="sxs-lookup"><span data-stu-id="e7f6a-102">IHostIoCompletionManager::CreateIoCompletionPort Method</span></span>
<span data-ttu-id="e7f6a-103">Demande que l’hôte crée un nouveau port de terminaison d’e/s.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-103">Requests that the host create a new I/O completion port.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e7f6a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7f6a-104">Syntax</span></span>  
  
```  
HRESULT CreateIoCompletionPort (  
    [out] HANDLE *phPort  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e7f6a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7f6a-105">Parameters</span></span>  
 `phPort`  
 <span data-ttu-id="e7f6a-106">[out] Pointeur vers un handle vers le port de terminaison d’e/s nouvellement créé, ou 0 (zéro) si le port n’a pas pu être créé.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-106">[out] A pointer to a handle to the newly created I/O completion port, or 0 (zero), if the port could not be created.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e7f6a-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e7f6a-107">Return Value</span></span>  
  
|<span data-ttu-id="e7f6a-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="e7f6a-108">HRESULT</span></span>|<span data-ttu-id="e7f6a-109">Description</span><span class="sxs-lookup"><span data-stu-id="e7f6a-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="e7f6a-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="e7f6a-110">S_OK</span></span>|<span data-ttu-id="e7f6a-111">`CreateIoCompletionPort` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-111">`CreateIoCompletionPort` returned successfully.</span></span>|  
|<span data-ttu-id="e7f6a-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="e7f6a-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="e7f6a-113">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="e7f6a-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="e7f6a-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="e7f6a-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-115">The call timed out.</span></span>|  
|<span data-ttu-id="e7f6a-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="e7f6a-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="e7f6a-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="e7f6a-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="e7f6a-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="e7f6a-119">Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="e7f6a-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e7f6a-120">E_FAIL</span></span>|<span data-ttu-id="e7f6a-121">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="e7f6a-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="e7f6a-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="e7f6a-124">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="e7f6a-124">E_OUTOFMEMORY</span></span>|<span data-ttu-id="e7f6a-125">Mémoire était insuffisante pour allouer la ressource demandée.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-125">Not enough memory was available to allocate the requested resource.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e7f6a-126">Notes</span><span class="sxs-lookup"><span data-stu-id="e7f6a-126">Remarks</span></span>  
 <span data-ttu-id="e7f6a-127">Le CLR appelle la `CreateIoCompletionPort` méthode pour demander que l’hôte crée un nouveau port de terminaison d’e/s.</span><span class="sxs-lookup"><span data-stu-id="e7f6a-127">The CLR calls the `CreateIoCompletionPort` method to request that the host create a new I/O completion port.</span></span> <span data-ttu-id="e7f6a-128">Elle lie les opérations d’e/s à ce port via un appel à la [IHostIoCompletionManager::Bind](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-bind-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="e7f6a-128">It binds I/O operations to this port through a call to the [IHostIoCompletionManager::Bind](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-bind-method.md) method.</span></span> <span data-ttu-id="e7f6a-129">L’hôte signale l’état au CLR en appelant [ICLRIoCompletionManager::OnComplete](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-oncomplete-method.md).</span><span class="sxs-lookup"><span data-stu-id="e7f6a-129">The host reports status back to the CLR by calling [ICLRIoCompletionManager::OnComplete](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-oncomplete-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e7f6a-130">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e7f6a-130">Requirements</span></span>  
 <span data-ttu-id="e7f6a-131">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e7f6a-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e7f6a-132">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="e7f6a-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e7f6a-133">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e7f6a-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e7f6a-134">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e7f6a-134">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e7f6a-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7f6a-135">See Also</span></span>  
 [<span data-ttu-id="e7f6a-136">ICLRIoCompletionManager, interface</span><span class="sxs-lookup"><span data-stu-id="e7f6a-136">ICLRIoCompletionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-interface.md)  
 [<span data-ttu-id="e7f6a-137">IHostIoCompletionManager, interface</span><span class="sxs-lookup"><span data-stu-id="e7f6a-137">IHostIoCompletionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-interface.md)
