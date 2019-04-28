---
title: IHostFilter::MarkToken, méthode
ms.date: 03/30/2017
api_name:
- IHostFilter.MarkToken
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostFilter::MarkToken
helpviewer_keywords:
- MarkToken method, IHostFilter interface [.NET Framework metadata]
- IHostFilter::MarkToken method [.NET Framework metadata]
ms.assetid: d7061343-d0a3-4fd5-b312-61974f98bd62
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f3214a21dda27fda01054e96400997b15d11f71b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61905422"
---
# <a name="ihostfiltermarktoken-method"></a>IHostFilter::MarkToken, méthode
Indique que le jeton de métadonnées spécifié est traité.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT MarkToken (  
    [in]  mdToken         tk  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `tk`  
 [in] Le jeton de métadonnées à traiter.  
  
## <a name="remarks"></a>Notes  
 En règle générale, vous souhaitez un jeton à traiter si elle est dans la portée de métadonnées. Le `MarkToken` méthode est passée au moteur de métadonnées via le [IMetaDataEmit::SetHandler](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-sethandler-method.md) (méthode).  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de métadonnées](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)
- [IHostFilter, interface](../../../../docs/framework/unmanaged-api/metadata/ihostfilter-interface.md)
