---
title: IDebuggerThreadControl, interface
ms.date: 03/30/2017
api_name:
- IDebuggerThreadControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IDebuggerThreadControl
helpviewer_keywords:
- IDebuggerThreadControl interface [.NET Framework hosting]
ms.assetid: 0a270c42-a7d1-45f1-a64d-fa3e84d14532
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7a551d3cc6ab3dd3887f232018f8201de4036d1b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61699654"
---
# <a name="idebuggerthreadcontrol-interface"></a>IDebuggerThreadControl, interface
Fournit des méthodes pour notifier l’hôte sur le blocage et déblocage des threads par les services de débogage.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[ThreadIsBlockingForDebugger, méthode](../../../../docs/framework/unmanaged-api/hosting/idebuggerthreadcontrol-threadisblockingfordebugger-method.md)|Avertit l’hôte que le thread qui envoie ce rappel concerne à blocs dans les services de débogage.|  
|[ReleaseAllRuntimeThreads, méthode](../../../../docs/framework/unmanaged-api/hosting/idebuggerthreadcontrol-releaseallruntimethreads-method.md)|Avertit l’hôte que les services de débogage sont sur le point de mise en production de tous les threads qui sont bloqués.|  
|[StartBlockingForDebugger, méthode](../../../../docs/framework/unmanaged-api/hosting/idebuggerthreadcontrol-startblockingfordebugger-method.md)|Avertit l’hôte que les services de débogage sont sur le point de démarrer tous les threads de blocage.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
