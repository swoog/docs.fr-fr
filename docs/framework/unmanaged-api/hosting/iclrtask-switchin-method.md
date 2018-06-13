---
title: ICLRTask::SwitchIn, méthode
ms.date: 03/30/2017
api_name:
- ICLRTask.SwitchIn
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask::SwitchIn
helpviewer_keywords:
- ICLRTask::SwitchIn method [.NET Framework hosting]
- SwitchIn method [.NET Framework hosting]
ms.assetid: 3d37ce20-aa65-4043-8f13-7c728b5d8a52
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 13e4119da7af4c54387c24ee576ff9577da56ca9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33438039"
---
# <a name="iclrtaskswitchin-method"></a>ICLRTask::SwitchIn, méthode
Notifie le common language runtime (CLR) que la tâche qui en cours [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) instance représente est maintenant en état de fonctionnement.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT SwitchIn (  
    [in] HANDLE threadHandle  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `threadHandle`  
 [in] Un handle du thread physique sur lequel la tâche est représentée par le `ICLRTask` instance est en cours d’exécution.  
  
## <a name="return-value"></a>Valeur de retour  
  
|HRESULT|Description|  
|-------------|-----------------|  
|S_OK|`SwitchIn` retourné avec succès.|  
|HOST_E_CLRNOTAVAILABLE|Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.|  
|HOST_E_TIMEOUT|L’appel a expiré.|  
|HOST_E_NOT_OWNER|L’appelant ne possède pas le verrou.|  
|HOST_E_ABANDONED|Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.|  
|E_FAIL|Une défaillance grave et inconnue s’est produite. Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus. Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.|  
|HOST_E_INVALIDOPERATION|`SwitchIn` a été appelé sans un appel précédent à [SwitchOut, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrtask-switchout-method.md).|  
  
## <a name="remarks"></a>Notes  
 Le `threadHandle` paramètre représente un handle vers le thread de système d’exploitation sur lequel la tâche est représentée par le `ICLRTask` instance a été planifiée. Si l’emprunt d’identité s’est produite sur ce thread, vous devez appeler [IHostSecurityManager::RevertToSelf](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-reverttoself-method.md) avant de basculer dans la tâche.  
  
> [!NOTE]
>  Un appel à `SwitchIn` sans un appel précédent à `SwitchOut` échoue avec une valeur HRESULT de HOST_E_INVALIDOPERATION.  
  
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
