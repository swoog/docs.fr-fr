---
title: Méthode ICLRStrongName::StrongNameTokenFromPublicKey
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameTokenFromPublicKey
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameTokenFromPublicKey
helpviewer_keywords:
- ICLRStrongName::StrongNameTokenFromPublicKey method [.NET Framework hosting]
- StrongNameTokenFromPublicKey method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: 7962ce88-7e86-4a6f-8298-621b01ffc3c2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 98c0dbbbe65d8f8c0b0196c82db1a8fd2b0ee3dd
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43468244"
---
# <a name="iclrstrongnamestrongnametokenfrompublickey-method"></a>Méthode ICLRStrongName::StrongNameTokenFromPublicKey
Obtient un jeton qui représente une clé publique. Un jeton de nom fort est la forme abrégée d’une clé publique.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT StrongNameTokenFromPublicKey (   
    [in]  BYTE    *pbPublicKeyBlob,  
    [in]  ULONG   cbPublicKeyBlob,  
    [out] BYTE    **ppbStrongNameToken,  
    [out] ULONG   *pcbStrongNameToken  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `pbPublicKeyBlob`  
 [in] Une structure de type [PublicKeyBlob](../../../../docs/framework/unmanaged-api/strong-naming/publickeyblob-structure.md) qui contient la partie publique de la paire de clés utilisée pour générer la signature de nom fort.  
  
 `cbPublicKeyBlob`  
 [in] La taille, en octets, de `pbPublicKeyBlob`.  
  
 `ppbStrongNameToken`  
 [out] Le jeton de nom fort correspondant à la clé passée dans `pbPublicKeyBlob`. Le common language runtime alloue la mémoire dans lequel retourner le jeton. L’appelant doit libérer cette mémoire en utilisant la [ICLRStrongName::StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamefreebuffer-method.md) (méthode).  
  
 `pcbStrongNameToken`  
 [out] La taille, en octets, du jeton de nom fort retourné.  
  
## <a name="return-value"></a>Valeur de retour  
 `S_OK` Si la méthode a réussi ; Sinon, une valeur HRESULT qui indique un échec (consultez [valeurs HRESULT courantes](https://go.microsoft.com/fwlink/?LinkId=213878) pour obtenir la liste).  
  
## <a name="remarks"></a>Notes  
 Un jeton de nom fort est la forme abrégée d’une clé publique qui permet d’économiser de l’espace lorsque vous stockez des informations de clé dans les métadonnées. Plus précisément, les jetons de nom fort sont utilisés dans les références d’assembly pour faire référence à l’assembly dépendant.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MetaHost.h  
  
 **Bibliothèque :** inclus en tant que ressource dans mscoree.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [StrongNameGetPublicKey, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetpublickey-method.md)  
 [PublicKeyBlob, structure](../../../../docs/framework/unmanaged-api/strong-naming/publickeyblob-structure.md)  
 [ICLRStrongName, interface](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
