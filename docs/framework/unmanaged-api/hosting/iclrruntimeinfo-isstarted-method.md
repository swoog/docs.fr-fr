---
title: ICLRRuntimeInfo::IsStarted, méthode
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.IsStarted
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::IsStarted
helpviewer_keywords:
- IsStarted method [.NET Framework hosting]
- ICLRRuntimeInfo::IsStarted method [.NET Framework hosting]
ms.assetid: ef6f2662-323b-4534-aa82-6d1afb7b9309
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8934a2a51ea4bc86166bf99a6087124d03ab11d9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33434114"
---
# <a name="iclrruntimeinfoisstarted-method"></a>ICLRRuntimeInfo::IsStarted, méthode
Indique si le runtime a été démarré (autrement dit, si le [méthode ICLRRuntimeHost::Start](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-start-method.md) a été appelée et a réussi).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT IsStarted(  
        [out] BOOL     *pbStarted,  
        [out] DWORD    *pdwStartupFlags);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `pbStarted`  
 [out] `true` si cette exécution est démarrée ; sinon, `false`.  
  
 `pdwStartupFlags`  
 [out] Retourne les indicateurs utilisés pour démarrer le runtime.  
  
## <a name="return-value"></a>Valeur de retour  
 Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.  
  
|HRESULT|Description|  
|-------------|-----------------|  
|S_OK|La commande s'est correctement terminée.|  
|E_NOTIMPL|La version du common language runtime (CLR) est antérieure à la version du CLR dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].|  
  
## <a name="remarks"></a>Notes  
 Cette méthode ne fonctionne avec les versions CLR antérieures à la version du CLR dans le [!INCLUDE[net_v40_short](../../../../includes/net-v40-short-md.md)].  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MetaHost.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [ICLRRuntimeInfo, interface](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)  
 [Interfaces d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)  
 [Hébergement](../../../../docs/framework/unmanaged-api/hosting/index.md)
