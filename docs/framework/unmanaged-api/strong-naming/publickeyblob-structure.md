---
title: PublicKeyBlob, structure
ms.date: 03/30/2017
api_name:
- PublicKeyBlob
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- PublicKeyBlob
helpviewer_keywords:
- PublicKeyBlob structure [.NET Framework strong naming]
ms.assetid: b9240712-829c-4c8d-9a09-a6e7aa63f63a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fd7a4b19613ea771a055af7dd91ec368859ee191
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43475970"
---
# <a name="publickeyblob-structure"></a>PublicKeyBlob, structure
Représente, dans un format binaire, la clé publique d’une paire de clés publique/privée.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef struct {  
    unsigned int SigAlgId;  
    unsigned int HashAlgId;  
    ULONG cbPublicKey;  
    BYTE PublicKey[1]  
} PublicKeyBlob;   
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`SigAlgId`|L’identificateur de l’algorithme de signature (de type `ALG_ID`, comme défini dans WinCrypt.h) de la clé publique.|  
|`HashAlgId`|L’identificateur de l’algorithme de hachage (de type `ALG_ID`, comme défini dans WinCrypt.h) de la clé publique.|  
|`cbPublicKey`|La longueur de la clé en octets.|  
|`PublicKey`|Tableau d’octets de longueur variable qui contient la valeur de clé dans le format retourné par l’interface CryptoAPI.|  
  
## <a name="remarks"></a>Notes  
 Le `PublicKeyBlob` structure est utilisée par [StrongNameGetPublicKey](../../../../docs/framework/unmanaged-api/strong-naming/strongnamegetpublickey-function.md), [StrongNameSignatureGeneration](../../../../docs/framework/unmanaged-api/strong-naming/strongnamesignaturegeneration-function.md)et d’autres fonctions de nom fort pour représenter la clé publique d’une paire de clés publique/privée.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** StrongName.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [StrongNameGetPublicKey, fonction](../../../../docs/framework/unmanaged-api/strong-naming/strongnamegetpublickey-function.md)  
 [StrongNameSignatureGeneration, fonction](../../../../docs/framework/unmanaged-api/strong-naming/strongnamesignaturegeneration-function.md)  
 [Structures de noms forts](https://msdn.microsoft.com/library/4b041a2f-fd12-4b91-aacd-bc3b34a5124d)
