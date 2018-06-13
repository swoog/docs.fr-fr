---
title: ICLRTask2::BeginPreventAsyncAbort, méthode
ms.date: 03/30/2017
api_name:
- ICLRTask2.BeginPreventAsyncAbort
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask2::BeginPreventAsyncAbort
helpviewer_keywords:
- ICLRTask2::BeginPreventAsyncAbort method [.NET Framework hosting]
- BeginPreventAsyncAbort method [.NET Framework hosting]
ms.assetid: 75754c2f-38c7-4707-85fe-559db4542729
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5e1b5c0f5636748b96cc7d9667155581f1595a4e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33438403"
---
# <a name="iclrtask2beginpreventasyncabort-method"></a>ICLRTask2::BeginPreventAsyncAbort, méthode
Nouveau thread de retards interrompre les requêtes à partir de ce qui entraîne un abandons de thread sur le thread actuel.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT BeginPreventAsyncAbort();  
```  
  
## <a name="return-value"></a>Valeur de retour  
 Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.  
  
|HRESULT|Description|  
|-------------|-----------------|  
|S_OK|La commande s'est correctement terminée.|  
|HOST_E_INVALIDOPERATION|La méthode a été appelée sur un thread qui n’est pas le thread actuel.|  
  
## <a name="remarks"></a>Notes  
 Appel de cette méthode d’incrémente le compteur de délai d’abandon de thread pour le thread actuel d’une unité.  
  
 Les appels à `BeginPreventAsyncAbort` et [ICLRTask2::EndPreventAsyncAbort](../../../../docs/framework/unmanaged-api/hosting/iclrtask2-endpreventasyncabort-method.md) peuvent être imbriquées. Tant que le compteur est supérieur à zéro, pour le thread actuel abandons de thread. Si cet appel n’est pas associé à un appel à la `EndPreventAsyncAbort` (méthode), il est possible d’atteindre un état dans le thread abandons ne peut pas être remis au thread actuel.  
  
 Le délai d’attente d’un thread qui abandonne lui-même n’est pas reconnue.  
  
 La fonctionnalité exposée par cette fonctionnalité est utilisée en interne par la machine virtuelle (VM). Utilisation incorrecte de ces méthodes peut entraîner un comportement non spécifié dans la machine virtuelle. Par exemple, l’appel `EndPreventAsyncAbort` sans appeler d’abord `BeginPreventAsyncAbort` Impossible de définir le compteur à zéro lorsque la machine virtuelle a précédemment incrémenté. De même, le compteur interne n’est pas vérifié pour le dépassement de capacité. Si elle dépasse sa limite intégrale, car il est incrémenté par l’hôte et la machine virtuelle, le comportement résultant n’est pas spécifié.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [EndPreventAsyncAbort, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrtask2-endpreventasyncabort-method.md)  
 [ICLRTask2, interface](../../../../docs/framework/unmanaged-api/hosting/iclrtask2-interface.md)  
 [ICLRTaskManager, interface](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)  
 [IHostTask, interface](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)  
 [IHostTaskManager, interface](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)  
 [Interfaces d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
