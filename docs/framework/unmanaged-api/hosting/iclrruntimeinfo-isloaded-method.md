---
title: ICLRRuntimeInfo::IsLoaded, méthode
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.IsLoaded
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::IsLoaded
helpviewer_keywords:
- IsLoaded method [.NET Framework hosting]
- ICLRRuntimeInfo::IsLoaded method [.NET Framework hosting]
ms.assetid: fdc5a3a7-71ff-4025-99a1-59e4ee0bfe1b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5ff1723cb481ee946e0c5c433009d3d6d7460cf5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33434661"
---
# <a name="iclrruntimeinfoisloaded-method"></a>ICLRRuntimeInfo::IsLoaded, méthode
Indique si le common language runtime (CLR) associées à la [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface est chargé dans un processus. Un runtime peut être chargé sans également en cours de démarrage.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT IsLoaded(  
[in]  HANDLE hndProcess,  
[out, retval] BOOL *pbLoaded);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `hndProcess`  
 [in] Handle vers le processus.  
  
 `pbLoaded`  
 [out] `true` si le CLR est chargé dans le processus ; sinon, `false`.  
  
## <a name="return-value"></a>Valeur de retour  
 Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.  
  
|HRESULT|Description|  
|-------------|-----------------|  
|S_OK|La commande s'est correctement terminée.|  
|E_POINTER|`pbLoaded` a la valeur null.|  
  
## <a name="remarks"></a>Notes  
 Cette méthode est à compatibilité descendante avec les fonctions et les interfaces suivantes :  
  
-   [ICorRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md) interface (dans l’API d’hébergement .NET Framework version 1).  
  
-   [ICLRRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md) interface (dans l’API d’hébergement .NET Framework 2.0).  
  
-   Deprecated `CorBindTo*` fonctions (consultez [déconseillée des fonctions d’hébergement CLR](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md) dans l’API d’hébergement .NET Framework 2.0).  
  
 Un hôte peut appeler une des déconseillées `CorBindTo*` fonctions, telles que la [CorBindToRuntime](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntime-function.md) fonction, pour instancier une version spécifique du CLR. L’hôte peut ensuite appeler la [ICLRMetaHost::GetRuntime](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-getruntime-method.md) (méthode) et spécifiez le numéro de version pour obtenir un [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface.  
  
 Si l’hôte appelle ensuite la `IsLoaded` méthode sur le [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface, `pbLoaded` retourne `true`; sinon, elle retourne `false`.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MetaHost.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [ICLRRuntimeInfo, interface](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)  
 [Interfaces d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)  
 [Hébergement](../../../../docs/framework/unmanaged-api/hosting/index.md)
