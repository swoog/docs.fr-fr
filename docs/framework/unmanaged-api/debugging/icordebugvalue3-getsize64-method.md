---
title: ICorDebugValue3::GetSize64, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugValue3::GetSize64
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue3::GetSize64
helpviewer_keywords:
- GetSize64 method, ICorDebugValue3 interface [.NET Framework debugging]
- ICorDebugValue3::GetSize64 method [.NET Framework debugging]
ms.assetid: fee56a29-3154-4192-958d-71da2ced3740
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7c0b45e08f7b88d9374023f95c6e3e22139c8949
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59144766"
---
# <a name="icordebugvalue3getsize64-method"></a>ICorDebugValue3::GetSize64, méthode
Obtient la taille, en octets, de ce [ICorDebugValue3](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-interface.md) objet.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetSize64(  
    [out] ULONG64 *pSize  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 pSize  
 [out] Pointeur vers la taille, en octets, de cet objet.  
  
## <a name="remarks"></a>Notes  
 Si le type de cette valeur est un type référence, cette méthode retourne la taille du pointeur plutôt que la taille de l’objet.  
  
 Le `ICorDebugValue3::GetSize` méthode diffère de la [ICorDebugValue::GetSize](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-getsize-method.md) méthode dans le type de son paramètre de sortie. Dans [ICorDebugValue::GetSize](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-getsize-method.md), le paramètre de sortie est un `ULONG32`; dans `ICorDebugValue3::GetSize`, il est un `ULONG64`. Cela permet la [ICorDebugValue3](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-interface.md) interface pour signaler la taille des tableaux qui dépassent 2 Go.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorDebugValue3, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-interface.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
