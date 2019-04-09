---
title: CorDebugJITCompilerFlags, énumération
ms.date: 03/30/2017
api_name:
- CorDebugJITCompilerFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugJITCompilerFlags
helpviewer_keywords:
- CorDebugJITCompilerFlags enumeration [.NET Framework debugging]
ms.assetid: c0774f70-5bed-45e8-9922-fdad778c4c33
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 66a8ba59d221bb3fa2e815a1cbcfa79c474666cc
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59105467"
---
# <a name="cordebugjitcompilerflags-enumeration"></a>CorDebugJITCompilerFlags, énumération
Contient des valeurs qui influencent le comportement du compilateur juste-à-temps managé.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum CorDebugJITCompilerFlags {  
  
    CORDEBUG_JIT_DEFAULT = 0x1,  
    CORDEBUG_JIT_DISABLE_OPTIMIZATION = 0x3,  
    CORDEBUG_JIT_ENABLE_ENC = 0x7  
  
} CorDebugJITCompilerFlags;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`CORDEBUG_JIT_DEFAULT`|Spécifie que le compilateur doit suivre des données de compilation et permet des optimisations.|  
|`CORDEBUG_JIT_DISABLE_OPTIMIZATION`|Spécifie que le compilateur doit suivre des données de compilation, mais désactive les optimisations.|  
|`CORDEBUG_JIT_ENABLE_ENC`|Spécifie que le compilateur doit suivre des données de compilation, désactive les optimisations, et permet aux technologies Modifier & Continue.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Énumérations de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
