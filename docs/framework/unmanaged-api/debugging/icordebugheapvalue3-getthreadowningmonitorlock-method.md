---
title: ICorDebugHeapValue3::GetThreadOwningMonitorLock, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugHeapValue3.GetThreadOwningMonitorLock
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapValue3::GetThreadOwningMonitorLock
helpviewer_keywords:
- GetThreadOwningMonitorLock method [.NET Framework debugging]
- ICorDebugHeapValue3::GetThreadOwningMonitorLock method [.NET Framework debugging]
ms.assetid: e06fc19d-2cf4-4cad-81a3-137a68af8969
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7ba09991e9452a86c6b7a1cbb08a38a71ba2aeaa
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="icordebugheapvalue3getthreadowningmonitorlock-method"></a>ICorDebugHeapValue3::GetThreadOwningMonitorLock, méthode
Retourne le thread managé qui possède le verrou du moniteur sur cet objet.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetThreadOwningMonitorLock (  
    [out] ICorDebugThread   **ppThread,  
    [out] DWORD              *pAcquisitionCount  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `ppThread`  
 [out] Le thread managé qui possède le verrou du moniteur sur cet objet.  
  
 `pAcquisitionCount`  
 [out] Le nombre de fois où que ce thread aurait pour libérer le verrou avant qu’il redevienne sans propriétaire.  
  
## <a name="return-value"></a>Valeur de retour  
 Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.  
  
|HRESULT|Description|  
|-------------|-----------------|  
|S_OK|La commande s'est correctement terminée.|  
|S_FALSE|Aucun thread managé ne possède le verrou du moniteur sur cet objet.|  
  
## <a name="exceptions"></a>Exceptions  
  
## <a name="remarks"></a>Notes  
 Si un thread managé possède le verrou du moniteur sur cet objet :  
  
-   La méthode retourne S_OK.  
  
-   L’objet thread est valide jusqu'à ce que le thread se ferme.  
  
 Si aucun thread managé possède le verrou du moniteur sur cet objet, `ppThread` et `pAcquisitionCount` sont identiques, et la méthode retourne S_FALSE.  
  
 Si `ppThread` ou `pAcquisitionCount` n’est pas un pointeur valid, le résultat est indéfini.  
  
 Si une erreur se produit et il ne peut pas déterminer qui, le cas échéant, le thread possède le verrou du moniteur sur cet objet, la méthode retourne un HRESULT qui indique un échec.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
