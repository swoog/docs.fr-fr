---
title: GetHashFromHandle, fonction
ms.date: 03/30/2017
api_name:
- GetHashFromHandle
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetHashFromHandle
helpviewer_keywords:
- GetHashFromHandle function [.NET Framework strong naming]
ms.assetid: 9e00337f-b307-4602-9bc3-965a8dbf02cd
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 30aad6fc62c8fee7448163ca69117b804203d505
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33456480"
---
# <a name="gethashfromhandle-function"></a>GetHashFromHandle, fonction
Génère un hachage sur le contenu du fichier avec le handle de fichier spécifié, à l’aide de l’algorithme de hachage spécifié.  
  
 Cette fonction est déconseillée. Utilisez le [ICLRStrongName::GetHashFromHandle](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromhandle-method.md) méthode à la place.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetHashFromHandle (  
    [in]  HANDLE   hFile,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE     *pbHash,  
    [in]  DWORD    cchHash,  
    [out] DWORD    *pchHash  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `hFile`  
 [in] Le handle du fichier à hacher.  
  
 `piHashAlg`  
 [dans, out] Constante qui spécifie l’algorithme de hachage. Utilisez zéro pour l’algorithme par défaut.  
  
 `pbHash`  
 [out] La mémoire tampon de hachage retournée.  
  
 `cchHash`  
 [in] La taille maximum demandée `pbHash`.  
  
 `pchHash`  
 [out] La taille, en octets, de retourné `pbHash`.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** StrongName.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [GetHashFromHandle, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromhandle-method.md)  
 [ICLRStrongName, interface](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
