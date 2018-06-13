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
ms.openlocfilehash: 8f6a3d425d4c2ae2146723a6acfc5ab9893f0fe0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33438439"
---
# <a name="ihostmemorymanagerreleasedvirtualaddressspace-method"></a><span data-ttu-id="ca284-102">IHostMemoryManager::ReleasedVirtualAddressSpace, méthode</span><span class="sxs-lookup"><span data-stu-id="ca284-102">IHostMemoryManager::ReleasedVirtualAddressSpace Method</span></span>
<span data-ttu-id="ca284-103">Avertit l’hôte que le common language runtime (CLR) a terminé d’utiliser la mémoire spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ca284-103">Notifies the host that the common language runtime (CLR) has finished using the specified memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ca284-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca284-104">Syntax</span></span>  
  
```  
HRESULT ReleasedVirtualAddressSpace(  
    [in] LPVOID startAddress  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ca284-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca284-105">Parameters</span></span>  
 `startAddress`  
 <span data-ttu-id="ca284-106">[in] Pointeur vers l’adresse de départ de la mémoire à libérer.</span><span class="sxs-lookup"><span data-stu-id="ca284-106">[in] Pointer to the starting address of the memory to be released.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ca284-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ca284-107">Remarks</span></span>  
 <span data-ttu-id="ca284-108">Le `ReleasedVirtualAddressSpace` méthode est une méthode de rappel et doit être implémentée par le writer de l’application d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="ca284-108">The `ReleasedVirtualAddressSpace` method is a callback method and must be implemented by the writer of the hosting application.</span></span> <span data-ttu-id="ca284-109">Elle est appelée par le CLR.</span><span class="sxs-lookup"><span data-stu-id="ca284-109">It is called by the CLR.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ca284-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ca284-110">Requirements</span></span>  
 <span data-ttu-id="ca284-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ca284-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ca284-112">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="ca284-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ca284-113">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ca284-113">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ca284-114">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ca284-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ca284-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca284-115">See Also</span></span>  
 [<span data-ttu-id="ca284-116">IHostMemoryManager, interface</span><span class="sxs-lookup"><span data-stu-id="ca284-116">IHostMemoryManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md)
