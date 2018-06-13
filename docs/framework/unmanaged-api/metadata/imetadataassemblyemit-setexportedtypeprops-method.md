---
title: IMetaDataAssemblyEmit::SetExportedTypeProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyEmit.SetExportedTypeProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyEmit::SetExportedTypeProps
helpviewer_keywords:
- SetExportedTypeProps method [.NET Framework metadata]
- IMetaDataAssemblyEmit::SetExportedTypeProps method [.NET Framework metadata]
ms.assetid: 1c090153-fd5f-46c7-9cff-39a78d992c8f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 8643a4d207fb570195caa00a1ac659c78c2ff2b8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33445064"
---
# <a name="imetadataassemblyemitsetexportedtypeprops-method"></a>IMetaDataAssemblyEmit::SetExportedTypeProps, méthode
Modifie la structure de métadonnées `ExportedType` spécifiée.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT SetExportedTypeProps (  
    [in] mdExportedType   ct,   
    [in] mdToken          tkImplementation,  
    [in] mdTypeDef        tkTypeDef,  
    [in] DWORD            dwExportedTypeFlags  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `ct`  
 [in] Le jeton de métadonnées qui spécifie le `ExportedType` structure de métadonnées.  
  
 `tkImplementation`  
 [in] Le jeton, de type `File`, `AssemblyRef`, ou `ExportedType`, qui spécifie la façon dont ce type est implémenté.  
  
 `tkTypeDef`  
 [in] Le `TypeDef` jeton référencé dans le fichier de code.  
  
 `dwExportedTypeFlags`  
 [in] Combinaison de bits de valeurs qui spécifient les attributs du type.  
  
## <a name="remarks"></a>Notes  
 Pour créer un `ExportedType` structure des métadonnées, utilisez le [IMetaDataAssemblyEmit::DefineExportedType](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineexportedtype-method.md) (méthode).  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [IMetaDataAssemblyEmit, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md)
