---
title: ICorProfilerCallback::RemotingClientInvocationFinished, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RemotingClientInvocationFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RemotingClientInvocationFinished
helpviewer_keywords:
- RemotingClientInvocationFinished method [.NET Framework profiling]
- ICorProfilerCallback::RemotingClientInvocationFinished method [.NET Framework profiling]
ms.assetid: ea4b283b-1210-4f41-a7a2-c398b1adde4e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2722497db5622dee4adcfd9381837477b89a8f63
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62041884"
---
# <a name="icorprofilercallbackremotingclientinvocationfinished-method"></a><span data-ttu-id="e719e-102">ICorProfilerCallback::RemotingClientInvocationFinished, méthode</span><span class="sxs-lookup"><span data-stu-id="e719e-102">ICorProfilerCallback::RemotingClientInvocationFinished Method</span></span>
<span data-ttu-id="e719e-103">Informe le profileur qu’un appel de communication à distance a jusqu'à la fin sur le client.</span><span class="sxs-lookup"><span data-stu-id="e719e-103">Notifies the profiler that a remoting call has run to completion on the client.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e719e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e719e-104">Syntax</span></span>  
  
```  
HRESULT RemotingClientInvocationFinished();  
```  
  
## <a name="remarks"></a><span data-ttu-id="e719e-105">Notes</span><span class="sxs-lookup"><span data-stu-id="e719e-105">Remarks</span></span>  
 <span data-ttu-id="e719e-106">Si l’appel de communication à distance était synchrone, il a également exécuté jusqu'à la fin sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="e719e-106">If the remoting call was synchronous, it has also run to completion on the server.</span></span> <span data-ttu-id="e719e-107">Si l’appel de communication à distance était asynchrone, une réponse peut encore être attendue lorsque l’appel est géré.</span><span class="sxs-lookup"><span data-stu-id="e719e-107">If the remoting call was asynchronous, a reply might still be expected when the call is handled.</span></span> <span data-ttu-id="e719e-108">Si une réponse est attendue, cela se produit comme un appel à [ICorProfilerCallback::RemotingClientReceivingReply](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingclientreceivingreply-method.md) et un appel supplémentaire à `RemotingClientInvocationFinished` pour indiquer le traitement secondaire requis d’un appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e719e-108">If a reply is expected, it will occur as a call to [ICorProfilerCallback::RemotingClientReceivingReply](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingclientreceivingreply-method.md) and an additional call to `RemotingClientInvocationFinished` to indicate the required secondary processing of an asynchronous call.</span></span>  
  
 <span data-ttu-id="e719e-109">Chacune des paires de rappels suivantes se produit sur le même thread :</span><span class="sxs-lookup"><span data-stu-id="e719e-109">Each of the following pairs of callbacks will occur on the same thread:</span></span>  
  
- <span data-ttu-id="e719e-110">`RemotingClientInvocationStarted` et [ICorProfilerCallback::RemotingClientSendingMessage](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingclientsendingmessage-method.md)</span><span class="sxs-lookup"><span data-stu-id="e719e-110">`RemotingClientInvocationStarted` and [ICorProfilerCallback::RemotingClientSendingMessage](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingclientsendingmessage-method.md)</span></span>  
  
- <span data-ttu-id="e719e-111">[ICorProfilerCallback::RemotingClientReceivingReply](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingclientreceivingreply-method.md) et [ICorProfilerCallback::RemotingClientInvocationFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingclientinvocationfinished-method.md)</span><span class="sxs-lookup"><span data-stu-id="e719e-111">[ICorProfilerCallback::RemotingClientReceivingReply](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingclientreceivingreply-method.md) and [ICorProfilerCallback::RemotingClientInvocationFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingclientinvocationfinished-method.md)</span></span>  
  
- <span data-ttu-id="e719e-112">[ICorProfilerCallback::RemotingServerInvocationReturned](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingserverinvocationreturned-method.md) et [ICorProfilerCallback::RemotingServerSendingReply](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingserversendingreply-method.md)</span><span class="sxs-lookup"><span data-stu-id="e719e-112">[ICorProfilerCallback::RemotingServerInvocationReturned](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingserverinvocationreturned-method.md) and [ICorProfilerCallback::RemotingServerSendingReply](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingserversendingreply-method.md)</span></span>  
  
 <span data-ttu-id="e719e-113">Vous devez être conscient des problèmes suivants avec les rappels de communication à distance :</span><span class="sxs-lookup"><span data-stu-id="e719e-113">You should be aware of the following issues with the remoting callbacks:</span></span>  
  
- <span data-ttu-id="e719e-114">Exécution d’une fonction de communication à distance n’est pas reflétée par le profileur API, afin de notifications pour les fonctions qui sont appelées à partir du client et exécutées sur le serveur ne sont pas correctement reçues.</span><span class="sxs-lookup"><span data-stu-id="e719e-114">Execution of a remoting function is not reflected by the profiler API, so notifications for functions that are called from the client and executed on the server are not properly received.</span></span> <span data-ttu-id="e719e-115">L’appel réel se produit via un objet proxy ; le profileur, il semble que certaines fonctions sont compilé par JIT mais jamais utilisé.</span><span class="sxs-lookup"><span data-stu-id="e719e-115">The actual invocation happens via a proxy object; to the profiler, it appears that certain functions are JIT-compiled but never used.</span></span>  
  
- <span data-ttu-id="e719e-116">Le profileur ne reçoit pas de notifications exactes pour les événements de communication à distance asynchrone.</span><span class="sxs-lookup"><span data-stu-id="e719e-116">The profiler does not receive accurate notifications for asynchronous remoting events.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e719e-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e719e-117">Requirements</span></span>  
 <span data-ttu-id="e719e-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e719e-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e719e-119">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e719e-119">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e719e-120">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e719e-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e719e-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e719e-121">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e719e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e719e-122">See also</span></span>

- [<span data-ttu-id="e719e-123">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="e719e-123">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
