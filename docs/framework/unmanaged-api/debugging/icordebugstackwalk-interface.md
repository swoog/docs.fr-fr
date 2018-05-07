---
title: ICorDebugStackWalk, interface
ms.date: 03/30/2017
api_name:
- ICorDebugStackWalk
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStackWalk
helpviewer_keywords:
- ICorDebugStackWalk interface [.NET Framework debugging]
ms.assetid: 16d695e8-975d-431b-8421-e9e6c3e3f476
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 612e0f84302d5bee6479264ef2dbba4c7152657e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="icordebugstackwalk-interface"></a>ICorDebugStackWalk, interface
Fournit des méthodes pour obtenir les méthodes managées, ou frames, sur la pile d'un thread.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[GetContext, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-getcontext-method.md)|Retourne le contexte pour le frame actuel dans le `ICorDebugStackWalk` objet.|  
|[SetContext, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-setcontext-method.md)|Définit le `ICorDebugStackWalk` contexte actuel de l’objet à un contexte valid pour le thread.|  
|[Next, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-next-method.md)|Déplace le `ICorDebugStackWalk` objet à l’image suivante.|  
|[GetFrame, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-getframe-method.md)|Obtient le frame actuel le `ICorDebugStackWalk` objet.|  
  
## <a name="remarks"></a>Notes  
  
> [!NOTE]
>  Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
