---
title: IHostMAlloc::DebugAlloc, méthode
ms.date: 03/30/2017
api_name:
- IHostMAlloc.DebugAlloc
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMAlloc::DebugAlloc
helpviewer_keywords:
- DebugAlloc method [.NET Framework hosting]
- IHostMAlloc::DebugAlloc method [.NET Framework hosting]
ms.assetid: 0bfbc527-bea2-43ce-b041-69186f4440dd
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6e089d133374f112dea13e91f9bd571bd2b5af07
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59132923"
---
# <a name="ihostmallocdebugalloc-method"></a><span data-ttu-id="1622f-102">IHostMAlloc::DebugAlloc, méthode</span><span class="sxs-lookup"><span data-stu-id="1622f-102">IHostMAlloc::DebugAlloc Method</span></span>
<span data-ttu-id="1622f-103">Demande que l’hôte alloue la quantité de mémoire spécifiée à partir du tas et en outre suivre où la mémoire a été allouée.</span><span class="sxs-lookup"><span data-stu-id="1622f-103">Requests that the host allocate the specified amount of memory from the heap, and additionally track where the memory was allocated.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1622f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1622f-104">Syntax</span></span>  
  
```  
HRESULT DebugAlloc (  
    [in]  SIZE_T  cbSize,   
    [in]  EMemoryCriticalLevel dwCriticalLevel,   
    [in]  char*   pszFileName,   
    [in]  int     iLineNo,   
    [out] void**  ppMem  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1622f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1622f-105">Parameters</span></span>  
 `cbSize`  
 <span data-ttu-id="1622f-106">[in] La taille, en octets, de la demande d’allocation de mémoire actuelle.</span><span class="sxs-lookup"><span data-stu-id="1622f-106">[in] The size, in bytes, of the current memory allocation request.</span></span>  
  
 `dwCriticalLevel`  
 <span data-ttu-id="1622f-107">[in] Parmi les [EMemoryCriticalLevel](../../../../docs/framework/unmanaged-api/hosting/ememorycriticallevel-enumeration.md) valeurs, indiquant l’impact d’un échec d’allocation.</span><span class="sxs-lookup"><span data-stu-id="1622f-107">[in] One of the [EMemoryCriticalLevel](../../../../docs/framework/unmanaged-api/hosting/ememorycriticallevel-enumeration.md) values, indicating the impact of an allocation failure.</span></span>  
  
 `pszFileName`  
 <span data-ttu-id="1622f-108">[in] Le fichier de code de l’exécutable en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="1622f-108">[in] The code file of the executable being debugged.</span></span>  
  
 `iLineNo`  
 <span data-ttu-id="1622f-109">[in] Numéro de ligne dans `pszFileName` où l’allocation a été demandée.</span><span class="sxs-lookup"><span data-stu-id="1622f-109">[in] The line number in `pszFileName` where the allocation was requested.</span></span>  
  
 `ppMem`  
 <span data-ttu-id="1622f-110">[out] Pointeur vers la mémoire allouée, ou null si la demande n’a pas pu être effectuée.</span><span class="sxs-lookup"><span data-stu-id="1622f-110">[out] A pointer to the allocated memory, or null if the request could not be completed.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1622f-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="1622f-111">Return Value</span></span>  
  
|<span data-ttu-id="1622f-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="1622f-112">HRESULT</span></span>|<span data-ttu-id="1622f-113">Description</span><span class="sxs-lookup"><span data-stu-id="1622f-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="1622f-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="1622f-114">S_OK</span></span>|`DebugAlloc` <span data-ttu-id="1622f-115">retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="1622f-115">returned successfully.</span></span>|  
|<span data-ttu-id="1622f-116">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="1622f-116">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="1622f-117">Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="1622f-117">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="1622f-118">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="1622f-118">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="1622f-119">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="1622f-119">The call timed out.</span></span>|  
|<span data-ttu-id="1622f-120">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="1622f-120">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="1622f-121">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="1622f-121">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="1622f-122">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="1622f-122">HOST_E_ABANDONED</span></span>|<span data-ttu-id="1622f-123">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="1622f-123">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="1622f-124">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="1622f-124">E_FAIL</span></span>|<span data-ttu-id="1622f-125">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="1622f-125">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="1622f-126">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="1622f-126">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="1622f-127">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="1622f-127">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="1622f-128">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="1622f-128">E_OUTOFMEMORY</span></span>|<span data-ttu-id="1622f-129">Mémoire était insuffisante pour terminer la demande d’allocation.</span><span class="sxs-lookup"><span data-stu-id="1622f-129">Not enough memory was available to complete the allocation request.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1622f-130">Notes</span><span class="sxs-lookup"><span data-stu-id="1622f-130">Remarks</span></span>  
 <span data-ttu-id="1622f-131">Le CLR obtient un pointeur d’interface vers un [IHostMalloc](../../../../docs/framework/unmanaged-api/hosting/ihostmalloc-interface.md) instance en appelant le [IHostMemoryManager::CreateMalloc](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-createmalloc-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="1622f-131">The CLR gets an interface pointer to an [IHostMalloc](../../../../docs/framework/unmanaged-api/hosting/ihostmalloc-interface.md) instance by calling the [IHostMemoryManager::CreateMalloc](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-createmalloc-method.md) method.</span></span> `DebugAlloc` <span data-ttu-id="1622f-132">permet au runtime obtenir des informations de fichier de code pour une utilisation pendant le débogage.</span><span class="sxs-lookup"><span data-stu-id="1622f-132">allows the runtime to get code file information for use during debugging.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1622f-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1622f-133">Requirements</span></span>  
 <span data-ttu-id="1622f-134">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1622f-134">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1622f-135">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="1622f-135">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="1622f-136">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1622f-136">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="1622f-137">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="1622f-137">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="1622f-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1622f-138">See also</span></span>

- [<span data-ttu-id="1622f-139">IHostMemoryManager, interface</span><span class="sxs-lookup"><span data-stu-id="1622f-139">IHostMemoryManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md)
- [<span data-ttu-id="1622f-140">IHostMalloc, interface</span><span class="sxs-lookup"><span data-stu-id="1622f-140">IHostMalloc Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmalloc-interface.md)
