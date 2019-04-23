---
title: ICorProfilerCallback3, interface
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback3
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback3
helpviewer_keywords:
- ICorProfilerCallback3 interface [.NET Framework profiling]
ms.assetid: be83af41-3dec-4c77-8529-9dd6b8042af6
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 66e6a67ce022365fa8c9e1005dfecbe4b23abd10
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59158378"
---
# <a name="icorprofilercallback3-interface"></a>ICorProfilerCallback3, interface
Fournit des méthodes de rappel que le common language runtime (CLR) utilise pour communiquer attachement et détachement des informations d’état au profileur.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[InitializeForAttach, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback3-initializeforattach-method.md)|Appelé par le CLR pour permettre au profileur d’initialiser son état après une opération d’attachement.|  
|[ProfilerAttachComplete, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback3-profilerattachcomplete-method.md)|Appelé par le CLR pour indiquer que le profileur peut maintenant appeler les méthodes de rattrapage.|  
|[ProfilerDetachSucceeded, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback3-profilerdetachsucceeded-method.md)|Indique au profileur que le Common Language Runtime (CLR) est sur le point de décharger sa DLL.|  
  
## <a name="remarks"></a>Notes  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de profilage](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [ICorProfilerInfo, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
- [ICorProfilerCallback2, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-interface.md)
- [ICorProfilerCallback4, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-interface.md)
