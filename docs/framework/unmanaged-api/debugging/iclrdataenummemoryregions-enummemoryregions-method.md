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
ms.openlocfilehash: 16d91156427c2ef7bdabd5ab11b01894fbced64c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33406613"
---
# <a name="iclrdataenummemoryregionsenummemoryregions-method"></a><span data-ttu-id="b1dfe-102">ICLRDataEnumMemoryRegions::EnumMemoryRegions, méthode</span><span class="sxs-lookup"><span data-stu-id="b1dfe-102">ICLRDataEnumMemoryRegions::EnumMemoryRegions Method</span></span>
<span data-ttu-id="b1dfe-103">Énumère les zones de mémoire spécifiées.</span><span class="sxs-lookup"><span data-stu-id="b1dfe-103">Enumerates specified areas of memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b1dfe-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1dfe-104">Syntax</span></span>  
  
```  
HRESULT EnumMemoryRegions (  
    [in] ICLRDataEnumMemoryRegionsCallback  *callback,  
    [in] ULONG32                            miniDumpFlags,  
    [in] CLRDataEnumMemoryFlags             clrFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b1dfe-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1dfe-105">Parameters</span></span>  
 `callback`  
 <span data-ttu-id="b1dfe-106">[in] Un pointeur vers un [ICLRDataEnumMemoryRegionsCallback](../../../../docs/framework/unmanaged-api/debugging/iclrdataenummemoryregionscallback-interface.md) instance qui est appelée par cette méthode pour chaque région de mémoire énumérée, afin d’informer le débogueur du résultat.</span><span class="sxs-lookup"><span data-stu-id="b1dfe-106">[in] A pointer to an [ICLRDataEnumMemoryRegionsCallback](../../../../docs/framework/unmanaged-api/debugging/iclrdataenummemoryregionscallback-interface.md) instance that is called by this method for each memory region being enumerated to notify the debugger of the result.</span></span>  
  
 <span data-ttu-id="b1dfe-107">L’énumération de régions de mémoire continue même si le rappel indique un échec.</span><span class="sxs-lookup"><span data-stu-id="b1dfe-107">The enumeration of memory regions continues even if the callback indicates a failure.</span></span>  
  
 `miniDumpFlags`  
 <span data-ttu-id="b1dfe-108">[in] Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="b1dfe-108">[in] Not used.</span></span>  
  
 `clrFlags`  
 <span data-ttu-id="b1dfe-109">[in] Une valeur de la [CLRDataEnumMemoryFlags](../../../../docs/framework/unmanaged-api/debugging/clrdataenummemoryflags-enumeration.md) énumération qui spécifie les régions de mémoire à énumérer.</span><span class="sxs-lookup"><span data-stu-id="b1dfe-109">[in] A value of the [CLRDataEnumMemoryFlags](../../../../docs/framework/unmanaged-api/debugging/clrdataenummemoryflags-enumeration.md) enumeration that specifies the regions of memory to be enumerated.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b1dfe-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b1dfe-110">Remarks</span></span>  
 <span data-ttu-id="b1dfe-111">Cette méthode utilise le [ICLRDataEnumMemoryRegionsCallback](../../../../docs/framework/unmanaged-api/debugging/iclrdataenummemoryregionscallback-interface.md) instance pour informer l’appelant des résultats.</span><span class="sxs-lookup"><span data-stu-id="b1dfe-111">This method uses the specified [ICLRDataEnumMemoryRegionsCallback](../../../../docs/framework/unmanaged-api/debugging/iclrdataenummemoryregionscallback-interface.md) instance to notify the caller of results.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b1dfe-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b1dfe-112">Requirements</span></span>  
 <span data-ttu-id="b1dfe-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b1dfe-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b1dfe-114">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="b1dfe-114">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="b1dfe-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b1dfe-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b1dfe-116">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b1dfe-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b1dfe-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1dfe-117">See Also</span></span>  
 [<span data-ttu-id="b1dfe-118">ICLRDataEnumMemoryRegions, interface</span><span class="sxs-lookup"><span data-stu-id="b1dfe-118">ICLRDataEnumMemoryRegions Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdataenummemoryregions-interface.md)
