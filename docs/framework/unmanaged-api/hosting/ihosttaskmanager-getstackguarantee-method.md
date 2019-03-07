---
title: IHostTaskManager::GetStackGuarantee, méthode
ms.date: 03/30/2017
api_name:
- IHostTaskManager.GetStackGuarantee
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::GetStackGuarantee
helpviewer_keywords:
- GetStackGuarantee method [.NET Framework hosting]
- IHostTaskManager::GetStackGuarantee method [.NET Framework hosting]
ms.assetid: 8176d732-c25c-4520-811d-e3310f339947
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 100bb73356379d2f251513bbbed0cf1e90752ff5
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57494370"
---
# <a name="ihosttaskmanagergetstackguarantee-method"></a>IHostTaskManager::GetStackGuarantee, méthode
Obtient la quantité d’espace de pile qui est garanti pour être disponible après qu’une opération de pile se termine, mais avant la fermeture d’un processus.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetStackGuarantee(  
    [out] ULONG *pGuarantee  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pGuarantee`  
 [out] Pointeur vers le nombre d’octets qui sont disponibles.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [IHostTaskManager, interface](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
