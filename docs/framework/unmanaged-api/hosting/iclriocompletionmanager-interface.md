---
title: ICLRIoCompletionManager, interface
ms.date: 03/30/2017
api_name:
- ICLRIoCompletionManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRIoCompletionManager
helpviewer_keywords:
- ICLRIoCompletionManager interface [.NET Framework hosting]
ms.assetid: c6c3ace6-e5e7-4450-8cc5-a9a48208c493
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7864bb81c3b457bf8ec07cd194d24b29a42bd441
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61767466"
---
# <a name="iclriocompletionmanager-interface"></a>ICLRIoCompletionManager, interface
Implémente une méthode de rappel qui permet à l’hôte notifier le common language runtime (CLR) de l’état des e/s spécifié demande.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[OnComplete, méthode](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-oncomplete-method.md)|Notifie le CLR de l’état d’une requête d’e/s qui a été effectuée à l’aide d’un appel à la [IHostIoCompletionManager::Bind](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-bind-method.md) (méthode).|  
  
## <a name="remarks"></a>Notes  
 L’hôte implémente l’abstraction de terminaison d’e/s à l’aide de la [IHostIoCompletionManager](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-interface.md) interface. Le CLR effectue les demandes d’e/s via cette interface et l’hôte notifie l’exécution du résultat de ces demandes à l’aide de la `ICLRIoCompletionManager` interface.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IHostIoCompletionManager, interface](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-interface.md)
- [IHostThreadPoolManager, interface](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-interface.md)
- [Interfaces d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
