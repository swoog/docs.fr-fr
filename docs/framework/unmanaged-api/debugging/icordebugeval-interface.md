---
title: ICorDebugEval, interface
ms.date: 03/30/2017
api_name:
- ICorDebugEval
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval
helpviewer_keywords:
- ICorDebugEval interface [.NET Framework debugging]
ms.assetid: 3a5c9815-832d-47e1-b7f7-bbba135d7cf1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 745917af176de47999737c87833c23df9c75ea7b
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59080863"
---
# <a name="icordebugeval-interface"></a>ICorDebugEval, interface

Fournit des méthodes pour permettre au débogueur d'exécuter le code à l'intérieur du contexte du code en cours de débogage.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[Abort, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugeval-abort-method.md)|Abandonne le calcul cela `ICorDebugEval` est en train d’objet.|  
|[CallFunction, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugeval-callfunction-method.md)|Définit un appel à la fonction spécifiée. (Obsolète dans .NET Framework version 2.0 ; utilisez [ICorDebugEval2::CallParameterizedFunction](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-callparameterizedfunction-method.md) à la place.)|  
|[CreateValue, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugeval-createvalue-method.md)|Obtient un pointeur d’interface vers un objet « ICorDebugValue » du type spécifié, avec une valeur initiale de zéro ou null. (Obsolète dans .NET Framework 2.0 ; utilisez [ICorDebugEval2::CreateValueForType](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-createvaluefortype-method.md) à la place.)|  
|[GetResult, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugeval-getresult-method.md)|Obtient un pointeur d’interface vers un `ICorDebugValue` qui contient les résultats de l’évaluation.|  
|[GetThread, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugeval-getthread-method.md)|Obtient un pointeur d’interface vers le « ICorDebugThread » où cette évaluation s’exécute ou s’exécutera.|  
|[IsActive, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugeval-isactive-method.md)|Obtient une valeur qui indique si ce `ICorDebugEval` objet est en cours d’exécution.|  
|[NewArray, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugeval-newarray-method.md)|Alloue un nouveau tableau du type d’élément spécifié et des dimensions. (Obsolète dans .NET Framework 2.0 ; utilisez [ICorDebugEval2::NewParameterizedArray](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-newparameterizedarray-method.md) à la place.)|  
|[NewObject, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugeval-newobject-method.md)|Alloue une nouvelle instance d’objet et appelle la méthode de constructeur spécifié. (Obsolète dans .NET Framework 2.0 ; utilisez [ICorDebugEval2::NewParameterizedObject](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-newparameterizedobject-method.md) à la place.)|  
|[NewObjectNoConstructor, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugeval-newobjectnoconstructor-method.md)|Alloue une nouvelle instance d’objet du type spécifié, sans tenter d’appeler une méthode de constructeur. (Obsolète dans .NET Framework 2.0 ; utilisez [ICorDebugEval2::NewParameterizedObjectNoConstructor](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-newparameterizedobjectnoconstructor-method.md) à la place.)|  
|[NewString, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugeval-newstring-method.md)|Alloue un nouvel objet de chaîne avec le contenu spécifié.|  
  
## <a name="remarks"></a>Notes  
 Un `ICorDebugEval` objet est créé dans le contexte d’un thread spécifique qui est utilisé pour exécuter les évaluations. Tous les objets et les types utilisés dans une évaluation donnée doivent résider dans le même domaine d’application. Ce domaine d’application ne doive pas être le même que le domaine d’application actuel du thread. Évaluations peuvent être imbriquées.  
  
 Opérations de l’évaluation ne se terminent pas jusqu'à ce que le débogueur appelle [ICorDebugController::Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md), puis reçoit un [ICorDebugManagedCallback::EvalComplete](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-evalcomplete-method.md) rappel. Si vous avez besoin d’utiliser la fonctionnalité d’évaluation sans permettre à d’autres threads exécuter, suspendre des threads à l’aide [ICorDebugController::SetAllThreadsDebugState](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-setallthreadsdebugstate-method.md) ou [ICorDebugController::Stop](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-stop-method.md)avant d’appeler [ICorDebugController::Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md).  
  
 Étant donné que le code utilisateur est en cours d’exécution lorsque l’évaluation est en cours d’exécution, des événements de débogage peuvent se produire, notamment les chargements de classe et des points d’arrêt. Le débogueur reçoit des rappels, comme d’habitude, pour ces événements. L’état de la version d’évaluation est visibles dans le cadre de l’inspection de l’état normal du programme. La chaîne de la pile sera un `CHAIN_FUNC_EVAL` chaîne (consultez l’énumération « CorDebugStepReason » et le [ICorDebugChain::GetReason](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getreason-method.md) méthode). L’API de débogage complète continuera de fonctionner normalement.  
  
 En cas d’une situation de boucle bloquée ou infinie, le code utilisateur peut ne jamais se terminer. Dans ce cas, vous devez appeler [ICorDebugEval::Abort](../../../../docs/framework/unmanaged-api/debugging/icordebugeval-abort-method.md) avant de reprendre le programme.  
  
> [!NOTE]
>  Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
