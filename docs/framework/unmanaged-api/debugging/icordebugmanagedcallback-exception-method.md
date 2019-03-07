---
title: ICorDebugManagedCallback::Exception, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.Exception
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::Exception
helpviewer_keywords:
- Exception method, ICorDebugManagedCallback interface [.NET Framework debugging]
- ICorDebugManagedCallback::Exception method [.NET Framework debugging]
ms.assetid: ab18a509-dff3-4930-b585-bd15e0414176
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e985d82fcce404e15344f2277d27a6aab45f9efc
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57472498"
---
# <a name="icordebugmanagedcallbackexception-method"></a>ICorDebugManagedCallback::Exception, méthode
Notifie le débogueur qu’une exception a été levée à partir du code managé.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT Exception (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread    *pThread,  
    [in] BOOL                unhandled  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pAppDomain`  
 [in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application dans lequel l’exception a été levée.  
  
 `pThread`  
 [in] Pointeur vers un objet ICorDebugThread qui représente le thread dans lequel l’exception a été levée.  
  
 `unhandled`  
 [in] Si cette valeur est `false`, l’exception n’a pas encore été traitée par l’application ; sinon, l’exception n’est pas gérée et le processus prendra fin.  
  
## <a name="remarks"></a>Notes  
 L’exception spécifique peut être récupérée à partir de l’objet thread.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICorDebugManagedCallback, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
