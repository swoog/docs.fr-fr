---
title: ImportFile, méthode
ms.date: 03/30/2017
api_name:
- IALink.ImportFile
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ImportFile
helpviewer_keywords:
- ImportFile method
ms.assetid: bcbe321f-b83a-4e9a-9f10-8d913e244dc9
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 69e48c6c3179ced167fdc39ae4df859f161727ec
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59077249"
---
# <a name="importfile-method"></a>ImportFile, méthode
Importe des assemblys et modules indépendants.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT ImportFile(  
    LPCWSTR pszFilename,  
    LPCWSTR pszTargetName,  
    BOOL fSmartImport,  
    mdToken* pImportToken,  
    IMetaDataAssemblyImport** ppAssemblyScope,  
    DWORD* pdwCountOfScopes  
) PURE;  
```  
  
## <a name="parameters"></a>Paramètres  
 `pszFilename`  
 Nom qualifié complet du fichier à importer.  
  
 `pszTargetName`  
 Nom de fichier de sortie facultatif qui peut être utilisé pour renommer le fichier car il est lié dans l’assembly.  
  
 `fSmartImport`  
 Si la valeur est TRUE, ImportTypes est utilisé, sinon l’importation doit être effectuée manuellement.  
  
 `pImportToken`  
 Pointeur vers le jeton où un ID de fichier unique sera stocké. Le fichier peut être un assembly ou un fichier.  
  
 `ppAssemblyScope`  
 Reçoit le pointeur vers [IMetaDataAssemblyImport, Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md). Peut être NULL si le fichier n'est pas un assembly.  
  
 `pdwCountOfScopes`  
 Pointeur vers le nombre de fichiers et/ou des étendues qui ont été importés.  
  
## <a name="return-value"></a>Valeur de retour  
 Retourne S_OK si la méthode réussit.  
  
## <a name="requirements"></a>Configuration requise  
 Nécessite alink.h  
  
## <a name="see-also"></a>Voir aussi

- [IALink, interface](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [IALink2, interface](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [API ALink](../../../../docs/framework/unmanaged-api/alink/index.md)
