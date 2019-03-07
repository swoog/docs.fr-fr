---
title: ICorDebugManagedCallback::UnloadClass, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.UnloadClass
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::UnloadClass
helpviewer_keywords:
- ICorDebugManagedCallback::UnloadClass method [.NET Framework debugging]
- UnloadClass method [.NET Framework debugging]
ms.assetid: 66a59b18-ce9a-41f4-b23b-4dd6753d6d36
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 020774778b21cf0f6029a666e0022fe83845c4ed
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57472445"
---
# <a name="icordebugmanagedcallbackunloadclass-method"></a>ICorDebugManagedCallback::UnloadClass, méthode
Notifie le débogueur qu’une classe est déchargée.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT UnloadClass (  
    [in] ICorDebugAppDomain  *pAppDomain,  
    [in] ICorDebugClass      *c  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pAppDomain`  
 [in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application contenant la classe.  
  
 `c`  
 [in] Pointeur vers un objet ICorDebugClass qui représente la classe.  
  
## <a name="remarks"></a>Notes  
 La classe ne doit pas être référencée après cet appel.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [LoadClass, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-loadclass-method.md)
- [ICorDebugManagedCallback, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
