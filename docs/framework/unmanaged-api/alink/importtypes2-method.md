---
title: ImportTypes2, méthode
ms.date: 03/30/2017
api_name:
- IALink2.ImportTypes2
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ImportTypes2
helpviewer_keywords:
- ImportTypes2 method
ms.assetid: 32f3ba58-9695-41e9-ba58-fd19e45ed396
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f14822a58f3982d6f9fee1328c10b960657c056f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61753502"
---
# <a name="importtypes2-method"></a>ImportTypes2, méthode
Lance l’importation de types. Appelez cette méthode pour commencer l’importation de types de chaque portée importée par [ImportFile, méthode](../../../../docs/framework/unmanaged-api/alink/importfile-method.md).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT ImportTypes2(  
    mdAssembly AssemblyID,  
    mdToken FileToken,  
    DWORD dwScope,  
    HALINKENUM* phEnum,  
    IMetaDataImport2** ppImportScope,  
    DWORD* pdwCountOfTypes  
) PURE;  
```  
  
## <a name="parameters"></a>Paramètres  
 `AssemblyID`  
 ID de l’assembly dans lequel vous voulez importer.  
  
 `FileToken`  
 ID du fichier à partir duquel importer.  
  
 `dwScope`  
 Portée de base zéro à partir duquel importer.  
  
 `phEnum`  
 Reçoit le handle d’énumérateur pour les types dans l’étendue donnée.  
  
 `ppImportScope`  
 Si vous le souhaitez reçoit [IMetaDataImport2, Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md) interface.  
  
 `pdwCountOfTypes`  
 Si vous le souhaitez reçoit le nombre de types dans la portée spécifiée.  
  
## <a name="return-value"></a>Valeur de retour  
 Retourne S_OK si la méthode réussit.  
  
## <a name="requirements"></a>Configuration requise  
 Nécessite alink.h  
  
## <a name="see-also"></a>Voir aussi

- [IALink2, interface](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [IALink, interface](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [API ALink](../../../../docs/framework/unmanaged-api/alink/index.md)
