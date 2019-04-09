---
title: IHostMemoryManager::AcquiredVirtualAddressSpace, méthode
ms.date: 03/30/2017
api_name:
- IHostMemoryManager.AcquiredVirtualAddressSpace
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMemoryManager::AcquiredVirtualAddressSpace
helpviewer_keywords:
- IHostMemoryManager::AcquiredVirtualAddressSpace method [.NET Framework hosting]
- AcquiredVirtualAddressSpace method [.NET Framework hosting]
ms.assetid: ef2f83c2-127e-4c38-8385-306c03cd2167
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4675c34bfe8d1d79c184c43e5f7f5dd3a03be6a3
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59200998"
---
# <a name="ihostmemorymanageracquiredvirtualaddressspace-method"></a><span data-ttu-id="8fb62-102">IHostMemoryManager::AcquiredVirtualAddressSpace, méthode</span><span class="sxs-lookup"><span data-stu-id="8fb62-102">IHostMemoryManager::AcquiredVirtualAddressSpace Method</span></span>
<span data-ttu-id="8fb62-103">Avertit l’hôte que le common language runtime (CLR) a acquis la mémoire spécifiée à partir du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8fb62-103">Notifies the host that the common language runtime (CLR) has acquired the specified memory from the operating system.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8fb62-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8fb62-104">Syntax</span></span>  
  
```  
HRESULT AcquiredVirtualAddressSpace(  
    [in] LPVOID  startAddress,  
    [in] SIZE_T  size  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8fb62-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8fb62-105">Parameters</span></span>  
 `startAddress`  
 <span data-ttu-id="8fb62-106">[in] Adresse de départ de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="8fb62-106">[in] The starting address of the memory.</span></span>  
  
 `size`  
 <span data-ttu-id="8fb62-107">[in] La taille, en octets, de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="8fb62-107">[in] The size, in bytes, of the memory.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8fb62-108">Notes</span><span class="sxs-lookup"><span data-stu-id="8fb62-108">Remarks</span></span>  
 <span data-ttu-id="8fb62-109">Le `AcquiredVirtualAddressSpace` méthode est une méthode de rappel et doit être implémentée par le writer de l’application d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="8fb62-109">The `AcquiredVirtualAddressSpace` method is a callback method and must be implemented by the writer of the hosting application.</span></span> <span data-ttu-id="8fb62-110">Elle est appelée par le CLR.</span><span class="sxs-lookup"><span data-stu-id="8fb62-110">It is called by the CLR.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8fb62-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fb62-111">Requirements</span></span>  
 <span data-ttu-id="8fb62-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8fb62-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8fb62-113">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="8fb62-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="8fb62-114">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8fb62-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="8fb62-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="8fb62-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="8fb62-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fb62-116">See also</span></span>

- [<span data-ttu-id="8fb62-117">IHostMemoryManager, interface</span><span class="sxs-lookup"><span data-stu-id="8fb62-117">IHostMemoryManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md)
