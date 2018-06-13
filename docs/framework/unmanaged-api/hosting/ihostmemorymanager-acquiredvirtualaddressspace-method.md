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
ms.openlocfilehash: d93c50968192a7789cbf08968d7ec272c9775d6f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33438511"
---
# <a name="ihostmemorymanageracquiredvirtualaddressspace-method"></a><span data-ttu-id="5ba69-102">IHostMemoryManager::AcquiredVirtualAddressSpace, méthode</span><span class="sxs-lookup"><span data-stu-id="5ba69-102">IHostMemoryManager::AcquiredVirtualAddressSpace Method</span></span>
<span data-ttu-id="5ba69-103">Avertit l’hôte que le common language runtime (CLR) a acquis la mémoire spécifiée à partir du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="5ba69-103">Notifies the host that the common language runtime (CLR) has acquired the specified memory from the operating system.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5ba69-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ba69-104">Syntax</span></span>  
  
```  
HRESULT AcquiredVirtualAddressSpace(  
    [in] LPVOID  startAddress,  
    [in] SIZE_T  size  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="5ba69-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ba69-105">Parameters</span></span>  
 `startAddress`  
 <span data-ttu-id="5ba69-106">[in] Adresse de départ de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="5ba69-106">[in] The starting address of the memory.</span></span>  
  
 `size`  
 <span data-ttu-id="5ba69-107">[in] La taille, en octets, de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="5ba69-107">[in] The size, in bytes, of the memory.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5ba69-108">Notes</span><span class="sxs-lookup"><span data-stu-id="5ba69-108">Remarks</span></span>  
 <span data-ttu-id="5ba69-109">Le `AcquiredVirtualAddressSpace` méthode est une méthode de rappel et doit être implémentée par le writer de l’application d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="5ba69-109">The `AcquiredVirtualAddressSpace` method is a callback method and must be implemented by the writer of the hosting application.</span></span> <span data-ttu-id="5ba69-110">Elle est appelée par le CLR.</span><span class="sxs-lookup"><span data-stu-id="5ba69-110">It is called by the CLR.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5ba69-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5ba69-111">Requirements</span></span>  
 <span data-ttu-id="5ba69-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5ba69-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5ba69-113">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="5ba69-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="5ba69-114">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5ba69-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5ba69-115">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5ba69-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5ba69-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ba69-116">See Also</span></span>  
 [<span data-ttu-id="5ba69-117">IHostMemoryManager, interface</span><span class="sxs-lookup"><span data-stu-id="5ba69-117">IHostMemoryManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md)
