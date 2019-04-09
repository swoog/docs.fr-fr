---
title: ICorProfilerCallback3, interface
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback3
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback3
helpviewer_keywords:
- ICorProfilerCallback3 interface [.NET Framework profiling]
ms.assetid: be83af41-3dec-4c77-8529-9dd6b8042af6
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 66e6a67ce022365fa8c9e1005dfecbe4b23abd10
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59158378"
---
# <a name="icorprofilercallback3-interface"></a><span data-ttu-id="0cc96-102">ICorProfilerCallback3, interface</span><span class="sxs-lookup"><span data-stu-id="0cc96-102">ICorProfilerCallback3 Interface</span></span>
<span data-ttu-id="0cc96-103">Fournit des méthodes de rappel que le common language runtime (CLR) utilise pour communiquer attachement et détachement des informations d’état au profileur.</span><span class="sxs-lookup"><span data-stu-id="0cc96-103">Provides callback methods that the common language runtime (CLR) uses to communicate attach and detach state information to the profiler.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="0cc96-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0cc96-104">Methods</span></span>  
  
|<span data-ttu-id="0cc96-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="0cc96-105">Method</span></span>|<span data-ttu-id="0cc96-106">Description</span><span class="sxs-lookup"><span data-stu-id="0cc96-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="0cc96-107">InitializeForAttach, méthode</span><span class="sxs-lookup"><span data-stu-id="0cc96-107">InitializeForAttach Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback3-initializeforattach-method.md)|<span data-ttu-id="0cc96-108">Appelé par le CLR pour permettre au profileur d’initialiser son état après une opération d’attachement.</span><span class="sxs-lookup"><span data-stu-id="0cc96-108">Called by the CLR to give the profiler an opportunity to initialize its state after an attach operation.</span></span>|  
|[<span data-ttu-id="0cc96-109">ProfilerAttachComplete, méthode</span><span class="sxs-lookup"><span data-stu-id="0cc96-109">ProfilerAttachComplete Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback3-profilerattachcomplete-method.md)|<span data-ttu-id="0cc96-110">Appelé par le CLR pour indiquer que le profileur peut maintenant appeler les méthodes de rattrapage.</span><span class="sxs-lookup"><span data-stu-id="0cc96-110">Called by the CLR to indicate that the profiler can now call the catch-up methods.</span></span>|  
|[<span data-ttu-id="0cc96-111">ProfilerDetachSucceeded, méthode</span><span class="sxs-lookup"><span data-stu-id="0cc96-111">ProfilerDetachSucceeded Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback3-profilerdetachsucceeded-method.md)|<span data-ttu-id="0cc96-112">Indique au profileur que le Common Language Runtime (CLR) est sur le point de décharger sa DLL.</span><span class="sxs-lookup"><span data-stu-id="0cc96-112">Notifies the profiler that the common language runtime (CLR) is about to unload the profiler DLL.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0cc96-113">Notes</span><span class="sxs-lookup"><span data-stu-id="0cc96-113">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0cc96-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0cc96-114">Requirements</span></span>  
 <span data-ttu-id="0cc96-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0cc96-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0cc96-116">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="0cc96-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="0cc96-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0cc96-117">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="0cc96-118">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="0cc96-118">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="0cc96-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0cc96-119">See also</span></span>

- [<span data-ttu-id="0cc96-120">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="0cc96-120">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [<span data-ttu-id="0cc96-121">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="0cc96-121">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
- [<span data-ttu-id="0cc96-122">ICorProfilerCallback2, interface</span><span class="sxs-lookup"><span data-stu-id="0cc96-122">ICorProfilerCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-interface.md)
- [<span data-ttu-id="0cc96-123">ICorProfilerCallback4, interface</span><span class="sxs-lookup"><span data-stu-id="0cc96-123">ICorProfilerCallback4 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-interface.md)
