---
title: ICorDebugHeapSegmentEnum, interface
ms.date: 03/30/2017
api_name:
- ICorDebugHealRegionEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapSegmentEnum
helpviewer_keywords:
- ICorDebugHeapSegmentEnum interface [.NET Framework debugging]
ms.assetid: 20fc1b9d-e228-4107-bd76-53934c1724b9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 73036d1c12c46cbfda8031073a005bc9b376040e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59137642"
---
# <a name="icordebugheapsegmentenum-interface"></a><span data-ttu-id="1a8c8-102">ICorDebugHeapSegmentEnum, interface</span><span class="sxs-lookup"><span data-stu-id="1a8c8-102">ICorDebugHeapSegmentEnum Interface</span></span>
<span data-ttu-id="1a8c8-103">Fournit un énumérateur pour les régions de mémoire du tas managé.</span><span class="sxs-lookup"><span data-stu-id="1a8c8-103">Provides an enumerator for the memory regions of the managed heap.</span></span> <span data-ttu-id="1a8c8-104">Cette interface est une sous-classe de l’interface ICorDebugEnum.</span><span class="sxs-lookup"><span data-stu-id="1a8c8-104">This interface is a subclass of the ICorDebugEnum interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="1a8c8-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1a8c8-105">Methods</span></span>  
  
|<span data-ttu-id="1a8c8-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="1a8c8-106">Method</span></span>|<span data-ttu-id="1a8c8-107">Description</span><span class="sxs-lookup"><span data-stu-id="1a8c8-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="1a8c8-108">Next, méthode</span><span class="sxs-lookup"><span data-stu-id="1a8c8-108">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugheapsegmentenum-next-method.md)|<span data-ttu-id="1a8c8-109">Obtient le nombre spécifié de [COR_HEAPOBJECT](../../../../docs/framework/unmanaged-api/debugging/cor-heapobject-structure.md) instances qui contiennent des informations sur les régions du tas managé.</span><span class="sxs-lookup"><span data-stu-id="1a8c8-109">Gets the specified number of [COR_HEAPOBJECT](../../../../docs/framework/unmanaged-api/debugging/cor-heapobject-structure.md) instances that contain information about regions of the managed heap.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1a8c8-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1a8c8-110">Remarks</span></span>  
 <span data-ttu-id="1a8c8-111">Le `ICorDebugHeapSegmentEnum` interface implémente l’interface ICorDebugEnum.</span><span class="sxs-lookup"><span data-stu-id="1a8c8-111">The `ICorDebugHeapSegmentEnum` interface implements the ICorDebugEnum interface.</span></span>  
  
 <span data-ttu-id="1a8c8-112">Un `ICorDebugHeapSegmentEnum` instance est remplie avec [COR_HEAPOBJECT](../../../../docs/framework/unmanaged-api/debugging/cor-heapobject-structure.md) instances en appelant le [ICorDebugProcess5::EnumerateHeapRegions](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-enumerateheapregions-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="1a8c8-112">An `ICorDebugHeapSegmentEnum` instance is populated with [COR_HEAPOBJECT](../../../../docs/framework/unmanaged-api/debugging/cor-heapobject-structure.md) instances by calling the [ICorDebugProcess5::EnumerateHeapRegions](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-enumerateheapregions-method.md) method.</span></span> <span data-ttu-id="1a8c8-113">Le [COR_HEAPOBJECT](../../../../docs/framework/unmanaged-api/debugging/cor-heapobject-structure.md) objets dans la collection peuvent être énumérés en appelant le [ICorDebugHeapSegmentEnum::Next](../../../../docs/framework/unmanaged-api/debugging/icordebugheapsegmentenum-next-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="1a8c8-113">The [COR_HEAPOBJECT](../../../../docs/framework/unmanaged-api/debugging/cor-heapobject-structure.md) objects in the collection can be enumerated by calling the [ICorDebugHeapSegmentEnum::Next](../../../../docs/framework/unmanaged-api/debugging/icordebugheapsegmentenum-next-method.md) method.</span></span>  
  
 <span data-ttu-id="1a8c8-114">Un `ICorDebugHeapSegmentEnum` objet de collection énumère toutes les régions de mémoire qui peuvent contenir des objets gérés, mais cela ne garantit pas que les objets gérés qui résident dans ces régions.</span><span class="sxs-lookup"><span data-stu-id="1a8c8-114">An `ICorDebugHeapSegmentEnum` collection object enumerates all memory regions that may contain managed objects, but it does not guarantee that managed objects actually reside in those regions.</span></span> <span data-ttu-id="1a8c8-115">Il peut inclure des informations sur les régions de mémoire vide ou réservée.</span><span class="sxs-lookup"><span data-stu-id="1a8c8-115">It may include information about empty or reserved memory regions.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1a8c8-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a8c8-116">Requirements</span></span>  
 <span data-ttu-id="1a8c8-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1a8c8-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1a8c8-118">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1a8c8-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1a8c8-119">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1a8c8-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1a8c8-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1a8c8-120">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1a8c8-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a8c8-121">See also</span></span>

- [<span data-ttu-id="1a8c8-122">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="1a8c8-122">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
