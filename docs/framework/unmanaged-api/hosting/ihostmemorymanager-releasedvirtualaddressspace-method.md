---
title: IHostMemoryManager::ReleasedVirtualAddressSpace, méthode
ms.date: 03/30/2017
api_name:
- IHostMemoryManager.ReleasedVirtualAddressSpace
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMemoryManager::ReleasedVirtualAddressSpace
helpviewer_keywords:
- ReleasedVirtualAddressSpace method [.NET Framework hosting]
- IHostMemoryManager::ReleasedVirtualAddressSpace method [.NET Framework hosting]
ms.assetid: d1876601-6ab9-48e1-8ebd-184af1d0cd76
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0acbf4163e98b1171510260c4fac72c3d6f6fb1d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59189285"
---
# <a name="ihostmemorymanagerreleasedvirtualaddressspace-method"></a><span data-ttu-id="066ce-102">IHostMemoryManager::ReleasedVirtualAddressSpace, méthode</span><span class="sxs-lookup"><span data-stu-id="066ce-102">IHostMemoryManager::ReleasedVirtualAddressSpace Method</span></span>
<span data-ttu-id="066ce-103">Avertit l’hôte que le common language runtime (CLR) a fini d’utiliser la mémoire spécifiée.</span><span class="sxs-lookup"><span data-stu-id="066ce-103">Notifies the host that the common language runtime (CLR) has finished using the specified memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="066ce-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="066ce-104">Syntax</span></span>  
  
```  
HRESULT ReleasedVirtualAddressSpace(  
    [in] LPVOID startAddress  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="066ce-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="066ce-105">Parameters</span></span>  
 `startAddress`  
 <span data-ttu-id="066ce-106">[in] Pointeur vers l’adresse de départ de la mémoire à libérer.</span><span class="sxs-lookup"><span data-stu-id="066ce-106">[in] Pointer to the starting address of the memory to be released.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="066ce-107">Notes</span><span class="sxs-lookup"><span data-stu-id="066ce-107">Remarks</span></span>  
 <span data-ttu-id="066ce-108">Le `ReleasedVirtualAddressSpace` méthode est une méthode de rappel et doit être implémentée par le writer de l’application d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="066ce-108">The `ReleasedVirtualAddressSpace` method is a callback method and must be implemented by the writer of the hosting application.</span></span> <span data-ttu-id="066ce-109">Elle est appelée par le CLR.</span><span class="sxs-lookup"><span data-stu-id="066ce-109">It is called by the CLR.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="066ce-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="066ce-110">Requirements</span></span>  
 <span data-ttu-id="066ce-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="066ce-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="066ce-112">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="066ce-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="066ce-113">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="066ce-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="066ce-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="066ce-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="066ce-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="066ce-115">See also</span></span>

- [<span data-ttu-id="066ce-116">IHostMemoryManager, interface</span><span class="sxs-lookup"><span data-stu-id="066ce-116">IHostMemoryManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md)
