---
title: ICorDebugReferenceValue::GetValue, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugReferenceValue.GetValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugReferenceValue::GetValue
helpviewer_keywords:
- GetValue method, ICorDebugReferenceValue interface [.NET Framework debugging]
- ICorDebugReferenceValue::GetValue method [.NET Framework debugging]
ms.assetid: 5da07f99-6c70-46ec-b997-5ab6fb7106cd
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e52ef20f2b8e3937911dc37e68f8a338ab0d85d9
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57468869"
---
# <a name="icordebugreferencevaluegetvalue-method"></a>ICorDebugReferenceValue::GetValue, méthode
Obtient l’adresse mémoire actuelle de l’objet référencé.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetValue (  
    [out] CORDB_ADDRESS   *pValue  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pValue`  
 [out] Un pointeur vers un `CORDB_ADDRESS` valeur qui spécifie l’adresse de l’objet vers lequel pointe cet objet ICorDebugReferenceValue.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
