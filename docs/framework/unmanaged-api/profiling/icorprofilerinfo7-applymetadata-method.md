---
title: ICorProfilerInfo7::ApplyMetaData (méthode)
ms.date: 02/15/2019
dev_langs:
- cpp
api_name:
- ICorProfilerInfo7.ApplyMetaData
api_location:
- mscorwks.dll
api_type:
- COM
ms.assetid: a1bfb649-4584-4d35-b3e6-8fe59b53992a
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8f261b02dd19ead0d6803cae543f39a06c99f033
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64586698"
---
# <a name="icorprofilerinfo7applymetadata-method"></a>ICorProfilerInfo7::ApplyMetaData (méthode)
[Prise en charge dans le .NET Framework 4.6.1 et versions ultérieures]  
  
 Applique les métadonnées qui vient d’être définie par le `IMetadataEmit::Define*` méthodes à un module spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp
HRESULT ApplyMetaData(  
        [in] ModuleID moduleID  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `moduleID`  
 [in] L’identificateur du module dont les métadonnées a été modifiée.  
  
## <a name="remarks"></a>Notes  
 Si des modifications de métadonnées sont apportées après le [ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md) rappel, vous devez appeler cette méthode avant d’utiliser les nouvelles métadonnées.  
  
 `ApplyMetaData` prend uniquement en charge l’ajout de types de métadonnées suivants :  
  
- `AssemblyRef` les enregistrements, vous créez en appelant le [IMetaDataAssemblyEmit::DefineAssemblyRef](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineassemblyref-method.md). .  
  
- `TypeRef` les enregistrements, vous créez en appelant le [IMetaDataEmit::DefineTypeRefByName](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definetyperefbyname-method.md) (méthode).  
  
- `TypeSpec` les enregistrements, vous créez en appelant le [IMetaDataEmit::GetTokenFromTypeSpec](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-gettokenfromtypespec-method.md) (méthode).  
  
- `MemberRef` les enregistrements, vous créez en appelant le [IMetaDataEmit::DefineMemberRef](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definememberref-method.md) (méthode).  
  
- `MemberSpec` les enregistrements, vous créez en appelant le [IMetaDataEmit2::DefineMethodSpec](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-definemethodspec-method.md) (méthode).  
  
- `UserString` les enregistrements, vous créez en appelant le [IMetaDataEmit::DefineUserString](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineuserstring-method.md) (méthode).  

En commençant par .NET Core 3.0, `ApplyMetaData` prend également en charge les types suivants :

- `TypeDef` les enregistrements, vous créez en appelant le [IMetaDataEmit::DefineTypeDef](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definetypedef-method.md) (méthode).

- `MethodDef` les enregistrements, vous créez en appelant le [IMetaDataEmit::DefineMethod](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-definemethod-method.md) (méthode). Toutefois, l’ajout de méthodes virtuelles à un type existant n’est pas pris en charge. Méthodes virtuelles doivent être ajoutés avant le [ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md) rappel.

## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorProfilerInfo7, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-interface.md)
