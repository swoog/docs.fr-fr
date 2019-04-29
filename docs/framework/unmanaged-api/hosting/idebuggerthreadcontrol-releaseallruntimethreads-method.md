---
title: IDebuggerThreadControl::ReleaseAllRuntimeThreads, méthode
ms.date: 03/30/2017
api_name:
- IDebuggerThreadControl.ReleaseAllRuntimeThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ReleaseAllRuntimeThreads
helpviewer_keywords:
- ReleaseAllRuntimeThreads method [.NET Framework hosting]
- IDebuggerThreadControl::ReleaseAllRuntimeThreads method [.NET Framework hosting]
ms.assetid: 1a2995ff-5f02-4b49-84dc-3a5f9cfd7d55
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 136dab5c05c310d85a5e18bcdc6da0de901d3ace
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61699862"
---
# <a name="idebuggerthreadcontrolreleaseallruntimethreads-method"></a>IDebuggerThreadControl::ReleaseAllRuntimeThreads, méthode
Avertit l’hôte que les services de débogage sont sur le point de mise en production de tous les threads qui sont bloqués.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT ReleaseAllRuntimeThreads ( );  
```  
  
## <a name="remarks"></a>Notes  
 Le `ReleaseAllRuntimeThreads` méthode ne sera jamais appelée sur un thread d’exécution. Si l’hôte a un thread du runtime bloqué, il doit le libérer maintenant.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IDebuggerThreadControl, interface](../../../../docs/framework/unmanaged-api/hosting/idebuggerthreadcontrol-interface.md)
