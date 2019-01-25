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
ms.openlocfilehash: 40bbde940538d7b06aa74ab55986da2dca3ec225
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54599502"
---
# <a name="icorprofilercallbackthreaddestroyed-method"></a><span data-ttu-id="879b0-102">ICorProfilerCallback::ThreadDestroyed, méthode</span><span class="sxs-lookup"><span data-stu-id="879b0-102">ICorProfilerCallback::ThreadDestroyed Method</span></span>
<span data-ttu-id="879b0-103">Informe le profileur qu’un thread a été détruit.</span><span class="sxs-lookup"><span data-stu-id="879b0-103">Notifies the profiler that a thread has been destroyed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="879b0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="879b0-104">Syntax</span></span>  
  
```  
HRESULT ThreadDestroyed(  
    [in] ThreadID threadId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="879b0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="879b0-105">Parameters</span></span>  
 `threadId`  
 <span data-ttu-id="879b0-106">[in] L’ID du thread qui a été détruite.</span><span class="sxs-lookup"><span data-stu-id="879b0-106">[in] The ID of the thread that has been destroyed.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="879b0-107">Notes</span><span class="sxs-lookup"><span data-stu-id="879b0-107">Remarks</span></span>  
 <span data-ttu-id="879b0-108">Le `threadId` valeur n’est plus valide au moment de cet appel.</span><span class="sxs-lookup"><span data-stu-id="879b0-108">The `threadId` value is no longer valid at the time of this call.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="879b0-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="879b0-109">Requirements</span></span>  
 <span data-ttu-id="879b0-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="879b0-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="879b0-111">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="879b0-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="879b0-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="879b0-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="879b0-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="879b0-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="879b0-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="879b0-114">See also</span></span>
- [<span data-ttu-id="879b0-115">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="879b0-115">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="879b0-116">ThreadCreated, méthode</span><span class="sxs-lookup"><span data-stu-id="879b0-116">ThreadCreated Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-threadcreated-method.md)
