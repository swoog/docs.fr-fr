---
title: IHostMemoryManager::NeedsVirtualAddressSpace, méthode
ms.date: 03/30/2017
api_name:
- IHostMemoryManager.NeedsVirtualAddressSpace
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMemoryManager::NeedsVirtualAddressSpace
helpviewer_keywords:
- IHostMemoryManager::NeedsVirtualAddressSpace method [.NET Framework hosting]
- NeedsVirtualAddressSpace method [.NET Framework hosting]
ms.assetid: 71f0eab5-0170-46f8-9f88-1df5abdeb34a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 87c97a678fce4c25a113670a4668515a898e5251
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33438416"
---
# <a name="ihostmemorymanagerneedsvirtualaddressspace-method"></a><span data-ttu-id="f0abb-102">IHostMemoryManager::NeedsVirtualAddressSpace, méthode</span><span class="sxs-lookup"><span data-stu-id="f0abb-102">IHostMemoryManager::NeedsVirtualAddressSpace Method</span></span>
<span data-ttu-id="f0abb-103">Avertit l’hôte que le common language runtime (CLR) va tenter d’utiliser la mémoire spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f0abb-103">Notifies the host that the common language runtime (CLR) is going to attempt to use the specified memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f0abb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0abb-104">Syntax</span></span>  
  
```  
HRESULT NeedsVirtualAddressSpace (  
    [in] LPVOID  startAddress,  
    [in] SIZE_T  size  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f0abb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0abb-105">Parameters</span></span>  
 `startAddress`  
 <span data-ttu-id="f0abb-106">[in] Adresse de départ de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="f0abb-106">[in] The starting address of the memory.</span></span>  
  
 `size`  
 <span data-ttu-id="f0abb-107">[in] La taille, en octets, de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="f0abb-107">[in] The size, in bytes, of the memory.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f0abb-108">Notes</span><span class="sxs-lookup"><span data-stu-id="f0abb-108">Remarks</span></span>  
 <span data-ttu-id="f0abb-109">Le `NeedsVirtualAddressSpace` méthode est une méthode de rappel et doit être implémentée par le writer de l’application d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="f0abb-109">The `NeedsVirtualAddressSpace` method is a callback method and must be implemented by the writer of the hosting application.</span></span> <span data-ttu-id="f0abb-110">Elle est appelée par le CLR.</span><span class="sxs-lookup"><span data-stu-id="f0abb-110">It is called by the CLR.</span></span>  
  
 <span data-ttu-id="f0abb-111">Si l’hôte ne souhaite pas que le CLR à utiliser la mémoire spécifiée, elle peut retourner un HRESULT E_OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f0abb-111">If the host does not want the CLR to use the specified memory, it may return an E_OUTOFMEMORY HRESULT.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f0abb-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f0abb-112">Requirements</span></span>  
 <span data-ttu-id="f0abb-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f0abb-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f0abb-114">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="f0abb-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f0abb-115">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f0abb-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f0abb-116">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f0abb-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f0abb-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0abb-117">See Also</span></span>  
 [<span data-ttu-id="f0abb-118">IHostMemoryManager, interface</span><span class="sxs-lookup"><span data-stu-id="f0abb-118">IHostMemoryManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md)
