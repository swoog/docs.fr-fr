---
title: ICorProfilerCallback::ThreadAssignedToOSThread, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ThreadAssignedToOSThread
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ThreadAssignedToOSThread
helpviewer_keywords:
- ThreadAssignedToOSThread method [.NET Framework profiling]
- ICorProfilerCallback::ThreadAssignedToOSThread method [.NET Framework profiling]
ms.assetid: f9671e5a-7b14-4f5b-8404-58136422c8b2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 0e955d2fdca67448897ed49b3200542075b4d534
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57466776"
---
# <a name="icorprofilercallbackthreadassignedtoosthread-method"></a>ICorProfilerCallback::ThreadAssignedToOSThread, méthode
Notifie le profileur qu’un thread managé est implémenté à l’aide d’un thread de système d’exploitation particulier.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT ThreadAssignedToOSThread(  
    [in] ThreadID managedThreadId,  
    [in] DWORD    osThreadId);  
```  
  
## <a name="parameters"></a>Paramètres  
 `managedThreadId`  
 [in] L’identificateur du thread managé.  
  
 `osThreadId`  
 [in] L’identificateur du thread de système d’exploitation.  
  
## <a name="remarks"></a>Notes  
 Le `ThreadAssignedToOSThread` rappel existe afin que le profileur peut assurer un mappage précis entre les fibres de threads de système d’exploitation et les threads managés.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICorProfilerCallback, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
