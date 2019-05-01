---
title: ICorProfilerCallback::RemotingServerSendingReply, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RemotingServerSendingReply
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RemotingServerSendingReply
helpviewer_keywords:
- RemotingServerSendingReply method [.NET Framework profiling]
- ICorProfilerCallback::RemotingServerSendingReply method [.NET Framework profiling]
ms.assetid: dfe84a19-2e03-4be2-8b25-f02bad38e4a9
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 024b1f3f7e08dc21582789de7f3899e8e44d5e39
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62041832"
---
# <a name="icorprofilercallbackremotingserversendingreply-method"></a><span data-ttu-id="8cd97-102">ICorProfilerCallback::RemotingServerSendingReply, méthode</span><span class="sxs-lookup"><span data-stu-id="8cd97-102">ICorProfilerCallback::RemotingServerSendingReply Method</span></span>
<span data-ttu-id="8cd97-103">Notifie le profileur que le processus a fini de traiter une demande d’appel de méthode distant et doit transmettre la réponse via un canal.</span><span class="sxs-lookup"><span data-stu-id="8cd97-103">Notifies the profiler that the process has finished processing a remote method invocation request and is about to transmit the reply through a channel.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8cd97-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8cd97-104">Syntax</span></span>  
  
```  
HRESULT RemotingServerSendingReply(  
    [in] GUID *pCookie,  
    [in] BOOL fIsAsync);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8cd97-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8cd97-105">Parameters</span></span>  
 `pCookie`  
 <span data-ttu-id="8cd97-106">[in] Un pointeur vers un GUID qui correspondra à la valeur fournie dans [ICorProfilerCallback::RemotingClientReceivingReply](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingclientreceivingreply-method.md) dans ces conditions :</span><span class="sxs-lookup"><span data-stu-id="8cd97-106">[in] A pointer to a GUID that will correspond with the value provided in [ICorProfilerCallback::RemotingClientReceivingReply](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingclientreceivingreply-method.md) under these conditions:</span></span>  
  
- <span data-ttu-id="8cd97-107">Les cookies GUID de communication à distance sont actifs.</span><span class="sxs-lookup"><span data-stu-id="8cd97-107">Remoting GUID cookies are active.</span></span>  
  
- <span data-ttu-id="8cd97-108">Le canal réussit à transmettre le message.</span><span class="sxs-lookup"><span data-stu-id="8cd97-108">The channel succeeds in transmitting the message.</span></span>  
  
- <span data-ttu-id="8cd97-109">Les cookies GUID sont actifs sur le processus côté client.</span><span class="sxs-lookup"><span data-stu-id="8cd97-109">GUID cookies are active on the client-side process.</span></span>  
  
 <span data-ttu-id="8cd97-110">Cela permet un appariement simple d’appels de communication à distance et de la création d’une pile d’appel logique.</span><span class="sxs-lookup"><span data-stu-id="8cd97-110">This allows easy pairing of remoting calls and the creation of a logical call stack.</span></span>  
  
 `fIsAsync`  
 <span data-ttu-id="8cd97-111">[in] Une valeur qui est `true` si l’appel est asynchrone ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="8cd97-111">[in] A value that is `true` if the call is asynchronous; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8cd97-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8cd97-112">Requirements</span></span>  
 <span data-ttu-id="8cd97-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8cd97-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8cd97-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="8cd97-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="8cd97-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8cd97-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8cd97-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8cd97-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8cd97-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8cd97-117">See also</span></span>

- [<span data-ttu-id="8cd97-118">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="8cd97-118">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
