---
title: IMetaDataEmit2::DefineGenericParam, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit2.DefineGenericParam
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit2::DefineGenericParam
helpviewer_keywords:
- IMetaDataEmit2::DefineGenericParam method [.NET Framework metadata]
- DefineGenericParam method [.NET Framework metadata]
ms.assetid: 47b2a3b6-907d-43dc-858d-1ae7dca1316a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: de8547ed0ee83bafe4612bdcd62607fc94fb3f69
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59163720"
---
# <a name="imetadataemit2definegenericparam-method"></a>IMetaDataEmit2::DefineGenericParam, méthode
Crée une définition pour un paramètre de type générique et obtient un jeton pour ce paramètre de type générique.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT DefineGenericParam (   
    [in]  mdToken         tk,   
    [in]  ULONG           ulParamSeq,   
    [in]  DWORD           dwParamFlags,   
    [in]  LPCWSTR         szname,   
    [in]  DWORD           reserved,   
    [in]  mdToken         rtkConstraints[],   
    [out] mdGenericParam  *pgp  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `tk`  
 [in] Un `mdTypeDef` ou `mdMethodDef` jeton qui représente la méthode ou le constructeur pour lequel définir un paramètre générique.  
  
 `ulParamSeq`  
 [in] L’index du paramètre générique.  
  
 `dwParamFlags`  
 [in] Une valeur de la [CorGenericParamAttr](../../../../docs/framework/unmanaged-api/metadata/corgenericparamattr-enumeration.md) énumération qui décrit le type du paramètre générique.  
  
 `szname`  
 [in] Le nom du paramètre.  
  
 `reserved`  
 [in] Ce paramètre est réservé pour une extensibilité future.  
  
 `rtkConstraints`  
 [in] Un tableau de contraintes de type se terminant par zéro. Les membres de tableau doivent être un `mdTypeDef`, `mdTypeRef`, ou `mdTypeSpec` jeton de métadonnées.  
  
 `pgp`  
 [out] Un jeton qui représente le paramètre générique.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IMetaDataEmit2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
- [IMetaDataEmit, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
