---
title: IMetaDataEmit::Merge, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.Merge
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::Merge
helpviewer_keywords:
- IMetaDataEmit::Merge method [.NET Framework metadata]
- Merge method [.NET Framework metadata]
ms.assetid: 7596220c-f699-4b6c-8ae7-c83220610650
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7ebc86ad9c1f84156e7e228c1ddf3fe7b86b7e60
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54576263"
---
# <a name="imetadataemitmerge-method"></a>IMetaDataEmit::Merge, méthode
Ajoute la portée importée spécifiée à la liste des étendues à fusionner.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT Merge (   
    [in]  IMetaDataImport  *pImport,   
    [in]  IMapToken        *pHostMapToken,   
    [in]  IUnknown         *pHandler   
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `pImport`  
 [in] Un pointeur vers un [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) objet qui identifie la portée importée à fusionner.  
  
 `pIMap`  
 [in] Un pointeur vers un [IMapToken](../../../../docs/framework/unmanaged-api/metadata/imaptoken-interface.md) objet qui spécifie le jeton remapper.  
  
 `pHandleer`  
 [in] Un pointeur vers un [IUnknown](/cpp/atl/iunknown) objet qui spécifie les erreurs.  
  
## <a name="remarks"></a>Notes  
 Appelez [IMetaDataEmit::MergeEnd](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-mergeend-method.md) pour déclencher la fusion des métadonnées dans une seule portée.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [IMetaDataEmit, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [IMetaDataEmit2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
