---
title: IMetaDataImport2::EnumMethodSpecs, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport2.EnumMethodSpecs
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport2::EnumMethodSpecs
helpviewer_keywords:
- IMetaDataImport2::EnumMethodSpecs method [.NET Framework metadata]
- EnumMethodSpecs method [.NET Framework metadata]
ms.assetid: b3fc1e6c-bcb6-4915-baf8-7dc0a31b8724
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6c2122c06c6e4f1137173f02e37fb0982864e7ec
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="imetadataimport2enummethodspecs-method"></a>IMetaDataImport2::EnumMethodSpecs, méthode
Obtient un énumérateur pour un tableau de jetons MethodSpec associé MethodDef ou MemberRef spécifié de jeton.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT EnumMethodSpecs (  
    [in, out] HCORENUM      *phEnum,   
    [in]      mdToken       tk,  
    [out]     mdMethodSpec  rMethodSpecs[],  
    [in]      ULONG         cMax,  
    [out]     ULONG         *pcMethodSpecs  
);   
```  
  
#### <a name="parameters"></a>Paramètres  
 `phEnum`  
 [dans, out] Un pointeur vers l’énumérateur pour `rMethodSpecs`.  
  
 `tk`  
 [in] Jeton MemberRef ou MethodDef qui représente la méthode dont les jetons MethodSpec doivent être énumérés. Si la valeur de `tk` est 0 (zéro), tous les jetons MethodSpec dans la portée seront énumérés.  
  
 `rMethodSpecs`  
 [out] Tableau de jetons MethodSpec à énumérer.  
  
 `cMax`  
 [in] Nombre maximal demandé de jetons à placer dans `rMethodSpecs`.  
  
 `pcMethodSpecs`  
 [out] Le nombre retourné de jetons placé dans `rMethodSpecs`.  
  
## <a name="return-value"></a>Valeur de retour  
  
|HRESULT|Description|  
|-------------|-----------------|  
|`S_OK`|`EnumMethodSpecs` retourné avec succès.|  
|`S_FALSE`|`phEnum` ne contient aucun élément de membre. Dans ce cas, `pcMethodSpecs` est définie sur 0 (zéro).|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [IMetaDataImport2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)  
 [IMetaDataImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
