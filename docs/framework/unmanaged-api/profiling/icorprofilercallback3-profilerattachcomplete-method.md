---
title: ICorProfilerCallback3::ProfilerAttachComplete, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback3.ProfilerAttachComplete Method
api_location:
- Mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback3::ProfilerAttachComplete
helpviewer_keywords:
- ProfilerAttachComplete method [.NET Framework profiling]
- ICorProfilerCallback3::ProfilerAttachComplete method [.NET Framework profiling]
ms.assetid: 257d6076-06e0-4d93-bb33-651fbb2b92d7
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6a181ca2da8385107d63cd94ea832846c4211ad5
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64650382"
---
# <a name="icorprofilercallback3profilerattachcomplete-method"></a><span data-ttu-id="b7bba-102">ICorProfilerCallback3::ProfilerAttachComplete, méthode</span><span class="sxs-lookup"><span data-stu-id="b7bba-102">ICorProfilerCallback3::ProfilerAttachComplete Method</span></span>
<span data-ttu-id="b7bba-103">Appelé par le common language runtime (CLR) pour indiquer que le profileur peut maintenant appeler le [ICorProfilerInfo3::EnumJITedFunctions](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-enumjitedfunctions-method.md) et [ICorProfilerInfo3::EnumModules](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-enummodules-method.md) méthodes de rattrapage.</span><span class="sxs-lookup"><span data-stu-id="b7bba-103">Called by the common language runtime (CLR) to indicate that the profiler can now call the [ICorProfilerInfo3::EnumJITedFunctions](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-enumjitedfunctions-method.md) and [ICorProfilerInfo3::EnumModules](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-enummodules-method.md) catch-up methods.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b7bba-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7bba-104">Syntax</span></span>  
  
```  
HRESULT ProfilerAttachComplete ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="b7bba-105">Notes</span><span class="sxs-lookup"><span data-stu-id="b7bba-105">Remarks</span></span>  
 <span data-ttu-id="b7bba-106">Le `ProfilerAttachComplete` rappel est émis après la [ICorProfilerCallback3::InitializeForAttach](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback3-initializeforattach-method.md) méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="b7bba-106">The `ProfilerAttachComplete` callback is issued after the [ICorProfilerCallback3::InitializeForAttach](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback3-initializeforattach-method.md) method is called.</span></span> <span data-ttu-id="b7bba-107">Il indique ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="b7bba-107">It indicates the following:</span></span>  
  
- <span data-ttu-id="b7bba-108">Les rappels demandés par le profileur dans `InitializeForAttach` ont été activés.</span><span class="sxs-lookup"><span data-stu-id="b7bba-108">The callbacks that were requested by the profiler in `InitializeForAttach` have been activated.</span></span>  
  
- <span data-ttu-id="b7bba-109">Le profileur peut désormais exécuter un rattrapage sur les ID associés sans risquer de manquer des notifications.</span><span class="sxs-lookup"><span data-stu-id="b7bba-109">The profiler can now perform catch-up on the associated IDs without being concerned about missing notifications.</span></span>  
  
 <span data-ttu-id="b7bba-110">Le CLR ignore la valeur de retour de ce rappel.</span><span class="sxs-lookup"><span data-stu-id="b7bba-110">The CLR ignores the return value from this callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b7bba-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7bba-111">Requirements</span></span>  
 <span data-ttu-id="b7bba-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b7bba-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b7bba-113">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="b7bba-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="b7bba-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b7bba-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b7bba-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b7bba-115">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b7bba-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7bba-116">See also</span></span>

- [<span data-ttu-id="b7bba-117">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="b7bba-117">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="b7bba-118">ICorProfilerInfo3, interface</span><span class="sxs-lookup"><span data-stu-id="b7bba-118">ICorProfilerInfo3 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-interface.md)
- [<span data-ttu-id="b7bba-119">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="b7bba-119">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [<span data-ttu-id="b7bba-120">Profilage</span><span class="sxs-lookup"><span data-stu-id="b7bba-120">Profiling</span></span>](../../../../docs/framework/unmanaged-api/profiling/index.md)
