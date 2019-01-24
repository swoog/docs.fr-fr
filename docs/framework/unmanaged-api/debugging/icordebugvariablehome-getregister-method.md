---
title: ICorDebugVariableHome::GetRegister (méthode)
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHome.GetRegister
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHome::GetRegister
helpviewer_keywords:
- ICorDebugVariableHome::GetRegister method [.NET Framework debugging]
- GetRegister method, ICorDebugVariableHome interface [.NET Framework debugging]
ms.assetid: a5eecd7b-b04c-4266-bff2-7c8771d519a8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7d678b6f52719287a1e8bbe88d178fa47b2893ca
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54563143"
---
# <a name="icordebugvariablehomegetregister-method"></a>ICorDebugVariableHome::GetRegister (méthode)
Obtient le Registre qui contient une variable avec un type d’emplacement de `VLT_REGISTER`, le Registre de base et d’une variable avec un type d’emplacement de `VLT_REGISTER_RELATIVE`.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetRegister(  
    [out] CorDebugRegister *pRegister  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `pRegister`  
 [out] Une valeur d’énumération CorDebugRegister qui indique le Registre pour une variable avec un type d’emplacement de `VLT_REGISTER`, le Registre de base et d’une variable avec un type d’emplacement de `VLT_REGISTER_RELATIVE`.  
  
## <a name="return-value"></a>Valeur de retour  
 La méthode retourne les valeurs suivantes :  
  
|Value|Description|  
|-----------|-----------------|  
|`S_OK`|La variable est dans le Registre indiqué par le `pRegister` argument.|  
|`E_FAIL`|La variable n’est pas dans un Registre ou un emplacement relative au Registre.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [VariableLocationType, énumération](../../../../docs/framework/unmanaged-api/debugging/variablelocationtype-enumeration.md)
- [ICorDebugVariableHome, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md)
