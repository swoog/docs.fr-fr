---
title: ICorDebugValue3, interface
ms.date: 03/30/2017
api_name:
- ICorDebugValue3
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue3
helpviewer_keywords:
- ICorDebugValue3 interface [.NET Framework debugging]
ms.assetid: 7d5385d3-f4a5-47c4-8478-a3513b5e9406
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 34e1dd6adaa9906babca80f4cc610c157bd00534
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54648243"
---
# <a name="icordebugvalue3-interface"></a>ICorDebugValue3, interface
Étend les interfaces de « ICorDebugValue » et « ICorDebugValue2 » pour prendre en charge pour les tableaux qui sont supérieures à 2 Go.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[GetSize64, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-getsize64-method.md)|Obtient la taille, en octets, de ce `ICorDebugValue3` objet.|  
  
## <a name="remarks"></a>Notes  
 Le [ICorDebugValue::GetSize](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-getsize64-method.md) méthode retourne une taille de l’objet qui est compris entre 0 et 2 147 483 647 octets. Dans le [!INCLUDE[net_v45](../../../../includes/net-v45-md.md)], la taille des tableaux peut dépasser 2 Go. Le `ICorDebugValue3` interface vous permet de déterminer la taille de ces tableaux.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi


- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
