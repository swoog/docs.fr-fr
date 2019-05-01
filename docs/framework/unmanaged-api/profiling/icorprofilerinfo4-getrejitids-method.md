---
title: ICorProfilerInfo4::GetReJITIDs, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo4.GetReJITIDs
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo4::GetReJITIDs
helpviewer_keywords:
- GetReJITIDs method, ICorProfilerInfo4 interface [.NET Framework profiling]
- ICorProfilerInfo4::GetReJITIDs method [.NET Framework profiling]
ms.assetid: 634ac28c-a5b7-4fc3-af84-256c24ca8177
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9d2d48e5fb070ec0334de579d2e28146177a87b1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62049477"
---
# <a name="icorprofilerinfo4getrejitids-method"></a>ICorProfilerInfo4::GetReJITIDs, méthode
Retourne un tableau d’ID qui identifient tous les-recompilée juste les versions de la fonction spécifiée qui sont toujours allouées. Cela inclut-recompilée juste les versions de fonctions qui ont été annulées par la suite, mais pas encore libérées (par exemple, lorsque le domaine d’application qui contient la fonction de restauration est en cours d’utilisation).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetReJITIDs (  
     [in]  FunctionID          functionId,  
     [in]  ULONG               cReJitIds,  
     [out] ULONG *             pcReJitIds,  
     [out, size_is(cReJitIds), length_is(*pcReJitIds)]   ReJITID        reJitIds[]);  
```  
  
## <a name="parameters"></a>Paramètres  
 `functionId`  
 [in] Le `FunctionID` de l’instance de fonction pour lequel énumérer des versions.  
  
 `cReJitIds`  
 [in] Le nombre d’ID recompilée juste alloués dans le `reJitIds` tableau.  
  
 `pcReJitIds`  
 [out] Le nombre réel d’ID recompilé de JIT.  
  
 `reJitIds`  
 [out] Tableau alloué par l’appelant qui contiendra les ID recompilée juste pour la fonction spécifiée.  
  
## <a name="remarks"></a>Notes  
 `GetReJITIDs` énumère les ID recompilée juste actives pour une instance de la fonction donnée. Il suit le même modèle d’utilisation en tant qu’autre `ICorProfilerInfo` fonctions qui acceptent les mémoires tampons allouées par l’appelant.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorProfilerInfo4, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-interface.md)
- [Interfaces de profilage](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [Profilage](../../../../docs/framework/unmanaged-api/profiling/index.md)
