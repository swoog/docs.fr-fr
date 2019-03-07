---
title: IMetaDataConverter::GetTypeLibFromMetaData, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataConverter.GetTypeLibFromMetaData
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataConverter::GetTypeLibFromMetaData
helpviewer_keywords:
- GetTypeLibFromMetaData method [.NET Framework metadata]
- IMetaDataConverter::GetTypeLibFromMetaData method [.NET Framework metadata]
ms.assetid: 90eab7b3-1fae-4af4-8bce-f7bc0e188a99
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9ab1d39ddb53e08e6fd36016f544162e2b11edb0
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57472068"
---
# <a name="imetadataconvertergettypelibfrommetadata-method"></a>IMetaDataConverter::GetTypeLibFromMetaData, méthode
Obtient un pointeur vers un `ITypeLib` instance qui représente la bibliothèque de types qui contient les noms de module et de bibliothèque spécifiés.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetTypeLibFromMetaData (  
    [in]  BSTR     strModule,   
    [in]  BSTR     strTlbName,   
    [out] ITypeLib **ppITL  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `strModule`  
 [in] Le nom du module de la bibliothèque de types.  
  
 `strTlbName`  
 [in] Le nom de la bibliothèque de types.  
  
 `ppITL`  
 [out] Un pointeur vers un emplacement qui reçoit l’adresse de la `ITypeLib` instance qui représente la bibliothèque de types.  
  
## <a name="requirements"></a>Spécifications  
 **Plateforme :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [IMetaDataConverter, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataconverter-interface.md)
