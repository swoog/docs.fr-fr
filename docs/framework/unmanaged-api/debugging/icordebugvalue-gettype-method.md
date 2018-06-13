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
ms.openlocfilehash: 0fc0dd03abc1adb8eeea76a1053fb4d58de4ecf8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33419830"
---
# <a name="icordebugvaluegettype-method"></a>ICorDebugValue::GetType, méthode
Obtient le type primitif de cet objet « ICorDebugValue ».  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetType (  
    [out] CorElementType   *pType  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `pType`  
 [out] Pointeur vers une valeur de l’énumération « CorElementType » qui indique le type de valeur.  
  
## <a name="remarks"></a>Notes  
 Si l’objet est un type d’exécution complexe, ce type peut être examiné via les sous-classes appropriées de le `ICorDebugValue` interface. Par exemple, « ICorDebugObjectValue » qui hérite de `ICorDebugValue`, représente un type complexe.  
  
 Le `GetType` et [ICorDebugObjectValue::GetClass](../../../../docs/framework/unmanaged-api/debugging/icordebugobjectvalue-getclass-method.md) méthodes retournent des informations sur le type d’une valeur. Les deux sont remplacées par les compatible avec les génériques [ICorDebugValue2::GetExactType](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue2-getexacttype-method.md) (méthode).  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 
