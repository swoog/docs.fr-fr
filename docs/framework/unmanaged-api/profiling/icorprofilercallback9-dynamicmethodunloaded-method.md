---
title: ICorProfilerCallback9::DynamicMethodUnloaded (méthode)
ms.date: 04/10/2018
api_name:
- ICorProfilerCallback9.DynamicMethodUnloaded
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 16b3334647922f845645e6eb58db3146f4c9b936
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33452401"
---
# <a name="icorprofilercallback9dynamicmethodunloaded-method"></a>ICorProfilerCallback9::DynamicMethodUnloaded (méthode)
[Pris en charge dans le .NET Framework 4.7.2 et versions ultérieures]  
  
Notifie le profileur chaque fois qu’une méthode dynamique est garbage collector et déchargé par la suite.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT DynamicMethodUnloaded(  
     [in]  FunctionID  functionId
);  
```  
  
#### <a name="parameters"></a>Paramètres  
[in] `functionId`  
Identificateur de la fonction en mémoire qui a été garbage collector et de déchargement.   

## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  
  
## <a name="see-also"></a>Voir aussi  
[ICorProfilerCallback8.DynamicMethodJITCompilationStarted (méthode)](icorprofilercallback8-dynamicmethodjitcompilationstarted-method.md)  
[ICorProfilerCallback8.DynamicMethodJITCompilationFinished (méthode)](icorprofilercallback8-dynamicmethodjitcompilationfinished-method.md)  
[Interface de ICorProfilerCallback9](icorprofilercallback9-interface.md)   
[COR_PRF_HIGH_MONITOR_DYNAMIC_FUNCTION_UNLOADS](cor-prf-high-monitor-enumeration.md)
