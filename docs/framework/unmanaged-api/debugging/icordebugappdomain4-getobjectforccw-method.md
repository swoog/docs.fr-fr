---
title: ICorDebugAppDomain4::GetObjectForCCW, méthode
ms.date: 03/30/2017
ms.assetid: 2cacdb85-e7b8-42e7-b310-c3e8c22e5d33
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 985d98059c0c763f560d5e0f06133c45e75fa51a
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57490422"
---
# <a name="icordebugappdomain4getobjectforccw-method"></a>ICorDebugAppDomain4::GetObjectForCCW, méthode
Obtient un objet managé à partir d'un pointeur de wrapper CCW (COM Callable Wrapper).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetObjectForCCW(  
   [in]CORDB_ADDRESS ccwPointer,   
   [out]ICorDebugValue **ppManagedObject  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `ccwPointer`  
 [in] Pointeur vers un wrapper CCW (COM Callable Wrapper)  
  
 `ppManagedObject`  
 [out] Pointeur vers l’adresse d’un objet « ICorDebugValue » qui représente l’objet managé qui correspond au pointeur CCW donné.  
  
## <a name="remarks"></a>Notes  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICorDebugAppDomain4, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain4-interface.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
