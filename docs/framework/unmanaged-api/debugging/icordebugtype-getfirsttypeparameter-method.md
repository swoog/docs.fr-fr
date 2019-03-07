---
title: ICorDebugType::GetFirstTypeParameter, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugType.GetFirstTypeParameter
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugType::GetFirstTypeParameter
helpviewer_keywords:
- ICorDebugType::GetFirstTypeParameter method [.NET Framework debugging]
- GetFirstTypeParameter method [.NET Framework debugging]
ms.assetid: 35bb594f-af6a-4349-83fe-e98702674e03
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4d872e4a65c0556dddac468336e6a42dd7d7923c
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57477647"
---
# <a name="icordebugtypegetfirsttypeparameter-method"></a>ICorDebugType::GetFirstTypeParameter, méthode
Obtient un pointeur d’interface ICorDebugType qui représente le premier <xref:System.Type> paramètre du type représenté par ce `ICorDebugType`.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetFirstTypeParameter (  
    [out] ICorDebugType   **value  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `value`  
 [out] Un pointeur vers l’adresse d’un `ICorDebugType` objet qui représente le premier paramètre.  
  
## <a name="remarks"></a>Notes  
 `GetFirstTypeParameter` peut être appelée dans les cas où les informations supplémentaires sur le type impliquent, au maximum, un paramètre de type. En particulier, il peut être utilisé si le type est un ELEMENT_TYPE_ARRAY ELEMENT_TYPE_SZARRAY, ELEMENT_TYPE_BYREF ou ELEMENT_TYPE_PTR, comme indiqué par le [ICorDebugType::GetType](../../../../docs/framework/unmanaged-api/debugging/icordebugtype-gettype-method.md) (méthode).  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]
