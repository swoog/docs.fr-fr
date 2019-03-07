---
title: ICorDebugBreakpoint::IsActive, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugBreakpoint.IsActive
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugBreakpoint::IsActive
helpviewer_keywords:
- ICorDebugBreakpoint::IsActive method [.NET Framework debugging]
- IsActive method, ICorDebugBreakpoint interface [.NET Framework debugging]
ms.assetid: 06e583d6-d88a-4ff5-bb95-5c48618a461c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5df5bed730211676acc4770c91cc6551bde0179b
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57464722"
---
# <a name="icordebugbreakpointisactive-method"></a>ICorDebugBreakpoint::IsActive, méthode
Obtient une valeur qui indique si ce `ICorDebugBreakpoint` est actif.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT IsActive (  
    [out] BOOL *pbActive  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pbActive`  
 [out] `true` si ce point d’arrêt est actif ; sinon, `false`.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
