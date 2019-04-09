---
title: ICorProfilerCallback::RuntimeResumeStarted, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RuntimeResumeStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RuntimeResumeStarted
helpviewer_keywords:
- ICorProfilerCallback::RuntimeResumeStarted method [.NET Framework profiling]
- RuntimeResumeStarted method [.NET Framework profiling]
ms.assetid: 5854bfb2-c568-4f19-904a-7c9d41e7b995
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2b163d41280c8ea49554cecb845c4be757f55dfc
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59168088"
---
# <a name="icorprofilercallbackruntimeresumestarted-method"></a><span data-ttu-id="21437-102">ICorProfilerCallback::RuntimeResumeStarted, méthode</span><span class="sxs-lookup"><span data-stu-id="21437-102">ICorProfilerCallback::RuntimeResumeStarted Method</span></span>
<span data-ttu-id="21437-103">Notifie le profileur que le runtime reprend tous les threads d’exécution.</span><span class="sxs-lookup"><span data-stu-id="21437-103">Notifies the profiler that the runtime is resuming all run-time threads.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="21437-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21437-104">Syntax</span></span>  
  
```  
HRESULT RuntimeResumeStarted();  
```  
  
## <a name="requirements"></a><span data-ttu-id="21437-105">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21437-105">Requirements</span></span>  
 <span data-ttu-id="21437-106">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="21437-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="21437-107">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="21437-107">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="21437-108">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="21437-108">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="21437-109">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="21437-109">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="21437-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21437-110">See also</span></span>

- [<span data-ttu-id="21437-111">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="21437-111">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [<span data-ttu-id="21437-112">RuntimeResumeFinished, méthode</span><span class="sxs-lookup"><span data-stu-id="21437-112">RuntimeResumeFinished Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimeresumefinished-method.md)
