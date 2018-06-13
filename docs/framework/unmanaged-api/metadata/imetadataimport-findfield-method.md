---
title: IMetaDataImport::FindField, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.FindField
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::FindField
helpviewer_keywords:
- IMetaDataImport::FindField method [.NET Framework metadata]
- FindField method [.NET Framework metadata]
ms.assetid: 38cd4e16-fbb2-471c-aa73-ac51a1931ad2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ac69bab45ccd39b6a055fe4d2f74950ab47da779
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33447030"
---
# <a name="imetadataimportfindfield-method"></a>IMetaDataImport::FindField, méthode
Obtient un pointeur vers le FieldDef jeton pour le champ est placé entre la <xref:System.Type> et qui possède la signature de nom et de métadonnées spécifiée.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT FindField (  
   [in]  mdTypeDef         td,  
   [in]  LPCWSTR           szName,  
   [in]  PCCOR_SIGNATURE   pvSigBlob,  
   [in]  ULONG             cbSigBlob,  
   [out] mdFieldDef        *pmb  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `td`  
 [in] Le jeton TypeDef pour la classe ou interface qui définit le champ à rechercher. Si cette valeur est `mdTokenNil`, la recherche est effectuée pour une variable globale.  
  
 `szName`  
 [in] Le nom du champ à rechercher.  
  
 `pvSigBlob`  
 [in] Pointeur vers la signature de métadonnées binaires du champ.  
  
 `cbSigBlob`  
 [in] La taille en octets de `pvSigBlob`.  
  
 `pmb`  
 [out] Pointeur vers le jeton FieldDef correspondant.  
  
## <a name="remarks"></a>Notes  
 Vous spécifiez le champ à l’aide de son interface ou la classe englobante (`td`), son nom (`szName`) et éventuellement de sa signature (`pvSigBlob`).  
  
 La signature passée à `FindField` doit avoir été générée dans la portée actuelle, car les signatures sont liées à une étendue spécifique. Une signature peut incorporer un jeton qui identifie le type de valeur ou de la classe englobant. (Le jeton est un index dans la table TypeDef locale). Vous ne peut pas générer une signature d’exécution en dehors du contexte de la portée actuelle et utiliser cette signature comme entrée pour `FindField`.  
  
 `FindField` recherche uniquement les champs qui ont été définis directement dans la classe ou interface ; Il ne trouve pas les champs hérités.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [IMetaDataImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [IMetaDataImport2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
