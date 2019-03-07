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
ms.openlocfilehash: a13e750029fed2f2261064dd69d6c1d800d59989
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57473901"
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
  
## <a name="parameters"></a>Paramètres  
 `phEnum`  
 [in, out] Pointeur vers l’énumérateur. Cela doit être une valeur null valeur lorsque le `EnumManifestResources` méthode est appelée pour la première fois.  
  
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
|`S_FALSE`|Il n’existe pas de jetons à énumérer. Dans ce cas, `pcTokens` est défini à zéro.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [IMetaDataAssemblyImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)
