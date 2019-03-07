---
title: ImportTypes, méthode
ms.date: 03/30/2017
api_name:
- IALink.ImportTypes
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ImportTypes
helpviewer_keywords:
- ImportTypes method
ms.assetid: 351d4b4c-c939-486d-9471-51914a55f471
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 92dfc2bec33501a5cd9ca6b4ec4c3629b6d89946
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57487952"
---
# <a name="importtypes-method"></a>ImportTypes, méthode
Lance l’importation de types de chaque portée importée par [ImportFile, méthode](../../../../docs/framework/unmanaged-api/alink/importfile-method.md).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT ImportTypes(  
    mdAssembly AssemblyID,  
    mdToken FileToken,  
    DWORD dwScope,  
    HALINKENUM* phEnum,  
    IMetaDataImport** ppImportScope,  
    DWORD* pdwCountOfTypes  
) PURE;  
```  
  
## <a name="parameters"></a>Paramètres  
 `AssemblyID`  
 ID de l’assembly à importer dans.  
  
 `FileToken`  
 ID du fichier à importer à partir de.  
  
 `dwScope`  
 Portée de base zéro à importer.  
  
 `phEnum`  
 Reçoit le handle d’énumérateur pour les types dans cette portée.  
  
 `ppImportScope`  
 Si vous le souhaitez reçoit [IMetaDataImport Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) interface.  
  
 `pdwCountOfTypes`  
 Si vous le souhaitez reçoit le nombre de types dans la portée indiquée.  
  
## <a name="return-value"></a>Valeur de retour  
 Retourne S_OK si la méthode réussit.  
  
## <a name="requirements"></a>Spécifications  
 Nécessite alink.h  
  
## <a name="see-also"></a>Voir aussi
- [IALink, interface](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [IALink2, interface](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [API ALink](../../../../docs/framework/unmanaged-api/alink/index.md)
