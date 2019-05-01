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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61992145"
---
# <a name="icorprofilercallbackremotingserverinvocationstarted-method"></a><span data-ttu-id="f5d4f-102">ICorProfilerCallback::RemotingServerInvocationStarted, méthode</span><span class="sxs-lookup"><span data-stu-id="f5d4f-102">ICorProfilerCallback::RemotingServerInvocationStarted Method</span></span>
<span data-ttu-id="f5d4f-103">Notifie le profileur que le processus appelle une méthode en réponse à une demande d’appel de méthode distant.</span><span class="sxs-lookup"><span data-stu-id="f5d4f-103">Notifies the profiler that the process is invoking a method in response to a remote method invocation request.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f5d4f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5d4f-104">Syntax</span></span>  
  
```  
HRESULT RemotingServerInvocationStarted();  
```  
  
## <a name="requirements"></a><span data-ttu-id="f5d4f-105">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5d4f-105">Requirements</span></span>  
 <span data-ttu-id="f5d4f-106">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f5d4f-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f5d4f-107">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="f5d4f-107">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="f5d4f-108">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f5d4f-108">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f5d4f-109">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f5d4f-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f5d4f-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5d4f-110">See also</span></span>

- [<span data-ttu-id="f5d4f-111">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="f5d4f-111">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
