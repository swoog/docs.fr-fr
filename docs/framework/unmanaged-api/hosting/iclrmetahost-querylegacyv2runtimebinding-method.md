---
title: ICLRMetaHost::QueryLegacyV2RuntimeBinding, méthode
ms.date: 03/30/2017
api_name:
- ICLRMetaHost.RequestRuntimeLoadedNotification
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMetaHost::QueryLegacyV2RuntimeBinding
helpviewer_keywords:
- QueryLegacyV2RuntimeBinding method [.NET Framework hosting]
- ICLRMetaHost::QueryLegacyV2RuntimeBinding method [.NET Framework hosting]
ms.assetid: 9929817e-acc9-40b7-960c-598664e04b60
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1664c47e580730fb0000465f9010e024c64fec2b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33432942"
---
# <a name="iclrmetahostquerylegacyv2runtimebinding-method"></a>ICLRMetaHost::QueryLegacyV2RuntimeBinding, méthode
Retourne une interface qui représente un runtime auquel une stratégie d’activation héritée a été liée, par exemple, à l’aide de la `useLegacyV2RuntimeActivationPolicy` de l’attribut le [ \<démarrage > élément](../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md) entrée de fichier de configuration, en utilisant directement des API d’activation hérité ou en appelant le [ICLRRuntimeInfo::BindAsLegacyV2Runtime](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-bindaslegacyv2runtime-method.md) (méthode).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT QueryLegacyV2RuntimeBinding (  
    [in] REFIID riid,  
    [out, iid_is(riid), retval] LPVOID *ppUnk);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `riid`  
 [in] La seule valeur valide pour ce paramètre est de Required.Currently `IID_ICLRRuntimeInfo`.  
  
 `ppUnk`  
 [out] Obligatoire. Lorsque cette méthode est retournée, contient un pointeur vers le [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interface qui représente un runtime qui a été lié à la stratégie d’activation héritée.  
  
## <a name="return-value"></a>Valeur de retour  
 Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.  
  
|HRESULT|Description|  
|-------------|-----------------|  
|S_OK|La méthode s'est terminée correctement et a retourné un runtime lié à une stratégie d'activation héritée.|  
|S_FALSE|La méthode s'est terminée correctement, mais un runtime hérité n'a pas encore été lié.|  
|E_NOINTERFACE|La méthode a trouvé un runtime lié à une stratégie d'activation héritée, mais `riid` n'est pas pris en charge par ce runtime.|  
  
## <a name="remarks"></a>Notes  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MetaHost.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [ICLRMetaHost, interface](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-interface.md)  
 [Hébergement](../../../../docs/framework/unmanaged-api/hosting/index.md)
