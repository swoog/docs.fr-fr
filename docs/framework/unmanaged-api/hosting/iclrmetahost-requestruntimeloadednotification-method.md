---
title: ICLRMetaHost::RequestRuntimeLoadedNotification, méthode
ms.date: 03/30/2017
api_name:
- ICLRMetaHost.RequestRuntimeLoadedNotification
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMetaHost::RequestRuntimeLoadedNotification
helpviewer_keywords:
- RequestRuntimeLoadedNotification method [.NET Framework hosting]
- ICLRMetaHost::RequestRuntimeLoadedNotification method [.NET Framework hosting]
ms.assetid: 0d5ccc4d-0193-41f5-af54-45d7b70d5321
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 61fce3e06b5245872f7061716e8d995dd5f5043c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59224875"
---
# <a name="iclrmetahostrequestruntimeloadednotification-method"></a>ICLRMetaHost::RequestRuntimeLoadedNotification, méthode
Fournit une fonction de rappel qui est garantie être appelée lorsqu’une version du common language runtime (CLR) est chargée en premier, mais pas encore démarrée. Cette méthode remplace la [LockClrVersion](../../../../docs/framework/unmanaged-api/hosting/lockclrversion-function.md) (fonction).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT RequestRuntimeLoadedNotification (  
    [in] RuntimeLoadedCallbackFnPtr pCallbackFunction);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pCallbackFunction`  
 [in] La fonction de rappel qui est appelée lorsqu’un nouveau runtime a été chargé.  
  
## <a name="return-value"></a>Valeur de retour  
 Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.  
  
|HRESULT|Description|  
|-------------|-----------------|  
|S_OK|La commande s'est correctement terminée.|  
|E_POINTER|`pCallbackFunction` a la valeur null.|  
  
## <a name="remarks"></a>Notes  
 Le rappel fonctionne de la façon suivante :  
  
-   Le rappel est appelé uniquement lorsqu’un runtime est chargé pour la première fois.  
  
-   Le rappel n’est pas appelé pour les chargements réentrants du même runtime.  
  
-   Pour les chargements de runtime non réentrants, les appels à la fonction de rappel sont sérialisés.  
  
 La fonction de rappel a le prototype suivant :  
  
```  
typedef void (__stdcall *RuntimeLoadedCallbackFnPtr)(  
                     ICLRRuntimeInfo *pRuntimeInfo,  
                     CallbackThreadSetFnPtr pfnCallbackThreadSet,  
                     CallbackThreadUnsetFnPtr pfnCallbackThreadUnset);  
```  
  
 Les prototypes de fonction de rappel sont les suivantes :  
  
-   `pfnCallbackThreadSet`:  
  
    ```  
    typedef HRESULT (__stdcall *CallbackThreadSetFnPtr)();  
    ```  
  
-   `pfnCallbackThreadUnset`:  
  
    ```  
    typedef HRESULT (__stdcall *CallbackThreadUnsetFnPtr)();  
    ```  
  
 Si l’hôte a l’intention de charger ou de provoquer un autre runtime à charger de manière réentrante, la `pfnCallbackThreadSet` et `pfnCallbackThreadUnset` les paramètres qui sont fournies dans le rappel de fonction doit être utilisée de la façon suivante :  
  
-   `pfnCallbackThreadSet` doit être appelée par le thread qui peut entraîner une charge de l’exécution avant la tentative de type de charge.  
  
-   `pfnCallbackThreadUnset` doit être appelée lorsque le thread ne provoquera plus tel un chargement de runtime (et avant le retour du rappel initial).  
  
-   `pfnCallbackThreadSet` et `pfnCallbackThreadUnset` sont tous deux non réentrante.  
  
> [!NOTE]
>  Héberger des applications ne doivent pas appeler `pfnCallbackThreadSet` et `pfnCallbackThreadUnset` sort du cadre de la `pCallbackFunction` paramètre.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MetaHost.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICLRMetaHost, interface](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-interface.md)
- [Hébergement](../../../../docs/framework/unmanaged-api/hosting/index.md)
