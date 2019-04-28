---
title: ICorProfilerCallback2::GarbageCollectionStarted, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback2.GarbageCollectionStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback2::GarbageCollectionStarted
helpviewer_keywords:
- GarbageCollectionStarted method [.NET Framework profiling]
- ICorProfilerCallback2::GarbageCollectionStarted method [.NET Framework profiling]
ms.assetid: 44eef087-f21f-4fe2-b481-f8a0ee022e7d
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f5f9104dded44540c47c955c15354d8d76a27650
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61914364"
---
# <a name="icorprofilercallback2garbagecollectionstarted-method"></a><span data-ttu-id="b7eb4-102">ICorProfilerCallback2::GarbageCollectionStarted, méthode</span><span class="sxs-lookup"><span data-stu-id="b7eb4-102">ICorProfilerCallback2::GarbageCollectionStarted Method</span></span>
<span data-ttu-id="b7eb4-103">Notifie le profileur de code que le garbage collection a démarré.</span><span class="sxs-lookup"><span data-stu-id="b7eb4-103">Notifies the code profiler that garbage collection has started.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b7eb4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7eb4-104">Syntax</span></span>  
  
```  
HRESULT GarbageCollectionStarted(  
    [in] int cGenerations,  
    [in, size_is(cGenerations), length_is(cGenerations)] BOOL generationCollected[],  
    [in] COR_PRF_GC_REASON reason);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b7eb4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7eb4-105">Parameters</span></span>  
 `cGenerations`  
 <span data-ttu-id="b7eb4-106">[in] Le nombre total d’entrées dans le `generationCollected` tableau.</span><span class="sxs-lookup"><span data-stu-id="b7eb4-106">[in] The total number of entries in the `generationCollected` array.</span></span>  
  
 `generationCollected`  
 <span data-ttu-id="b7eb4-107">[in] Un tableau de valeurs booléennes, qui sont `true` si la génération qui correspond à l’index de tableau est collecté par ce garbage collection ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="b7eb4-107">[in] An array of Boolean values, which are `true` if the generation that corresponds to the array index is being collected by this garbage collection; otherwise, `false`.</span></span>  
  
 <span data-ttu-id="b7eb4-108">Le tableau est indexé par une valeur de la [COR_PRF_GC_GENERATION](../../../../docs/framework/unmanaged-api/profiling/cor-prf-gc-generation-enumeration.md) énumération, qui indique la génération.</span><span class="sxs-lookup"><span data-stu-id="b7eb4-108">The array is indexed by a value of the [COR_PRF_GC_GENERATION](../../../../docs/framework/unmanaged-api/profiling/cor-prf-gc-generation-enumeration.md) enumeration, which indicates the generation.</span></span>  
  
 `reason`  
 <span data-ttu-id="b7eb4-109">[in] Une valeur de la [COR_PRF_GC_REASON](../../../../docs/framework/unmanaged-api/profiling/cor-prf-gc-reason-enumeration.md) énumération qui indique la raison pour laquelle le garbage collection a été INDUITE.</span><span class="sxs-lookup"><span data-stu-id="b7eb4-109">[in] A value of the [COR_PRF_GC_REASON](../../../../docs/framework/unmanaged-api/profiling/cor-prf-gc-reason-enumeration.md) enumeration that indicates the reason the garbage collection was induced.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b7eb4-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b7eb4-110">Remarks</span></span>  
 <span data-ttu-id="b7eb4-111">Tous les rappels qui se rapportent à ce garbage collection seront produit entre le `GarbageCollectionStarted` rappel et le correspondantes [ICorProfilerCallback2::GarbageCollectionFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionfinished-method.md) rappel.</span><span class="sxs-lookup"><span data-stu-id="b7eb4-111">All callbacks that pertain to this garbage collection will occur between the `GarbageCollectionStarted` callback and the corresponding [ICorProfilerCallback2::GarbageCollectionFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionfinished-method.md) callback.</span></span> <span data-ttu-id="b7eb4-112">Ces rappels ne doivent pas se produire sur le même thread.</span><span class="sxs-lookup"><span data-stu-id="b7eb4-112">These callbacks need not occur on the same thread.</span></span>  
  
 <span data-ttu-id="b7eb4-113">Il est possible que le profileur inspecter les objets dans leurs emplacements d’origine pendant le `GarbageCollectionStarted` rappel.</span><span class="sxs-lookup"><span data-stu-id="b7eb4-113">It is safe for the profiler to inspect objects in their original locations during the `GarbageCollectionStarted` callback.</span></span> <span data-ttu-id="b7eb4-114">Le garbage collector commencera à déplacer les objets après le retour de `GarbageCollectionStarted`.</span><span class="sxs-lookup"><span data-stu-id="b7eb4-114">The garbage collector will begin moving objects after the return from `GarbageCollectionStarted`.</span></span> <span data-ttu-id="b7eb4-115">Une fois que le profileur a retourné à partir de ce rappel, le profileur doit considérer tous les ID d’objet est non valide jusqu'à ce qu’il reçoive un `ICorProfilerCallback2::GarbageCollectionFinished` rappel.</span><span class="sxs-lookup"><span data-stu-id="b7eb4-115">After the profiler has returned from this callback, the profiler should consider all object IDs to be invalid until it receives a `ICorProfilerCallback2::GarbageCollectionFinished` callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b7eb4-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7eb4-116">Requirements</span></span>  
 <span data-ttu-id="b7eb4-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b7eb4-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b7eb4-118">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="b7eb4-118">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="b7eb4-119">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b7eb4-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b7eb4-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b7eb4-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b7eb4-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7eb4-121">See also</span></span>

- [<span data-ttu-id="b7eb4-122">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="b7eb4-122">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="b7eb4-123">ICorProfilerCallback2, interface</span><span class="sxs-lookup"><span data-stu-id="b7eb4-123">ICorProfilerCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-interface.md)
