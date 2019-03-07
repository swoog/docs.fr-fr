---
title: ICorDebugProcess::ModifyLogSwitch, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.ModifyLogSwitch
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::ModifyLogSwitch
helpviewer_keywords:
- ICorDebugProcess::ModifyLogSwitch method [.NET Framework debugging]
- ModifyLogSwitch method [.NET Framework debugging]
ms.assetid: 5fd30875-555e-4e96-877b-5dd266cde7c4
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4b1c85499e5269027da2c2a01ab67aab2c5da626
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57488173"
---
# <a name="icordebugprocessmodifylogswitch-method"></a>ICorDebugProcess::ModifyLogSwitch, méthode
Définit le niveau de gravité du commutateur de journal spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT ModifyLogSwitch(  
    [in] WCHAR *pLogSwitchName,  
    [in] LONG  lLevel);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pLogSwitchName`  
 [in] Un pointeur vers une chaîne qui spécifie le nom du commutateur de journal.  
  
 `lLevel`  
 [in] Le niveau de gravité à définir pour le commutateur de journal spécifié.  
  
## <a name="remarks"></a>Notes  
 Cette méthode est valide uniquement après la [ICorDebugManagedCallback::CreateProcess](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-createprocess-method.md) rappel s’est produite.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]
