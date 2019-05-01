---
title: ICorProfilerCallback::ThreadDestroyed, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ThreadDestroyed
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ThreadDestroyed
helpviewer_keywords:
- ThreadDestroyed method [.NET Framework profiling]
- ICorProfilerCallback::ThreadDestroyed method [.NET Framework profiling]
ms.assetid: 4c2b66fd-0595-40a3-8931-f9c4fff97ac8
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d4c45290b1ef4360e51b5ed8e1b0fac3dcdde727
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62041624"
---
# <a name="icorprofilercallbackthreaddestroyed-method"></a><span data-ttu-id="a8c33-102">ICorProfilerCallback::ThreadDestroyed, méthode</span><span class="sxs-lookup"><span data-stu-id="a8c33-102">ICorProfilerCallback::ThreadDestroyed Method</span></span>
<span data-ttu-id="a8c33-103">Informe le profileur qu’un thread a été détruit.</span><span class="sxs-lookup"><span data-stu-id="a8c33-103">Notifies the profiler that a thread has been destroyed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a8c33-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8c33-104">Syntax</span></span>  
  
```  
HRESULT ThreadDestroyed(  
    [in] ThreadID threadId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a8c33-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8c33-105">Parameters</span></span>  
 `threadId`  
 <span data-ttu-id="a8c33-106">[in] L’ID du thread qui a été détruite.</span><span class="sxs-lookup"><span data-stu-id="a8c33-106">[in] The ID of the thread that has been destroyed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a8c33-107">Notes</span><span class="sxs-lookup"><span data-stu-id="a8c33-107">Remarks</span></span>  
 <span data-ttu-id="a8c33-108">Le `threadId` valeur n’est plus valide au moment de cet appel.</span><span class="sxs-lookup"><span data-stu-id="a8c33-108">The `threadId` value is no longer valid at the time of this call.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a8c33-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8c33-109">Requirements</span></span>  
 <span data-ttu-id="a8c33-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a8c33-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a8c33-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="a8c33-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="a8c33-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a8c33-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a8c33-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a8c33-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a8c33-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8c33-114">See also</span></span>

- [<span data-ttu-id="a8c33-115">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="a8c33-115">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="a8c33-116">ThreadCreated, méthode</span><span class="sxs-lookup"><span data-stu-id="a8c33-116">ThreadCreated Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-threadcreated-method.md)
