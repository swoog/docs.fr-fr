---
title: IHostMAlloc::Alloc, méthode
ms.date: 03/30/2017
api_name:
- IHostMAlloc.Alloc
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMAlloc::Alloc
helpviewer_keywords:
- Alloc method, IHostMAlloc interface [.NET Framework hosting]
- IHostMAlloc::Alloc method [.NET Framework hosting]
ms.assetid: a3007f5e-d75d-4b37-842b-704e9edced5e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 32499e74e8af9a865347bd800d3db4c303a7344c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59126384"
---
# <a name="ihostmallocalloc-method"></a><span data-ttu-id="b660c-102">IHostMAlloc::Alloc, méthode</span><span class="sxs-lookup"><span data-stu-id="b660c-102">IHostMAlloc::Alloc Method</span></span>
<span data-ttu-id="b660c-103">Demande que l’hôte alloue la quantité de mémoire spécifiée à partir du tas.</span><span class="sxs-lookup"><span data-stu-id="b660c-103">Requests that the host allocate the specified amount of memory from the heap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b660c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b660c-104">Syntax</span></span>  
  
```  
HRESULT Alloc (  
    [in] SIZE_T  cbSize,   
    [in] EMemoryCriticalLevel dwCriticalLevel,   
    [out] void** ppMem  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b660c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b660c-105">Parameters</span></span>  
 `cbSize`  
 <span data-ttu-id="b660c-106">[in] La taille, en octets, de la demande d’allocation de mémoire actuelle.</span><span class="sxs-lookup"><span data-stu-id="b660c-106">[in] The size, in bytes, of the current memory allocation request.</span></span>  
  
 `dwCriticalLevel`  
 <span data-ttu-id="b660c-107">[in] Parmi les [EMemoryCriticalLevel](../../../../docs/framework/unmanaged-api/hosting/ememorycriticallevel-enumeration.md) valeurs, indiquant l’impact d’un échec d’allocation.</span><span class="sxs-lookup"><span data-stu-id="b660c-107">[in] One of the [EMemoryCriticalLevel](../../../../docs/framework/unmanaged-api/hosting/ememorycriticallevel-enumeration.md) values, indicating the impact of an allocation failure.</span></span>  
  
 `ppMem`  
 <span data-ttu-id="b660c-108">[out] Pointeur vers la mémoire allouée, ou null si la demande n’a pas pu être effectuée.</span><span class="sxs-lookup"><span data-stu-id="b660c-108">[out] A pointer to the allocated memory, or null if the request could not be completed.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b660c-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b660c-109">Return Value</span></span>  
  
|<span data-ttu-id="b660c-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="b660c-110">HRESULT</span></span>|<span data-ttu-id="b660c-111">Description</span><span class="sxs-lookup"><span data-stu-id="b660c-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="b660c-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="b660c-112">S_OK</span></span>|`Alloc` <span data-ttu-id="b660c-113">retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="b660c-113">returned successfully.</span></span>|  
|<span data-ttu-id="b660c-114">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="b660c-114">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="b660c-115">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="b660c-115">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="b660c-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="b660c-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="b660c-117">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="b660c-117">The call timed out.</span></span>|  
|<span data-ttu-id="b660c-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="b660c-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="b660c-119">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="b660c-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="b660c-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="b660c-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="b660c-121">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="b660c-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="b660c-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="b660c-122">E_FAIL</span></span>|<span data-ttu-id="b660c-123">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="b660c-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="b660c-124">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="b660c-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="b660c-125">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="b660c-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="b660c-126">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="b660c-126">E_OUTOFMEMORY</span></span>|<span data-ttu-id="b660c-127">Mémoire était insuffisante pour terminer la demande d’allocation.</span><span class="sxs-lookup"><span data-stu-id="b660c-127">Not enough memory was available to complete the allocation request.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b660c-128">Notes</span><span class="sxs-lookup"><span data-stu-id="b660c-128">Remarks</span></span>  
 <span data-ttu-id="b660c-129">Le CLR obtient un pointeur d’interface vers un `IHostMalloc` instance en appelant le [IHostMemoryManager::CreateMalloc](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-createmalloc-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="b660c-129">The CLR gets an interface pointer to an `IHostMalloc` instance by calling the [IHostMemoryManager::CreateMalloc](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-createmalloc-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b660c-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b660c-130">Requirements</span></span>  
 <span data-ttu-id="b660c-131">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b660c-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b660c-132">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="b660c-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="b660c-133">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b660c-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="b660c-134">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="b660c-134">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="b660c-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b660c-135">See also</span></span>

- [<span data-ttu-id="b660c-136">IHostMemoryManager, interface</span><span class="sxs-lookup"><span data-stu-id="b660c-136">IHostMemoryManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md)
- [<span data-ttu-id="b660c-137">IHostMalloc, interface</span><span class="sxs-lookup"><span data-stu-id="b660c-137">IHostMalloc Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmalloc-interface.md)
