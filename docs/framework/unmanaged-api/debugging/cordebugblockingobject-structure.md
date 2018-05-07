---
title: CorDebugBlockingObject, structure
ms.date: 03/30/2017
api_name:
- CorDebugBlockingObject Structure
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugBlockingObject
helpviewer_keywords:
- CorDebugBlockingObject structure [.NET Framework debugging]
ms.assetid: 5944edd1-0914-4efa-aba0-d5a277c38b1a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ed7db321b32657087b791758096c692f25f3d7f5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="cordebugblockingobject-structure"></a>CorDebugBlockingObject, structure
Définit un objet qui bloque un thread et la raison spécifique que le thread est bloqué.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Typedef struct CorDebugBlockingObject  
{  
ICorDebugValue pBlockingObject;  
DWORD dwTimeout;  
CorDebugBlockingReason blockingReason;  
}  CorDebugBlockingObject;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`pBlockingObject`|L’objet sur lequel le thread est bloqué. Cet objet est valide uniquement pour la durée de l’état synchronisé actuel. Si deux threads se bloquent sur le même objet dans le même état synchronisé, vous pouvez attendre la [ICorDebugValue::GetAddress](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-getaddress-method.md) la même valeur de retour de méthode. Toutefois, les interfaces peuvent ou ne peuvent pas être équivalent du pointeur.|  
|`dwTimeout`|Le nombre de millisecondes avant l’opération de blocage est le délai d’attente ou la valeur infinie, ce qui indique qu’il n'expirera pas. La valeur de délai d’attente spécifie la durée totale de l’opération de blocage, pas le temps restant.|  
|`blockingReason`|La raison est que le thread est bloqué sur cet objet.|  
  
## <a name="remarks"></a>Notes  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Structures de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)  
 [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
