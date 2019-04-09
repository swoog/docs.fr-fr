---
title: ICorDebugMDA::GetOSThreadId, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugMDA.GetOSThreadId
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugMDA::GetOSThreadId
helpviewer_keywords:
- ICorDebugMDA::GetOSThreadId method [.NET Framework debugging]
- GetOSThreadId method [.NET Framework debugging]
ms.assetid: 7ca7c364-ade4-4219-b434-9f6ae2359be6
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 51d29fed3d53611daa0042251ce09638399f7ed5
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59195798"
---
# <a name="icordebugmdagetosthreadid-method"></a>ICorDebugMDA::GetOSThreadId, méthode
Obtient l’identificateur de thread de système d’exploitation (se) sur lequel l’assistant débogage managé (MDA) représenté par [ICorDebugMDA](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md) s’exécute.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetOSThreadId (  
    [out] DWORD    *pOsTid  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pOsTid`  
 [out] Pointeur vers l’identificateur du thread du système d’exploitation.  
  
## <a name="remarks"></a>Notes  
 Le thread de système d’exploitation est utilisé au lieu d’un ICorDebugThread pour les situations dans lesquelles un MDA est déclenché sur un thread natif ou sur un thread managé qui n’a pas encore entré le code managé.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorDebugMDA, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md)
- [Diagnostic d'erreurs avec les Assistants de débogage managés](../../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
