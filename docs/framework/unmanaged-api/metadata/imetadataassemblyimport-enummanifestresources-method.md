---
title: IMetaDataAssemblyImport::EnumManifestResources, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.EnumManifestResources
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::EnumManifestResources
helpviewer_keywords:
- IMetaDataAssemblyImport::EnumManifestResources method [.NET Framework metadata]
- EnumManifestResources method [.NET Framework metadata]
ms.assetid: 9543b111-5705-40c9-935c-a3ffc7a581aa
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 707e482a6952ee1266950dc181fbc85e5d6ef398
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33448053"
---
# <a name="imetadataassemblyimportenummanifestresources-method"></a>IMetaDataAssemblyImport::EnumManifestResources, méthode
Obtient un pointeur vers un énumérateur pour les ressources référencées dans le manifeste d’assembly actuel.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT EnumManifestResources (  
    [in, out] HCORENUM         *phEnum,   
    [out] mdManifestResource   rManifestResources[],   
    [in]  ULONG                cMax,   
    [out] ULONG                *pcTokens  
);   
```  
  
#### <a name="parameters"></a>Paramètres  
 `phEnum`  
 [dans, out] Pointeur vers l’énumérateur. Cela doit être une valeur null lorsque la valeur du `EnumManifestResources` méthode est appelée pour la première fois.  
  
 `rManifestResources`  
 [out] Tableau utilisé pour stocker le `mdManifestResource` des jetons de métadonnées.  
  
 `cMax`  
 [in] Le nombre maximal de `mdManifestResource` jetons qui peuvent être placés dans `rManifestResources`.  
  
 `pcTokens`  
 [out] Le nombre de `mdManifestResource` jetons placés dans `rManifestResources`.  
  
## <a name="return-value"></a>Valeur de retour  
  
|HRESULT|Description|  
|-------------|-----------------|  
|`S_OK`|`EnumManifestResources` retourné avec succès.|  
|`S_FALSE`|Il n’existe pas de jetons à énumérer. Dans ce cas, `pcTokens` est définie sur zéro.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [IMetaDataAssemblyImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)
