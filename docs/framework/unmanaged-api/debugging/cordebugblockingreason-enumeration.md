---
title: CorDebugBlockingReason, énumération
ms.date: 03/30/2017
api_name:
- CorDebugBlockingReason
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugBlockingReason
helpviewer_keywords:
- CorDebugBlockingReason enumeration [.NET Framework debugging]
ms.assetid: a6ac2531-ddfe-46fd-88fe-8b1eabe0b255
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c867945f8a75cade5c7405b2908e2819f5d261d9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54706970"
---
# <a name="cordebugblockingreason-enumeration"></a>CorDebugBlockingReason, énumération
Spécifie les raisons pour lesquelles un thread peut être bloqué sur un objet donné.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Typedef enum CorDebugBlockingReason  
{  
   BLOCKING_NONE = 0  
   BLOCKING_MONITOR_CRITICAL_SECTION = 1  
   BLOCKING_MONITOR_EVENT = 2  
}  CorDebugBlockingReason;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`BLOCKING_NONE`|Usage interne uniquement.|  
|`BLOCKING_MONITOR_CRITICAL_SECTION`|Un thread essaie d’acquérir la section critique qui est associée avec le verrou du moniteur sur un objet. En règle générale, cela se produit lorsque vous appelez une de la <xref:System.Threading.Monitor.Enter%2A?displayProperty=nameWithType> ou <xref:System.Threading.Monitor.TryEnter%2A?displayProperty=nameWithType> méthodes.|  
|`BLOCKING_MONITOR_EVENT`|Un thread est en attente sur l’événement qui est associé à un verrou du moniteur pour un objet. En règle générale, cela se produit lorsque vous appelez une de la <xref:System.Threading.Monitor?displayProperty=nameWithType> `Wait` méthodes.|  
  
## <a name="remarks"></a>Notes  
 Lorsque le `BLOCKING_MONITOR_CRITICAL_SECTION` ou `BLOCKING_MONITOR_EVENT` membre est utilisé dans un [CorDebugBlockingObject](../../../../docs/framework/unmanaged-api/debugging/cordebugblockingobject-structure.md) structure, le `pBlockingObject` membre de la structure pointe vers une interface « ICorDebugValue » qui représente l’objet qui est entré . Il est garanti que pour implémenter le [ICorDebugHeapValue3](../../../../docs/framework/unmanaged-api/debugging/icordebugheapvalue3-interface.md) interface.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [Énumérations de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
- [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
