---
title: ICorProfilerCallback::ThreadAssignedToOSThread, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ThreadAssignedToOSThread
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ThreadAssignedToOSThread
helpviewer_keywords:
- ThreadAssignedToOSThread method [.NET Framework profiling]
- ICorProfilerCallback::ThreadAssignedToOSThread method [.NET Framework profiling]
ms.assetid: f9671e5a-7b14-4f5b-8404-58136422c8b2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: eefcd4436a28fdf52cbe55da5d4bb7eea4449463
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59158455"
---
# <a name="icorprofilercallbackthreadassignedtoosthread-method"></a><span data-ttu-id="dd2e1-102">ICorProfilerCallback::ThreadAssignedToOSThread, méthode</span><span class="sxs-lookup"><span data-stu-id="dd2e1-102">ICorProfilerCallback::ThreadAssignedToOSThread Method</span></span>
<span data-ttu-id="dd2e1-103">Notifie le profileur qu’un thread managé est implémenté à l’aide d’un thread de système d’exploitation particulier.</span><span class="sxs-lookup"><span data-stu-id="dd2e1-103">Notifies the profiler that a managed thread is being implemented using a particular operating system thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dd2e1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd2e1-104">Syntax</span></span>  
  
```  
HRESULT ThreadAssignedToOSThread(  
    [in] ThreadID managedThreadId,  
    [in] DWORD    osThreadId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="dd2e1-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd2e1-105">Parameters</span></span>  
 `managedThreadId`  
 <span data-ttu-id="dd2e1-106">[in] L’identificateur du thread managé.</span><span class="sxs-lookup"><span data-stu-id="dd2e1-106">[in] The identifier of the managed thread.</span></span>  
  
 `osThreadId`  
 <span data-ttu-id="dd2e1-107">[in] L’identificateur du thread de système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="dd2e1-107">[in] The identifier of the operating system thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dd2e1-108">Notes</span><span class="sxs-lookup"><span data-stu-id="dd2e1-108">Remarks</span></span>  
 <span data-ttu-id="dd2e1-109">Le `ThreadAssignedToOSThread` rappel existe afin que le profileur peut assurer un mappage précis entre les fibres de threads de système d’exploitation et les threads managés.</span><span class="sxs-lookup"><span data-stu-id="dd2e1-109">The `ThreadAssignedToOSThread` callback exists so that the profiler can maintain an accurate mapping across fibers of operating system threads to managed threads.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dd2e1-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd2e1-110">Requirements</span></span>  
 <span data-ttu-id="dd2e1-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="dd2e1-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dd2e1-112">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="dd2e1-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="dd2e1-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="dd2e1-113">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="dd2e1-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="dd2e1-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="dd2e1-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd2e1-115">See also</span></span>

- [<span data-ttu-id="dd2e1-116">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="dd2e1-116">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
