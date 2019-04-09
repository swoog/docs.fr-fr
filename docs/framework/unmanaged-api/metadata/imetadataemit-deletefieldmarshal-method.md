---
title: IMetaDataEmit::DeleteFieldMarshal, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DeleteFieldMarshal
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DeleteFieldMarshal
helpviewer_keywords:
- IMetaDataEmit::DeleteFieldMarshal method [.NET Framework metadata]
- DeleteFieldMarshal method [.NET Framework metadata]
ms.assetid: 7c75aef9-c742-4b33-a14b-56ff94b0f725
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 78f2405bba9172b775b01e5417860c3f3d2dd4a4
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59206926"
---
# <a name="imetadataemitdeletefieldmarshal-method"></a>IMetaDataEmit::DeleteFieldMarshal, méthode
Détruit la signature de métadonnées pour l’objet référencé par le jeton spécifié de marshaling de PInvoke.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT DeleteFieldMarshal (  
    [in]  mdToken     tk  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `tk`  
 [in] Un `mdFieldDef` ou `mdParamDef` jeton qui représente le champ ou le paramètre pour lequel supprimer la signature de métadonnées de marshaling.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IMetaDataEmit, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [IMetaDataEmit2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
