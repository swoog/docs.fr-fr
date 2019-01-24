---
title: ICLRDataEnumMemoryRegions::EnumMemoryRegions, méthode
ms.date: 03/30/2017
api_name:
- ICLRDataEnumMemoryRegions.EnumMemoryRegions
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataEnumMemoryRegions::EnumMemoryRegions
helpviewer_keywords:
- ICLRDataEnumMemoryRegions::EnumMemoryRegions method [.NET Framework debugging]
- EnumMemoryRegions method [.NET Framework debugging]
ms.assetid: 22d2e339-f174-40b5-a478-0b744501566f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bd29f6a0b0dfc0b7ab5b57bb61a3540d5caf66d0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54639643"
---
# <a name="iclrdataenummemoryregionsenummemoryregions-method"></a><span data-ttu-id="2a3d9-102">ICLRDataEnumMemoryRegions::EnumMemoryRegions, méthode</span><span class="sxs-lookup"><span data-stu-id="2a3d9-102">ICLRDataEnumMemoryRegions::EnumMemoryRegions Method</span></span>
<span data-ttu-id="2a3d9-103">Énumère les zones de mémoire spécifiées.</span><span class="sxs-lookup"><span data-stu-id="2a3d9-103">Enumerates specified areas of memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2a3d9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a3d9-104">Syntax</span></span>  
  
```  
HRESULT EnumMemoryRegions (  
    [in] ICLRDataEnumMemoryRegionsCallback  *callback,  
    [in] ULONG32                            miniDumpFlags,  
    [in] CLRDataEnumMemoryFlags             clrFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2a3d9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2a3d9-105">Parameters</span></span>  
 `callback`  
 <span data-ttu-id="2a3d9-106">[in] Un pointeur vers un [ICLRDataEnumMemoryRegionsCallback](../../../../docs/framework/unmanaged-api/debugging/iclrdataenummemoryregionscallback-interface.md) instance qui est appelée par cette méthode pour chaque région de mémoire énumérée, afin d’informer le débogueur du résultat.</span><span class="sxs-lookup"><span data-stu-id="2a3d9-106">[in] A pointer to an [ICLRDataEnumMemoryRegionsCallback](../../../../docs/framework/unmanaged-api/debugging/iclrdataenummemoryregionscallback-interface.md) instance that is called by this method for each memory region being enumerated to notify the debugger of the result.</span></span>  
  
 <span data-ttu-id="2a3d9-107">L’énumération des régions de la mémoire continue même si le rappel indique un échec.</span><span class="sxs-lookup"><span data-stu-id="2a3d9-107">The enumeration of memory regions continues even if the callback indicates a failure.</span></span>  
  
 `miniDumpFlags`  
 <span data-ttu-id="2a3d9-108">[in] Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="2a3d9-108">[in] Not used.</span></span>  
  
 `clrFlags`  
 <span data-ttu-id="2a3d9-109">[in] Une valeur de la [CLRDataEnumMemoryFlags](../../../../docs/framework/unmanaged-api/debugging/clrdataenummemoryflags-enumeration.md) énumération qui spécifie les régions de mémoire à énumérer.</span><span class="sxs-lookup"><span data-stu-id="2a3d9-109">[in] A value of the [CLRDataEnumMemoryFlags](../../../../docs/framework/unmanaged-api/debugging/clrdataenummemoryflags-enumeration.md) enumeration that specifies the regions of memory to be enumerated.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2a3d9-110">Notes</span><span class="sxs-lookup"><span data-stu-id="2a3d9-110">Remarks</span></span>  
 <span data-ttu-id="2a3d9-111">Cette méthode utilise spécifié [ICLRDataEnumMemoryRegionsCallback](../../../../docs/framework/unmanaged-api/debugging/iclrdataenummemoryregionscallback-interface.md) instance pour informer l’appelant des résultats.</span><span class="sxs-lookup"><span data-stu-id="2a3d9-111">This method uses the specified [ICLRDataEnumMemoryRegionsCallback](../../../../docs/framework/unmanaged-api/debugging/iclrdataenummemoryregionscallback-interface.md) instance to notify the caller of results.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2a3d9-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2a3d9-112">Requirements</span></span>  
 <span data-ttu-id="2a3d9-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2a3d9-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2a3d9-114">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="2a3d9-114">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="2a3d9-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2a3d9-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2a3d9-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2a3d9-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2a3d9-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a3d9-117">See also</span></span>
- [<span data-ttu-id="2a3d9-118">ICLRDataEnumMemoryRegions, interface</span><span class="sxs-lookup"><span data-stu-id="2a3d9-118">ICLRDataEnumMemoryRegions Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdataenummemoryregions-interface.md)
