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
ms.openlocfilehash: 64e362be57a96bbe0f61b964ab413234f30d0ed1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61782536"
---
# <a name="icorprofilerinfo2getobjectgeneration-method"></a><span data-ttu-id="9bc31-102">ICorProfilerInfo2::GetObjectGeneration, méthode</span><span class="sxs-lookup"><span data-stu-id="9bc31-102">ICorProfilerInfo2::GetObjectGeneration Method</span></span>
<span data-ttu-id="9bc31-103">Obtient le segment du segment de mémoire qui contient l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="9bc31-103">Gets the segment of the heap that contains the specified object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9bc31-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9bc31-104">Syntax</span></span>  
  
```  
HRESULT GetObjectGeneration(  
    [in] ObjectID objectId,  
    [out] COR_PRF_GC_GENERATION_RANGE *range);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9bc31-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9bc31-105">Parameters</span></span>  
 `objectId`  
 <span data-ttu-id="9bc31-106">[in] L’ID de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9bc31-106">[in] The ID of the object.</span></span>  
  
 `range`  
 <span data-ttu-id="9bc31-107">[out] Un pointeur vers un [COR_PRF_GC_GENERATION_RANGE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-gc-generation-range-structure.md) structure qui décrit une plage (autrement dit, un bloc) de mémoire dans la génération qui subit le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="9bc31-107">[out] A pointer to a [COR_PRF_GC_GENERATION_RANGE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-gc-generation-range-structure.md) structure, which describes a range (that is, a block) of memory within the generation that is undergoing garbage collection.</span></span> <span data-ttu-id="9bc31-108">Cette plage contient l’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="9bc31-108">This range contains the specified object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9bc31-109">Notes</span><span class="sxs-lookup"><span data-stu-id="9bc31-109">Remarks</span></span>  
 <span data-ttu-id="9bc31-110">Le `GetObjectGeneration` méthode peut être appelée à partir de tout rappel de profileur, à condition que le garbage collection n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="9bc31-110">The `GetObjectGeneration` method may be called from any profiler callback, provided that garbage collection is not in progress.</span></span> <span data-ttu-id="9bc31-111">Autrement dit, il peut être appelée à partir de tout rappel, à l’exception de ceux qui interviennent entre [ICorProfilerCallback2::GarbageCollectionStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionstarted-method.md) et [ICorProfilerCallback2::GarbageCollectionFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionfinished-method.md).</span><span class="sxs-lookup"><span data-stu-id="9bc31-111">That is, it may be called from any callback except those that occur between [ICorProfilerCallback2::GarbageCollectionStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionstarted-method.md) and [ICorProfilerCallback2::GarbageCollectionFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionfinished-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9bc31-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9bc31-112">Requirements</span></span>  
 <span data-ttu-id="9bc31-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9bc31-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9bc31-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="9bc31-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="9bc31-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9bc31-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9bc31-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9bc31-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9bc31-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bc31-117">See also</span></span>

- [<span data-ttu-id="9bc31-118">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="9bc31-118">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
- [<span data-ttu-id="9bc31-119">ICorProfilerInfo2, interface</span><span class="sxs-lookup"><span data-stu-id="9bc31-119">ICorProfilerInfo2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-interface.md)
