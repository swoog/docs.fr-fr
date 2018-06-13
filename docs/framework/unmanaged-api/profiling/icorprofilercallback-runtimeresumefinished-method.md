---
title: ICorProfilerCallback::RuntimeResumeFinished, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RuntimeResumeFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RuntimeResumeFinished
helpviewer_keywords:
- RuntimeResumeFinished method [.NET Framework profiling]
- ICorProfilerCallback::RuntimeResumeFinished method [.NET Framework profiling]
ms.assetid: 76de0494-dc49-426b-887d-bee98806a982
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f6b983db7da258fb94f941d01914ece0f7b1359f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33453305"
---
# <a name="icorprofilercallbackruntimeresumefinished-method"></a><span data-ttu-id="979d2-102">ICorProfilerCallback::RuntimeResumeFinished, méthode</span><span class="sxs-lookup"><span data-stu-id="979d2-102">ICorProfilerCallback::RuntimeResumeFinished Method</span></span>
<span data-ttu-id="979d2-103">Notifie le profileur que le runtime a repris tous les threads d’exécution et a retourné un fonctionnement normal.</span><span class="sxs-lookup"><span data-stu-id="979d2-103">Notifies the profiler that the runtime has resumed all runtime threads and has returned to normal operation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="979d2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="979d2-104">Syntax</span></span>  
  
```  
HRESULT RuntimeResumeFinished();  
```  
  
## <a name="remarks"></a><span data-ttu-id="979d2-105">Notes</span><span class="sxs-lookup"><span data-stu-id="979d2-105">Remarks</span></span>  
 <span data-ttu-id="979d2-106">Le `RuntimeResumeFinished` n’est pas garanti que le rappel se produisent sur le même thread que le [ICorProfilerCallback::RuntimeSuspendStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimesuspendstarted-method.md) rappel.</span><span class="sxs-lookup"><span data-stu-id="979d2-106">The `RuntimeResumeFinished` callback is not guaranteed to occur on the same thread as the [ICorProfilerCallback::RuntimeSuspendStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimesuspendstarted-method.md) callback.</span></span> <span data-ttu-id="979d2-107">Toutefois, il correspond systématiquement à se produire sur le même thread que le [ICorProfilerCallback::RuntimeResumeStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimeresumestarted-method.md) rappel.</span><span class="sxs-lookup"><span data-stu-id="979d2-107">However, it is guaranteed to occur on the same thread as the [ICorProfilerCallback::RuntimeResumeStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimeresumestarted-method.md) callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="979d2-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="979d2-108">Requirements</span></span>  
 <span data-ttu-id="979d2-109">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="979d2-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="979d2-110">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="979d2-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="979d2-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="979d2-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="979d2-112">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="979d2-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="979d2-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="979d2-113">See Also</span></span>  
 [<span data-ttu-id="979d2-114">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="979d2-114">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
