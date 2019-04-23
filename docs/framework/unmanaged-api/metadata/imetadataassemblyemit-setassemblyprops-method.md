---
title: IMetaDataAssemblyEmit::SetAssemblyProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyEmit.SetAssemblyProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyEmit::SetAssemblyProps
helpviewer_keywords:
- SetAssemblyProps method [.NET Framework metadata]
- IMetaDataAssemblyEmit::SetAssemblyProps method [.NET Framework metadata]
ms.assetid: 91b633d7-9e75-43c3-a8d2-2144984e5f9e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 3361212f9a7f7ff0739e8544419a2b67abc8f457
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59214648"
---
# <a name="imetadataassemblyemitsetassemblyprops-method"></a>IMetaDataAssemblyEmit::SetAssemblyProps, méthode
Modifie la structure de métadonnées `Assembly` spécifiée.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT SetAssemblyProps (  
    [in] mdAssembly               pma,  
    [in] const void               *pbPublicKey,  
    [in] ULONG                    cbPublicKey,  
    [in] ULONG                    ulHashAlgId,  
    [in] LPCWSTR                  szName,  
    [in] const ASSEMBLYMETADATA   *pMetaData,  
    [in] DWORD                    dwAssemblyFlags  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pma`  
 [in] Le jeton de métadonnées qui spécifie le `Assembly` structure des métadonnées à modifier.  
  
 `pbPublicKey`  
 [in] Pointeur vers la clé publique du serveur de publication de l’assembly.  
  
 `cbPublicKey`  
 [in] La taille en octets de `pbPublicKey`.  
  
 `ulHashAlgId`  
 [in] L’identificateur pour l’algorithme de hachage utilisé pour hacher les fichiers d’assembly.  
  
 `szName`  
 [in] Le nom lisible de l’assembly.  
  
 `pMetaData`  
 [in] Pointeur vers le ASSEMBLYMETADATA qui contient des informations de version, la plateforme et aux paramètres régionaux de l’assembly.  
  
 `dwAssemblyFlags`  
 [in] Une combinaison au niveau du bit de [AssemblyFlags](../../../../docs/framework/unmanaged-api/metadata/assemblyflags-enumeration.md) valeurs qui spécifient différents attributs de l’assembly.  
  
## <a name="remarks"></a>Notes  
 Pour créer un `Assembly` structure des métadonnées, utilisez le [IMetaDataAssemblyEmit::DefineAssembly](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineassembly-method.md) (méthode).  
  
## <a name="requirements"></a>Configuration requise  
 **Plateforme :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IMetaDataAssemblyEmit, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md)
