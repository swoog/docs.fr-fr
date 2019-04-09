---
title: ICorProfilerCallback::RemotingServerInvocationReturned, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RemotingServerInvocationReturned
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RemotingServerInvocationReturned
helpviewer_keywords:
- ICorProfilerCallback::RemotingServerInvocationReturned method [.NET Framework profiling]
- RemotingServerInvocationReturned method [.NET Framework profiling]
ms.assetid: a4de6805-e159-4280-99e5-3390c86166d0
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 00f5fd44d340a76200537871a9860f67601b66d9
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59208707"
---
# <a name="icorprofilercallbackremotingserverinvocationreturned-method"></a><span data-ttu-id="40418-102">ICorProfilerCallback::RemotingServerInvocationReturned, méthode</span><span class="sxs-lookup"><span data-stu-id="40418-102">ICorProfilerCallback::RemotingServerInvocationReturned Method</span></span>
<span data-ttu-id="40418-103">Notifie le profileur que le processus a fini d’appeler une méthode en réponse à une demande d’appel de méthode distant.</span><span class="sxs-lookup"><span data-stu-id="40418-103">Notifies the profiler that the process has finished invoking a method in response to a remote method invocation request.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="40418-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40418-104">Syntax</span></span>  
  
```  
HRESULT RemotingServerInvocationReturned();  
```  
  
## <a name="requirements"></a><span data-ttu-id="40418-105">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40418-105">Requirements</span></span>  
 <span data-ttu-id="40418-106">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="40418-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="40418-107">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="40418-107">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="40418-108">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="40418-108">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="40418-109">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="40418-109">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="40418-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40418-110">See also</span></span>

- [<span data-ttu-id="40418-111">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="40418-111">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
