---
title: ICorDebugVirtualUnwinder (interface)
ms.date: 03/30/2017
ms.assetid: a09e9ccc-0b37-43e3-95c1-bc5fa7ee5f42
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bb04ac42b3cc77db3af53c87efb0d1f1f75da928
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33421283"
---
# <a name="icordebugvirtualunwinder-interface"></a>ICorDebugVirtualUnwinder (interface)
Fournit des méthodes pour faciliter le déroulement de la pile.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Name|  
|------------|----------|  
|[GetContext, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugvirtualunwinder-getcontext-method.md)|Obtient le contexte actuel de ce dérouleur.|  
|[Next, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugvirtualunwinder-next-method.md)|Avance jusqu'au contexte de l'appelant.|  
  
## <a name="remarks"></a>Notes  
 Les membres de l'interface `ICorDebugVirtualUnwinder` sont implémentés par le débogueur pour faciliter le déroulement de la pile.  
  
> [!NOTE]
>  Cette interface est uniquement disponible avec .NET Native. Si vous implémentez cette interface pour des scénarios ICorDebug en dehors de .NET Native, le Common Language Runtime ignore cette interface.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
