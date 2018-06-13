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
ms.openlocfilehash: cc63a0a42c1da11daa5d38ecce505296a893616b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33453933"
---
# <a name="icorprofilercallback3-interface"></a><span data-ttu-id="02860-102">ICorProfilerCallback3, interface</span><span class="sxs-lookup"><span data-stu-id="02860-102">ICorProfilerCallback3 Interface</span></span>
<span data-ttu-id="02860-103">Fournit des méthodes de rappel que le common language runtime (CLR) utilise pour communiquer attachement et détachement des informations d’état au profileur.</span><span class="sxs-lookup"><span data-stu-id="02860-103">Provides callback methods that the common language runtime (CLR) uses to communicate attach and detach state information to the profiler.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="02860-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="02860-104">Methods</span></span>  
  
|<span data-ttu-id="02860-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="02860-105">Method</span></span>|<span data-ttu-id="02860-106">Description</span><span class="sxs-lookup"><span data-stu-id="02860-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="02860-107">InitializeForAttach, méthode</span><span class="sxs-lookup"><span data-stu-id="02860-107">InitializeForAttach Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback3-initializeforattach-method.md)|<span data-ttu-id="02860-108">Appelée par le CLR pour permettre au profileur d’initialiser son état après une opération d’attachement.</span><span class="sxs-lookup"><span data-stu-id="02860-108">Called by the CLR to give the profiler an opportunity to initialize its state after an attach operation.</span></span>|  
|[<span data-ttu-id="02860-109">ProfilerAttachComplete, méthode</span><span class="sxs-lookup"><span data-stu-id="02860-109">ProfilerAttachComplete Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback3-profilerattachcomplete-method.md)|<span data-ttu-id="02860-110">Appelée par le CLR pour indiquer que le profileur peut appeler désormais les méthodes de rattrapage.</span><span class="sxs-lookup"><span data-stu-id="02860-110">Called by the CLR to indicate that the profiler can now call the catch-up methods.</span></span>|  
|[<span data-ttu-id="02860-111">ProfilerDetachSucceeded, méthode</span><span class="sxs-lookup"><span data-stu-id="02860-111">ProfilerDetachSucceeded Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback3-profilerdetachsucceeded-method.md)|<span data-ttu-id="02860-112">Indique au profileur que le Common Language Runtime (CLR) est sur le point de décharger sa DLL.</span><span class="sxs-lookup"><span data-stu-id="02860-112">Notifies the profiler that the common language runtime (CLR) is about to unload the profiler DLL.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="02860-113">Notes</span><span class="sxs-lookup"><span data-stu-id="02860-113">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="02860-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="02860-114">Requirements</span></span>  
 <span data-ttu-id="02860-115">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="02860-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="02860-116">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="02860-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="02860-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="02860-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="02860-118">**Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="02860-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="02860-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02860-119">See Also</span></span>  
 [<span data-ttu-id="02860-120">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="02860-120">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)  
 [<span data-ttu-id="02860-121">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="02860-121">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)  
 [<span data-ttu-id="02860-122">ICorProfilerCallback2, interface</span><span class="sxs-lookup"><span data-stu-id="02860-122">ICorProfilerCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-interface.md)  
 [<span data-ttu-id="02860-123">ICorProfilerCallback4, interface</span><span class="sxs-lookup"><span data-stu-id="02860-123">ICorProfilerCallback4 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-interface.md)
