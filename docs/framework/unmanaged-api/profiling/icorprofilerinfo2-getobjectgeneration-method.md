---
title: ICorProfilerInfo2::GetObjectGeneration, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.GetObjectGeneration
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::GetObjectGeneration
helpviewer_keywords:
- GetObjectGeneration method [.NET Framework profiling]
- ICorProfilerInfo2::GetObjectGeneration method [.NET Framework profiling]
ms.assetid: b0d25f76-0bd5-4aa6-96cf-bfec0e1de28b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 729ae390d36f82cbafd46385b396d6513489628e
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57474782"
---
# <a name="icorprofilerinfo2getobjectgeneration-method"></a><span data-ttu-id="b070d-102">ICorProfilerInfo2::GetObjectGeneration, méthode</span><span class="sxs-lookup"><span data-stu-id="b070d-102">ICorProfilerInfo2::GetObjectGeneration Method</span></span>
<span data-ttu-id="b070d-103">Obtient le segment du segment de mémoire qui contient l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="b070d-103">Gets the segment of the heap that contains the specified object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b070d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b070d-104">Syntax</span></span>  
  
```  
HRESULT GetObjectGeneration(  
    [in] ObjectID objectId,  
    [out] COR_PRF_GC_GENERATION_RANGE *range);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b070d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b070d-105">Parameters</span></span>  
 `objectId`  
 <span data-ttu-id="b070d-106">[in] L’ID de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b070d-106">[in] The ID of the object.</span></span>  
  
 `range`  
 <span data-ttu-id="b070d-107">[out] Un pointeur vers un [COR_PRF_GC_GENERATION_RANGE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-gc-generation-range-structure.md) structure qui décrit une plage (autrement dit, un bloc) de mémoire dans la génération qui subit le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="b070d-107">[out] A pointer to a [COR_PRF_GC_GENERATION_RANGE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-gc-generation-range-structure.md) structure, which describes a range (that is, a block) of memory within the generation that is undergoing garbage collection.</span></span> <span data-ttu-id="b070d-108">Cette plage contient l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="b070d-108">This range contains the specified object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b070d-109">Notes</span><span class="sxs-lookup"><span data-stu-id="b070d-109">Remarks</span></span>  
 <span data-ttu-id="b070d-110">Le `GetObjectGeneration` méthode peut être appelée à partir de tout rappel de profileur, à condition que le garbage collection n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="b070d-110">The `GetObjectGeneration` method may be called from any profiler callback, provided that garbage collection is not in progress.</span></span> <span data-ttu-id="b070d-111">Autrement dit, il peut être appelée à partir de tout rappel, à l’exception de ceux qui interviennent entre [ICorProfilerCallback2::GarbageCollectionStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionstarted-method.md) et [ICorProfilerCallback2::GarbageCollectionFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionfinished-method.md).</span><span class="sxs-lookup"><span data-stu-id="b070d-111">That is, it may be called from any callback except those that occur between [ICorProfilerCallback2::GarbageCollectionStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionstarted-method.md) and [ICorProfilerCallback2::GarbageCollectionFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionfinished-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b070d-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b070d-112">Requirements</span></span>  
 <span data-ttu-id="b070d-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b070d-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b070d-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="b070d-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="b070d-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b070d-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b070d-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b070d-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b070d-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b070d-117">See also</span></span>
- [<span data-ttu-id="b070d-118">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="b070d-118">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
- [<span data-ttu-id="b070d-119">ICorProfilerInfo2, interface</span><span class="sxs-lookup"><span data-stu-id="b070d-119">ICorProfilerInfo2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-interface.md)
