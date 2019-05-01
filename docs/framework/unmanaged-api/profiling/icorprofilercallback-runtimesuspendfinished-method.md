---
title: ICorProfilerCallback::RuntimeSuspendFinished, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RuntimeSuspendFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RuntimeSuspendFinished
helpviewer_keywords:
- ICorProfilerCallback::RuntimeSuspendFinished method [.NET Framework profiling]
- RuntimeSuspendFinished method [.NET Framework profiling]
ms.assetid: b7723f58-c55c-4399-9972-1bbf3b866694
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 07e2ebe8afe6002dee6c45f56fa1f11a4083d6bb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61992132"
---
# <a name="icorprofilercallbackruntimesuspendfinished-method"></a><span data-ttu-id="09561-102">ICorProfilerCallback::RuntimeSuspendFinished, méthode</span><span class="sxs-lookup"><span data-stu-id="09561-102">ICorProfilerCallback::RuntimeSuspendFinished Method</span></span>
<span data-ttu-id="09561-103">Notifie le profileur que le runtime a fini de suspendre tous les threads d’exécution.</span><span class="sxs-lookup"><span data-stu-id="09561-103">Notifies the profiler that the runtime has completed suspension of all runtime threads.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="09561-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09561-104">Syntax</span></span>  
  
```  
HRESULT RuntimeSuspendFinished();  
```  
  
## <a name="remarks"></a><span data-ttu-id="09561-105">Notes</span><span class="sxs-lookup"><span data-stu-id="09561-105">Remarks</span></span>  
 <span data-ttu-id="09561-106">Tous les threads de runtime qui se trouvent dans le code non managé sont autorisés à continuer à s’exécuter jusqu'à ce qu’ils essaient d’entrer à nouveau le runtime.</span><span class="sxs-lookup"><span data-stu-id="09561-106">All runtime threads that are in unmanaged code are allowed to continue running until they try to re-enter the runtime.</span></span> <span data-ttu-id="09561-107">À ce stade qu’ils seront aussi suspendues jusqu'à ce que le runtime reprend.</span><span class="sxs-lookup"><span data-stu-id="09561-107">At that point they will also be suspended until the runtime resumes.</span></span> <span data-ttu-id="09561-108">Cela s’applique également aux nouveaux threads qui entrent dans le runtime.</span><span class="sxs-lookup"><span data-stu-id="09561-108">This also applies to new threads that enter the runtime.</span></span> <span data-ttu-id="09561-109">Tous les threads dans le runtime sont qu'immédiatement suspendus s’ils sont déjà dans du code interruptible, ou ils sont invités à s’interrompre lorsqu’ils atteignent du code interruptible.</span><span class="sxs-lookup"><span data-stu-id="09561-109">All threads in the runtime are either suspended immediately if they are already in interruptible code, or they are asked to suspend when they reach interruptible code.</span></span>  
  
 <span data-ttu-id="09561-110">Le `RuntimeSuspendFinished` rappel est assuré de se produire sur le même thread que le [ICorProfilerCallback::RuntimeSuspendStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimesuspendstarted-method.md) rappel.</span><span class="sxs-lookup"><span data-stu-id="09561-110">The `RuntimeSuspendFinished` callback is guaranteed to occur on the same thread as the [ICorProfilerCallback::RuntimeSuspendStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimesuspendstarted-method.md) callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="09561-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09561-111">Requirements</span></span>  
 <span data-ttu-id="09561-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="09561-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="09561-113">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="09561-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="09561-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="09561-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="09561-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="09561-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="09561-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09561-116">See also</span></span>

- [<span data-ttu-id="09561-117">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="09561-117">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="09561-118">RuntimeSuspendAborted, méthode</span><span class="sxs-lookup"><span data-stu-id="09561-118">RuntimeSuspendAborted Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimesuspendaborted-method.md)
