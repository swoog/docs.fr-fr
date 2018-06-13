---
title: IMetaDataImport::GetClassLayout, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetClassLayout
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetClassLayout
helpviewer_keywords:
- IMetaDataImport::GetClassLayout method [.NET Framework metadata]
- GetClassLayout method, IMetaDataImport interface [.NET Framework metadata]
ms.assetid: 8f35414d-f40b-4b99-8768-9adb675c622a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b031fc35a4687a8535e3cb5e9ef2a53bab9fe376
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33445505"
---
# <a name="imetadataimportgetclasslayout-method"></a>IMetaDataImport::GetClassLayout, méthode
Obtient les informations de disposition pour la classe référencée par le jeton TypeDef spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetClassLayout  (   
   [in]  mdTypeDef          td,   
   [out] DWORD              *pdwPackSize,  
   [out] COR_FIELD_OFFSET   rFieldOffset[],  
   [in]  ULONG              cMax,  
   [out] ULONG              *pcFieldOffset,  
   [out] ULONG              *pulClassSize  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `td`  
 [in] Le jeton TypeDef pour la classe avec la disposition à retourner.  
  
 `pdwPackSize`  
 [out] Une des valeurs 1, 2, 4, 8 ou 16, qui représente la taille de pack de la classe.  
  
 `rFieldOffset`  
 [out] Un tableau de [COR_FIELD_OFFSET](../../../../docs/framework/unmanaged-api/metadata/cor-field-offset-structure.md) valeurs.  
  
 `cMax`  
 [in] Taille maximale du tableau `rFieldOffset`.  
  
 `pcFieldOffset`  
 [out] Le nombre d’éléments retournés dans `rFieldOffset`.  
  
 `pulClassSize`  
 [out] La taille en octets de la classe représentée par `td`.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [IMetaDataImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [IMetaDataImport2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
