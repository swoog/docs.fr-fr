---
title: CorDebugSetContextFlag, énumération
ms.date: 03/30/2017
api_name:
- CorDebugSetContextFlag
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugSetContextFlag
helpviewer_keywords:
- CorDebugSetContextFlag enumeration [.NET Framework debugging]
ms.assetid: b30280bb-fe75-44ed-8589-bcff081fae44
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: badd79926e8f039cf6b947dd6655e2cd679e3000
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33406973"
---
# <a name="cordebugsetcontextflag-enumeration"></a>CorDebugSetContextFlag, énumération
Indique si le contexte provient du frame (ou feuille) actif ou s'il a été calculé par déroulement à partir d'un autre frame.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum CorDebugSetContextFlag  
{  
   SET_CONTEXT_FLAG_ACTIVE_FRAME = 1  
   SET_CONTEXT_FLAG_UNWIND_FRAME = 2  
}  CorDebugSetContextFlag;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|SET_CONTEXT_FLAG_ACTIVE_FRAME|Le contexte est le contexte du thread actif.|  
|SET_CONTEXT_FLAG_UNWIND_FRAME|Le contexte a été calculé par déroulement à partir d’un autre frame.|  
  
## <a name="remarks"></a>Notes  
 `CorDebugSetContextFlag` Fournit des valeurs qui sont utilisées par le [ICorDebugStackWalk::SetContext](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-setcontext-method.md) (méthode).  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Énumérations de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)  
 [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
