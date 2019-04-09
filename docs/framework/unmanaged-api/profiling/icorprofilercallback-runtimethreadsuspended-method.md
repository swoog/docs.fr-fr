---
title: ICorProfilerCallback::RuntimeThreadSuspended, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RuntimeThreadSuspended
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RuntimeThreadSuspended
helpviewer_keywords:
- RuntimeThreadSuspended method [.NET Framework profiling]
- ICorProfilerCallback::RuntimeThreadSuspended method [.NET Framework profiling]
ms.assetid: de830a8b-6ee1-4900-ace3-4237108f6b12
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a0748802599926f4ec218362e6f7d086aab2d8f9
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59080226"
---
# <a name="icorprofilercallbackruntimethreadsuspended-method"></a><span data-ttu-id="b1963-102">ICorProfilerCallback::RuntimeThreadSuspended, méthode</span><span class="sxs-lookup"><span data-stu-id="b1963-102">ICorProfilerCallback::RuntimeThreadSuspended Method</span></span>
<span data-ttu-id="b1963-103">Notifie le profileur que le thread spécifié a été suspendu ou qu’il doit être interrompu.</span><span class="sxs-lookup"><span data-stu-id="b1963-103">Notifies the profiler that the specified thread has been suspended or is about to be suspended.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b1963-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1963-104">Syntax</span></span>  
  
```  
HRESULT RuntimeThreadSuspended(  
    [in] ThreadID threadId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b1963-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1963-105">Parameters</span></span>  
 `threadId`  
 <span data-ttu-id="b1963-106">[in] L’ID du thread qui a été suspendu.</span><span class="sxs-lookup"><span data-stu-id="b1963-106">[in] The ID of the thread that has been suspended.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b1963-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b1963-107">Remarks</span></span>  
 <span data-ttu-id="b1963-108">Le `RuntimeThreadSuspended` notification peut se produire à tout moment entre le [ICorProfilerCallback::RuntimeSuspendStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimesuspendstarted-method.md) et associé [ICorProfilerCallback::RuntimeResumeStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimeresumestarted-method.md) rappels.</span><span class="sxs-lookup"><span data-stu-id="b1963-108">The `RuntimeThreadSuspended` notification can occur any time between the [ICorProfilerCallback::RuntimeSuspendStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimesuspendstarted-method.md) and the associated [ICorProfilerCallback::RuntimeResumeStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimeresumestarted-method.md) callbacks.</span></span> <span data-ttu-id="b1963-109">Les notifications qui se produisent entre [ICorProfilerCallback::RuntimeSuspendFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimesuspendfinished-method.md) et `RuntimeResumeStarted` concernent les threads qui étaient exécutés dans du code non managé et ont été suspendus lors de l’entrée à l’exécution.</span><span class="sxs-lookup"><span data-stu-id="b1963-109">Notifications that occur between [ICorProfilerCallback::RuntimeSuspendFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimesuspendfinished-method.md) and `RuntimeResumeStarted` are for threads that had been running in unmanaged code and were suspended upon entry to the runtime.</span></span>  
  
 <span data-ttu-id="b1963-110">En règle générale, ce rappel se produit juste après qu’un thread est suspendu.</span><span class="sxs-lookup"><span data-stu-id="b1963-110">Generally, this callback occurs just after a thread is suspended.</span></span> <span data-ttu-id="b1963-111">Toutefois, si le thread en cours d’exécution (le thread qui a appelé ce rappel) est celui qui est suspendu, ce rappel se produit juste avant que le thread est suspendu.</span><span class="sxs-lookup"><span data-stu-id="b1963-111">However, if the currently executing thread (the thread that called this callback) is the one that is being suspended, this callback will occur just before the thread is suspended.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b1963-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1963-112">Requirements</span></span>  
 <span data-ttu-id="b1963-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b1963-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b1963-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="b1963-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="b1963-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b1963-115">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="b1963-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="b1963-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="b1963-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1963-117">See also</span></span>

- [<span data-ttu-id="b1963-118">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="b1963-118">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="b1963-119">RuntimeThreadResumed, méthode</span><span class="sxs-lookup"><span data-stu-id="b1963-119">RuntimeThreadResumed Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimethreadresumed-method.md)
