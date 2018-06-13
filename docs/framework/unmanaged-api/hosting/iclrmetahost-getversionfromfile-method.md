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
ms.openlocfilehash: 538e596c3a705020150f52c9e55605a49434ce8f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33434049"
---
# <a name="iclrmetahostgetversionfromfile-method"></a>ICLRMetaHost::GetVersionFromFile, méthode
Obtient d’origine .NET Framework version de compilation d’un assembly (stockée dans les métadonnées), étant donnée son chemin d’accès de fichier. Cette méthode remplace la [GetFileVersion](../../../../docs/framework/unmanaged-api/hosting/getfileversion-function.md) (fonction).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetVersionFromFile (  
    [in] LPCWSTR pwzFilePath,  
    [out, size_is(*pcchBuffer)] LPWSTR pwzBuffer,  
    [in, out] DWORD *pcchBuffer);  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `pwzFilePath`  
 [in] Le chemin d’accès de fichier d’assembly complet.  
  
 `pwzbuffer`  
 [out] La version de compilation .NET Framework stockée dans les métadonnées, au format « v*A*. *B*[. *X*] ». *A*, *B*, et *X* sont des nombres décimaux qui correspondent à la version principale, la version secondaire et le numéro de build. La longueur de cette chaîne est limitée à MAX_PATH.  
  
> [!NOTE]
>  Cette sortie correspond au nom de répertoire pour la version de .NET Framework, tel qu’il apparaît sous C:\Windows\Microsoft.NET\Framework.  
  
 Exemples de valeurs sont « v1.0.3705 », « v1.1.4322 », « v2.0.50727 » et « v4.0. *X*», où *X* varie selon le numéro de build installé. Notez que le préfixe « v » est obligatoire.  
  
 `pcchBuffer`  
 [dans, out] La taille de `pwzbuffer` pour éviter les dépassements de mémoire tampon.  
  
## <a name="return-value"></a>Valeur de retour  
 Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.  
  
|HRESULT|Description|  
|-------------|-----------------|  
|S_OK|La commande s'est correctement terminée.|  
|E_POINTER|`pwzbuffer` ou `pcchBuffer` est null.|  
|HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)|La mémoire tampon est trop petite.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MetaHost.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [ICLRMetaHost, interface](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-interface.md)  
 [Hébergement](../../../../docs/framework/unmanaged-api/hosting/index.md)
