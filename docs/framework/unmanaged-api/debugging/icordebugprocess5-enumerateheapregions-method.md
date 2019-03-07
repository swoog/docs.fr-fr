---
title: ICorDebugProcess5::EnumerateHeapRegions, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugProcess5.EnumerateHeapRegions
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess5::EnumerateHeapRegions
helpviewer_keywords:
- EnumerateHeapRegions method, ICorDebugProcess5 interface [.NET Framework debugging]
- ICorDebugProcess5::EnumerateHeapRegions method [.NET Framework debugging]
ms.assetid: b1edba68-9c36-4f69-be9f-678ce0b33480
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5632e6a68b5fcaf77885d67c64915fca5f8cf519
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57502534"
---
# <a name="icordebugprocess5enumerateheapregions-method"></a><span data-ttu-id="654f8-102">ICorDebugProcess5::EnumerateHeapRegions, méthode</span><span class="sxs-lookup"><span data-stu-id="654f8-102">ICorDebugProcess5::EnumerateHeapRegions Method</span></span>
<span data-ttu-id="654f8-103">Obtient un énumérateur pour les plages de mémoire du tas managé.</span><span class="sxs-lookup"><span data-stu-id="654f8-103">Gets an enumerator for the memory ranges of the managed heap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="654f8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="654f8-104">Syntax</span></span>  
  
```  
HRESULT EnumerateHeapRegions(  
   [out] ICorDebugHeapSegmentEnum **ppRegions  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="654f8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="654f8-105">Parameters</span></span>  
 `ppRegions`  
 <span data-ttu-id="654f8-106">[out] Un pointeur vers l’adresse d’un [ICorDebugHeapSegmentEnum](../../../../docs/framework/unmanaged-api/debugging/icordebugheapsegmentenum-interface.md) objet d’interface qui est un énumérateur pour les plages de mémoire dans lequel les objets résident dans le tas managé.</span><span class="sxs-lookup"><span data-stu-id="654f8-106">[out] A pointer to the address of an [ICorDebugHeapSegmentEnum](../../../../docs/framework/unmanaged-api/debugging/icordebugheapsegmentenum-interface.md) interface object that is an enumerator for the ranges of memory in which objects reside in the managed heap.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="654f8-107">Notes</span><span class="sxs-lookup"><span data-stu-id="654f8-107">Remarks</span></span>  
 <span data-ttu-id="654f8-108">Avant d’appeler le `ICorDebugProcess5::EnumerateHeapRegions` (méthode), vous devez appeler la [ICorDebugProcess5::GetGCHeapInformation](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-getgcheapinformation-method.md) (méthode) et examinez la valeur de la `areGCStructuresValid` champ retourné [COR_HEAPINFO](../../../../docs/framework/unmanaged-api/debugging/cor-heapinfo-structure.md) objet pour vous assurer que le tas de garbage collection dans son état actuel est énumérable.</span><span class="sxs-lookup"><span data-stu-id="654f8-108">Before calling the `ICorDebugProcess5::EnumerateHeapRegions` method, you should call the [ICorDebugProcess5::GetGCHeapInformation](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-getgcheapinformation-method.md) method and examine the value of the `areGCStructuresValid` field of the returned [COR_HEAPINFO](../../../../docs/framework/unmanaged-api/debugging/cor-heapinfo-structure.md) object to ensure that the garbage collection heap in its current state is enumerable.</span></span> <span data-ttu-id="654f8-109">En outre, le `ICorDebugProcess5::EnumerateHeapRegions` retourne de la méthode `E_FAIL` si vous attachez trop tôt dans la durée de vie du processus, régions sont créées avant la mémoire.</span><span class="sxs-lookup"><span data-stu-id="654f8-109">In addition, the `ICorDebugProcess5::EnumerateHeapRegions` method returns `E_FAIL` if you attach too early in the lifetime of the process, before memory regions are created.</span></span>  
  
 <span data-ttu-id="654f8-110">Cette méthode est garantie pour énumérer toutes les régions de mémoire qui peuvent contenir des objets gérés, mais cela ne garantit pas que les objets gérés qui résident dans ces régions.</span><span class="sxs-lookup"><span data-stu-id="654f8-110">This method is guaranteed to enumerate all memory regions that may contain managed objects, but it does not guarantee that managed objects actually reside in those regions.</span></span> <span data-ttu-id="654f8-111">Le [ICorDebugHeapSegmentEnum](../../../../docs/framework/unmanaged-api/debugging/icordebugheapsegmentenum-interface.md) objet de collection peut inclure des régions de mémoire vide ou réservée.</span><span class="sxs-lookup"><span data-stu-id="654f8-111">The [ICorDebugHeapSegmentEnum](../../../../docs/framework/unmanaged-api/debugging/icordebugheapsegmentenum-interface.md) collection object may include empty or reserved memory regions.</span></span>  
  
 <span data-ttu-id="654f8-112">Le [ICorDebugHeapSegmentEnum](../../../../docs/framework/unmanaged-api/debugging/icordebugheapsegmentenum-interface.md) objet d’interface est un énumérateur standard dérivé de l’interface ICorDebugEnum qui vous permet d’énumérer les [COR_SEGMENT](../../../../docs/framework/unmanaged-api/debugging/cor-segment-structure.md) objets.</span><span class="sxs-lookup"><span data-stu-id="654f8-112">The [ICorDebugHeapSegmentEnum](../../../../docs/framework/unmanaged-api/debugging/icordebugheapsegmentenum-interface.md) interface object is a standard enumerator derived from the ICorDebugEnum interface that allows you to enumerate [COR_SEGMENT](../../../../docs/framework/unmanaged-api/debugging/cor-segment-structure.md) objects.</span></span> <span data-ttu-id="654f8-113">Chaque [COR_SEGMENT](../../../../docs/framework/unmanaged-api/debugging/cor-segment-structure.md) objet fournit des informations sur la plage de mémoire d’un segment particulier, ainsi que la génération des objets dans ce segment.</span><span class="sxs-lookup"><span data-stu-id="654f8-113">Each [COR_SEGMENT](../../../../docs/framework/unmanaged-api/debugging/cor-segment-structure.md) object provides information about the memory range of a particular segment, along with the generation of the objects in that segment.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="654f8-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="654f8-114">Requirements</span></span>  
 <span data-ttu-id="654f8-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="654f8-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="654f8-116">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="654f8-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="654f8-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="654f8-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="654f8-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="654f8-118">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="654f8-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="654f8-119">See also</span></span>
- [<span data-ttu-id="654f8-120">ICorDebugProcess5, interface</span><span class="sxs-lookup"><span data-stu-id="654f8-120">ICorDebugProcess5 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-interface.md)
- [<span data-ttu-id="654f8-121">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="654f8-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
