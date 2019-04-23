---
title: IMetaDataEmit::DefineField, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineField
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineField
helpviewer_keywords:
- IMetaDataEmit::DefineField method [.NET Framework metadata]
- DefineField method, IMetaDataEmit interface [.NET Framework metadata
ms.assetid: 6b5be4fc-2e86-499c-8b09-833160bca767
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a8ba8a762c56a666c67b25b9ce0420099fce419a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59223522"
---
# <a name="imetadataemitdefinefield-method"></a>IMetaDataEmit::DefineField, méthode
Crée une définition pour un champ avec la signature de métadonnées spécifiée et obtient un jeton pour cette définition de champ.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT DefineField (   
    [in]  mdTypeDef   td,   
    [in]  LPCWSTR     szName,   
    [in]  DWORD       dwFieldFlags,   
    [in]  PCCOR_SIGNATURE pvSigBlob,   
    [in]  ULONG       cbSigBlob,   
    [in]  DWORD       dwCPlusTypeFlag,   
    [in]  void const  *pValue,   
    [in]  ULONG       cchValue,   
    [out] mdFieldDef  *pmd   
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `td`  
 [in] Le `mdTypeDef` jeton pour l’interface ou la classe englobante.  
  
 `szName`  
 [in] Le nom du champ au format Unicode.  
  
 `dwFieldFlags`  
 [in] Les attributs de champ. Il s’agit d’un masque de bits de `CorFieldAttr` valeurs.  
  
 `pvSigBlob`  
 [in] La signature de champ comme un objet BLOB.  
  
 `cbSigBlob`  
 [in] Le nombre d’octets dans `pvSigBlob`.  
  
 `dwCPlusTypeFlag`  
 [in] Le `ELEMENT_TYPE_` *\** pour la valeur de constante. Il s’agit d’un `CorElementType` valeur. Si vous ne définissez pas une valeur constante pour le champ, utilisez `ELEMENT_TYPE_END`.  
  
 `pValue`  
 [in] La valeur de constante pour le champ.  
  
 `cchValue`  
 [in] La taille en caractères (Unicode) de `pValue`.  
  
 `pmd`  
 [out] Le `mdFieldDef` jeton attribué.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IMetaDataEmit, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [IMetaDataEmit2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
