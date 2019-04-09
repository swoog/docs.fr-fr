---
title: ICorDebugMutableDataTarget::ContinueStatusChanged, méthode
ms.date: 03/30/2017
ms.assetid: 5a66d3f4-dd16-4d62-9dcc-0eab7041d894
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 52b5c63f35732655834768eb5b914406203d423c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59135614"
---
# <a name="icordebugmutabledatatargetcontinuestatuschanged-method"></a>ICorDebugMutableDataTarget::ContinueStatusChanged, méthode
Modifie l'état de continuation de l'événement de débogage en suspens sur le thread spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT ContinueStatusChanged(  
   [in] DWORD dwThreadId,  
   [in] CORDB_CONTINUE_STATUS continueStatus);  
```  
  
## <a name="parameters"></a>Paramètres  
 `dwThreadId`  
 Identificateur de thread défini par le système d'exploitation.  
  
 `continueStatus`  
 Valeur [COREDB_CONTINUE_STATUS](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md) qui représente le nouvel état de continuation demandé.  
  
## <a name="remarks"></a>Notes  
 Le débogueur appelle la méthode `ContinueStatusChanged` quand il appelle une méthode ICorDebug qui nécessite une gestion potentiellement anormale de l'événement de débogage actif. Par exemple, si une exception est en suspens et que le débogueur demande une opération susceptible d’annuler l’exception (comme [ICorDebugILFrame::SetIP](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-setip-method.md) ou `FuncEval`), cette API permet de demander l’annulation de l’exception.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorDebugMutableDataTarget, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugmutabledatatarget-interface.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
