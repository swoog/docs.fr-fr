---
title: IMetaDataEmit::DefineProperty, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineProperty
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineProperty
helpviewer_keywords:
- IMetaDataEmit::DefineProperty method [.NET Framework metadata]
- DefineProperty method [.NET Framework metadata]
ms.assetid: 5c4c1dc2-d40d-4173-bbe6-7058fb21c98f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5c250a577f2ccdbbfefb35225b880c0e4317db36
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="imetadataemitdefineproperty-method"></a>IMetaDataEmit::DefineProperty, méthode
Crée une définition de propriété pour le type spécifié, avec l’objet `get` et `set` accesseurs de méthode et obtient un jeton pour cette définition de propriété.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT DefineProperty (   
    [in]  mdTypeDef          td,   
    [in]  LPCWSTR            szProperty,   
    [in]  DWORD              dwPropFlags,   
    [in]  PCCOR_SIGNATURE    pvSig,   
    [in]  ULONG              cbSig,   
    [in]  DWORD              dwCPlusTypeFlag,   
    [in]  void const         *pValue,   
    [in]  ULONG              cchValue,   
    [in]  mdMethodDef        mdSetter,   
    [in]  mdMethodDef        mdGetter,   
    [in]  mdMethodDef        rmdOtherMethods[],   
    [out] mdProperty         *pmdProp   
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `td`  
 [in] Le jeton pour la classe ou une interface sur lequel la propriété est définie.  
  
 `szProperty`  
 [in] Le nom de la propriété.  
  
 `dwPropFlags`  
 [in] Les indicateurs de propriété.  
  
 `pvSig`  
 [in] La signature de propriété.  
  
 `cbSig`  
 [in] Le nombre d’octets dans `pvSig`.  
  
 `dwCPlusTypeFlag`  
 [in] Le type de la valeur de propriété par défaut.  
  
 `pValue`  
 [in] La valeur par défaut pour la propriété.  
  
 `cchValue`  
 [in] Le nombre de caractères (Unicode) caractères `pValue`.  
  
 `mdSetter`  
 [in] La méthode qui définit la valeur de propriété.  
  
 `mdGetter`  
 [in] La méthode qui obtient la valeur de propriété.  
  
 `rmdOtherMethods[]`  
 [in] Un tableau des autres méthodes associées à la propriété. Terminez le tableau avec une `mdTokenNil`.  
  
 `pmdProp`  
 [out] Le `mdProperty` jeton assigné.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** utilisé en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [IMetaDataEmit, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [IMetaDataEmit2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
