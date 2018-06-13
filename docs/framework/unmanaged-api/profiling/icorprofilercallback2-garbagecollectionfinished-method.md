---
title: ICorProfilerCallback2::GarbageCollectionFinished, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback2.GarbageCollectionFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback2::GarbageCollectionFinished
helpviewer_keywords:
- ICorProfilerCallback2::GarbageCollectionFinished method [.NET Framework profiling]
- GarbageCollectionFinished method [.NET Framework profiling]
ms.assetid: 1a5758ea-2354-43c0-92a3-32c9909d64e1
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 21f7e9fa0e567063c49caa390ace09c43454b092
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33451680"
---
# <a name="icorprofilercallback2garbagecollectionfinished-method"></a><span data-ttu-id="7a083-102">ICorProfilerCallback2::GarbageCollectionFinished, méthode</span><span class="sxs-lookup"><span data-stu-id="7a083-102">ICorProfilerCallback2::GarbageCollectionFinished Method</span></span>
<span data-ttu-id="7a083-103">Notifie le profileur que le garbage collection est terminée et que tous les rappels de garbage collection ont été publiés.</span><span class="sxs-lookup"><span data-stu-id="7a083-103">Notifies the profiler that garbage collection has completed and all garbage collection callbacks have been issued for it.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7a083-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a083-104">Syntax</span></span>  
  
```  
HRESULT GarbageCollectionFinished();  
```  
  
## <a name="remarks"></a><span data-ttu-id="7a083-105">Notes</span><span class="sxs-lookup"><span data-stu-id="7a083-105">Remarks</span></span>  
 <span data-ttu-id="7a083-106">Il est possible pour le profileur d’inspecter des objets dans leurs emplacements finaux lorsque le `GarbageCollectionFinished` méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="7a083-106">It is safe for the profiler to inspect objects in their final locations when the `GarbageCollectionFinished` method is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7a083-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7a083-107">Requirements</span></span>  
 <span data-ttu-id="7a083-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7a083-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7a083-109">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="7a083-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="7a083-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7a083-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7a083-111">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7a083-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7a083-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a083-112">See Also</span></span>  
 [<span data-ttu-id="7a083-113">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="7a083-113">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="7a083-114">ICorProfilerCallback2, interface</span><span class="sxs-lookup"><span data-stu-id="7a083-114">ICorProfilerCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-interface.md)
