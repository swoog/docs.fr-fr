---
title: ICLRMetaHost::GetVersionFromFile, méthode
ms.date: 03/30/2017
api_name:
- ICLRMetaHost.GetVersionFromFile
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMetaHost::GetVersionFromFile
helpviewer_keywords:
- ICLRMetaHost::GetVersionFromFile method [.NET Framework hosting]
- GetVersionFromFile method [.NET Framework hosting]
ms.assetid: 55bb3eb4-f665-42fc-973c-465567570e82
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e1c8f5ea20d00d692e0eea0cba93ec4e73038e8a
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57497442"
---
# <a name="iclrmetahostgetversionfromfile-method"></a>ICLRMetaHost::GetVersionFromFile, méthode
Obtient d’origine compilation version du .NET Framework d’un assembly (stockée dans les métadonnées), son chemin d’accès donnée. Cette méthode remplace la [GetFileVersion](../../../../docs/framework/unmanaged-api/hosting/getfileversion-function.md) (fonction).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetVersionFromFile (  
    [in] LPCWSTR pwzFilePath,  
    [out, size_is(*pcchBuffer)] LPWSTR pwzBuffer,  
    [in, out] DWORD *pcchBuffer);  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pwzFilePath`  
 [in] Le chemin d’accès de fichier d’assembly complet.  
  
 `pwzbuffer`  
 [out] La version de compilation .NET Framework stockée dans les métadonnées, au format « v*A*. *B*[. *X*] ». *Un*, *B*, et *X* sont des nombres décimaux qui correspondent à la version principale, la version secondaire et le numéro de build. La longueur de cette chaîne est limitée à MAX_PATH.  
  
> [!NOTE]
>  Cette sortie correspond au nom de répertoire pour la version de .NET Framework, tel qu’il apparaît sous C:\Windows\Microsoft.NET\Framework.  
  
 Exemples de valeurs : « v1.0.3705 », « v1.1.4322 », « v2.0.50727 » et « v4.0. *X*», où *X* varie selon le numéro de build installé. Notez que le préfixe « v » est obligatoire.  
  
 `pcchBuffer`  
 [in, out] La taille de `pwzbuffer` pour éviter les dépassements de mémoire tampon.  
  
## <a name="return-value"></a>Valeur de retour  
 Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.  
  
|HRESULT|Description|  
|-------------|-----------------|  
|S_OK|La commande s'est correctement terminée.|  
|E_POINTER|`pwzbuffer` ou `pcchBuffer` a la valeur null.|  
|HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)|La mémoire tampon est trop petite.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MetaHost.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICLRMetaHost, interface](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-interface.md)
- [Hébergement](../../../../docs/framework/unmanaged-api/hosting/index.md)
