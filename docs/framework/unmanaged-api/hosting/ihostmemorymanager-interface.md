---
title: IHostMemoryManager, interface
ms.date: 03/30/2017
api_name:
- IHostMemoryManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMemoryManager
helpviewer_keywords:
- IHostMemoryManager interface [.NET Framework hosting]
ms.assetid: a945d439-3b34-4aa4-b575-8413dd7806ce
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 57f34ed1796f6fa411d31fca83baeff693f85d70
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59137351"
---
# <a name="ihostmemorymanager-interface"></a><span data-ttu-id="d8bfb-102">IHostMemoryManager, interface</span><span class="sxs-lookup"><span data-stu-id="d8bfb-102">IHostMemoryManager Interface</span></span>
<span data-ttu-id="d8bfb-103">Fournit des méthodes qui permettent le common language runtime (CLR) pour effectuer des demandes de mémoire virtuelle via l’hôte, au lieu d’utiliser les fonctions de mémoire virtuelle Win32 standards.</span><span class="sxs-lookup"><span data-stu-id="d8bfb-103">Provides methods that allow the common language runtime (CLR) to make virtual memory requests through the host, instead of using the standard Win32 virtual memory functions.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d8bfb-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d8bfb-104">Methods</span></span>  
  
|<span data-ttu-id="d8bfb-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="d8bfb-105">Method</span></span>|<span data-ttu-id="d8bfb-106">Description</span><span class="sxs-lookup"><span data-stu-id="d8bfb-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d8bfb-107">AcquiredVirtualAddressSpace, méthode</span><span class="sxs-lookup"><span data-stu-id="d8bfb-107">AcquiredVirtualAddressSpace Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-acquiredvirtualaddressspace-method.md)|<span data-ttu-id="d8bfb-108">Avertit l’hôte que le common language runtime (CLR) a acquis la mémoire spécifiée à partir du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d8bfb-108">Notifies the host that the common language runtime (CLR) has acquired the specified memory from the operating system.</span></span>|  
|[<span data-ttu-id="d8bfb-109">CreateMAlloc, méthode</span><span class="sxs-lookup"><span data-stu-id="d8bfb-109">CreateMAlloc Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-createmalloc-method.md)|<span data-ttu-id="d8bfb-110">Obtient un pointeur d’interface vers un [IHostMAlloc](../../../../docs/framework/unmanaged-api/hosting/ihostmalloc-interface.md) instance qui est utilisé pour demander des allocations de mémoire à partir d’un tas créé par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="d8bfb-110">Gets an interface pointer to an [IHostMAlloc](../../../../docs/framework/unmanaged-api/hosting/ihostmalloc-interface.md) instance that is used to request memory allocations from a heap created by the host.</span></span>|  
|[<span data-ttu-id="d8bfb-111">GetMemoryLoad, méthode</span><span class="sxs-lookup"><span data-stu-id="d8bfb-111">GetMemoryLoad Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-getmemoryload-method.md)|<span data-ttu-id="d8bfb-112">Obtient la quantité de mémoire physique qui est actuellement utilisé, comme indiqué par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="d8bfb-112">Gets the amount of physical memory that is currently being used, as reported by the host.</span></span>|  
|[<span data-ttu-id="d8bfb-113">NeedsVirtualAddressSpace, méthode</span><span class="sxs-lookup"><span data-stu-id="d8bfb-113">NeedsVirtualAddressSpace Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-needsvirtualaddressspace-method.md)|<span data-ttu-id="d8bfb-114">Avertit l’hôte que le CLR va essayer d’utiliser la mémoire spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d8bfb-114">Notifies the host that the CLR is going to attempt to use the specified memory.</span></span>|  
|[<span data-ttu-id="d8bfb-115">RegisterMemoryNotificationCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="d8bfb-115">RegisterMemoryNotificationCallback Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-registermemorynotificationcallback-method.md)|<span data-ttu-id="d8bfb-116">Enregistre un pointeur vers une fonction de rappel que l’hôte appelle pour informer le CLR de la charge actuelle de la mémoire sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d8bfb-116">Registers a pointer to a callback function that the host invokes to notify the CLR of the current memory load on the computer.</span></span>|  
|[<span data-ttu-id="d8bfb-117">ReleasedVirtualAddressSpace, méthode</span><span class="sxs-lookup"><span data-stu-id="d8bfb-117">ReleasedVirtualAddressSpace Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-releasedvirtualaddressspace-method.md)|<span data-ttu-id="d8bfb-118">Avertit l’hôte que le CLR a fini d’utiliser la mémoire spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d8bfb-118">Notifies the host that the CLR has finished using the specified memory.</span></span>|  
|[<span data-ttu-id="d8bfb-119">VirtualAlloc, méthode</span><span class="sxs-lookup"><span data-stu-id="d8bfb-119">VirtualAlloc Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-virtualalloc-method.md)|<span data-ttu-id="d8bfb-120">Sert de wrapper logique pour la fonction Win32 correspondante, qui se réserve ou valide une région de pages dans l’espace d’adressage virtuel du processus appelant.</span><span class="sxs-lookup"><span data-stu-id="d8bfb-120">Serves as a logical wrapper for the corresponding Win32 function, which reserves or commits a region of pages in the virtual address space of the calling process.</span></span>|  
|[<span data-ttu-id="d8bfb-121">VirtualFree, méthode</span><span class="sxs-lookup"><span data-stu-id="d8bfb-121">VirtualFree Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-virtualfree-method.md)|<span data-ttu-id="d8bfb-122">Sert de wrapper logique pour la fonction Win32 correspondante, qui libère, annule la validation, ou bien libère et annule la validation d’une région de pages au sein de l’espace d’adressage virtuel du processus appelant.</span><span class="sxs-lookup"><span data-stu-id="d8bfb-122">Serves as a logical wrapper for the corresponding Win32 function, which releases, decommits, or releases and decommits a region of pages within the virtual address space of the calling process.</span></span>|  
|[<span data-ttu-id="d8bfb-123">VirtualProtect, méthode</span><span class="sxs-lookup"><span data-stu-id="d8bfb-123">VirtualProtect Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-virtualprotect-method.md)|<span data-ttu-id="d8bfb-124">Sert de wrapper logique pour la fonction Win32 correspondante, qui modifie la protection sur une région de pages validées dans l’espace d’adressage virtuel du processus appelant.</span><span class="sxs-lookup"><span data-stu-id="d8bfb-124">Serves as a logical wrapper for the corresponding Win32 function, which changes the protection on a region of committed pages in the virtual address space of the calling process.</span></span>|  
|[<span data-ttu-id="d8bfb-125">VirtualQuery, méthode</span><span class="sxs-lookup"><span data-stu-id="d8bfb-125">VirtualQuery Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-virtualquery-method.md)|<span data-ttu-id="d8bfb-126">Sert de wrapper logique pour la fonction Win32 correspondante, qui Récupère des informations sur une plage de pages dans l’espace d’adressage virtuel du processus appelant.</span><span class="sxs-lookup"><span data-stu-id="d8bfb-126">Serves as a logical wrapper for the corresponding Win32 function, which retrieves information about a range of pages in the virtual address space of the calling process.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d8bfb-127">Notes</span><span class="sxs-lookup"><span data-stu-id="d8bfb-127">Remarks</span></span>  
 `IHostMemoryManager` <span data-ttu-id="d8bfb-128">fournit également des méthodes pour le CLR obtenir un pointeur par le biais duquel pour effectuer des demandes de mémoire sur le tas et obtenir le niveau de pression de mémoire dans le processus, comme indiqué par l’hôte.</span><span class="sxs-lookup"><span data-stu-id="d8bfb-128">also provides methods for the CLR to obtain a pointer through which to make memory requests on the heap and to get the level of memory pressure in the process, as reported by the host.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d8bfb-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8bfb-129">Requirements</span></span>  
 <span data-ttu-id="d8bfb-130">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d8bfb-130">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d8bfb-131">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="d8bfb-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="d8bfb-132">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d8bfb-132">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="d8bfb-133">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="d8bfb-133">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="d8bfb-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8bfb-134">See also</span></span>

- [<span data-ttu-id="d8bfb-135">IHostMalloc, interface</span><span class="sxs-lookup"><span data-stu-id="d8bfb-135">IHostMalloc Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmalloc-interface.md)
- [<span data-ttu-id="d8bfb-136">Interfaces d'hébergement</span><span class="sxs-lookup"><span data-stu-id="d8bfb-136">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
