---
title: GetPublicKeyToken, méthode
ms.date: 03/30/2017
api_name:
- IALink2.GetPublicKeyToken
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetPublicKeyToken
helpviewer_keywords:
- GetPublicKeyToken method
ms.assetid: 4a16374c-94b0-47b0-9fed-88c2b0cdccd4
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f0481cfc3fa88aeb6fd7cd6ba93554d426f8eb2e
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57492047"
---
# <a name="getpublickeytoken-method"></a>GetPublicKeyToken, méthode
Récupère le jeton de clé publique pour un fichier de clé ou conteneur de clé.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetPublicKeyToken(  
    LPCWSTR pszKeyFile,  
    LPCWSTR pszKeyContainer,  
    void* pvPublicKeyToken,  
    DWORD* pcbPublicKeyToken  
) PURE;  
```  
  
## <a name="parameters"></a>Paramètres  
 `pszKeyFile`  
 Nom de fichier de la clé.  
  
 `pszKeyContainer`  
 Nom du conteneur de clé.  
  
 `pvPublicKeyToken`  
 Adresse où le jeton de clé doit être stocké.  
  
 `pcbPublicKeyToken`  
 Spécifie la taille, en octets, de la mémoire tampon indiqué par `pvPublicKeyToken`. Au retour, contient le nombre réel d’octets utilisés.  
  
## <a name="return-value"></a>Valeur de retour  
 Retourne S_OK si la méthode réussit.  
  
## <a name="requirements"></a>Spécifications  
 Nécessite alink.h.  
  
## <a name="see-also"></a>Voir aussi
- [IALink2, interface](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [IALink, interface](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [API ALink](../../../../docs/framework/unmanaged-api/alink/index.md)
