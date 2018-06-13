---
title: IMetaDataImport::EnumFieldsWithName, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumFieldsWithName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumFieldsWithName
helpviewer_keywords:
- IMetaDataImport::EnumFieldsWithName method [.NET Framework metadata]
- EnumFieldsWithName method [.NET Framework metadata]
ms.assetid: 42145e8d-000f-4d0b-ae43-c08201190fa2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6ed8bbbd9699fe707d638bb8d07064e508b6f2fb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33447770"
---
# <a name="imetadataimportenumfieldswithname-method"></a>IMetaDataImport::EnumFieldsWithName, méthode
Énumère les jetons FieldDef du type spécifié avec le nom spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT EnumFieldsWithName (  
   [in, out] HCORENUM    *phEnum,   
   [in]  mdTypeDef       cl,   
   [in]  LPCWSTR         szName,   
   [out] mdFieldDef      rFields[],   
   [in]  ULONG           cMax,   
   [out] ULONG           *pcTokens   
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `phEnum`  
 [dans, out] Pointeur vers l’énumérateur.  
  
 `cl`  
 [in] Le jeton du type dont les champs doivent être énumérés.  
  
 `szName`  
 [in] Le nom du champ qui limite la portée de l’énumération.  
  
 `rFields`  
 [out] Tableau utilisé pour stocker les jetons FieldDef.  
  
 `cMax`  
 [in] Taille maximale du tableau `rFields`.  
  
 `pcTokens`  
 [out] Le nombre réel de jetons FieldDef retournés dans `rFields`.  
  
## <a name="remarks"></a>Notes  
 Contrairement aux [IMetaDataImport::EnumFields](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-enumfields-method.md), `EnumFieldsWithName` ignore tous les jetons de champ qui n’ont pas le nom spécifié.  
  
## <a name="return-value"></a>Valeur de retour  
  
|HRESULT|Description|  
|-------------|-----------------|  
|`S_OK`|`EnumFieldsWithName` retourné avec succès.|  
|`S_FALSE`|Il n’existe pas de champs à énumérer. Dans ce cas, `pcTokens` est égal à zéro.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [IMetaDataImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [IMetaDataImport2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
