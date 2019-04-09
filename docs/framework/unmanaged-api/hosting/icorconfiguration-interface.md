---
title: ICorConfiguration, interface
ms.date: 03/30/2017
api_name:
- ICorConfiguration
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorConfiguration
helpviewer_keywords:
- ICorConfiguration interface [.NET Framework hosting]
ms.assetid: aaf96116-372b-4538-afb1-9e0fcdac1f98
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b24e278b3449d0e17377495cef0f445c1ebed734
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59149810"
---
# <a name="icorconfiguration-interface"></a>ICorConfiguration, interface
Fournit des méthodes pour configurer le common language runtime (CLR).  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[AddDebuggerSpecialThread, méthode](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-adddebuggerspecialthread-method.md)|Pour les services de débogage, indique qu’un thread particulier doit être autorisé à continuer à s’exécuter pendant que le débogueur arrête les scénarios de débogage managées ou une application.|  
|[SetDebuggerThreadControl, méthode](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-setdebuggerthreadcontrol-method.md)|Définit l’interface de rappel qui appellent les services de débogage comme des threads CLR sont bloqués et débloqués pour le débogage.|  
|[SetGCHostControl, méthode](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-setgchostcontrol-method.md)|Définit l’interface de rappel à utiliser par le garbage collector de demander à l’hôte de modifier les limites de mémoire virtuelle.|  
|[SetGCThreadControl, méthode](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-setgcthreadcontrol-method.md)|Définit l’interface de rappel pour la planification des threads pour les tâches non-runtime qui seraient sinon bloqués pour un garbage collection.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces d'hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [CorRuntimeHost, coclasse](../../../../docs/framework/unmanaged-api/hosting/corruntimehost-coclass.md)
