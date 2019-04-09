---
title: IMetaDataImport::EnumModuleRefs, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumModuleRefs
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumModuleRefs
helpviewer_keywords:
- EnumModuleRefs method [.NET Framework metadata]
- IMetaDataImport::EnumModuleRefs method [.NET Framework metadata]
ms.assetid: 53441f3a-68d2-477c-906e-37c55dfcfb4d
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d66d24da05bc3b8f0c3d0a828456d7c61613d219
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59188304"
---
# <a name="imetadataimportenummodulerefs-method"></a>IMetaDataImport::EnumModuleRefs, méthode
Énumère les jetons ModuleRef qui représentent des modules importés.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT EnumModuleRefs (  
   [in, out] HCORENUM     *phEnum,  
   [out]     mdModuleRef  rModuleRefs[],  
   [in]      ULONG        cMax,  
   [out]     ULONG        *pcModuleRefs  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `phEnum`  
 [in, out] Pointeur vers l’énumérateur. Cela doit être NULL pour le premier appel de cette méthode.  
  
 `rModuleRefs`  
 [out] Tableau utilisé pour stocker les jetons ModuleRef.  
  
 `cMax`  
 [in] Taille maximale du tableau `rModuleRefs`.  
  
 `pcModuleRefs`  
 [out] Le nombre de jetons ModuleRef retournés dans `rModuleRefs`.  
  
## <a name="return-value"></a>Valeur de retour  
  
|HRESULT|Description|  
|-------------|-----------------|  
|`S_OK`|`EnumModuleRefs` retourné avec succès.|  
|`S_FALSE`|Il n’existe pas de jetons à énumérer. Dans ce cas, `pcModuleRefs` est égal à zéro.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IMetaDataImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [IMetaDataImport2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
