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
ms.openlocfilehash: 0bdd5e92ce7423fbbe0708f8a35368b871508a70
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54493428"
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
 [in] Le jeton de métadonnées qui spécifie le `ExportedType` structure des métadonnées à modifier.  
  
 `tkImplementation`  
 [in] Le jeton, de type `File`, `AssemblyRef`, ou `ExportedType`, qui spécifie la façon dont ce type est implémenté.  
  
 `tkTypeDef`  
 [in] Le `TypeDef` jeton référencé dans le fichier de code.  
  
 `dwExportedTypeFlags`  
 [in] Combinaison de bits de valeurs qui spécifient les attributs du type.  
  
## <a name="remarks"></a>Notes  
 Pour créer un `ExportedType` structure des métadonnées, utilisez le [IMetaDataAssemblyEmit::DefineExportedType](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineexportedtype-method.md) (méthode).  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [IMetaDataAssemblyEmit, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md)
