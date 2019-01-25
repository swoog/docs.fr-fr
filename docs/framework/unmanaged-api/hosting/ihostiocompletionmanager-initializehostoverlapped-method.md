---
title: IHostIoCompletionManager::InitializeHostOverlapped, méthode
ms.date: 03/30/2017
api_name:
- IHostIoCompletionManager.InitializeHostOverlapped
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostIoCompletionManager::InitializeHostOverlapped
helpviewer_keywords:
- IHostIoCompletionManager::InitializeHostOverlapped method [.NET Framework hosting]
- InitializeHostOverlapped method [.NET Framework hosting]
ms.assetid: c35199bf-bc47-4901-b467-4e8a37644bbb
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2951b408efa39e1ac2afbd7d8ebcb5ea139a8a71
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54582447"
---
# <a name="ihostiocompletionmanagerinitializehostoverlapped-method"></a><span data-ttu-id="65ffa-102">IHostIoCompletionManager::InitializeHostOverlapped, méthode</span><span class="sxs-lookup"><span data-stu-id="65ffa-102">IHostIoCompletionManager::InitializeHostOverlapped Method</span></span>
<span data-ttu-id="65ffa-103">Fournit à l’hôte avec la possibilité d’initialiser toutes les données personnalisées à ajouter à un Win32 `OVERLAPPED` structure qui est utilisé pour les demandes d’e/s asynchrones.</span><span class="sxs-lookup"><span data-stu-id="65ffa-103">Provides the host with an opportunity to initialize any custom data to append to a Win32 `OVERLAPPED` structure that is used for asynchronous I/O requests.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="65ffa-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65ffa-104">Syntax</span></span>  
  
```  
HRESULT InitializeHostOverlapped (  
    [in] void* pvOverlapped  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="65ffa-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65ffa-105">Parameters</span></span>  
 `pvOverlapped`  
 <span data-ttu-id="65ffa-106">[in] Un pointeur vers Win32 `OVERLAPPED` structure pour être inclus dans la demande d’e/s.</span><span class="sxs-lookup"><span data-stu-id="65ffa-106">[in] A pointer to the Win32 `OVERLAPPED` structure to be included with the I/O request.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="65ffa-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="65ffa-107">Return Value</span></span>  
  
|<span data-ttu-id="65ffa-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="65ffa-108">HRESULT</span></span>|<span data-ttu-id="65ffa-109">Description</span><span class="sxs-lookup"><span data-stu-id="65ffa-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="65ffa-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="65ffa-110">S_OK</span></span>|<span data-ttu-id="65ffa-111">`InitializeHostOverlapped` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="65ffa-111">`InitializeHostOverlapped` returned successfully.</span></span>|  
|<span data-ttu-id="65ffa-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="65ffa-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="65ffa-113">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="65ffa-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="65ffa-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="65ffa-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="65ffa-115">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="65ffa-115">The call timed out.</span></span>|  
|<span data-ttu-id="65ffa-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="65ffa-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="65ffa-117">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="65ffa-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="65ffa-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="65ffa-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="65ffa-119">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="65ffa-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="65ffa-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="65ffa-120">E_FAIL</span></span>|<span data-ttu-id="65ffa-121">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="65ffa-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="65ffa-122">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="65ffa-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="65ffa-123">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="65ffa-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="65ffa-124">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="65ffa-124">E_OUTOFMEMORY</span></span>|<span data-ttu-id="65ffa-125">Mémoire était insuffisante pour allouer la ressource demandée.</span><span class="sxs-lookup"><span data-stu-id="65ffa-125">Not enough memory was available to allocate the requested resource.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="65ffa-126">Notes</span><span class="sxs-lookup"><span data-stu-id="65ffa-126">Remarks</span></span>  
 <span data-ttu-id="65ffa-127">La plateforme Windows fonctions utilisent la `OVERLAPPED` structure pour stocker l’état des demandes d’e/s asynchrones.</span><span class="sxs-lookup"><span data-stu-id="65ffa-127">The Windows Platform functions use the `OVERLAPPED` structure to store state for asynchronous I/O requests.</span></span> <span data-ttu-id="65ffa-128">Le CLR appelle le `InitializeHostOverlapped` méthode pour permettre à l’hôte pour ajouter des données personnalisées à un `OVERLAPPED` instance.</span><span class="sxs-lookup"><span data-stu-id="65ffa-128">The CLR calls the `InitializeHostOverlapped` method to give the host the opportunity to append custom data to an `OVERLAPPED` instance.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="65ffa-129">Pour atteindre le début de leur bloc de données personnalisées, les hôtes doivent définir le décalage à la taille de la `OVERLAPPED` structure (`sizeof(OVERLAPPED)`).</span><span class="sxs-lookup"><span data-stu-id="65ffa-129">To get to the beginning of their custom data block, hosts must set the offset to the size of the `OVERLAPPED` structure (`sizeof(OVERLAPPED)`).</span></span>  
  
 <span data-ttu-id="65ffa-130">Une valeur de retour E_OUTOFMEMORY indique que l’hôte n’a pas pu initialiser ses données personnalisées.</span><span class="sxs-lookup"><span data-stu-id="65ffa-130">A return value of E_OUTOFMEMORY indicates that the host has failed to initialize its custom data.</span></span> <span data-ttu-id="65ffa-131">Dans ce cas, le CLR signale une erreur et fait échouer l’appel.</span><span class="sxs-lookup"><span data-stu-id="65ffa-131">In this case, the CLR reports an error and fails the call.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="65ffa-132">Spécifications</span><span class="sxs-lookup"><span data-stu-id="65ffa-132">Requirements</span></span>  
 <span data-ttu-id="65ffa-133">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="65ffa-133">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="65ffa-134">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="65ffa-134">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="65ffa-135">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="65ffa-135">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="65ffa-136">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="65ffa-136">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="65ffa-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65ffa-137">See also</span></span>
- [<span data-ttu-id="65ffa-138">ICLRIoCompletionManager, interface</span><span class="sxs-lookup"><span data-stu-id="65ffa-138">ICLRIoCompletionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-interface.md)
- [<span data-ttu-id="65ffa-139">GetHostOverlappedSize, méthode</span><span class="sxs-lookup"><span data-stu-id="65ffa-139">GetHostOverlappedSize Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-gethostoverlappedsize-method.md)
- [<span data-ttu-id="65ffa-140">IHostIoCompletionManager, interface</span><span class="sxs-lookup"><span data-stu-id="65ffa-140">IHostIoCompletionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-interface.md)
