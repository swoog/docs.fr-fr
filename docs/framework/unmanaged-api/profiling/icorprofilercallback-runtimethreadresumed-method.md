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
ms.openlocfilehash: 810875d1b91265fe886ce3cd11970cad7fee122d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59228859"
---
# <a name="icorprofilercallbackruntimethreadresumed-method"></a><span data-ttu-id="f0097-102">ICorProfilerCallback::RuntimeThreadResumed, méthode</span><span class="sxs-lookup"><span data-stu-id="f0097-102">ICorProfilerCallback::RuntimeThreadResumed Method</span></span>
<span data-ttu-id="f0097-103">Notifie le profileur que le thread spécifié a repris après avoir été interrompue.</span><span class="sxs-lookup"><span data-stu-id="f0097-103">Notifies the profiler that the specified thread has resumed after being suspended.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f0097-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0097-104">Syntax</span></span>  
  
```  
HRESULT RuntimeThreadResumed(  
    [in] ThreadID threadId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f0097-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0097-105">Parameters</span></span>  
 `threadId`  
 <span data-ttu-id="f0097-106">[in] L’ID du thread qui a été repris.</span><span class="sxs-lookup"><span data-stu-id="f0097-106">[in] The ID of the thread that has been resumed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f0097-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0097-107">Requirements</span></span>  
 <span data-ttu-id="f0097-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f0097-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f0097-109">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="f0097-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="f0097-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f0097-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f0097-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f0097-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f0097-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0097-112">See also</span></span>

- [<span data-ttu-id="f0097-113">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="f0097-113">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="f0097-114">RuntimeThreadSuspended, méthode</span><span class="sxs-lookup"><span data-stu-id="f0097-114">RuntimeThreadSuspended Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimethreadsuspended-method.md)
