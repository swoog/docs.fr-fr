---
title: Interface ICorProfilerCallback7
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback7
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
ms.assetid: a0be019e-aaa1-4036-990f-565f114d4b5c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f681001b610f42fef28181ffe3b47d702aabdf6e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33452689"
---
# <a name="icorprofilercallback7-interface"></a>Interface ICorProfilerCallback7
[Prise en charge dans le .NET Framework 4.6.1 et versions ultérieures]  
  
 Sous-classe de [ICorProfilerCallback6](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback6-interface.md) qui fournit une méthode de rappel que le Common Language Runtime utilise pour informer le profileur de la mise à jour du flux de symbole associé à un module en mémoire.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[ModuleInMemorySymbolsUpdated, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback7-moduleinmemorysymbolsupdated-method.md)|Notifie le profileur de la mise à jour du flux de symbole associé à un module en mémoire.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Interfaces de profilage](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
