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
ms.openlocfilehash: 8f83d2ac9ca96145fa89b283fec42c71858097f6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59080825"
---
# <a name="icordebuggcreferenceenum-interface"></a><span data-ttu-id="3fb0b-102">ICorDebugGCReferenceEnum, interface</span><span class="sxs-lookup"><span data-stu-id="3fb0b-102">ICorDebugGCReferenceEnum Interface</span></span>
<span data-ttu-id="3fb0b-103">Fournit un énumérateur pour les objets qui sont récupérés par le récupérateur de mémoire.</span><span class="sxs-lookup"><span data-stu-id="3fb0b-103">Provides an enumerator for objects that will be garbage-collected.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3fb0b-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3fb0b-104">Methods</span></span>  
  
|<span data-ttu-id="3fb0b-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="3fb0b-105">Method</span></span>|<span data-ttu-id="3fb0b-106">Description</span><span class="sxs-lookup"><span data-stu-id="3fb0b-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="3fb0b-107">Next, méthode</span><span class="sxs-lookup"><span data-stu-id="3fb0b-107">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuggcreferenceenum-next-method.md)|<span data-ttu-id="3fb0b-108">Obtient le nombre spécifié de [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) instances qui contiennent des informations sur les objets qui seront le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="3fb0b-108">Gets the specified number of [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) instances that contain information about objects that will be garbage-collected.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3fb0b-109">Notes</span><span class="sxs-lookup"><span data-stu-id="3fb0b-109">Remarks</span></span>  
 <span data-ttu-id="3fb0b-110">Le `ICorDebugGCReferenceEnum` interface implémente l’interface « ICorDebugEnum ».</span><span class="sxs-lookup"><span data-stu-id="3fb0b-110">The `ICorDebugGCReferenceEnum` interface implements the "ICorDebugEnum" interface.</span></span>  
  
 <span data-ttu-id="3fb0b-111">Un `ICorDebugGCReferenceEnum` instance est remplie avec [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) instances en appelant le [ICorDebugProcess5::EnumerateGCReferences](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-enumerategcreferences-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="3fb0b-111">An `ICorDebugGCReferenceEnum` instance is populated with [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) instances by calling the [ICorDebugProcess5::EnumerateGCReferences](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-enumerategcreferences-method.md) method.</span></span> <span data-ttu-id="3fb0b-112">[COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) objets peuvent être énumérés en appelant le [ICorDebugGCReference::Next](../../../../docs/framework/unmanaged-api/debugging/icordebuggcreferenceenum-next-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="3fb0b-112">[COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) objects can be enumerated by calling the [ICorDebugGCReference::Next](../../../../docs/framework/unmanaged-api/debugging/icordebuggcreferenceenum-next-method.md) method.</span></span>  
  
 <span data-ttu-id="3fb0b-113">Le [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) trois types d’objets représentent des objets dans la collection remplie par cette méthode :</span><span class="sxs-lookup"><span data-stu-id="3fb0b-113">The [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) objects in the collection populated by this method represent three kinds of objects:</span></span>  
  
-   <span data-ttu-id="3fb0b-114">Objets à partir de toutes les piles gérées.</span><span class="sxs-lookup"><span data-stu-id="3fb0b-114">Objects from all managed stacks.</span></span> <span data-ttu-id="3fb0b-115">Cela inclut des références en direct dans le code managé, ainsi que les objets créés par le common language runtime.</span><span class="sxs-lookup"><span data-stu-id="3fb0b-115">This includes live references in managed code as well as objects created by the common language runtime.</span></span>  
  
-   <span data-ttu-id="3fb0b-116">Objets à partir de la table de handles.</span><span class="sxs-lookup"><span data-stu-id="3fb0b-116">Objects from the handle table.</span></span> <span data-ttu-id="3fb0b-117">Cela inclut des références fortes (`HNDTYPE_STRONG` et `HNDTYPE_REFCOUNT`) et les variables statiques dans un module.</span><span class="sxs-lookup"><span data-stu-id="3fb0b-117">This includes strong references (`HNDTYPE_STRONG` and `HNDTYPE_REFCOUNT`) and static variables in a module.</span></span>  
  
-   <span data-ttu-id="3fb0b-118">Objets à partir de la file d’attente du finaliseur.</span><span class="sxs-lookup"><span data-stu-id="3fb0b-118">Objects from the finalizer queue.</span></span> <span data-ttu-id="3fb0b-119">La file d’attente du finaliseur racines des objets jusqu'à ce que le finaliseur s’est exécutée.</span><span class="sxs-lookup"><span data-stu-id="3fb0b-119">The finalizer queue roots objects until the finalizer has run.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3fb0b-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3fb0b-120">Requirements</span></span>  
 <span data-ttu-id="3fb0b-121">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3fb0b-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3fb0b-122">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3fb0b-122">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3fb0b-123">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3fb0b-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3fb0b-124">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3fb0b-124">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3fb0b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3fb0b-125">See also</span></span>

- [<span data-ttu-id="3fb0b-126">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="3fb0b-126">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
