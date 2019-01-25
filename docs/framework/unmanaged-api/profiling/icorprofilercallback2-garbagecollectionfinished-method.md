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
ms.openlocfilehash: 040c51723a2505a1320d2ecde38c9ed1cd19d254
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54734920"
---
# <a name="icorprofilercallback2garbagecollectionfinished-method"></a><span data-ttu-id="2d6de-102">ICorProfilerCallback2::GarbageCollectionFinished, méthode</span><span class="sxs-lookup"><span data-stu-id="2d6de-102">ICorProfilerCallback2::GarbageCollectionFinished Method</span></span>
<span data-ttu-id="2d6de-103">Notifie le profileur que le garbage collection est terminée et que tous les rappels de garbage collection ont été publiés.</span><span class="sxs-lookup"><span data-stu-id="2d6de-103">Notifies the profiler that garbage collection has completed and all garbage collection callbacks have been issued for it.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2d6de-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d6de-104">Syntax</span></span>  
  
```  
HRESULT GarbageCollectionFinished();  
```  
  
## <a name="remarks"></a><span data-ttu-id="2d6de-105">Notes</span><span class="sxs-lookup"><span data-stu-id="2d6de-105">Remarks</span></span>  
 <span data-ttu-id="2d6de-106">Il est possible que le profileur inspecter les objets dans leurs emplacements finaux lorsque la `GarbageCollectionFinished` méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="2d6de-106">It is safe for the profiler to inspect objects in their final locations when the `GarbageCollectionFinished` method is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2d6de-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2d6de-107">Requirements</span></span>  
 <span data-ttu-id="2d6de-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2d6de-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2d6de-109">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="2d6de-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="2d6de-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2d6de-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2d6de-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2d6de-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2d6de-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d6de-112">See also</span></span>
- [<span data-ttu-id="2d6de-113">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="2d6de-113">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="2d6de-114">ICorProfilerCallback2, interface</span><span class="sxs-lookup"><span data-stu-id="2d6de-114">ICorProfilerCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-interface.md)
