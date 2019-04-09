---
title: IHostMemoryManager::VirtualQuery, méthode
ms.date: 03/30/2017
api_name:
- IHostMemoryManager.VirtualQuery
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMemoryManager::VirtualQuery
helpviewer_keywords:
- IHostMemoryManager::VirtualQuery method [.NET Framework hosting]
- VirtualQuery method [.NET Framework hosting]
ms.assetid: 757af1e6-b9e8-49e7-b5db-342be3aa205f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 028ca0b9cb917d3e6cc0242cbc8c3f4a5a19ab39
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59199620"
---
# <a name="ihostmemorymanagervirtualquery-method"></a><span data-ttu-id="51211-102">IHostMemoryManager::VirtualQuery, méthode</span><span class="sxs-lookup"><span data-stu-id="51211-102">IHostMemoryManager::VirtualQuery Method</span></span>
<span data-ttu-id="51211-103">Sert de wrapper logique pour la fonction Win32 correspondante.</span><span class="sxs-lookup"><span data-stu-id="51211-103">Serves as a logical wrapper for the corresponding Win32 function.</span></span> <span data-ttu-id="51211-104">L’implémentation Win32 de `VirtualQuery` récupère des informations sur une plage de pages dans l’espace d’adressage virtuel du processus appelant.</span><span class="sxs-lookup"><span data-stu-id="51211-104">The Win32 implementation of `VirtualQuery` retrieves information about a range of pages in the virtual address space of the calling process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="51211-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51211-105">Syntax</span></span>  
  
```  
HRESULT VirtualQuery (  
    [in]  void*    lpAddress,  
    [out] void*    lpBuffer,  
    [in]  SIZE_T   dwLength,  
    [out] SIZE_T*  pResult  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="51211-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51211-106">Parameters</span></span>  
 `lpAddress`  
 <span data-ttu-id="51211-107">[in] Pointeur vers l’adresse dans la mémoire virtuelle à interroger.</span><span class="sxs-lookup"><span data-stu-id="51211-107">[in] A pointer to the address in virtual memory to be queried.</span></span>  
  
 `lpBuffer`  
 <span data-ttu-id="51211-108">[out] Un pointeur vers une structure qui contient des informations sur la région de mémoire spécifié.</span><span class="sxs-lookup"><span data-stu-id="51211-108">[out] A pointer to a structure that contains information about the specified memory region.</span></span>  
  
 `dwLength`  
 <span data-ttu-id="51211-109">[in] La taille, en octets, de la mémoire tampon qui `lpBuffer` pointe vers.</span><span class="sxs-lookup"><span data-stu-id="51211-109">[in] The size, in bytes, of the buffer that `lpBuffer` points to.</span></span>  
  
 `pResult`  
 <span data-ttu-id="51211-110">[out] Pointeur vers le nombre d’octets retournés par la mémoire tampon d’informations.</span><span class="sxs-lookup"><span data-stu-id="51211-110">[out] A pointer to the number of bytes returned by the information buffer.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="51211-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="51211-111">Return Value</span></span>  
  
|<span data-ttu-id="51211-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="51211-112">HRESULT</span></span>|<span data-ttu-id="51211-113">Description</span><span class="sxs-lookup"><span data-stu-id="51211-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="51211-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="51211-114">S_OK</span></span>|`VirtualQuery` <span data-ttu-id="51211-115">retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="51211-115">returned successfully.</span></span>|  
|<span data-ttu-id="51211-116">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="51211-116">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="51211-117">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="51211-117">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="51211-118">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="51211-118">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="51211-119">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="51211-119">The call timed out.</span></span>|  
|<span data-ttu-id="51211-120">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="51211-120">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="51211-121">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="51211-121">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="51211-122">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="51211-122">HOST_E_ABANDONED</span></span>|<span data-ttu-id="51211-123">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="51211-123">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="51211-124">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="51211-124">E_FAIL</span></span>|<span data-ttu-id="51211-125">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="51211-125">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="51211-126">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="51211-126">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="51211-127">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="51211-127">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="51211-128">Notes</span><span class="sxs-lookup"><span data-stu-id="51211-128">Remarks</span></span>  
 `VirtualQuery` <span data-ttu-id="51211-129">Fournit des informations sur une plage de pages dans l’espace d’adressage virtuel du processus appelant.</span><span class="sxs-lookup"><span data-stu-id="51211-129">provides information about a range of pages in the virtual address space of the calling process.</span></span> <span data-ttu-id="51211-130">Cette implémentation définit la valeur de la `pResult` paramètre pour le nombre d’octets retournés dans la mémoire tampon d’informations et retourne une valeur HRESULT.</span><span class="sxs-lookup"><span data-stu-id="51211-130">This implementation sets the value of the `pResult` parameter to the number of bytes returned in the information buffer, and returns an HRESULT value.</span></span> <span data-ttu-id="51211-131">Dans Win32 `VirtualQuery` (fonction), la valeur de retour est la taille du tampon.</span><span class="sxs-lookup"><span data-stu-id="51211-131">In the Win32 `VirtualQuery` function, the return value is the buffer size.</span></span> <span data-ttu-id="51211-132">Pour plus d’informations, consultez la documentation de la plateforme de Windows.</span><span class="sxs-lookup"><span data-stu-id="51211-132">For more information, see the Windows Platform documentation.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="51211-133">Implémentation du système d’exploitation de `VirtualQuery` n’entraîne pas d’interblocage et peut s’exécuter intégralement avec des threads aléatoires interrompus dans le code utilisateur.</span><span class="sxs-lookup"><span data-stu-id="51211-133">The operating system's implementation of `VirtualQuery` does not incur deadlock and can run to completion with random threads suspended in user code.</span></span> <span data-ttu-id="51211-134">Procédez avec précaution lors de l’implémentation d’une version hébergée de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="51211-134">Use great caution when implementing a hosted version of this method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="51211-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51211-135">Requirements</span></span>  
 <span data-ttu-id="51211-136">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="51211-136">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="51211-137">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="51211-137">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="51211-138">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="51211-138">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="51211-139">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="51211-139">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="51211-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51211-140">See also</span></span>

- [<span data-ttu-id="51211-141">IHostMemoryManager, interface</span><span class="sxs-lookup"><span data-stu-id="51211-141">IHostMemoryManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md)
