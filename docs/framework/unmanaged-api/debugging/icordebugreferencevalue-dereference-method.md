---
title: ICorDebugReferenceValue::Dereference, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugReferenceValue.Dereference
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugReferenceValue::Dereference
helpviewer_keywords:
- ICorDebugReferenceValue::Dereference method [.NET Framework debugging]
- Dereference method [.NET Framework debugging]
ms.assetid: 5ec8cf76-3deb-4ce6-9a49-77a4c35d80b9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2a0fd1981e7da5af19cf3a422c6008d373e9ac92
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33416590"
---
# <a name="icordebugreferencevaluedereference-method"></a>ICorDebugReferenceValue::Dereference, méthode
Obtient l’objet qui est référencé.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT Dereference (  
    [out] ICorDebugValue  **ppValue  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `ppValue`  
 [out] Pointeur vers l’adresse d’un ICorDebugValue qui représente l’objet vers lequel pointe cet objet ICorDebugReferenceValue.  
  
## <a name="remarks"></a>Notes  
 Le `ICorDebugValue` objet est valide uniquement lors de sa référence n’a pas été désactivé.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
