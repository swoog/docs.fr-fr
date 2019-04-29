---
title: ICorDebugEval::GetResult, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugEval.GetResult
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval::GetResult
helpviewer_keywords:
- ICorDebugEval::GetResult method [.NET Framework debugging]
- GetResult method [.NET Framework debugging]
ms.assetid: 50dbb9af-58a1-41f4-b56d-3da20011884f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b8e7fcb4f44d6bdf6f18c93b1046b549331621a4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61667117"
---
# <a name="icordebugevalgetresult-method"></a>ICorDebugEval::GetResult, méthode
Obtient les résultats de cette évaluation.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetResult (  
    [out] ICorDebugValue    **ppResult  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `ppResult`  
 [out] Pointeur vers l’adresse d’un objet ICorDebugValue qui représente les résultats de cette évaluation, si l’évaluation se termine normalement.  
  
## <a name="remarks"></a>Notes  
 Le `GetResult` méthode est valide uniquement lorsque la version d’évaluation est terminée.  
  
 Si la version d’évaluation se termine normalement, `ppResult` spécifie les résultats. Si elle se termine par une exception, le résultat est l’exception levée. Si l’évaluation a été d’un nouvel objet, le résultat est la référence au nouvel objet.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
