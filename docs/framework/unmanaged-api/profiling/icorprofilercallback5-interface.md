---
title: ICorProfilerCallback5, interface
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback5
api_location:
- Mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback5
helpviewer_keywords:
- ICorProfilerCallback5 interface [.NET Framework profiling]
ms.assetid: 61d2e9ef-5f1f-4771-8847-239616e35d84
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: e6481d647541af40b956c38a76d281ccb84e7c7f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54602544"
---
# <a name="icorprofilercallback5-interface"></a><span data-ttu-id="82ac3-102">ICorProfilerCallback5, interface</span><span class="sxs-lookup"><span data-stu-id="82ac3-102">ICorProfilerCallback5 Interface</span></span>
<span data-ttu-id="82ac3-103">Complètent les informations pour identifier un profileur de la fermeture complète d’objets actifs, lorsqu’il est utilisé avec soit le [ICorProfilerCallback::RootReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-rootreferences-method.md) ou [ICorProfilerCallback2::RootReferences2](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-rootreferences2-method.md)méthode avec le [ICorProfilerCallback::ObjectReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-objectreferences-method.md) et [ConditionalWeakTableElementReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback5-conditionalweaktableelementreferences-method.md) méthodes.</span><span class="sxs-lookup"><span data-stu-id="82ac3-103">Supplements information to help a profiler identify the full closure of live objects, when used with either the [ICorProfilerCallback::RootReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-rootreferences-method.md) or [ICorProfilerCallback2::RootReferences2](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-rootreferences2-method.md) method together with the [ICorProfilerCallback::ObjectReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-objectreferences-method.md) and [ConditionalWeakTableElementReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback5-conditionalweaktableelementreferences-method.md) methods.</span></span>  
  
 <span data-ttu-id="82ac3-104">`ICorProfilerCallback5` doit être implémentée par un profileur de mémoire managée pour s'abonner aux notifications relatives aux handles dépendants.</span><span class="sxs-lookup"><span data-stu-id="82ac3-104">`ICorProfilerCallback5` must be implemented by a managed memory profiler to subscribe to notifications related to dependent handles.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="82ac3-105">Notes</span><span class="sxs-lookup"><span data-stu-id="82ac3-105">Remarks</span></span>  
  
## <a name="methods"></a><span data-ttu-id="82ac3-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="82ac3-106">Methods</span></span>  
  
|<span data-ttu-id="82ac3-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="82ac3-107">Method</span></span>|<span data-ttu-id="82ac3-108">Description</span><span class="sxs-lookup"><span data-stu-id="82ac3-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="82ac3-109">ConditionalWeakTableElementReferences, méthode</span><span class="sxs-lookup"><span data-stu-id="82ac3-109">ConditionalWeakTableElementReferences Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback5-conditionalweaktableelementreferences-method.md)|<span data-ttu-id="82ac3-110">Identifie la fermeture transitive des objets référencés par ces racines via les références des champs des membres directs et via les dépendances de `ConditionalWeakTable`.</span><span class="sxs-lookup"><span data-stu-id="82ac3-110">Identifies the transitive closure of objects referenced by those roots through both direct member field references and through `ConditionalWeakTable` dependencies.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="82ac3-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="82ac3-111">Requirements</span></span>  
 <span data-ttu-id="82ac3-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="82ac3-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="82ac3-113">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="82ac3-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="82ac3-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="82ac3-114">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="82ac3-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82ac3-115">See also</span></span>
- [<span data-ttu-id="82ac3-116">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="82ac3-116">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [<span data-ttu-id="82ac3-117">ICorProfilerCallback2, interface</span><span class="sxs-lookup"><span data-stu-id="82ac3-117">ICorProfilerCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-interface.md)
