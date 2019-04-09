---
title: IMetaDataAssemblyEmit::SetFileProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyEmit.SetFileProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyEmit::SetFileProps
helpviewer_keywords:
- IMetaDataAssemblyEmit::SetFileProps method [.NET Framework metadata]
- SetFileProps method [.NET Framework metadata]
ms.assetid: 85667d38-611c-45a9-938d-930ac7a7b681
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: fd0c2da234fa89bbf92c2117d6428d64502da0c5
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59208174"
---
# <a name="imetadataassemblyemitsetfileprops-method"></a>IMetaDataAssemblyEmit::SetFileProps, méthode
Modifie la structure de métadonnées `File` spécifiée.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT SetFileProps (  
    [in] mdFile        file,  
    [in] const void    *pbHashValue,   
    [in] ULONG         cbHashValue,  
    [in] DWORD         dwFileFlags  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `file`  
 [in] Le jeton de métadonnées qui spécifie le `File` structure des métadonnées à modifier.  
  
 `pbHashValue`  
 [in] Un pointeur vers les données de hachage associés au fichier.  
  
 `cbHashValue`  
 [in] La taille en octets de `pbHashValue`.  
  
 `dwFileFlags`  
 [in] Une combinaison au niveau du bit de [CorFileFlags](../../../../docs/framework/unmanaged-api/metadata/corfileflags-enumeration.md) valeurs qui spécifient différents attributs du fichier.  
  
## <a name="remarks"></a>Notes  
 Pour créer un `File` structure des métadonnées, utilisez le [IMetaDataAssemblyEmit::DefineFile](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md) (méthode).  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IMetaDataAssemblyEmit, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md)
