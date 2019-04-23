---
title: ICorProfilerCallback9, interface
ms.date: 04/10/2018
api_name:
- ICorProfilerCallback9
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e1711def5e2aa41fd63912361ef8250ad160fb88
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59227754"
---
# <a name="icorprofilercallback9-interface"></a>ICorProfilerCallback9, interface
[Pris en charge dans le .NET Framework 4.7.2 et versions ultérieures]  

 Une sous-classe de [ICorProfilerCallback8](icorprofilercallback8-interface.md) qui fournit une méthode de rappel utilisée par le common language runtime pour informer le profileur qu’une méthode dynamique a été garbage collectées et déchargé par la suite.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[DynamicMethodUnloaded, méthode](ICorProfilerCallback9-dynamicmethodunloaded-method.md)|Notifie le profileur qu’une méthode dynamique a été garbage collectées et déchargé par la suite.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  

## <a name="see-also"></a>Voir aussi

- [Interfaces de profilage](profiling-interfaces.md)
- [ICorProfilerCallback8, interface](icorprofilercallback9-interface.md)
- [ICorProfilerCallback8.DynamicMethodJITCompilationStarted (méthode)](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)
- [ICorProfilerCallback8.DynamicMethodJITCompilationFinished (méthode)](icorprofilercallback8-dynamicmethodjitcompilationfinished-method.md)
