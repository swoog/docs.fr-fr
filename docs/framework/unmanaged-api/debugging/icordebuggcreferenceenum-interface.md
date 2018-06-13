---
title: ICorDebugGCReferenceEnum, interface
ms.date: 03/30/2017
api_name:
- ICorDebugGCReferenceEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugGCReferenceEnum
helpviewer_keywords:
- ICorDebugGCReferenceEnum interface [.NET Framework debugging]
ms.assetid: 5f3c91c9-c035-454f-96cc-011cab1ea06b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fa8c3160dc779b2475dec63be896af5283cf5346
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33418163"
---
# <a name="icordebuggcreferenceenum-interface"></a>ICorDebugGCReferenceEnum, interface
Fournit un énumérateur pour les objets qui sont récupérés par le récupérateur de mémoire.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[Next, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebuggcreferenceenum-next-method.md)|Obtient le nombre spécifié de [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) instances qui contiennent des informations sur les objets qui seront par le garbage collector.|  
  
## <a name="remarks"></a>Notes  
 Le `ICorDebugGCReferenceEnum` interface implémente l’interface « ICorDebugEnum ».  
  
 Un `ICorDebugGCReferenceEnum` instance est remplie avec [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) instances en appelant le [ICorDebugProcess5::EnumerateGCReferences](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-enumerategcreferences-method.md) (méthode). [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) objets peuvent être énumérées en appelant le [ICorDebugGCReference::Next](../../../../docs/framework/unmanaged-api/debugging/icordebuggcreferenceenum-next-method.md) (méthode).  
  
 Le [COR_GC_REFERENCE](../../../../docs/framework/unmanaged-api/debugging/cor-gc-reference-structure.md) trois types d’objets représentent des objets dans la collection remplie par cette méthode :  
  
-   Objets de toutes les piles managées. Cela inclut des références actives dans le code managé, ainsi que les objets créés par le common language runtime.  
  
-   Objets à partir de la table de handles. Cela inclut des références solides (`HNDTYPE_STRONG` et `HNDTYPE_REFCOUNT`) et les variables statiques dans un module.  
  
-   Objets à partir de la file d’attente du finaliseur. La file d’attente du finaliseur racines d’objets jusqu'à ce que le finaliseur a exécuté.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
