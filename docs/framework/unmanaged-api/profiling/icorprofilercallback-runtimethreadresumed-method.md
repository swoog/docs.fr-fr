---
title: ICorProfilerCallback::RuntimeThreadResumed, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RuntimeThreadResumed
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RuntimeThreadResumed
helpviewer_keywords:
- ICorProfilerCallback::RuntimeThreadResumed method [.NET Framework profiling]
- RuntimeThreadResumed method [.NET Framework profiling]
ms.assetid: da984f89-4f53-4ab0-ae6f-3e2ee6085994
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4f971c5175307c1e1df6890c136b306860e54d23
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33452707"
---
# <a name="icorprofilercallbackruntimethreadresumed-method"></a><span data-ttu-id="6ff56-102">ICorProfilerCallback::RuntimeThreadResumed, méthode</span><span class="sxs-lookup"><span data-stu-id="6ff56-102">ICorProfilerCallback::RuntimeThreadResumed Method</span></span>
<span data-ttu-id="6ff56-103">Notifie le profileur que le thread spécifié a repris après avoir été interrompue.</span><span class="sxs-lookup"><span data-stu-id="6ff56-103">Notifies the profiler that the specified thread has resumed after being suspended.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6ff56-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ff56-104">Syntax</span></span>  
  
```  
HRESULT RuntimeThreadResumed(  
    [in] ThreadID threadId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6ff56-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ff56-105">Parameters</span></span>  
 `threadId`  
 <span data-ttu-id="6ff56-106">[in] L’ID du thread qui a été repris.</span><span class="sxs-lookup"><span data-stu-id="6ff56-106">[in] The ID of the thread that has been resumed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6ff56-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6ff56-107">Requirements</span></span>  
 <span data-ttu-id="6ff56-108">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6ff56-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6ff56-109">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="6ff56-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="6ff56-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6ff56-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6ff56-111">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6ff56-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6ff56-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ff56-112">See Also</span></span>  
 [<span data-ttu-id="6ff56-113">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="6ff56-113">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="6ff56-114">RuntimeThreadSuspended, méthode</span><span class="sxs-lookup"><span data-stu-id="6ff56-114">RuntimeThreadSuspended Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimethreadsuspended-method.md)
