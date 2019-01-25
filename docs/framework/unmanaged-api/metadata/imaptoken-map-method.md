---
title: IMapToken::Map, méthode
ms.date: 03/30/2017
api_name:
- IMapToken.Map
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMapToken::Map
helpviewer_keywords:
- IMapToken::Map method [.NET Framework metadata]
- Map method [.NET Framework metadata]
ms.assetid: b9b4bf2f-1098-43d6-9619-a99b4bda1940
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 31c18061ad5f21e26665cd0d6883b0eb26afd1d4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54557473"
---
# <a name="imaptokenmap-method"></a>IMapToken::Map, méthode
Mappe une relation entre les assemblys à l’aide de signatures de métadonnées.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT Map (  
    [in]  mdToken tkImp,   
    [in]  mdToken tkEmit  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `tkImp`  
 [in] Le jeton de métadonnées qui représente l’objet de code importé.  
  
 `tkEmit`  
 [in] Le jeton de métadonnées qui représente l’objet de code émis.  
  
## <a name="remarks"></a>Notes  
 Lorsque le jeton remapper se produit pendant une fusion, le jeton d’origine est étendu dans la portée de métadonnées importées (source) et le nouveau jeton est limité dans la portée de métadonnées émise (cible).  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [IMapToken, interface](../../../../docs/framework/unmanaged-api/metadata/imaptoken-interface.md)
