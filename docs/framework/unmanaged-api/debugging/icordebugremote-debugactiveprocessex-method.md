---
title: ICorDebugRemote::DebugActiveProcessEx, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugRemote.DebugActiveProcessEx
api_location:
- CorDebug.dll
api_type:
- COM
f1_keywords:
- ICorDebugRemoteTarget::DebugActiveProcessEx
helpviewer_keywords:
- ICorDebugRemote::DebugActiveProcessEx method [.NET Framework debugging]
- DebugActiveProcessEx method, ICorDebugRemote interface [.NET Framework debugging]
ms.assetid: b0df5c5d-9a2e-47bf-894c-6f8a9fe24a1f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: eba0ff6e545a5da5d7733a157b73ddd66e717de9
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57477112"
---
# <a name="icordebugremotedebugactiveprocessex-method"></a>ICorDebugRemote::DebugActiveProcessEx, méthode
Lance un processus sur un ordinateur distant sous le débogueur.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT DebugActiveProcessEx (  
    [in]  ICorDebugRemoteTarget *   pRemoteTarget,  
    [in]  DWORD                     dwProcessId,  
    [in]  BOOL                      fWin32Attach,  
    [out] ICorDebugProcess **       ppProcess  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pRemoteTarget`  
 [in] Pointeur vers un [icordebugremotetarget, Interface](../../../../docs/framework/unmanaged-api/debugging/icordebugremotetarget-interface.md). Ce paramètre est utilisé pour déterminer l’ordinateur sur lequel le processus est en cours d’exécution.  
  
 `id`  
 [in] ID du processus auquel le débogueur doit être attaché.  
  
 `win32Attach`  
 [in] `true` si le débogueur doit se comporter comme le débogueur Win32 pour le processus et distribuer les rappels non managés ; sinon, `false`.  
  
 `ppProcess`  
 [out] Pointeur vers l’adresse d’un objet « ICorDebugProcess » qui représente le processus auquel le débogueur est attaché.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK  
 Correctement attaché au processus sur l’ordinateur distant.  
  
 E_FAIL (ou autres codes de retour E_)  
 Impossible de s’attacher au processus sur l’ordinateur distant.  
  
## <a name="remarks"></a>Notes  
 Le débogage en mode mixte n’est pas pris en charge dans Silverlight.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** 4.5, 4, 3.5 SP1  
  
## <a name="see-also"></a>Voir aussi
- [ICorDebugRemote, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugremote-interface.md)
- [ICorDebug, interface](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)

- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
