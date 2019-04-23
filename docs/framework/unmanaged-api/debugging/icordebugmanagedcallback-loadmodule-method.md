---
title: ICorDebugManagedCallback::LoadModule, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.LoadModule
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::LoadModule
helpviewer_keywords:
- ICorDebugManagedCallback::LoadModule method [.NET Framework debugging]
- LoadModule method [.NET Framework debugging]
ms.assetid: 66ec04e9-87cb-42ce-9720-81522abb5d5a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cfca06c656f3274f4c5ddb06373a0296dc5e6905
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59164539"
---
# <a name="icordebugmanagedcallbackloadmodule-method"></a>ICorDebugManagedCallback::LoadModule, méthode
Notifie le débogueur qu’un module du common language runtime (CLR) a été correctement chargé.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT LoadModule (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugModule    *pModule  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pAppDomain`  
 [in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application dans lequel le module a été chargé.  
  
 `pModule`  
 [in] Pointeur vers un objet ICorDebugModule qui représente le module CLR.  
  
## <a name="remarks"></a>Notes  
 Le `LoadModule` rappel fournit un bon moment pour examiner les métadonnées pour le module, définir des indicateurs de compilateur juste-à-temps (JIT), ou activer ou désactiver des rappels pour le module de chargement de classe.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [UnloadModule, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-unloadmodule-method.md)
- [ICorDebugManagedCallback, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
