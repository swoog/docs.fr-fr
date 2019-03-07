---
title: ICorProfilerInfo::GetModuleMetaData, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetModuleMetaData
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetModuleMetaData
helpviewer_keywords:
- GetModuleMetaData method [.NET Framework profiling]
- ICorProfilerInfo::GetModuleMetaData method [.NET Framework profiling]
ms.assetid: 7a439d92-348a-44dd-b60f-cad7cba56379
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 45795d4f3c0d043a46a750312484b93407ae8434
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57471548"
---
# <a name="icorprofilerinfogetmodulemetadata-method"></a>ICorProfilerInfo::GetModuleMetaData, méthode
Obtient une instance d’interface de métadonnées qui mappe au module spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetModuleMetaData(  
    [in]  ModuleID moduleId,  
    [in]  DWORD    dwOpenFlags,  
    [in]  REFIID   riid,  
    [out] IUnknown **ppOut);  
```  
  
## <a name="parameters"></a>Paramètres  
 `moduleId`  
 [in] L’ID du module à laquelle l’instance d’interface sera mappée.  
  
 `dwOpenFlags`  
 [in] Une valeur de la [CorOpenFlags](../../../../docs/framework/unmanaged-api/metadata/coropenflags-enumeration.md) énumération qui spécifie le mode d’ouverture des fichiers manifestes. Uniquement les `ofRead`, `ofWrite` et `ofNoTransform` bits sont valides.  
  
 `riid`  
 [in] La référence de ID (GUID) de l’interface de métadonnées dont l’instance sera récupérée. Consultez [Interfaces de métadonnées](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md) pour obtenir la liste des interfaces.  
  
 `ppOut`  
 [out] Pointeur vers l’adresse de l’instance d’interface de métadonnées.  
  
## <a name="remarks"></a>Notes  
 Allez-vous peut-être me demander pour les métadonnées à ouvrir en mode lecture/écriture, mais cela entraîne l’exécution des métadonnées plus lente du programme, car les modifications apportées aux métadonnées ne peut pas être optimisée comme il s’agissait de la compilation.  
  
 Certains modules (par exemple, des modules de ressources) ont pas de métadonnées. Dans ce cas, `GetModuleMetaData` retournera une valeur HRESULT S_FALSE, et une valeur null dans *`ppOut`.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICorProfilerInfo, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
