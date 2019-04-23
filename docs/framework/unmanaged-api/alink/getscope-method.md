---
title: GetScope, méthode
ms.date: 03/30/2017
api_name:
- IALink.GetScope
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- GetScope
helpviewer_keywords:
- GetScope method
ms.assetid: e1555328-2c71-4ece-b357-9eb6d3a8efc4
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 571612796d4e66be9dd8469d748c2380c839ddfa
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59165779"
---
# <a name="getscope-method"></a>GetScope, méthode
Obtient une portée d’importation.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetScope(  
    mdAssembly AssemblyID,  
    mdToken FileToken,  
    DWORD dwScope,  
    IMetaDataImport** ppImportScope  
) PURE;  
```  
  
## <a name="parameters"></a>Paramètres  
 `AssemblyID`  
 ID unique de l’assembly dans lequel importer.  
  
 `FileToken`  
 ID unique du fichier à importer à partir de.  
  
 `dwScope`  
 Portée de base zéro à importer.  
  
 `ppImportScope`  
 Reçoit [IMetaDataImport Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) interface pour l’étendue.  
  
## <a name="return-value"></a>Valeur de retour  
 Retourne S_OK si la méthode réussit.  
  
## <a name="requirements"></a>Configuration requise  
 Nécessite alink.h  
  
## <a name="see-also"></a>Voir aussi

- [IALink, interface](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [IALink2, interface](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [API ALink](../../../../docs/framework/unmanaged-api/alink/index.md)
