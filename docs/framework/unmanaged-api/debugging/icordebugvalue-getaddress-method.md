---
title: ICorDebugValue::GetAddress, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugValue.GetAddress
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue::GetAddress
helpviewer_keywords:
- ICorDebugValue::GetAddress method [.NET Framework debugging]
- GetAddress method, ICorDebugValue interface [.NET Framework debugging]
ms.assetid: a247c792-45e1-4538-9e1f-b46acca4a463
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ac550ee7b1d66612557b30d15c275c90cf09b8af
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59187329"
---
# <a name="icordebugvaluegetaddress-method"></a>ICorDebugValue::GetAddress, méthode
Obtient l’adresse de cet objet « ICorDebugValue », qui est en cours de débogage.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetAddress (  
    [out] CORDB_ADDRESS   *pAddress  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pAddress`  
 [out] Pointeur vers un `CORDB_ADDRESS` objet qui spécifie l’adresse de cet objet de valeur.  
  
## <a name="remarks"></a>Notes  
 Si la valeur n’est pas disponible, 0 (zéro) est retournée. Cela peut se produire si la valeur est au moins en partie dans les registres ou stockées dans un handle du RÉCUPÉRATEUR de mémoire (`GCHandle`).  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
