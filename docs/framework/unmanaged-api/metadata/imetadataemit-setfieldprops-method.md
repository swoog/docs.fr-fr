---
title: IMetaDataEmit::SetFieldProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetFieldProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetFieldProps
helpviewer_keywords:
- IMetaDataEmit::SetFieldProps method [.NET Framework metadata]
- SetFieldProps method [.NET Framework metadata]
ms.assetid: 47132dda-fa92-4bd1-ae4b-24cd9a60665a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6a2c38340614e633de4049515b38cb387031739b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="imetadataemitsetfieldprops-method"></a>IMetaDataEmit::SetFieldProps, méthode
Définit ou met à jour la valeur par défaut pour le champ référencé par le jeton de champ spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT SetFieldProps (  
    [in]  mdFieldDef  fd,   
    [in]  DWORD       dwFieldFlags,   
    [in]  DWORD       dwCPlusTypeFlag,   
    [in]  void const  *pValue,   
    [in]  ULONG       cchValue   
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `fd`  
 [in] Le jeton pour le champ cible.  
  
 `dwFieldFlags`  
 [in] Attributs de champ. Il s’agit d’un masque de bits de `CorFieldAttr` valeurs.  
  
 `dwCPlusTypeFlag`  
 [in] Le `ELEMENT_TYPE_` *\** pour la valeur de constante. Il s’agit d’un `CorElementType` valeur. Si une constante n’est pas définie, définissez cette valeur sur `ELEMENT_TYPE_END`.  
  
 `pValue`  
 [in] La valeur de constante pour le champ.  
  
 `cchValue`  
 [in] La taille, en caractères Unicode de `pValue`.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** utilisé en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [IMetaDataEmit, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [IMetaDataEmit2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
