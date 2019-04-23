---
title: ICorDebugStringValue, interface
ms.date: 03/30/2017
api_name:
- ICorDebugStringValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStringValue
helpviewer_keywords:
- ICorDebugStringValue interface [.NET Framework debugging]
ms.assetid: bf84d0af-53e1-4c04-bc5b-7e5f81ba2cc2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6709b14ce8e7bc131f9feb7a277fb41851ee4352
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59173990"
---
# <a name="icordebugstringvalue-interface"></a>ICorDebugStringValue, interface
Une sous-classe de ICorDebugHeapValue qui s’applique aux valeurs de chaîne.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[GetLength, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugstringvalue-getlength-method.md)|Obtient le nombre de caractères dans la chaîne référencée par ce `ICorDebugStringValue`.|  
|[GetString, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugstringvalue-getstring-method.md)|Obtient la chaîne référencée par ce `ICorDebugStringValue`.|  
  
## <a name="remarks"></a>Notes  
  
> [!NOTE]
>  Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
