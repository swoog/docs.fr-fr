---
title: ICLRDebugManager::SetDacl, méthode
ms.date: 03/30/2017
api_name:
- ICLRDebugManager.SetDacl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRDebugManager::SetDacl
helpviewer_keywords:
- SetDacl method [.NET Framework hosting]
- ICLRDebugManager::SetDacl method [.NET Framework hosting]
ms.assetid: 52f4af3f-e02b-4c20-9fd9-e8e4f4d6fc31
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c3847ec6df2e4c6f0cd7116e8219f194792c8b78
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33433045"
---
# <a name="iclrdebugmanagersetdacl-method"></a>ICLRDebugManager::SetDacl, méthode
Cette méthode n’est pas implémentée.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT SetDacl (  
    [in] PACL pacl  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `pacl`  
 [in] Pointeur vers la liste de contrôle d’accès (ACL).  
  
## <a name="return-value"></a>Valeur de retour  
  
|HRESULT|Description|  
|-------------|-----------------|  
|E_NOTIMPL|La méthode n’est pas implémentée.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [ICLRControl, interface](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)  
 [ICLRDebugManager, interface](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-interface.md)  
 [GetDacl, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-getdacl-method.md)  
 [IHostControl, interface](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md)
