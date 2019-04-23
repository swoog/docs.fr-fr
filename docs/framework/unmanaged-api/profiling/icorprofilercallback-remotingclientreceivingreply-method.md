---
title: ICorProfilerCallback::RemotingClientReceivingReply, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RemotingClientReceivingReply
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RemotingClientReceivingReply
helpviewer_keywords:
- ICorProfilerCallback::RemotingClientReceivingReply method [.NET Framework profiling]
- RemotingClientReceivingReply method [.NET Framework profiling]
ms.assetid: 15cfc300-8231-4ecb-9a04-19851c3eb484
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5865935af96260982d47b778d208f4235f6245e2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59164916"
---
# <a name="icorprofilercallbackremotingclientreceivingreply-method"></a><span data-ttu-id="8ee71-102">ICorProfilerCallback::RemotingClientReceivingReply, méthode</span><span class="sxs-lookup"><span data-stu-id="8ee71-102">ICorProfilerCallback::RemotingClientReceivingReply Method</span></span>
<span data-ttu-id="8ee71-103">Informe le profileur que la partie côté serveur d’un appel de communication à distance est terminée et le client reçoit maintenant et sur le point de traiter la réponse.</span><span class="sxs-lookup"><span data-stu-id="8ee71-103">Notifies the profiler that the server-side portion of a remoting call has completed and the client is now receiving and about to process the reply.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8ee71-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ee71-104">Syntax</span></span>  
  
```  
HRESULT RemotingClientReceivingReply(  
    [in] GUID *pCookie,  
    [in] BOOL fIsAsync);   
```  
  
## <a name="parameters"></a><span data-ttu-id="8ee71-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ee71-105">Parameters</span></span>  
 `pCookie`  
 <span data-ttu-id="8ee71-106">[in] Valeur qui correspond à la valeur fournie dans [ICorProfilerCallback::RemotingServerSendingReply](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingserversendingreply-method.md) dans ces conditions :</span><span class="sxs-lookup"><span data-stu-id="8ee71-106">[in] A value that will correspond with the value provided in [ICorProfilerCallback::RemotingServerSendingReply](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingserversendingreply-method.md) under these conditions:</span></span>  
  
-   <span data-ttu-id="8ee71-107">Les cookies GUID de communication à distance sont actifs.</span><span class="sxs-lookup"><span data-stu-id="8ee71-107">Remoting GUID cookies are active.</span></span>  
  
-   <span data-ttu-id="8ee71-108">Le canal réussit à transmettre le message.</span><span class="sxs-lookup"><span data-stu-id="8ee71-108">The channel succeeds in transmitting the message.</span></span>  
  
-   <span data-ttu-id="8ee71-109">Les cookies GUID sont actifs sur le processus côté serveur.</span><span class="sxs-lookup"><span data-stu-id="8ee71-109">GUID cookies are active on the server-side process.</span></span>  
  
 <span data-ttu-id="8ee71-110">Cela permet un appariement simple d’appels de communication à distance.</span><span class="sxs-lookup"><span data-stu-id="8ee71-110">This allows easy pairing of remoting calls.</span></span>  
  
 `fIsAsync`  
 <span data-ttu-id="8ee71-111">[in] Une valeur qui est `true` si l’appel est asynchrone ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="8ee71-111">[in] A value that is `true` if the call is asynchronous; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8ee71-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ee71-112">Requirements</span></span>  
 <span data-ttu-id="8ee71-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8ee71-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8ee71-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="8ee71-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="8ee71-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8ee71-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8ee71-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8ee71-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8ee71-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ee71-117">See also</span></span>

- [<span data-ttu-id="8ee71-118">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="8ee71-118">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
