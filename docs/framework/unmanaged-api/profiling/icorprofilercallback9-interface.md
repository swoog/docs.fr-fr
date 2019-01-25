---
title: ICorProfilerCallback9 Interface
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
ms.openlocfilehash: a6c480af921fb0259ef85beec8d8f65bdd430522
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54689308"
---
# <a name="icorprofilercallback9-interface"></a>ICorProfilerCallback9 Interface
[Pris en charge dans le .NET Framework 4.7.2 et versions ultérieures]  

 Une sous-classe de [ICorProfilerCallback8](icorprofilercallback8-interface.md) qui fournit une méthode de rappel utilisée par le common language runtime pour informer le profileur qu’une méthode dynamique a été garbage collectées et déchargé par la suite.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[DynamicMethodUnloaded, méthode](ICorProfilerCallback9-dynamicmethodunloaded-method.md)|Notifie le profileur qu’une méthode dynamique a été garbage collectées et déchargé par la suite.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  

## <a name="see-also"></a>Voir aussi
- [Interfaces de profilage](profiling-interfaces.md)
- [ICorProfilerCallback8, interface](icorprofilercallback9-interface.md)
- [ICorProfilerCallback8.DynamicMethodJITCompilationStarted (méthode)](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)
- [ICorProfilerCallback8.DynamicMethodJITCompilationFinished (méthode)](icorprofilercallback8-dynamicmethodjitcompilationfinished-method.md)
