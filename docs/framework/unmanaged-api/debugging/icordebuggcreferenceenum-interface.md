---
title: ICorDebugGCReferenceEnum, interface
ms.date: 03/30/2017
api_name:
- ICorDebugGCReferenceEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugGCReferenceEnum
helpviewer_keywords:
- ICorDebugGCReferenceEnum interface [.NET Framework debugging]
ms.assetid: 5f3c91c9-c035-454f-96cc-011cab1ea06b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fa8c3160dc779b2475dec63be896af5283cf5346
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33418163"
---
# <a name="icordebuggcreferenceenum-interface"></a><span data-ttu-id="9d05f-102">ICorDebugGCReferenceEnum, interface</span><span class="sxs-lookup"><span data-stu-id="9d05f-102">ICorDebugGCReferenceEnum Interface</span></span>
<span data-ttu-id="9d05f-103">Fournit un énumérateur pour les objets qui sont récupérés par le récupérateur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="9d05f-103">Provides an enumerator for objects that will be garbage-collected.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="9d05f-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9d05f-104">Methods</span></span>  
  
|<span data-ttu-id="9d05f-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="9d05f-105">Method</span></span>|<span data-ttu-id="9d05f-106">Description</span><span class="sxs-lookup"><span data-stu-id="9d05f-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="9d05f-107">Next, méthode</span><span class="sxs-lookup"><span data-stu-id="9d05f-107">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuggcreferenceenum-next-method.md)|<span data-ttu-id="9d05f-108">Obtient le nombre spécifié de [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) instances qui contiennent des informations sur les objets qui seront par le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="9d05f-108">Gets the specified number of [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) instances that contain information about objects that will be garbage-collected.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9d05f-109">Notes</span><span class="sxs-lookup"><span data-stu-id="9d05f-109">Remarks</span></span>  
 <span data-ttu-id="9d05f-110">Le `ICorDebugGCReferenceEnum` interface implémente l’interface « ICorDebugEnum ».</span><span class="sxs-lookup"><span data-stu-id="9d05f-110">The `ICorDebugGCReferenceEnum` interface implements the "ICorDebugEnum" interface.</span></span>  
  
 <span data-ttu-id="9d05f-111">Un `ICorDebugGCReferenceEnum` instance est remplie avec [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) instances en appelant le [ICorDebugProcess5::EnumerateGCReferences](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-enumerategcreferences-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="9d05f-111">An `ICorDebugGCReferenceEnum` instance is populated with [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) instances by calling the [ICorDebugProcess5::EnumerateGCReferences](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-enumerategcreferences-method.md) method.</span></span> <span data-ttu-id="9d05f-112">[COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) objets peuvent être énumérées en appelant le [ICorDebugGCReference::Next](../../../../docs/framework/unmanaged-api/debugging/icordebuggcreferenceenum-next-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="9d05f-112">[COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) objects can be enumerated by calling the [ICorDebugGCReference::Next](../../../../docs/framework/unmanaged-api/debugging/icordebuggcreferenceenum-next-method.md) method.</span></span>  
  
 <span data-ttu-id="9d05f-113">Le [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) trois types d’objets représentent des objets dans la collection remplie par cette méthode :</span><span class="sxs-lookup"><span data-stu-id="9d05f-113">The [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) objects in the collection populated by this method represent three kinds of objects:</span></span>  
  
-   <span data-ttu-id="9d05f-114">Objets de toutes les piles managées.</span><span class="sxs-lookup"><span data-stu-id="9d05f-114">Objects from all managed stacks.</span></span> <span data-ttu-id="9d05f-115">Cela inclut des références actives dans le code managé, ainsi que les objets créés par le common language runtime.</span><span class="sxs-lookup"><span data-stu-id="9d05f-115">This includes live references in managed code as well as objects created by the common language runtime.</span></span>  
  
-   <span data-ttu-id="9d05f-116">Objets à partir de la table de handles.</span><span class="sxs-lookup"><span data-stu-id="9d05f-116">Objects from the handle table.</span></span> <span data-ttu-id="9d05f-117">Cela inclut des références solides (`HNDTYPE_STRONG` et `HNDTYPE_REFCOUNT`) et les variables statiques dans un module.</span><span class="sxs-lookup"><span data-stu-id="9d05f-117">This includes strong references (`HNDTYPE_STRONG` and `HNDTYPE_REFCOUNT`) and static variables in a module.</span></span>  
  
-   <span data-ttu-id="9d05f-118">Objets à partir de la file d’attente du finaliseur.</span><span class="sxs-lookup"><span data-stu-id="9d05f-118">Objects from the finalizer queue.</span></span> <span data-ttu-id="9d05f-119">La file d’attente du finaliseur racines d’objets jusqu'à ce que le finaliseur a exécuté.</span><span class="sxs-lookup"><span data-stu-id="9d05f-119">The finalizer queue roots objects until the finalizer has run.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9d05f-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9d05f-120">Requirements</span></span>  
 <span data-ttu-id="9d05f-121">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9d05f-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9d05f-122">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9d05f-122">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9d05f-123">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9d05f-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9d05f-124">**Versions du .NET framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9d05f-124">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9d05f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d05f-125">See Also</span></span>  
 [<span data-ttu-id="9d05f-126">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="9d05f-126">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
