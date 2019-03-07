---
title: ICorDebugBreakpoint::Activate, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugBreakpoint.Activate
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugBreakpoint::Activate
helpviewer_keywords:
- ICorDebugBreakpoint::Activate method [.NET Framework debugging]
- Activate method [.NET Framework debugging]
ms.assetid: e30c29f7-3f19-4081-b572-a731aa14cd44
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2ac37df58762dac4e3a6161361cafd8ea87e2657
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57491358"
---
# <a name="icordebugbreakpointactivate-method"></a>ICorDebugBreakpoint::Activate, méthode
Définit l’état actif de ce `ICorDebugBreakpoint`.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT Activate (  
    [in] BOOL bActive  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `bActive`  
 [in] Définissez cette valeur sur `true` pour spécifier l’état actif ; sinon, définissez cette valeur sur `false`.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
