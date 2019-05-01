---
title: ICorProfilerCallback8, interface
ms.date: 04/10/2018
api_name:
- ICorProfilerCallback8
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e536e61a8d812e442e1e54188c99d6a1d4586757
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62049724"
---
# <a name="icorprofilercallback8-interface"></a>ICorProfilerCallback8, interface
[Pris en charge dans le .NET Framework 4.7 et versions ultérieures]  

 Une sous-classe de [ICorProfilerCallback7](icorprofilercallback7-interface.md) qui fournit des méthodes de rappel utilisés par le common language runtime pour informer le profileur de la compilation JIT d’une méthode dynamique a démarré et s’est terminé. 
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[DynamicMethodJITCompilationStarted, méthode](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)|Notifie le profileur que la compilation JIT d’une méthode dynamique a démarré.|  
|[DynamicMethodJITCompilationFinished, méthode](icorprofilercallback8-dynamicmethodjitcompilationfinished-method.md)|Notifie le profileur que la compilation JIT d’une méthode dynamique est terminée.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>Voir aussi

- [Interfaces de profilage](profiling-interfaces.md)
- [ICorProfilerCallback9, interface](icorprofilercallback9-interface.md)
