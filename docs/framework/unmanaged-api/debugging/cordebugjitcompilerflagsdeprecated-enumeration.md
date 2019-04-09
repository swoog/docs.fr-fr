---
title: CorDebugJITCompilerFlagsDeprecated, énumération
ms.date: 03/30/2017
api_name:
- CorDebugJITCompilerFlagsDeprecated
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugJITCompilerFlagsDeprecated
helpviewer_keywords:
- CorDebugJITCompilerFlagsDeprecated enumeration [.NET Framework debugging]
ms.assetid: af15e2ca-6be1-472b-bd36-03644a1e3ddd
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7f15a4557be0dc633fb9ecda5916896e340f00da
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59136888"
---
# <a name="cordebugjitcompilerflagsdeprecated-enumeration"></a>CorDebugJITCompilerFlagsDeprecated, énumération
Cette énumération est obsolète. Utilisez le `CORDEBUG_JIT_DEFAULT` membre de la [CorDebugJITCompilerFlags](../../../../docs/framework/unmanaged-api/debugging/cordebugjitcompilerflags-enumeration.md) énumération à la place.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum CorDebugJITCompilerFlagsDeprecated {  
    CORDEBUG_JIT_TRACK_DEBUG_INFO  = 0x1  
} CorDebugJITCompilerFlagsDeprecated;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`CORDEBUG_JIT_TRACK_DEBUG_INFO`|Utilisez plutôt `CORDEBUG_JIT_DEFAULT`.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** 1.0, 1.1  
  
## <a name="see-also"></a>Voir aussi

- [Énumérations de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
