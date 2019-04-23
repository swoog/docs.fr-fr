---
title: IHostMalloc, interface
ms.date: 03/30/2017
api_name:
- IHostMAlloc
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMAlloc
helpviewer_keywords:
- IHostMAlloc interface [.NET Framework hosting]
ms.assetid: e3c6643b-6fc7-4a99-959d-4b7b4e63fdee
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f2a7a29ef1dc85c2ad554995286e5137fcb104be
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59136407"
---
# <a name="ihostmalloc-interface"></a><span data-ttu-id="1b1e9-102">IHostMalloc, interface</span><span class="sxs-lookup"><span data-stu-id="1b1e9-102">IHostMalloc Interface</span></span>
<span data-ttu-id="1b1e9-103">Fournit des méthodes qui permettent le common language runtime (CLR) pour demander des allocations fines à partir du tas via l’hôte.</span><span class="sxs-lookup"><span data-stu-id="1b1e9-103">Provides methods that allow the common language runtime (CLR) to request fine-grained allocations from the heap through the host.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="1b1e9-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1b1e9-104">Methods</span></span>  
  
|<span data-ttu-id="1b1e9-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="1b1e9-105">Method</span></span>|<span data-ttu-id="1b1e9-106">Description</span><span class="sxs-lookup"><span data-stu-id="1b1e9-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="1b1e9-107">Alloc, méthode</span><span class="sxs-lookup"><span data-stu-id="1b1e9-107">Alloc Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmalloc-alloc-method.md)|<span data-ttu-id="1b1e9-108">Demande que l’hôte alloue la quantité de mémoire demandée à partir du tas.</span><span class="sxs-lookup"><span data-stu-id="1b1e9-108">Requests that the host allocate the requested amount of memory from the heap.</span></span>|  
|[<span data-ttu-id="1b1e9-109">DebugAlloc, méthode</span><span class="sxs-lookup"><span data-stu-id="1b1e9-109">DebugAlloc Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmalloc-debugalloc-method.md)|<span data-ttu-id="1b1e9-110">Demande que l’hôte alloue la quantité de mémoire demandée à partir du tas et en outre suivre où la mémoire a été allouée.</span><span class="sxs-lookup"><span data-stu-id="1b1e9-110">Requests that the host allocate the requested amount of memory from the heap, and additionally track where the memory was allocated.</span></span>|  
|[<span data-ttu-id="1b1e9-111">Free, méthode</span><span class="sxs-lookup"><span data-stu-id="1b1e9-111">Free Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmalloc-free-method.md)|<span data-ttu-id="1b1e9-112">Libère la mémoire qui a été alloué à l’aide de la `Alloc` (méthode).</span><span class="sxs-lookup"><span data-stu-id="1b1e9-112">Frees memory that was allocated by using the `Alloc` method.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1b1e9-113">Notes</span><span class="sxs-lookup"><span data-stu-id="1b1e9-113">Remarks</span></span>  
 <span data-ttu-id="1b1e9-114">Le CLR obtient un pointeur d’interface vers un `IHostMalloc` instance en appelant le [IHostMemoryManager::CreateMalloc](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-createmalloc-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="1b1e9-114">The CLR gets an interface pointer to an `IHostMalloc` instance by calling the [IHostMemoryManager::CreateMalloc](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-createmalloc-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1b1e9-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b1e9-115">Requirements</span></span>  
 <span data-ttu-id="1b1e9-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1b1e9-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1b1e9-117">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="1b1e9-117">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="1b1e9-118">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1b1e9-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1b1e9-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1b1e9-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1b1e9-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b1e9-120">See also</span></span>

- [<span data-ttu-id="1b1e9-121">IHostMemoryManager, interface</span><span class="sxs-lookup"><span data-stu-id="1b1e9-121">IHostMemoryManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md)
- [<span data-ttu-id="1b1e9-122">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="1b1e9-122">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
