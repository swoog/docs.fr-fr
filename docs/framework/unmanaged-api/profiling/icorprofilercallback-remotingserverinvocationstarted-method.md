---
title: ICorProfilerCallback::RemotingServerInvocationStarted, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RemotingServerInvocationStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RemotingServerInvocationStarted
helpviewer_keywords:
- RemotingServerInvocationStarted method [.NET Framework profiling]
- ICorProfilerCallback::RemotingServerInvocationStarted method [.NET Framework profiling]
ms.assetid: 86051a11-ad8e-4ace-9a11-ff0f982a5e11
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 83c9a4aa165057f1345de2c6f5bda80e4317d06c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59221806"
---
# <a name="icorprofilercallbackremotingserverinvocationstarted-method"></a><span data-ttu-id="53284-102">ICorProfilerCallback::RemotingServerInvocationStarted, méthode</span><span class="sxs-lookup"><span data-stu-id="53284-102">ICorProfilerCallback::RemotingServerInvocationStarted Method</span></span>
<span data-ttu-id="53284-103">Notifie le profileur que le processus appelle une méthode en réponse à une demande d’appel de méthode distant.</span><span class="sxs-lookup"><span data-stu-id="53284-103">Notifies the profiler that the process is invoking a method in response to a remote method invocation request.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="53284-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53284-104">Syntax</span></span>  
  
```  
HRESULT RemotingServerInvocationStarted();  
```  
  
## <a name="requirements"></a><span data-ttu-id="53284-105">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53284-105">Requirements</span></span>  
 <span data-ttu-id="53284-106">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="53284-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="53284-107">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="53284-107">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="53284-108">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="53284-108">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="53284-109">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="53284-109">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="53284-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53284-110">See also</span></span>

- [<span data-ttu-id="53284-111">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="53284-111">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
