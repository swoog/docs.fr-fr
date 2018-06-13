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
ms.openlocfilehash: 063ddd0bfa1734d43f90b4680166c21b80f5cc05
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33439105"
---
# <a name="ihostmemorymanagervirtualfree-method"></a><span data-ttu-id="c48d5-102">IHostMemoryManager::VirtualFree, méthode</span><span class="sxs-lookup"><span data-stu-id="c48d5-102">IHostMemoryManager::VirtualFree Method</span></span>
<span data-ttu-id="c48d5-103">Sert de wrapper logique pour la fonction Win32 correspondante.</span><span class="sxs-lookup"><span data-stu-id="c48d5-103">Serves as a logical wrapper for the corresponding Win32 function.</span></span> <span data-ttu-id="c48d5-104">L’implémentation Win32 de `VirtualFree` libère, annule sa validation ou libère et invalider une région de pages au sein de l’espace d’adressage virtuel du processus appelant.</span><span class="sxs-lookup"><span data-stu-id="c48d5-104">The Win32 implementation of `VirtualFree` releases, decommits, or releases and decommits a region of pages within the virtual address space of the calling process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c48d5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c48d5-105">Syntax</span></span>  
  
```  
HRESULT VirtualFree (  
    [in] LPVOID  lpAddress,  
    [in] SIZE_T  dwSize,  
    [in] DWORD   dwFreeType  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c48d5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c48d5-106">Parameters</span></span>  
 `lpAddress`  
 <span data-ttu-id="c48d5-107">[in] Pointeur vers l’adresse de base des pages de mémoire virtuelle à libérer.</span><span class="sxs-lookup"><span data-stu-id="c48d5-107">[in] A pointer to the base address of the virtual memory pages to be freed.</span></span>  
  
 `dwSize`  
 <span data-ttu-id="c48d5-108">[in] La taille, en octets, de la région à libérer.</span><span class="sxs-lookup"><span data-stu-id="c48d5-108">[in] The size, in bytes, of the region to be freed.</span></span>  
  
 `dwFreeType`  
 <span data-ttu-id="c48d5-109">[in] Le type d’opération de libération.</span><span class="sxs-lookup"><span data-stu-id="c48d5-109">[in] The type of freeing operation.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c48d5-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c48d5-110">Return Value</span></span>  
  
|<span data-ttu-id="c48d5-111">HRESULT</span><span class="sxs-lookup"><span data-stu-id="c48d5-111">HRESULT</span></span>|<span data-ttu-id="c48d5-112">Description</span><span class="sxs-lookup"><span data-stu-id="c48d5-112">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="c48d5-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="c48d5-113">S_OK</span></span>|<span data-ttu-id="c48d5-114">`VirtualFree` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="c48d5-114">`VirtualFree` returned successfully.</span></span>|  
|<span data-ttu-id="c48d5-115">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="c48d5-115">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="c48d5-116">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="c48d5-116">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="c48d5-117">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="c48d5-117">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="c48d5-118">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="c48d5-118">The call timed out.</span></span>|  
|<span data-ttu-id="c48d5-119">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="c48d5-119">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="c48d5-120">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="c48d5-120">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="c48d5-121">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="c48d5-121">HOST_E_ABANDONED</span></span>|<span data-ttu-id="c48d5-122">Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="c48d5-122">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="c48d5-123">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="c48d5-123">E_FAIL</span></span>|<span data-ttu-id="c48d5-124">Une défaillance grave et inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c48d5-124">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="c48d5-125">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus.</span><span class="sxs-lookup"><span data-stu-id="c48d5-125">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="c48d5-126">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="c48d5-126">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="c48d5-127">HOST_E_INVALIDOPERATION</span><span class="sxs-lookup"><span data-stu-id="c48d5-127">HOST_E_INVALIDOPERATION</span></span>|<span data-ttu-id="c48d5-128">Une tentative a été effectuée pour libérer de la mémoire n’est allouée par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="c48d5-128">An attempt was made to free memory that was not allocated through the host.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c48d5-129">Notes</span><span class="sxs-lookup"><span data-stu-id="c48d5-129">Remarks</span></span>  
 <span data-ttu-id="c48d5-130">`VirtualFree` Libère des pages de mémoire virtuelle associés à la `lpAddress` paramètre via un appel précédent à la [IHostMemoryManager::VirtualAlloc](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-virtualalloc-method.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="c48d5-130">`VirtualFree` frees virtual memory pages associated with the `lpAddress` parameter through an earlier call to the [IHostMemoryManager::VirtualAlloc](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-virtualalloc-method.md) function.</span></span> <span data-ttu-id="c48d5-131">Tente de libérer de la mémoire n’est allouée par l’hôte doit retourner HOST_E_INVALIDOPERATION.</span><span class="sxs-lookup"><span data-stu-id="c48d5-131">Attempts to free memory that was not allocated through the host should return HOST_E_INVALIDOPERATION.</span></span>  
  
 <span data-ttu-id="c48d5-132">La sémantique est identique à celles de l’implémentation Win32 de `VirtualFree`.</span><span class="sxs-lookup"><span data-stu-id="c48d5-132">The semantics are identical to those of the Win32 implementation of `VirtualFree`.</span></span> <span data-ttu-id="c48d5-133">Pour plus d’informations, consultez la documentation de la plateforme Windows.</span><span class="sxs-lookup"><span data-stu-id="c48d5-133">For more information, see the Windows Platform documentation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c48d5-134">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c48d5-134">Requirements</span></span>  
 <span data-ttu-id="c48d5-135">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c48d5-135">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c48d5-136">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="c48d5-136">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c48d5-137">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c48d5-137">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c48d5-138">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c48d5-138">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c48d5-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c48d5-139">See Also</span></span>  
 [<span data-ttu-id="c48d5-140">IHostMemoryManager, interface</span><span class="sxs-lookup"><span data-stu-id="c48d5-140">IHostMemoryManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md)  
 [<span data-ttu-id="c48d5-141">IHostMalloc, interface</span><span class="sxs-lookup"><span data-stu-id="c48d5-141">IHostMalloc Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmalloc-interface.md)
