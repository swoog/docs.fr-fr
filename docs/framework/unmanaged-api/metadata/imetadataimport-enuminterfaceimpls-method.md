---
title: IMetaDataImport::EnumInterfaceImpls, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumInterfaceImpls
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumInterfaceImpls
helpviewer_keywords:
- IMetaDataImport::EnumInterfaceImpls method [.NET Framework metadata]
- EnumInterfaceImpls method [.NET Framework metadata]
ms.assetid: ba6e178f-128b-4e47-a13c-b4be73eb106c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f6e4be2e05c573ec93cc23c8dd6eccc834b8b848
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59136498"
---
# <a name="imetadataimportenuminterfaceimpls-method"></a>IMetaDataImport::EnumInterfaceImpls, méthode
Énumère toutes les interfaces implémentées par le `TypeDef`. 
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT EnumInterfaceImpls (  
   [in, out]  HCORENUM       *phEnum,   
   [in]   mdTypeDef          td,  
   [out]  mdInterfaceImpl    rImpls[],   
   [in]   ULONG              cMax,  
   [out]  ULONG*             pcImpls  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `phEnum`  
 [in, out] Pointeur vers l’énumérateur.  
  
 `td`  
 [in] Le jeton du TypeDef dont les jetons MethodDef représentant des implémentations d’interface doivent être énumérés.  
  
 `rImpls`  
 [out] Tableau utilisé pour stocker les jetons MethodDef.  
  
 `cMax`  
 [in] Taille maximale du tableau `rImpls`.  
  
 `pcImpls`  
 [out] Le nombre réel de jetons retournés dans `rImpls`.  
  
## <a name="return-value"></a>Valeur de retour  
  
|HRESULT|Description|  
|-------------|-----------------|  
|`S_OK`|`EnumInterfaceImpls` retourné avec succès.|  
|`S_FALSE`|Il n’y a aucune jetons MethodDef à énumérer. Dans ce cas, `pcImpls` est défini à zéro.|  

## <a name="remarks"></a>Notes

L’énumération retourne une collection de `mdInterfaceImpl` jetons pour chaque interface implémentée par le `TypeDef`. Interface jetons sont retournés dans l’ordre les interfaces ont été spécifiés (via `DefineTypeDef` ou `SetTypeDefProps`). Propriétés de retourné `mdInterfaceImpl` jetons peuvent être interrogées à l’aide de [GetInterfaceImplProps](imetadataimport-getinterfaceimplprops-method.md).
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IMetaDataImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [IMetaDataImport2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
