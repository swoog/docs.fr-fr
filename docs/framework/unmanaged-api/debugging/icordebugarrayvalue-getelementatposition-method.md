---
title: ICorDebugArrayValue::GetElementAtPosition, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugArrayValue.GetElementAtPosition
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugArrayValue::GetElementAtPosition
helpviewer_keywords:
- GetElementAtPosition method [.NET Framework debugging]
- ICorDebugArrayValue::GetElementAtPosition method [.NET Framework debugging]
ms.assetid: 6fd5eaa4-1997-4910-82f5-3887480db764
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 76100116f2ca3a9b9a99477ca2352d5fa1335ab2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61645680"
---
# <a name="icordebugarrayvaluegetelementatposition-method"></a>ICorDebugArrayValue::GetElementAtPosition, méthode
Obtient l’élément à la position donnée, en traitant le tableau comme un tableau unidimensionnel de base zéro.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetElementAtPosition (  
    [in]  ULONG32          nPosition,  
    [out] ICorDebugValue   **ppValue  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `nPosition`  
 [in] La position de l’élément à récupérer.  
  
 `ppValue`  
 [out] Pointeur vers l’adresse d’un objet ICorDebugValue qui représente la valeur de l’élément.  
  
## <a name="remarks"></a>Notes  
 La disposition d’un tableau multidimensionnel suit le style C++ de disposition de tableau.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
