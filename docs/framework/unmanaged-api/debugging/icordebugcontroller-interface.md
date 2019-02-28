---
title: ICorDebugController, interface
ms.date: 03/30/2017
api_name:
- ICorDebugController
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController
helpviewer_keywords:
- ICorDebugController interface [.NET Framework debugging]
ms.assetid: dbb1c4dc-269a-459b-ab1d-6c70788782ce
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f81b671721e1416ab9717442d4d7fc727b938ee2
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56980488"
---
# <a name="icordebugcontroller-interface"></a>ICorDebugController, interface

Représente une portée, un <xref:System.Diagnostics.Process> ou un <xref:System.AppDomain>, où le contexte d'exécution du code peut être contrôlé.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|`ICorDebugController::CanCommitChanges`|Cette méthode est obsolète.|  
|`ICorDebugController::CommitChanges`|Cette méthode est obsolète.|  
|[Continue, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md)|Reprend l’exécution de threads managés après un appel à [ICorDebugController::Stop](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-stop-method.md).|  
|[Detach, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-detach-method.md)|Détache le débogueur du processus ou domaine d’application.|  
|[EnumerateThreads, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-enumeratethreads-method.md)|Obtient un énumérateur pour les threads managés actives dans le processus.|  
|[HasQueuedCallbacks, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-hasqueuedcallbacks-method.md)|Obtient une valeur qui indique si des rappels managés sont actuellement en file d’attente pour le thread spécifié.|  
|[IsRunning, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-isrunning-method.md)|Obtient une valeur qui indique si les threads dans le processus en cours d’exécution librement.|  
|[SetAllThreadsDebugState, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-setallthreadsdebugstate-method.md)|Définit l’état de débogage de tous les threads managés dans le processus.|  
|[Stop, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-stop-method.md)|Effectue un arrêt coopératif sur tous les threads qui exécutent du code managé dans le processus.|  
|[Terminate, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-terminate-method.md)|Met fin au processus avec le code de sortie spécifié.|  
  
## <a name="remarks"></a>Notes  
 Si `ICorDebugController` est contrôle un processus, l’étendue inclut tous les threads du processus. Si `ICorDebugController` est contrôlant un domaine d’application, l’étendue inclut uniquement les threads de ce domaine d’application particulier.  
  
> [!NOTE]
>  Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
