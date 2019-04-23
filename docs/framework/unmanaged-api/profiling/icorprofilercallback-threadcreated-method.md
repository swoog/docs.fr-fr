---
title: ICorProfilerCallback::ThreadCreated, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ThreadCreated
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ThreadCreated
helpviewer_keywords:
- ICorProfilerCallback::ThreadCreated method [.NET Framework profiling]
- ThreadCreated method [.NET Framework profiling]
ms.assetid: cca0f799-09b8-4689-a33c-6d6537943a9b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5f8eca3e8eb755e31e704e557ae614a6e5c1f534
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59107768"
---
# <a name="icorprofilercallbackthreadcreated-method"></a><span data-ttu-id="8625c-102">ICorProfilerCallback::ThreadCreated, méthode</span><span class="sxs-lookup"><span data-stu-id="8625c-102">ICorProfilerCallback::ThreadCreated Method</span></span>
<span data-ttu-id="8625c-103">Informe le profileur qu’un thread a été créé.</span><span class="sxs-lookup"><span data-stu-id="8625c-103">Notifies the profiler that a thread has been created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8625c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8625c-104">Syntax</span></span>  
  
```  
HRESULT ThreadCreated(  
    [in] ThreadID threadId);   
```  
  
## <a name="parameters"></a><span data-ttu-id="8625c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8625c-105">Parameters</span></span>  
 `threadId`  
 <span data-ttu-id="8625c-106">[in] L’ID du thread qui a été créé.</span><span class="sxs-lookup"><span data-stu-id="8625c-106">[in] The ID of the thread that has been created.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8625c-107">Notes</span><span class="sxs-lookup"><span data-stu-id="8625c-107">Remarks</span></span>  
 <span data-ttu-id="8625c-108">Le `threadId` valeur est immédiatement valide.</span><span class="sxs-lookup"><span data-stu-id="8625c-108">The `threadId` value is immediately valid.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8625c-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8625c-109">Requirements</span></span>  
 <span data-ttu-id="8625c-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8625c-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8625c-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="8625c-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="8625c-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8625c-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8625c-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8625c-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8625c-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8625c-114">See also</span></span>

- [<span data-ttu-id="8625c-115">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="8625c-115">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="8625c-116">ThreadDestroyed, méthode</span><span class="sxs-lookup"><span data-stu-id="8625c-116">ThreadDestroyed Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-threaddestroyed-method.md)
