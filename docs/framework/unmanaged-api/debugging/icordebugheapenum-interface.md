---
title: ICorDebugHeapEnum, interface
ms.date: 03/30/2017
api_name:
- ICorDebugHeapEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapEnum
helpviewer_keywords:
- ICorDebugHeapEnum interface [.NET Framework debugging]
ms.assetid: 99cbc1eb-d539-4f76-a0d8-b93348112f14
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 79ef77e52e14fede9949121e7ec4575d10b820c8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61775581"
---
# <a name="icordebugheapenum-interface"></a>ICorDebugHeapEnum, interface
Fournit un énumérateur pour les objets sur le tas managé. Cette interface est une sous-classe de l’interface ICorDebugEnum.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[Next, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugheapenum-next-method.md)|Obtient le nombre spécifié de [COR_HEAPOBJECT](../../../../docs/framework/unmanaged-api/debugging/cor-heapobject-structure.md) instances qui contiennent des informations sur les objets sur le tas managé.|  
  
## <a name="remarks"></a>Notes  
 Le `ICorDebugHeapEnum` interface implémente l’interface ICorDebugEnum.  
  
 Un `ICorDebugHeapEnum` instance est remplie avec [COR_HEAPOBJECT](../../../../docs/framework/unmanaged-api/debugging/cor-heapobject-structure.md) instances en appelant le [ICorDebugProcess5::EnumerateHeap](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-enumerateheap-method.md) (méthode). Chaque [COR_HEAPOBJECT](../../../../docs/framework/unmanaged-api/debugging/cor-heapobject-structure.md) instance dans la collection représente un objet en direct sur le tas ou un objet qui est associé à aucune racine par n’importe quel objet, mais n’a pas encore été collecté par le garbage collector. Le [COR_HEAPOBJECT](../../../../docs/framework/unmanaged-api/debugging/cor-heapobject-structure.md) objets dans la collection peuvent être énumérés en appelant le [ICorDebugHeapEnum::Next](../../../../docs/framework/unmanaged-api/debugging/icordebugheapenum-next-method.md) (méthode).  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
