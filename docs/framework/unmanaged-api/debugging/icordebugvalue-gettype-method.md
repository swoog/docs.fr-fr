---
title: ICorDebugValue::GetType, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugValue.GetType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue::GetType
helpviewer_keywords:
- ICorDebugValue::GetType method [.NET Framework debugging]
- GetType method, ICorDebugValue interface [.NET Framework debugging]
ms.assetid: 41e2d503-e1f1-407b-abe0-6a29adb3e0d1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f99495b04942b7902619e0383522caf9f78ae984
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57492502"
---
# <a name="icordebugvaluegettype-method"></a>ICorDebugValue::GetType, méthode
Obtient le type primitif de cet objet « ICorDebugValue ».  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetType (  
    [out] CorElementType   *pType  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pType`  
 [out] Pointeur vers une valeur de l’énumération « CorElementType » qui indique le type de valeur.  
  
## <a name="remarks"></a>Notes  
 Si l’objet est un type d’exécution complexe, ce type peut être examiné via les sous-classes appropriées de le `ICorDebugValue` interface. Par exemple, « ICorDebugObjectValue » qui hérite de `ICorDebugValue`, représente un type complexe.  
  
 Le `GetType` et [ICorDebugObjectValue::GetClass](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-getclass-method.md) méthodes retournent des informations sur le type d’une valeur. Les deux sont remplacées par les compatible avec les génériques [ICorDebugValue2::GetExactType](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue2-getexacttype-method.md) (méthode).  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

