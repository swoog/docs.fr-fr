---
title: CorDebugIntercept, énumération
ms.date: 03/30/2017
api_name:
- CorDebugIntercept
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugIntercept
helpviewer_keywords:
- CorDebugIntercept enumeration [.NET Framework debugging]
ms.assetid: 3d5b642e-7ef2-428b-a5ae-509c35ed461a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0791a59e0325668960dcfc98816920db55bcfb87
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61651699"
---
# <a name="cordebugintercept-enumeration"></a>CorDebugIntercept, énumération
Indique les types de code qui peuvent être interceptés (c'est-à-dire pouvant faire l'objet d'un pas à pas détaillé).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum CorDebugIntercept {  
    INTERCEPT_NONE                = 0x0,  
    INTERCEPT_CLASS_INIT          = 0x01,  
    INTERCEPT_EXCEPTION_FILTER    = 0x02,  
    INTERCEPT_SECURITY            = 0x04,  
    INTERCEPT_CONTEXT_POLICY      = 0x08,  
    INTERCEPT_INTERCEPTION        = 0x10,  
    INTERCEPT_ALL                 = 0xffff  
} CorDebugIntercept;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`INTERCEPT_NONE`|Aucun code ne peut être intercepté.|  
|`INTERCEPT_CLASS_INIT`|Un constructeur peut être intercepté.|  
|`INTERCEPT_EXCEPTION_FILTER`|Un filtre d'exception peut être intercepté.|  
|`INTERCEPT_SECURITY`|Le code qui applique la sécurité peut être intercepté.|  
|`INTERCEPT_CONTEXT_POLICY`|Une stratégie de contexte peut être interceptée.|  
|`INTERCEPT_INTERCEPTION`|Non utilisé.|  
|`INTERCEPT_ALL`|Aucun code ne peut être intercepté.|  
  
## <a name="remarks"></a>Notes  
 Utilisez le [ICorDebugStepper::SetInterceptMask](../../../../docs/framework/unmanaged-api/debugging/icordebugstepper-setinterceptmask-method.md) méthode pour définir les types de code qui peut être intercepté.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Énumérations de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
