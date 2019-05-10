---
title: ICorDebugEnum, interface
ms.date: 03/30/2017
api_name:
- ICorDebugEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEnum
helpviewer_keywords:
- ICorDebugEnum interface [.NET Framework debugging]
ms.assetid: 80be7efe-2c32-4b9f-8c52-40c6f6268219
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: eb3aca0713b8b11bdfaa23bf33c8e1a0b302e272
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64606536"
---
# <a name="icordebugenum-interface"></a><span data-ttu-id="2217b-102">ICorDebugEnum, interface</span><span class="sxs-lookup"><span data-stu-id="2217b-102">ICorDebugEnum Interface</span></span>

<span data-ttu-id="2217b-103">Sert de l’interface de base abstraite pour les énumérateurs qui sont utilisés par une application de débogage.</span><span class="sxs-lookup"><span data-stu-id="2217b-103">Serves as the abstract base interface for the enumerators that are used by a debugging application.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="2217b-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2217b-104">Methods</span></span>  
  
|<span data-ttu-id="2217b-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="2217b-105">Method</span></span>|<span data-ttu-id="2217b-106">Description</span><span class="sxs-lookup"><span data-stu-id="2217b-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="2217b-107">Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="2217b-107">Clone Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugenum-clone-method.md)|<span data-ttu-id="2217b-108">Crée une copie de cet `ICorDebugEnum` objet.</span><span class="sxs-lookup"><span data-stu-id="2217b-108">Creates a copy of this `ICorDebugEnum` object.</span></span>|  
|[<span data-ttu-id="2217b-109">GetCount, méthode</span><span class="sxs-lookup"><span data-stu-id="2217b-109">GetCount Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugenum-getcount-method.md)|<span data-ttu-id="2217b-110">Obtient le nombre d’éléments dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="2217b-110">Gets the number of items in the enumeration.</span></span>|  
|[<span data-ttu-id="2217b-111">Reset, méthode</span><span class="sxs-lookup"><span data-stu-id="2217b-111">Reset Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugenum-reset-method.md)|<span data-ttu-id="2217b-112">Déplace le curseur au début de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="2217b-112">Moves the cursor to the beginning of the enumeration.</span></span>|  
|[<span data-ttu-id="2217b-113">Skip, méthode</span><span class="sxs-lookup"><span data-stu-id="2217b-113">Skip Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugenum-skip-method.md)|<span data-ttu-id="2217b-114">Déplace le curseur vers l’avant dans l’énumération par le nombre spécifié d’éléments.</span><span class="sxs-lookup"><span data-stu-id="2217b-114">Moves the cursor forward in the enumeration by the specified number of items.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2217b-115">Notes</span><span class="sxs-lookup"><span data-stu-id="2217b-115">Remarks</span></span>  
 <span data-ttu-id="2217b-116">Les énumérateurs suivants dérivent `ICorDebugEnum`:</span><span class="sxs-lookup"><span data-stu-id="2217b-116">The following enumerators derive from `ICorDebugEnum`:</span></span>  
  
- <span data-ttu-id="2217b-117">"ICorDebugAppDomainEnum"</span><span class="sxs-lookup"><span data-stu-id="2217b-117">"ICorDebugAppDomainEnum"</span></span>  
  
- <span data-ttu-id="2217b-118">"ICorDebugAssemblyEnum"</span><span class="sxs-lookup"><span data-stu-id="2217b-118">"ICorDebugAssemblyEnum"</span></span>  
  
- [<span data-ttu-id="2217b-119">ICorDebugBlockingObjectEnum</span><span class="sxs-lookup"><span data-stu-id="2217b-119">ICorDebugBlockingObjectEnum</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugblockingobjectenum-interface.md)  
  
- <span data-ttu-id="2217b-120">"ICorDebugBreakpointEnum"</span><span class="sxs-lookup"><span data-stu-id="2217b-120">"ICorDebugBreakpointEnum"</span></span>  
  
- <span data-ttu-id="2217b-121">"ICorDebugChainEnum"</span><span class="sxs-lookup"><span data-stu-id="2217b-121">"ICorDebugChainEnum"</span></span>  
  
- <span data-ttu-id="2217b-122">"ICorDebugCodeEnum"</span><span class="sxs-lookup"><span data-stu-id="2217b-122">"ICorDebugCodeEnum"</span></span>  
  
- <span data-ttu-id="2217b-123">"ICorDebugErrorInfoEnum"</span><span class="sxs-lookup"><span data-stu-id="2217b-123">"ICorDebugErrorInfoEnum"</span></span>  
  
- [<span data-ttu-id="2217b-124">ICorDebugExceptionObjectCallStackEnum</span><span class="sxs-lookup"><span data-stu-id="2217b-124">ICorDebugExceptionObjectCallStackEnum</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptionobjectcallstackenum-interface.md)  
  
- <span data-ttu-id="2217b-125">"ICorDebugFrameEnum"</span><span class="sxs-lookup"><span data-stu-id="2217b-125">"ICorDebugFrameEnum"</span></span>  
  
- [<span data-ttu-id="2217b-126">ICorDebugGCReferenceEnum</span><span class="sxs-lookup"><span data-stu-id="2217b-126">ICorDebugGCReferenceEnum</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuggcreferenceenum-interface.md)  
  
- [<span data-ttu-id="2217b-127">ICorDebugGuidToTypeEnum</span><span class="sxs-lookup"><span data-stu-id="2217b-127">ICorDebugGuidToTypeEnum</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugguidtotypeenum-interface.md)  
  
- [<span data-ttu-id="2217b-128">ICorDebugHeapEnum</span><span class="sxs-lookup"><span data-stu-id="2217b-128">ICorDebugHeapEnum</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugheapenum-interface.md)  
  
- [<span data-ttu-id="2217b-129">ICorDebugHeapSegmentEnum</span><span class="sxs-lookup"><span data-stu-id="2217b-129">ICorDebugHeapSegmentEnum</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugheapsegmentenum-interface.md)  
  
- <span data-ttu-id="2217b-130">"ICorDebugModuleEnum"</span><span class="sxs-lookup"><span data-stu-id="2217b-130">"ICorDebugModuleEnum"</span></span>  
  
- <span data-ttu-id="2217b-131">"ICorDebugObjectEnum"</span><span class="sxs-lookup"><span data-stu-id="2217b-131">"ICorDebugObjectEnum"</span></span>  
  
- <span data-ttu-id="2217b-132">"ICorDebugProcessEnum"</span><span class="sxs-lookup"><span data-stu-id="2217b-132">"ICorDebugProcessEnum"</span></span>  
  
- <span data-ttu-id="2217b-133">"ICorDebugStepperEnum"</span><span class="sxs-lookup"><span data-stu-id="2217b-133">"ICorDebugStepperEnum"</span></span>  
  
- <span data-ttu-id="2217b-134">"ICorDebugThreadEnum"</span><span class="sxs-lookup"><span data-stu-id="2217b-134">"ICorDebugThreadEnum"</span></span>  
  
- <span data-ttu-id="2217b-135">"ICorDebugTypeEnum"</span><span class="sxs-lookup"><span data-stu-id="2217b-135">"ICorDebugTypeEnum"</span></span>  
  
- <span data-ttu-id="2217b-136">"ICorDebugValueEnum"</span><span class="sxs-lookup"><span data-stu-id="2217b-136">"ICorDebugValueEnum"</span></span>  
  
- [<span data-ttu-id="2217b-137">ICorDebugVariableHomeEnum</span><span class="sxs-lookup"><span data-stu-id="2217b-137">ICorDebugVariableHomeEnum</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehomeenum-interface.md)  
  
> [!NOTE]
>  <span data-ttu-id="2217b-138">Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.</span><span class="sxs-lookup"><span data-stu-id="2217b-138">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2217b-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2217b-139">Requirements</span></span>  
 <span data-ttu-id="2217b-140">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2217b-140">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2217b-141">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2217b-141">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2217b-142">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2217b-142">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2217b-143">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2217b-143">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2217b-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2217b-144">See also</span></span>

- [<span data-ttu-id="2217b-145">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="2217b-145">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
