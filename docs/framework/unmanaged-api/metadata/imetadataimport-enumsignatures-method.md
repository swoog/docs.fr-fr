---
title: IMetaDataImport::EnumSignatures, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumSignatures
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumSignatures
helpviewer_keywords:
- EnumSignatures method [.NET Framework metadata]
- IMetaDataImport::EnumSignatures method [.NET Framework metadata]
ms.assetid: d0d65060-6f90-42a2-95cf-6ffb04352996
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 193abe173b259ff2679642e229fce96151e37872
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59179676"
---
# <a name="imetadataimportenumsignatures-method"></a>IMetaDataImport::EnumSignatures, méthode
Énumère les jetons Signature représentant des signatures autonomes dans la portée actuelle.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT EnumSignatures (  
   [in, out] HCORENUM     *phEnum,  
   [out]     mdSignature  rSignatures[],  
   [in]      ULONG        cMax,  
   [out]     ULONG        *pcSignatures  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `phEnum`  
 [in, out] Pointeur vers l’énumérateur. Cela doit être NULL pour le premier appel de cette méthode.  
  
 `rSignatures`  
 [out] Tableau utilisé pour stocker les jetons de Signature.  
  
 `cMax`  
 [in] Taille maximale du tableau `rSignatures`.  
  
 `pcSignatures`  
 [out] Le nombre de jetons Signature retournés dans `rSignatures`.  
  
## <a name="return-value"></a>Valeur de retour  
  
|HRESULT|Description|  
|-------------|-----------------|  
|`S_OK`|`EnumSignatures` retourné avec succès.|  
|`S_FALSE`|Il n’existe pas de jetons à énumérer. Dans ce cas, `pcSignatures` est égal à zéro.|  
  
## <a name="remarks"></a>Notes  
 Les jetons de Signature sont créés par le [IMetaDataEmit::GetTokenFromSig](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-gettokenfromsig-method.md) (méthode).  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IMetaDataImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [IMetaDataImport2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
