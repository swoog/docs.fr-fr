---
title: ICorProfilerCallback2, interface
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback2
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback2
helpviewer_keywords:
- ICorProfilerCallback2 interface [.NET Framework profiling]
ms.assetid: 4a261dba-450d-4f1f-8d98-865b58bfc992
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 83c72704ccb01baf68a3cacb6252367e07909fa8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59178995"
---
# <a name="icorprofilercallback2-interface"></a>ICorProfilerCallback2, interface
Fournit des méthodes qui sont utilisées par le common language runtime (CLR) pour signaler un profileur de code qui se produisent les événements auxquels le profileur s’est abonnée. Le `ICorProfilerCallback2` interface est une extension de la [ICorProfilerCallback](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md) interface. Autrement dit, elle fournit des rappels nouvelle introduites dans .NET Framework version 2.0.  
  
> [!NOTE]
>  Chaque implémentation de la méthode doit retourner un HRESULT avec la valeur S_OK sur la réussite ou E_FAIL en cas d’échec. Actuellement, le CLR ignore le HRESULT retourné par chaque rappel à l’exception [ICorProfilerCallback::ObjectReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-objectreferences-method.md).  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[FinalizeableObjectQueued, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-finalizeableobjectqueued-method.md)|Notifie le profileur de code qu’un objet avec un finaliseur a été en file d’attente pour le thread finaliseur pour l’exécution de son `Finalize` (méthode).|  
|[GarbageCollectionFinished, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionfinished-method.md)|Informe le profileur qu’une garbage collection est terminé et que tous les rappels de garbage collection ont été publiés.|  
|[GarbageCollectionStarted, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionstarted-method.md)|Notifie le profileur de code qu’un garbage collection a démarré.|  
|[HandleCreated, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-handlecreated-method.md)|Notifie le profileur de code qu’un handle de garbage collection a été créé.|  
|[HandleDestroyed, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-handledestroyed-method.md)|Notifie le profileur de code qu’un handle de garbage collection a été détruit.|  
|[RootReferences2, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-rootreferences2-method.md)|Informe le profileur sur les références racine après qu’un garbage collection s’est produite. Cette méthode est une extension de la [ICorProfilerCallback::RootReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-rootreferences-method.md) (méthode).|  
|[SurvivingReferences, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-survivingreferences-method.md)|Informe le profileur sur les références d’objet qui ont survécu à un garbage collection.|  
|[ThreadNameChanged, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-threadnamechanged-method.md)|Notifie le profileur de code que le nom d’un thread a changé.|  
  
## <a name="remarks"></a>Notes  
 Le CLR appelle une méthode le `ICorProfilerCallback` (ou `ICorProfilerCallback2`) interface pour informer le profileur lorsqu’un événement, à laquelle le profileur était abonné se produit. Il s’agit de l’interface de rappel principale par le biais duquel le CLR communique avec le profileur de code.  
  
 Un profileur de code doit implémenter les méthodes de la `ICorProfilerCallback` interface. Pour le .NET Framework 2.0 et les versions ultérieures, le profileur doit également implémenter le `ICorProfilerCallback2` méthodes. Chaque implémentation de la méthode doit retourner un HRESULT avec la valeur S_OK sur la réussite ou E_FAIL en cas d’échec. Actuellement, le CLR ignore le HRESULT retourné par chaque rappel à l’exception [ICorProfilerCallback::ObjectReferences](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-objectreferences-method.md).  
  
 Un profileur de code doit inscrire dans le Registre de Microsoft Windows, son objet COM qui implémente le `ICorProfilerCallback` et `ICorProfilerCallback2` interfaces. Un profileur de code s’abonne aux événements pour lesquels il souhaite recevoir une notification en appelant [ICorProfilerInfo::SetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-seteventmask-method.md). Cela s’effectue habituellement dans l’implémentation du profileur de [ICorProfilerCallback::Initialize](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-initialize-method.md). Le profileur peut ensuite recevoir une notification du runtime lorsqu’un événement doit se produire ou s’est produite dans un processus d’exécution en cours d’exécution.  
  
> [!NOTE]
>  Le profileur enregistre un objet COM unique. Si le profileur cible .NET Framework version 1.0 ou 1.1, cet objet COM doit uniquement implémenter les méthodes de `ICorProfilerCallback`. Si elle cible .NET Framework version 2.0 et versions ultérieures, l’objet COM doit également implémenter les méthodes de `ICorProfilerCallback2`.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de profilage](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [ICorProfilerCallback, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [ICorProfilerCallback3, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback3-interface.md)
- [ICorProfilerCallback4, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-interface.md)
