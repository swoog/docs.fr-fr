---
title: IMetaDataConverter::GetMetaDataFromTypeInfo, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataConverter.GetMetaDataFromTypeInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataConverter::GetMetaDataFromTypeInfo
helpviewer_keywords:
- GetMetaDataFromTypeInfo method [.NET Framework metadata]
- IMetaDataConverter::GetMetaDataFromTypeInfo method [.NET Framework metadata]
ms.assetid: d44484bb-23a3-49c3-9e46-69d0d9ab4f0f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b87bc814179b35f594ec8fab812055ff0182c5c3
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59145845"
---
# <a name="imetadataconvertergetmetadatafromtypeinfo-method"></a>IMetaDataConverter::GetMetaDataFromTypeInfo, méthode
Obtient un pointeur vers un [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) instance qui représente la signature de métadonnées de la bibliothèque de types référencée par le `ITypeInfo` instance.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetMetaDataFromTypeInfo (  
    [in]  ITypeInfo         *pITI,  
    [out] IMetaDataImport   **ppMDI  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pITI`  
 [in] Un pointeur vers un `ITypeInfo` objet qui fait référence à la bibliothèque de types.  
  
 `ppMDI`  
 [out] Un pointeur vers un emplacement qui reçoit l’adresse de la `IMetaDataImport` instance qui représente la signature de métadonnées.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateforme :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IMetaDataEmit, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [IMetaDataImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
