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
ms.openlocfilehash: b3f32b9ab9b4e29dd101729dc43cde03985f5994
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33451222"
---
# <a name="icorprofilercallbackremotingserverinvocationreturned-method"></a><span data-ttu-id="d990d-102">ICorProfilerCallback::RemotingServerInvocationReturned, méthode</span><span class="sxs-lookup"><span data-stu-id="d990d-102">ICorProfilerCallback::RemotingServerInvocationReturned Method</span></span>
<span data-ttu-id="d990d-103">Notifie le profileur que le processus a fini d’appeler une méthode en réponse à une demande d’appel de méthode distant.</span><span class="sxs-lookup"><span data-stu-id="d990d-103">Notifies the profiler that the process has finished invoking a method in response to a remote method invocation request.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d990d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d990d-104">Syntax</span></span>  
  
```  
HRESULT RemotingServerInvocationReturned();  
```  
  
## <a name="requirements"></a><span data-ttu-id="d990d-105">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d990d-105">Requirements</span></span>  
 <span data-ttu-id="d990d-106">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d990d-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d990d-107">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d990d-107">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="d990d-108">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d990d-108">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d990d-109">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d990d-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d990d-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d990d-110">See Also</span></span>  
 [<span data-ttu-id="d990d-111">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="d990d-111">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
