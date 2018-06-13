---
title: ICorDebugThread2::GetTaskID, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugThread2.GetTaskID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread2::GetTaskID
helpviewer_keywords:
- ICorDebugThread2::GetTaskID method [.NET Framework debugging]
- GetTaskID method [.NET Framework debugging]
ms.assetid: 6ba3c6ee-4ba1-4c98-bf1e-8531acd3da09
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f5690856b526bf0f7bc4527d04ae8044cda1f6e5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33417864"
---
# <a name="icordebugthread2gettaskid-method"></a>ICorDebugThread2::GetTaskID, méthode
Obtient l’identificateur de la tâche en cours d’exécution sur ce thread.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetTaskID (  
    [out] TASKID  *pTaskId  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `pTaskId`  
 [out] Pointeur vers l’identificateur de la tâche en cours d’exécution sur le thread représenté par cet objet ICorDebugThread2.  
  
## <a name="remarks"></a>Notes  
 Une tâche peut uniquement être en cours d’exécution sur le thread si le thread est associé à une connexion. `GetTaskID` retourne zéro `pTaskId` si le thread n’est pas associé à une connexion.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]
