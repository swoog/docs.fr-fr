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
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59133183"
---
# <a name="icorprofilercallbackremotingclientsendingmessage-method"></a>ICorProfilerCallback::RemotingClientSendingMessage, méthode
Notifie le profileur que le client envoie une demande au serveur.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT RemotingClientSendingMessage(  
    [in] GUID *pCookie,  
    [in] BOOL fIsAsync);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pCookie`  
 [in] Une valeur qui correspond à la valeur fournie dans [ICorProfilerCallback::RemotingServerReceivingMessage](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-remotingserverreceivingmessage-method.md) dans ces conditions :  
  
-   Les cookies GUID de communication à distance sont actifs.  
  
-   Le canal réussit à transmettre le message.  
  
-   Les cookies GUID sont actifs sur le processus côté serveur.  
  
 Cela permet un appariement simple d’appels de communication à distance et de la création d’une pile d’appel logique.  
  
 `fIsAsync`  
 [in] Une valeur qui est `true` si l’appel est asynchrone ; sinon, `false`.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorProfilerCallback, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
