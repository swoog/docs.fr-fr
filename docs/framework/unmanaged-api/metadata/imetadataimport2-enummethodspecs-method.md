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
ms.openlocfilehash: 4d660deb69e694a70a140b6d00c355442e3c5094
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54558903"
---
# <a name="imetadataimport2enummethodspecs-method"></a>IMetaDataImport2::EnumMethodSpecs, méthode
Obtient un énumérateur pour un tableau de jetons MethodSpec associé à le MethodDef ou MemberRef spécifié de jeton.  
  
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
 [in, out] Un pointeur vers l’énumérateur pour `rMethodSpecs`.  
  
 `tk`  
 [in] Le jeton MemberRef ou MethodDef qui représente la méthode dont les jetons MethodSpec doivent être énumérés. Si la valeur de `tk` est 0 (zéro), tous les jetons MethodSpec dans la portée seront énumérés.  
  
 `rMethodSpecs`  
 [out] Le tableau de jetons MethodSpec à énumérer.  
  
 `cMax`  
 [in] Le nombre maximal demandé de jetons à placer dans `rMethodSpecs`.  
  
 `pcMethodSpecs`  
 [out] Le nombre retourné de jetons placés dans `rMethodSpecs`.  
  
## <a name="return-value"></a>Valeur de retour  
  
|HRESULT|Description|  
|-------------|-----------------|  
|`S_OK`|`EnumMethodSpecs` retourné avec succès.|  
|`S_FALSE`|`phEnum` ne contient aucun élément de membre. Dans ce cas, `pcMethodSpecs` est définie sur 0 (zéro).|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [IMetaDataImport2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
- [IMetaDataImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
