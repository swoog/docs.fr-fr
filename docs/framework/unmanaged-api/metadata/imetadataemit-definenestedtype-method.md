---
title: IMetaDataEmit::DefineNestedType, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineNestedType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineNestedType
helpviewer_keywords:
- IMetaDataEmit::DefineNestedType method [.NET Framework metadata]
- DefineNestedType method [.NET Framework metadata]
ms.assetid: 1e994de6-4628-459c-b967-b34be1e9fe4f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ee8e0dec469c7389a69c70567d7b2cb98d3404e6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54603909"
---
# <a name="imetadataemitdefinenestedtype-method"></a>IMetaDataEmit::DefineNestedType, méthode
Crée la signature de métadonnées d’une définition de type, retourne un `mdTypeDef` pour ce type de jeton et spécifie que le type défini est un membre du type référencé par le `tdEncloser` paramètre.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT DefineNestedType (   
    [in]  LPCWSTR     szTypeDef,  
    [in]  DWORD       dwTypeDefFlags,   
    [in]  mdToken     tkExtends,   
    [in]  mdToken     rtkImplements[],   
    [in]  mdTypeDef   tdEncloser,   
    [out] mdTypeDef   *ptd  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `szTypeDef`  
 [in] Le nom du type au format Unicode.  
  
 `dwTypeDefFlags`  
 [in] `TypeDef` attributs. Il s’agit d’un masque de bits de `CorTypeAttr` valeurs.  
  
 `tkExtends`  
 [in] Le jeton de la classe de base. Il s’agit soit un `mdTypeDef` ou un `mdTypeRef` jeton.  
  
 `rtkImplements`[]  
 [in] Un tableau de jetons qui spécifient les interfaces qui implémente cette classe ou une interface.  
  
 `tdEncloser`  
 [in] Le jeton du type englobant. Le dernier élément du tableau doit être `mdTokenNil`.  
  
 `ptd`  
 [out] Le `mdTypeDef` jeton attribué.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [IMetaDataEmit, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [IMetaDataEmit2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
