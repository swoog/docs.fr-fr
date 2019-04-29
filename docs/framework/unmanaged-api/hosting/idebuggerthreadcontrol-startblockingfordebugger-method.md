---
title: IDebuggerThreadControl::StartBlockingForDebugger, méthode
ms.date: 03/30/2017
api_name:
- IDebuggerThreadControl.StartBlockingForDebugger
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- StartBlockingForDebugger
helpviewer_keywords:
- IDebuggerThreadControl::StartBlockingForDebugger method [.NET Framework hosting]
- StartBlockingForDebugger method [.NET Framework hosting]
ms.assetid: 5c8f11b4-35d3-4c39-9bbd-58b896ba5ba6
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: dfc94c2de1a14842cc017e5c4ef6023154c20f2a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61699901"
---
# <a name="idebuggerthreadcontrolstartblockingfordebugger-method"></a>IDebuggerThreadControl::StartBlockingForDebugger, méthode
Avertit l’hôte que les services de débogage sont sur le point de démarrer tous les threads de blocage.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT StartBlockingForDebugger (  
    [in] DWORD dwUnused  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `dwUnused`  
 [in] Réservé pour une utilisation ultérieure.  
  
## <a name="remarks"></a>Notes  
 Le `StartBlockingForDebugger` méthode peut être appelée sur un thread d’exécution.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IDebuggerThreadControl, interface](../../../../docs/framework/unmanaged-api/hosting/idebuggerthreadcontrol-interface.md)
