---
title: ICorProfilerInfo2::GetGenerationBounds, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.GetGenerationBounds
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::GetGenerationBounds
helpviewer_keywords:
- ICorProfilerInfo2::GetGenerationBounds method [.NET Framework profiling]
- GetGenerationBounds method [.NET Framework profiling]
ms.assetid: 9c37185f-d1e0-4a6e-8b99-707f7df61d88
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 19288b5631fea8865530f936ac6d77c0286ee169
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59110376"
---
# <a name="icorprofilerinfo2getgenerationbounds-method"></a><span data-ttu-id="c68e5-102">ICorProfilerInfo2::GetGenerationBounds, méthode</span><span class="sxs-lookup"><span data-stu-id="c68e5-102">ICorProfilerInfo2::GetGenerationBounds Method</span></span>
<span data-ttu-id="c68e5-103">Obtient les régions de la mémoire, qui sont des segments du tas, composant les différentes générations de garbage collection.</span><span class="sxs-lookup"><span data-stu-id="c68e5-103">Gets the memory regions, which are segments of the heap, that make up the various garbage collection generations.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c68e5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c68e5-104">Syntax</span></span>  
  
```  
HRESULT GetGenerationBounds(  
    [in]  ULONG cObjectRanges,  
    [out] ULONG *pcObjectRanges,  
    [out, size_is(cObjectRanges), length_is(*pcObjectRanges)] COR_PRF_GC_GENERATION_RANGE ranges[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c68e5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c68e5-105">Parameters</span></span>  
 `cObjectRanges`  
 <span data-ttu-id="c68e5-106">[in] Nombre d'éléments alloués par l'appelant pour le tableau `ranges`.</span><span class="sxs-lookup"><span data-stu-id="c68e5-106">[in] The number of elements allocated by the caller for the `ranges` array.</span></span>  
  
 `pcObjectRanges`  
 <span data-ttu-id="c68e5-107">[out] Pointeur vers un entier qui spécifie le nombre total de plages, dont une partie ou la totalité sera retournée dans le tableau `ranges`.</span><span class="sxs-lookup"><span data-stu-id="c68e5-107">[out] A pointer to an integer that specifies the total number of ranges, some or all of which will be returned in the `ranges` array.</span></span>  
  
 `ranges`  
 <span data-ttu-id="c68e5-108">[out] Un tableau de [COR_PRF_GC_GENERATION_RANGE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-gc-generation-range-structure.md) structures, chacun d’eux décrit une plage (autrement dit, le bloc) de mémoire dans la génération qui subit le garbage collection.</span><span class="sxs-lookup"><span data-stu-id="c68e5-108">[out] An array of [COR_PRF_GC_GENERATION_RANGE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-gc-generation-range-structure.md) structures, each of which describes a range (that is, block) of memory within the generation that is undergoing garbage collection.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c68e5-109">Notes</span><span class="sxs-lookup"><span data-stu-id="c68e5-109">Remarks</span></span>  
 <span data-ttu-id="c68e5-110">La méthode `GetGenerationBounds` peut être appelée à partir de tout rappel de profileur, à condition que le garbage collection ne soit pas en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="c68e5-110">The `GetGenerationBounds` method can be called from any profiler callback, provided that garbage collection is not in progress.</span></span> <span data-ttu-id="c68e5-111">Autrement dit, elle peut être appelée à partir de tout rappel, à l’exception de ceux qui se produisent entre [ICorProfilerCallback2::GarbageCollectionStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionstarted-method.md) et [ICorProfilerCallback2::GarbageCollectionFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionfinished-method.md).</span><span class="sxs-lookup"><span data-stu-id="c68e5-111">That is, it can be called from any callback except those that occur between [ICorProfilerCallback2::GarbageCollectionStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionstarted-method.md) and [ICorProfilerCallback2::GarbageCollectionFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionfinished-method.md).</span></span>  
  
 <span data-ttu-id="c68e5-112">La plupart des décalages de générations ont lieu pendant les opérations de garbage collection.</span><span class="sxs-lookup"><span data-stu-id="c68e5-112">Most shifting of generations takes place during garbage collections.</span></span> <span data-ttu-id="c68e5-113">Les générations peuvent devenir plus volumineuses entre les collections, mais elles ne se déplacent généralement pas.</span><span class="sxs-lookup"><span data-stu-id="c68e5-113">Generations might grow between collections but generally do not move around.</span></span> <span data-ttu-id="c68e5-114">Par conséquent, les endroits les plus intéressants pour appeler `GetGenerationBounds` sont dans `ICorProfilerCallback2::GarbageCollectionStarted` et `ICorProfilerCallback2::GarbageCollectionFinished`.</span><span class="sxs-lookup"><span data-stu-id="c68e5-114">Therefore, the most interesting places to call `GetGenerationBounds` are in `ICorProfilerCallback2::GarbageCollectionStarted` and `ICorProfilerCallback2::GarbageCollectionFinished`.</span></span>  
  
 <span data-ttu-id="c68e5-115">Pendant le démarrage du programme, certains objets sont alloués par le Common Language Runtime (CLR) lui-même, en général dans les générations 3 et 0.</span><span class="sxs-lookup"><span data-stu-id="c68e5-115">During program startup, some objects are allocated by the common language runtime (CLR) itself, generally in generations 3 and 0.</span></span> <span data-ttu-id="c68e5-116">Ainsi, quand le code managé commence à s'exécuter, ces générations contiennent déjà des objets.</span><span class="sxs-lookup"><span data-stu-id="c68e5-116">Thus, by the time managed code starts executing, these generations will already contain objects.</span></span> <span data-ttu-id="c68e5-117">Normalement, les générations 1 et 2 sont vides, à l'exception des objets factices qui sont générés par le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="c68e5-117">Generations 1 and 2 will normally be empty, except for dummy objects that are generated by the garbage collector.</span></span> <span data-ttu-id="c68e5-118">(La taille des objets factices est de 12 octets dans les implémentations 32 bits du CLR ; elle est plus importante dans les implémentations 64 bits.) Vous verrez peut-être également des plages de génération 2 qui sont contenues dans les modules générés par le générateur d'images natives (NGen.exe).</span><span class="sxs-lookup"><span data-stu-id="c68e5-118">(The size of dummy objects is 12 bytes in 32-bit implementations of the CLR; the size is larger in 64-bit implementations.) You might also see generation 2 ranges that are inside modules produced by the Native Image Generator (NGen.exe).</span></span> <span data-ttu-id="c68e5-119">Dans ce cas, les objets dans la génération 2 sont *objets figés*, qui sont alloués quand NGen.exe s’exécute, plutôt que par le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="c68e5-119">In this case, the objects in generation 2 are *frozen objects*, which are allocated when NGen.exe runs rather than by the garbage collector.</span></span>  
  
 <span data-ttu-id="c68e5-120">Cette fonction utilise des mémoires tampons allouées par l'appelant.</span><span class="sxs-lookup"><span data-stu-id="c68e5-120">This function uses caller-allocated buffers.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c68e5-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c68e5-121">Requirements</span></span>  
 <span data-ttu-id="c68e5-122">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c68e5-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c68e5-123">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="c68e5-123">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="c68e5-124">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c68e5-124">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="c68e5-125">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="c68e5-125">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="c68e5-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c68e5-126">See also</span></span>

- [<span data-ttu-id="c68e5-127">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="c68e5-127">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
- [<span data-ttu-id="c68e5-128">ICorProfilerInfo2, interface</span><span class="sxs-lookup"><span data-stu-id="c68e5-128">ICorProfilerInfo2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-interface.md)
- [<span data-ttu-id="c68e5-129">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="c68e5-129">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [<span data-ttu-id="c68e5-130">Profilage</span><span class="sxs-lookup"><span data-stu-id="c68e5-130">Profiling</span></span>](../../../../docs/framework/unmanaged-api/profiling/index.md)
