---
title: ICorProfilerCallback::RemotingClientSendingMessage, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.RemotingClientSendingMessage
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RemotingClientSendingMessage
helpviewer_keywords:
- RemotingClientSendingMessage method [.NET Framework profiling]
- ICorProfilerCallback::RemotingClientSendingMessage method [.NET Framework profiling]
ms.assetid: 54d9a5a5-3877-49c1-a503-ce7c7943bc2a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 61a36ff23bf9deac25983f06387b2bbbfd49546b
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59133183"
---
# <a name="icorprofilercallbackremotingclientsendingmessage-method"></a><span data-ttu-id="17938-102">ICorProfilerCallback::RemotingClientSendingMessage, méthode</span><span class="sxs-lookup"><span data-stu-id="17938-102">ICorProfilerCallback::RemotingClientSendingMessage Method</span></span>
<span data-ttu-id="17938-103">Notifie le profileur que le client envoie une demande au serveur.</span><span class="sxs-lookup"><span data-stu-id="17938-103">Notifies the profiler that the client is sending a request to the server.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="17938-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17938-104">Syntax</span></span>  
  
```  
HRESULT RemotingClientSendingMessage(  
    [in] GUID *pCookie,  
    [in] BOOL fIsAsync);  
```  
  
## <a name="parameters"></a><span data-ttu-id="17938-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17938-105">Parameters</span></span>  
 `pCookie`  
 <span data-ttu-id="17938-106">[in] Une valeur qui correspond à la valeur fournie dans [ICorProfilerCallback::RemotingServerReceivingMessage](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingserverreceivingmessage-method.md) dans ces conditions :</span><span class="sxs-lookup"><span data-stu-id="17938-106">[in] A value that corresponds with the value provided in [ICorProfilerCallback::RemotingServerReceivingMessage](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingserverreceivingmessage-method.md) under these conditions:</span></span>  
  
-   <span data-ttu-id="17938-107">Les cookies GUID de communication à distance sont actifs.</span><span class="sxs-lookup"><span data-stu-id="17938-107">Remoting GUID cookies are active.</span></span>  
  
-   <span data-ttu-id="17938-108">Le canal réussit à transmettre le message.</span><span class="sxs-lookup"><span data-stu-id="17938-108">The channel succeeds in transmitting the message.</span></span>  
  
-   <span data-ttu-id="17938-109">Les cookies GUID sont actifs sur le processus côté serveur.</span><span class="sxs-lookup"><span data-stu-id="17938-109">GUID cookies are active on the server-side process.</span></span>  
  
 <span data-ttu-id="17938-110">Cela permet un appariement simple d’appels de communication à distance et de la création d’une pile d’appel logique.</span><span class="sxs-lookup"><span data-stu-id="17938-110">This allows easy pairing of remoting calls and the creation of a logical call stack.</span></span>  
  
 `fIsAsync`  
 <span data-ttu-id="17938-111">[in] Une valeur qui est `true` si l’appel est asynchrone ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="17938-111">[in] A value that is `true` if the call is asynchronous; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="17938-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17938-112">Requirements</span></span>  
 <span data-ttu-id="17938-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="17938-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="17938-114">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="17938-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="17938-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="17938-115">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="17938-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="17938-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="17938-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17938-117">See also</span></span>

- [<span data-ttu-id="17938-118">ICorProfilerCallback, interface</span><span class="sxs-lookup"><span data-stu-id="17938-118">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
