---
title: ICLRSyncManager::GetMonitorOwner, méthode
ms.date: 03/30/2017
api_name:
- ICLRSyncManager.GetMonitorOwner
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRSyncManager::GetMonitorOwner
helpviewer_keywords:
- ICLRSyncManager::GetMonitorOwner method [.NET Framework hosting]
- GetMonitorOwner method [.NET Framework hosting]
ms.assetid: 840983a4-396d-47b4-86a0-d35f9b437cdb
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4b14421bbe71b68ca677cf712512a7f10aa30583
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59208200"
---
# <a name="iclrsyncmanagergetmonitorowner-method"></a>ICLRSyncManager::GetMonitorOwner, méthode
Obtient le [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) instance qui possède l’analyseur identifié par le cookie spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetMonitorOwner (  
    [in]  SIZE_T     cookie,  
    [out] IHostTask *ppOwnerHostTask  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `cookie`  
 [in] Le cookie associé à l’analyse.  
  
 `ppOwnerHostTask`  
 [out] Un pointeur vers le `IHostTask` qui possède actuellement l’analyseur, ou null si aucune tâche n’est propriétaire.  
  
## <a name="return-value"></a>Valeur de retour  
  
|HRESULT|Description|  
|-------------|-----------------|  
|S_OK|`GetMonitorOwner` retourné avec succès.|  
|HOST_E_CLRNOTAVAILABLE|Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.|  
|HOST_E_TIMEOUT|L’appel a expiré.|  
|HOST_E_NOT_OWNER|L’appelant ne possède pas le verrou.|  
|HOST_E_ABANDONED|Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.|  
|E_FAIL|Une défaillance catastrophique inconnue s’est produite. Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus. Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.|  
  
## <a name="remarks"></a>Notes  
 L’hôte appelle généralement `GetMonitorOwner` en tant que partie d’un mécanisme de détection de blocage. Le cookie est associé à un analyseur lorsqu’il est créé à l’aide d’un appel à [IHostSyncManager::CreateMonitorEvent](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-createmonitorevent-method.md).  
  
> [!NOTE]
>  Un appel pour libérer l’événement sous-jacent de l’analyseur peut se bloquer, mais se bloquera pas — si un appel à cette méthode est actuellement en vigueur sur le cookie associé à cette analyse. Autres tâches peuvent également se bloquer si elles tentent d’acquérir ce moniteur.  
  
 `GetMonitorOwner` Retourne toujours immédiatement et peut être appelée à tout moment après un appel à `CreateMonitorEvent`. L’hôte n’a pas besoin d’attendre une tâche est en attente sur l’événement.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICLRSyncManager, interface](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)
- [IHostSyncManager, interface](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)
