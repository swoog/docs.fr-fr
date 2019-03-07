---
title: ICorDebugProcess6::ProcessStateChanged, méthode
ms.date: 03/30/2017
ms.assetid: fb6d30d9-54f3-462b-8ebf-ce0440791ad5
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6f25e25f94dae1a959cbb813a44a7f4f09eaa69c
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57474590"
---
# <a name="icordebugprocess6processstatechanged-method"></a>ICorDebugProcess6::ProcessStateChanged, méthode
Avertit [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) que le processus est en cours d’exécution.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT ProcessStateChanged(   [in] CorDebugStateChange change);  
```  
  
## <a name="parameters"></a>Paramètres  
 `change`  
 [in] Un membre de la [ProcessStateChanged](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-processstatechanged-method.md) énumération  
  
## <a name="remarks"></a>Notes  
 Le débogueur appelle cette méthode pour notifier [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) que le processus est en cours d’exécution.  
  
> [!NOTE]
>  Cette méthode est uniquement disponible avec .NET Native.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICorDebugProcess6, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-interface.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
