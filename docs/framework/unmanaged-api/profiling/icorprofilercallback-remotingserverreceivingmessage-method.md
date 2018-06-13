---
title: ICorProfilerCallback::RemotingServerReceivingMessage, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RemotingServerReceivingMessage
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RemotingServerReceivingMessage
helpviewer_keywords:
- ICorProfilerCallback::RemotingServerReceivingMessage method [.NET Framework profiling]
- RemotingServerReceivingMessage method [.NET Framework profiling]
ms.assetid: 5604d21f-e6b7-490e-b469-42122a7568e1
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c1874b5bea465eb31bcaad2d912b90d35cfc711b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33454099"
---
# <a name="icorprofilercallbackremotingserverreceivingmessage-method"></a><span data-ttu-id="e2371-102">ICorProfilerCallback::RemotingServerReceivingMessage, méthode</span><span class="sxs-lookup"><span data-stu-id="e2371-102">ICorProfilerCallback::RemotingServerReceivingMessage Method</span></span>
<span data-ttu-id="e2371-103">Notifie le profileur que le processus a reçu une demande d’appel ou de l’activation de méthode distante.</span><span class="sxs-lookup"><span data-stu-id="e2371-103">Notifies the profiler that the process has received a remote method invocation or activation request.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e2371-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2371-104">Syntax</span></span>  
  
```  
HRESULT RemotingClientSendingMessage(  
    [in] GUID *pCookie,  
    [in] BOOL fIsAsync);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e2371-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2371-105">Parameters</span></span>  
 `pCookie`  
 <span data-ttu-id="e2371-106">[in] Une valeur qui correspond à la valeur fournie dans [ICorProfilerCallback::RemotingClientSendingMessage](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingclientsendingmessage-method.md) dans ces conditions :</span><span class="sxs-lookup"><span data-stu-id="e2371-106">[in] A value that will correspond with the value provided in [ICorProfilerCallback::RemotingClientSendingMessage](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingclientsendingmessage-method.md) under these conditions:</span></span>  
  
-   <span data-ttu-id="e2371-107">Les cookies GUID de la communication à distance sont actives.</span><span class="sxs-lookup"><span data-stu-id="e2371-107">Remoting GUID cookies are active.</span></span>  
  
-   <span data-ttu-id="e2371-108">Le canal réussit à transmettre le message.</span><span class="sxs-lookup"><span data-stu-id="e2371-108">The channel succeeds in transmitting the message.</span></span>  
  
-   <span data-ttu-id="e2371-109">Les cookies GUID sont actifs sur le processus côté client.</span><span class="sxs-lookup"><span data-stu-id="e2371-109">GUID cookies are active on the client-side process.</span></span>  
  
 <span data-ttu-id="e2371-110">Cela permet un appariement aisé d’appels de communication à distance et de la création d’une pile d’appel logique.</span><span class="sxs-lookup"><span data-stu-id="e2371-110">This allows easy pairing of remoting calls and the creation of a logical call stack.</span></span>  
  
 `fIsAsync`  
 <span data-ttu-id="e2371-111">[in] Une valeur qui est `true` si l’appel est asynchrone ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="e2371-111">[in] A value that is `true` if the call is asynchronous; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e2371-112">Notes</span><span class="sxs-lookup"><span data-stu-id="e2371-112">Remarks</span></span>  
 <span data-ttu-id="e2371-113">Si la demande de message est asynchrone, la demande peut être traitée par n’importe quel thread arbitraire.</span><span class="sxs-lookup"><span data-stu-id="e2371-113">If the message request is asynchronous, the request can be serviced by any arbitrary thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e2371-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e2371-114">Requirements</span></span>  
 <span data-ttu-id="e2371-115">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e2371-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e2371-116">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e2371-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e2371-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e2371-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e2371-118">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e2371-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e2371-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2371-119">See Also</span></span>  
 [<span data-ttu-id="e2371-120">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="e2371-120">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
