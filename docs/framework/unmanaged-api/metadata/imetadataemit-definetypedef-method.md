---
title: IMetaDataEmit::DefineTypeDef, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineTypeDef
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineTypeDef
helpviewer_keywords:
- IMetaDataEmit::DefineTypeDef method [.NET Framework metadata]
- DefineTypeDef method [.NET Framework metadata]
ms.assetid: dd11c485-be95-4b97-9cd8-68679a4fb432
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 54691785e3b2619b5f4a2eecc510800b4b5cee07
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33446595"
---
# <a name="imetadataemitdefinetypedef-method"></a>IMetaDataEmit::DefineTypeDef, méthode
Crée une définition de type pour un type de common language runtime et obtient un jeton de métadonnées pour cette définition de type.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT DefineTypeDef (   
    [in]  LPCWSTR     szTypeDef,   
    [in]  DWORD       dwTypeDefFlags,   
    [in]  mdToken     tkExtends,   
    [in]  mdToken     rtkImplements[],   
    [out] mdTypeDef   *ptd  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `szTypeDef`  
 [in] Le nom du type au format Unicode.  
  
 `dwTypeDefFlags`  
 [in] `TypeDef` attributs. Il s’agit d’un masque de bits de `CoreTypeAttr` valeurs.  
  
 `tkExtends`  
 [in] Le jeton de la classe de base. Il doit être un `mdTypeDef` ou un `mdTypeRef` jeton.  
  
 `rtkImplements`  
 [in] Tableau des jetons spécifiant les interfaces que cette classe ou interface implémente.  
  
 `ptd`  
 [out] Le `mdTypeDef` jeton assigné.  
  
## <a name="remarks"></a>Notes  
 Un indicateur dans `dwTypeDefFlags` Spécifie si le type en cours de création est un type système référence type commun (classe ou interface) ou un type de valeur système type commun.  
  
 Selon les paramètres fournis, cette méthode, un effet secondaire peut également créer un `mdInterfaceImpl` enregistrement pour chaque interface héritée ou implémentée par ce type. Toutefois, cette méthode ne retourne pas un de ces `mdInterfaceImpl` jetons. Si un client souhaite ultérieurement ajouter ou modifier un `mdInterfaceImpl` jeton, elle doit utiliser le `IMetaDataImport` interface pour les énumérer. Si vous souhaitez utiliser une sémantique COM de le `[default]` interface, vous devez fournir l’interface par défaut en tant que le premier élément de `rtkImplements`; un attribut personnalisé est défini sur la classe indiquera que la classe possède une interface par défaut (qui est censé toujours pour être le tout d’abord `mdInterfaceImpl` jeton déclaré pour la classe).  
  
 Chaque élément de la `rtkImplements` tableau contient un `mdTypeDef` ou `mdTypeRef` jeton. Le dernier élément du tableau doit être `mdTokenNil`.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** utilisé en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [IMetaDataEmit, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [IMetaDataEmit2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
