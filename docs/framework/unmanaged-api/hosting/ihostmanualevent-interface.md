---
title: IHostManualEvent, interface
ms.date: 03/30/2017
api_name:
- IHostManualEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostManualEvent
helpviewer_keywords:
- IHostManualEvent interface [.NET Framework hosting]
ms.assetid: 300c2661-b7d1-4c39-b080-9ebdef0fd523
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ad580f7cab81323e09a24dc12db39f223be3aeb4
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59208629"
---
# <a name="ihostmanualevent-interface"></a>IHostManualEvent, interface
Fournit l’implémentation de l’hôte d’une représentation d’un événement de réinitialisation manuelle.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[Reset, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-reset-method.md)|Réinitialise l’actuel `IHostManualEvent` instance à un état non signalé.|  
|[Set, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-set-method.md)|Définit l’actuel `IHostManualEvent` instance à un état signalé.|  
|[Wait, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostmanualevent-wait-method.md)|Fait en `IHostManualEvent` instance à attendre jusqu'à ce qu’il appartient, ou un certain laps de temps.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICLRSyncManager, interface](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)
- [IHostAutoEvent, interface](../../../../docs/framework/unmanaged-api/hosting/ihostautoevent-interface.md)
- [IHostSemaphore, interface](../../../../docs/framework/unmanaged-api/hosting/ihostsemaphore-interface.md)
- [IHostSyncManager, interface](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)
- [Interfaces d'hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
