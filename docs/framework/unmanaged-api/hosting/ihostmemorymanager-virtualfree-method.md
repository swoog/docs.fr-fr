---
title: IHostMemoryManager::VirtualFree, méthode
ms.date: 03/30/2017
api_name:
- IHostMemoryManager.VirtualFree
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMemoryManager::VirtualFree
helpviewer_keywords:
- IHostMemoryManager::VirtualFree method [.NET Framework hosting]
- VirtualFree method [.NET Framework hosting]
ms.assetid: 1a436e89-eb28-4d15-bcf1-a072f86dbd99
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 03cac2b8433d6491d1fa474a0d4064ef4e260d6e
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59099909"
---
# <a name="ihostmemorymanagervirtualfree-method"></a><span data-ttu-id="0542c-102">IHostMemoryManager::VirtualFree, méthode</span><span class="sxs-lookup"><span data-stu-id="0542c-102">IHostMemoryManager::VirtualFree Method</span></span>
<span data-ttu-id="0542c-103">Sert de wrapper logique pour la fonction Win32 correspondante.</span><span class="sxs-lookup"><span data-stu-id="0542c-103">Serves as a logical wrapper for the corresponding Win32 function.</span></span> <span data-ttu-id="0542c-104">L’implémentation Win32 de `VirtualFree` libère, annule la validation, ou bien libère et annule la validation d’une région de pages au sein de l’espace d’adressage virtuel du processus appelant.</span><span class="sxs-lookup"><span data-stu-id="0542c-104">The Win32 implementation of `VirtualFree` releases, decommits, or releases and decommits a region of pages within the virtual address space of the calling process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0542c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0542c-105">Syntax</span></span>  
  
```  
HRESULT VirtualFree (  
    [in] LPVOID  lpAddress,  
    [in] SIZE_T  dwSize,  
    [in] DWORD   dwFreeType  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0542c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0542c-106">Parameters</span></span>  
 `lpAddress`  
 <span data-ttu-id="0542c-107">[in] Pointeur vers l’adresse de base des pages de mémoire virtuelle à libérer.</span><span class="sxs-lookup"><span data-stu-id="0542c-107">[in] A pointer to the base address of the virtual memory pages to be freed.</span></span>  
  
 `dwSize`  
 <span data-ttu-id="0542c-108">[in] La taille, en octets, de la région à libérer.</span><span class="sxs-lookup"><span data-stu-id="0542c-108">[in] The size, in bytes, of the region to be freed.</span></span>  
  
 `dwFreeType`  
 <span data-ttu-id="0542c-109">[in] Le type d’opération de libération.</span><span class="sxs-lookup"><span data-stu-id="0542c-109">[in] The type of freeing operation.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0542c-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0542c-110">Return Value</span></span>  
  
|<span data-ttu-id="0542c-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="0542c-111">HRESULT</span></span>|<span data-ttu-id="0542c-112">Description</span><span class="sxs-lookup"><span data-stu-id="0542c-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="0542c-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="0542c-113">S_OK</span></span>|`VirtualFree` <span data-ttu-id="0542c-114">retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="0542c-114">returned successfully.</span></span>|  
|<span data-ttu-id="0542c-115">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="0542c-115">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="0542c-116">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="0542c-116">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="0542c-117">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="0542c-117">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="0542c-118">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="0542c-118">The call timed out.</span></span>|  
|<span data-ttu-id="0542c-119">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="0542c-119">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="0542c-120">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="0542c-120">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="0542c-121">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="0542c-121">HOST_E_ABANDONED</span></span>|<span data-ttu-id="0542c-122">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="0542c-122">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="0542c-123">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0542c-123">E_FAIL</span></span>|<span data-ttu-id="0542c-124">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0542c-124">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="0542c-125">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="0542c-125">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="0542c-126">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="0542c-126">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="0542c-127">HOST_E_INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="0542c-127">HOST_E_INVALIDOPERATION</span></span>|<span data-ttu-id="0542c-128">Une tentative a été effectuée pour libérer la mémoire qui n’était pas alloué via l’hôte.</span><span class="sxs-lookup"><span data-stu-id="0542c-128">An attempt was made to free memory that was not allocated through the host.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0542c-129">Notes</span><span class="sxs-lookup"><span data-stu-id="0542c-129">Remarks</span></span>  
 `VirtualFree` <span data-ttu-id="0542c-130">Libère des pages de mémoire virtuelle associées à la `lpAddress` paramètre via un appel antérieur à la [IHostMemoryManager::VirtualAlloc](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-virtualalloc-method.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="0542c-130">frees virtual memory pages associated with the `lpAddress` parameter through an earlier call to the [IHostMemoryManager::VirtualAlloc](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-virtualalloc-method.md) function.</span></span> <span data-ttu-id="0542c-131">Tente de libérer de la mémoire qui n’était pas alloué via l’hôte doit retourner HOST_E_INVALIDOPERATION.</span><span class="sxs-lookup"><span data-stu-id="0542c-131">Attempts to free memory that was not allocated through the host should return HOST_E_INVALIDOPERATION.</span></span>  
  
 <span data-ttu-id="0542c-132">La sémantique est identique à ceux de l’implémentation Win32 de `VirtualFree`.</span><span class="sxs-lookup"><span data-stu-id="0542c-132">The semantics are identical to those of the Win32 implementation of `VirtualFree`.</span></span> <span data-ttu-id="0542c-133">Pour plus d’informations, consultez la documentation de la plateforme de Windows.</span><span class="sxs-lookup"><span data-stu-id="0542c-133">For more information, see the Windows Platform documentation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0542c-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0542c-134">Requirements</span></span>  
 <span data-ttu-id="0542c-135">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0542c-135">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0542c-136">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="0542c-136">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="0542c-137">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0542c-137">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="0542c-138">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="0542c-138">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="0542c-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0542c-139">See also</span></span>

- [<span data-ttu-id="0542c-140">IHostMemoryManager, interface</span><span class="sxs-lookup"><span data-stu-id="0542c-140">IHostMemoryManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md)
- [<span data-ttu-id="0542c-141">IHostMalloc, interface</span><span class="sxs-lookup"><span data-stu-id="0542c-141">IHostMalloc Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmalloc-interface.md)
