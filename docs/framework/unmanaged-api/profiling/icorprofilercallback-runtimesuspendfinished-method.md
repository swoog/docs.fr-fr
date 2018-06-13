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
ms.openlocfilehash: 0b243c507171a4d907ef4594ae0c715a074c965a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33452216"
---
# <a name="icorprofilercallbackruntimesuspendfinished-method"></a><span data-ttu-id="22a2b-102">ICorProfilerCallback::RuntimeSuspendFinished, méthode</span><span class="sxs-lookup"><span data-stu-id="22a2b-102">ICorProfilerCallback::RuntimeSuspendFinished Method</span></span>
<span data-ttu-id="22a2b-103">Notifie le profileur que le runtime a fini de suspendre tous les threads d’exécution.</span><span class="sxs-lookup"><span data-stu-id="22a2b-103">Notifies the profiler that the runtime has completed suspension of all runtime threads.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="22a2b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22a2b-104">Syntax</span></span>  
  
```  
HRESULT RuntimeSuspendFinished();  
```  
  
## <a name="remarks"></a><span data-ttu-id="22a2b-105">Notes</span><span class="sxs-lookup"><span data-stu-id="22a2b-105">Remarks</span></span>  
 <span data-ttu-id="22a2b-106">Tous les threads d’exécution qui se trouvent dans le code non managé peuvent continuer à s’exécuter jusqu'à ce qu’ils essaient d’entrer à nouveau le runtime.</span><span class="sxs-lookup"><span data-stu-id="22a2b-106">All runtime threads that are in unmanaged code are allowed to continue running until they try to re-enter the runtime.</span></span> <span data-ttu-id="22a2b-107">À ce stade qu’ils seront également suspendus jusqu'à la reprise du runtime.</span><span class="sxs-lookup"><span data-stu-id="22a2b-107">At that point they will also be suspended until the runtime resumes.</span></span> <span data-ttu-id="22a2b-108">Cela s’applique également aux nouveaux threads qui entrent dans le runtime.</span><span class="sxs-lookup"><span data-stu-id="22a2b-108">This also applies to new threads that enter the runtime.</span></span> <span data-ttu-id="22a2b-109">Tous les threads dans le runtime sont qu'immédiatement suspendus s’ils sont déjà dans du code interruptible, ou ils sont invités à s’interrompre lorsqu’ils atteignent du code interruptible.</span><span class="sxs-lookup"><span data-stu-id="22a2b-109">All threads in the runtime are either suspended immediately if they are already in interruptible code, or they are asked to suspend when they reach interruptible code.</span></span>  
  
 <span data-ttu-id="22a2b-110">Le `RuntimeSuspendFinished` rappel est assuré de se produire sur le même thread que le [ICorProfilerCallback::RuntimeSuspendStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimesuspendstarted-method.md) rappel.</span><span class="sxs-lookup"><span data-stu-id="22a2b-110">The `RuntimeSuspendFinished` callback is guaranteed to occur on the same thread as the [ICorProfilerCallback::RuntimeSuspendStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimesuspendstarted-method.md) callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="22a2b-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="22a2b-111">Requirements</span></span>  
 <span data-ttu-id="22a2b-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="22a2b-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="22a2b-113">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="22a2b-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="22a2b-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="22a2b-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="22a2b-115">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="22a2b-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="22a2b-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22a2b-116">See Also</span></span>  
 [<span data-ttu-id="22a2b-117">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="22a2b-117">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="22a2b-118">RuntimeSuspendAborted, méthode</span><span class="sxs-lookup"><span data-stu-id="22a2b-118">RuntimeSuspendAborted Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimesuspendaborted-method.md)
