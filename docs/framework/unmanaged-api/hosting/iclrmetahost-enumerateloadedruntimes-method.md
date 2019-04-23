---
title: ICLRMetaHost::EnumerateLoadedRuntimes, méthode
ms.date: 03/30/2017
api_name:
- ICLRMetaHost.EnumerateLoadedRuntimes
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMetaHost::EnumerateLoadedRuntimes
helpviewer_keywords:
- EnumerateLoadedRuntimes method [.NET Framework hosting]
- ICLRMetaHost::EnumerateLoadedRuntimes method [.NET Framework hosting]
ms.assetid: 22fc0a3f-dce4-4766-9a3c-9fab15f4b4ca
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b0e1213128f5728f17225fbf6906d877dc64e86d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59106611"
---
# <a name="iclrmetahostenumerateloadedruntimes-method"></a>ICLRMetaHost::EnumerateLoadedRuntimes, méthode
Retourne une énumération qui inclut un valide [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) pointeur d’interface pour chaque version du common language runtime (CLR) qui est chargé dans un processus donné. Cette méthode remplace la [GetVersionFromProcess](../../../../docs/framework/unmanaged-api/hosting/getversionfromprocess-function.md) (fonction).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT EnumerateLoadedRuntimes (  
    [in] HANDLE hndProcess,  
    [out, retval] IEnumUnknown **ppEnumerator  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `hndProcess`  
 [in] Le handle du processus à inspecter pour les runtimes chargés.  
  
 `ppEnumerator`  
 [out] Un <xref:Microsoft.VisualStudio.OLE.Interop.IEnumUnknown> énumération de [ICLRRuntimeInfo](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md) interfaces correspondant à chaque CLR qui est chargé par le processus.  
  
## <a name="return-value"></a>Valeur de retour  
 Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.  
  
|HRESULT|Description|  
|-------------|-----------------|  
|S_OK|La commande s'est correctement terminée.|  
|E_POINTER|`ppEnumerator` a la valeur null.|  
  
## <a name="remarks"></a>Notes  
 Cette méthode est répertorie toutes les exécutions chargées, même si elles ont été chargées avec les fonctions déconseillées comme [CorBindToRuntime](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntime-function.md).  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MetaHost.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICLRMetaHost, interface](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-interface.md)
- [Hébergement](../../../../docs/framework/unmanaged-api/hosting/index.md)
