---
title: CorDebugDecodeEventFlagsWindows, énumération
ms.date: 03/30/2017
api_name:
- CorDebugDecodeEventFlagsWindows
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: aa6cf962-30ae-4cfd-8895-826deeb46a54
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2d4e006a03db5b16de93dfd07ec7b964db4bfc1d
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59207732"
---
# <a name="cordebugdecodeeventflagswindows-enumeration"></a>CorDebugDecodeEventFlagsWindows, énumération
Fournit des informations supplémentaires sur les événements de débogage propres à la plateforme Windows.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum CorDebugDecodeEventFlagsWindows {  
    IS_FIRST_CHANCE = 1,  
} CorDebugDecodeEventFlagsWindows;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`IS_FIRST_CHANCE`|Indique que l'événement de débogage est une exception de première chance.|  
  
## <a name="remarks"></a>Notes  
 Le [ICorDebugProcess6::DecodeEvent](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-decodeevent-method.md) méthode inclut un `dwFlags` paramètre qui fournit des informations supplémentaires sur un événement de débogage et dont la valeur dépend de l’architecture cible. L'énumération `CorDebugDecodeEventFlagsWindows` peut être utilisée avec les événements de débogage sur la plateforme Windows.  
  
> [!NOTE]
>  Cette énumération est destinée à une utilisation dans des scénarios de débogage .NET Native uniquement.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Énumérations de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
