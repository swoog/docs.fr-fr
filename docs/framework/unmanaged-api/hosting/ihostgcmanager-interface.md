---
title: IHostGCManager, interface
ms.date: 03/30/2017
api_name:
- IHostGCManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostGCManager
helpviewer_keywords:
- IHostGCManager interface [.NET Framework hosting]
ms.assetid: 820330a4-244c-4f67-ab5e-f24b0b3c2080
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c4eac8abede82915386abc19c4c8389932451df4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33440374"
---
# <a name="ihostgcmanager-interface"></a>IHostGCManager, interface
Fournit des méthodes qui notifier l’hôte d’événements dans le mécanisme de garbage collection implémentés par le common language runtime (CLR).  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|[SuspensionEnding, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostgcmanager-suspensionending-method.md)|Avertit l’hôte que le CLR reprend l’exécution de tâches sur les threads qui avaient été interrompus pour un garbage collection.|  
|[SuspensionStarting, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostgcmanager-suspensionstarting-method.md)|Avertit l’hôte que le CLR interrompt l’exécution de tâches pour effectuer un garbage collection.|  
|[ThreadIsBlockingForSuspension, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostgcmanager-threadisblockingforsuspension-method.md)|Avertit l’hôte que le thread à partir de laquelle l’appel de méthode a été effectué sur le point de bloquer pour un garbage collection.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [ICLRTask, interface](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)  
 [ICLRTaskManager, interface](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)  
 [IHostTask, interface](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)  
 [IHostTaskManager, interface](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)  
 [Interfaces d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
