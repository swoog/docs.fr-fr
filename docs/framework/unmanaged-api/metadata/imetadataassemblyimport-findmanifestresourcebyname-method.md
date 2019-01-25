---
title: IMetaDataAssemblyImport::FindManifestResourceByName, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.FindManifestResourceByName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::FindManifestResourceByName
helpviewer_keywords:
- FindManifestResourceByName method [.NET Framework metadata]
- IMetaDataAssemblyImport::FindManifestResourceByName method [.NET Framework metadata]
ms.assetid: 7b72fa11-3866-402b-bdea-2b966b77cfe0
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b05c9a75bf870dd3b2316d2df7c50932b26894f3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54702741"
---
# <a name="imetadataassemblyimportfindmanifestresourcebyname-method"></a>IMetaDataAssemblyImport::FindManifestResourceByName, méthode
Obtient un pointeur vers la ressource de manifeste avec le nom spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT FindManifestResourceByName (  
    [in]  LPCWSTR                szName,   
    [out] mdManifestResource     *ptkManifestResource  
);   
```  
  
#### <a name="parameters"></a>Paramètres  
 `szName`  
 [in] Le nom de la ressource.  
  
 `ptkManifestResource`  
 [out] Tableau utilisé pour stocker le `mdManifestResource` des jetons de métadonnées, chacun représentant une ressource de manifeste.  
  
## <a name="remarks"></a>Notes  
 Le `FindManifestResourceByName` méthode utilise les règles standards employées par le common language runtime pour la résolution des références.  
  
## <a name="requirements"></a>Spécifications  
 **Plateforme :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [IMetaDataAssemblyImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)
- [Méthode de localisation des assemblys par le runtime](../../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md)
