---
title: ICorProfilerCallback6::GetAssemblyReferences, méthode
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICorProfilerCallback6.GetAssemblyReferences
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
ms.assetid: 8b391afb-d79f-41bd-94ce-43ce62c6b5fc
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2c5296fbab71c67572718a58fedb9f89b064f816
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62041494"
---
# <a name="icorprofilercallback6getassemblyreferences-method"></a>ICorProfilerCallback6::GetAssemblyReferences, méthode
[Pris en charge dans .NET Framework 4.5.2 et ultérieur]  
  
 Notifie le profileur qu'un assembly en est au tout début du chargement, quand le CLR (Common Langage Runtime) effectue un parcours de fermeture de références d'assembly.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp
HRESULT GetAssemblyReferences(        [in, string] const WCHAR* wszAssemblyPath,  
        [in] ICorProfilerAssemblyReferenceProvider* pAsmRefProvider  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `wszAssemblyPath`  
 [en entrée] Le chemin d’accès et le nom de l’assembly dont les métadonnées seront modifiées.  
  
 `pAsmRefProvider`  
 [in] Un pointeur vers l’adresse d’un [ICorProfilerAssemblyReferenceProvider](../../../../docs/framework/unmanaged-api/profiling/icorprofilerassemblyreferenceprovider-interface.md) interface qui spécifie l’assembly fait référence à ajouter.  
  
## <a name="return-value"></a>Valeur de retour  
 Les valeurs retournées depuis ce rappel sont ignorées.  
  
## <a name="remarks"></a>Notes  
 Ce rappel est contrôlé en définissant le [COR_PRF_HIGH_ADD_ASSEMBLY_REFERENCES](../../../../docs/framework/unmanaged-api/profiling/cor-prf-high-monitor-enumeration.md) indicateur de masque d’événement lors de l’appel le [ICorProfilerCallback5::SetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md) (méthode). Si le profileur s’inscrit à la [ICorProfilerCallback6::GetAssemblyReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback6-getassemblyreferences-method.md) méthode de rappel, le runtime passe le chemin d’accès et le nom de l’assembly à charger, ainsi qu’un pointeur vers un [ ICorProfilerAssemblyReferenceProvider](../../../../docs/framework/unmanaged-api/profiling/icorprofilerassemblyreferenceprovider-interface.md) objet d’interface à cette méthode. Le profileur peut ensuite appeler la [ICorProfilerAssemblyReferenceProvider::AddAssemblyReference](../../../../docs/framework/unmanaged-api/profiling/icorprofilerassemblyreferenceprovider-addassemblyreference-method.md) méthode avec un `COR_PRF_ASSEMBLY_REFERENCE_INFO` objet pour chaque assembly cible qu’il prévoit de référencer à partir de l’assembly spécifié dans le `GetAssemblyReferences` rappel.  
  
 Utilisez le rappel de `GetAssemblyReferences` seulement si le profileur doit modifier les métadonnées d'un assembly pour y ajouter des références d'assembly. (Toutefois, notez que la modification réelle des métadonnées d’un assembly s’effectue dans le [ICorProfilerCallback::ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md)méthode de rappel.) Le profileur doit implémenter la méthode de rappel de `GetAssemblyReferences` pour informer le CLR que des références d'assembly seront ajoutées quand le module aura été chargé.  Ceci permet de s'assurer que les décisions de partage des assemblys prises par le CLR au cours de cette phase restent valides même si le profileur prévoit de modifier ultérieurement les références d'assembly des métadonnées.  Cela permet d'éviter certaines instances où les modifications des métadonnées du profileur provoquent une erreur `SECURITY_E_INCOMPATIBLE_SHARE`.  
  
 Le profileur utilise le [ICorProfilerAssemblyReferenceProvider](../../../../docs/framework/unmanaged-api/profiling/icorprofilerassemblyreferenceprovider-interface.md) objet fourni par cette méthode pour ajouter des références d’assembly à l’Analyseur de fermeture de référence assembly CLR.  Le [ICorProfilerAssemblyReferenceProvider](../../../../docs/framework/unmanaged-api/profiling/icorprofilerassemblyreferenceprovider-interface.md) objet doit être utilisé uniquement dans ce rappel. Les appels à la [ICorProfilerAssemblyReferenceProvider::AddAssemblyReference](../../../../docs/framework/unmanaged-api/profiling/icorprofilerassemblyreferenceprovider-addassemblyreference-method.md) méthode à partir de ce rappel n’entraînent pas de modification des métadonnées, mais uniquement dans un parcours de fermeture de référence assembly modifié. Le profileur doit donc utiliser un [IMetaDataAssemblyEmit](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md) objet à ajouter explicitement les références d’assembly depuis le [ICorProfilerCallback::ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md) rappel pour le référencement assembly, même s’il implémente la `GetAssemblyReferences` rappel.  
  
 Le profileur doit être prêt à recevoir des appels en doublon à ce rappel pour le même assembly et doit répondre de façon identique pour chaque appel en double (en effectuant le même ensemble de [ICorProfilerAssemblyReferenceProvider :: AddAssemblyReference](../../../../docs/framework/unmanaged-api/profiling/icorprofilerassemblyreferenceprovider-addassemblyreference-method.md) appels).  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorProfilerCallback6, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback6-interface.md)
- [ModuleLoadFinished, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md)
- [COR_PRF_ASSEMBLY_REFERENCE_INFO, structure](../../../../docs/framework/unmanaged-api/profiling/cor-prf-assembly-reference-info-structure.md)
- [ICorProfilerAssemblyReferenceProvider, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerassemblyreferenceprovider-interface.md)
