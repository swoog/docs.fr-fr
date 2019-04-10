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
ms.openlocfilehash: f613842c12b50b8a58aac1b71bf2f3c53aaf961f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59231095"
---
# <a name="icorprofilercallback2garbagecollectionfinished-method"></a><span data-ttu-id="3fd82-102">ICorProfilerCallback2::GarbageCollectionFinished, méthode</span><span class="sxs-lookup"><span data-stu-id="3fd82-102">ICorProfilerCallback2::GarbageCollectionFinished Method</span></span>
<span data-ttu-id="3fd82-103">Notifie le profileur que le garbage collection est terminée et que tous les rappels de garbage collection ont été publiés.</span><span class="sxs-lookup"><span data-stu-id="3fd82-103">Notifies the profiler that garbage collection has completed and all garbage collection callbacks have been issued for it.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3fd82-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3fd82-104">Syntax</span></span>  
  
```  
HRESULT GarbageCollectionFinished();  
```  
  
## <a name="remarks"></a><span data-ttu-id="3fd82-105">Notes</span><span class="sxs-lookup"><span data-stu-id="3fd82-105">Remarks</span></span>  
 <span data-ttu-id="3fd82-106">Il est possible que le profileur inspecter les objets dans leurs emplacements finaux lorsque la `GarbageCollectionFinished` méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="3fd82-106">It is safe for the profiler to inspect objects in their final locations when the `GarbageCollectionFinished` method is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3fd82-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3fd82-107">Requirements</span></span>  
 <span data-ttu-id="3fd82-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3fd82-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3fd82-109">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="3fd82-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="3fd82-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3fd82-110">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="3fd82-111">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="3fd82-111">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="3fd82-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3fd82-112">See also</span></span>

- [<span data-ttu-id="3fd82-113">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="3fd82-113">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="3fd82-114">ICorProfilerCallback2, interface</span><span class="sxs-lookup"><span data-stu-id="3fd82-114">ICorProfilerCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-interface.md)
