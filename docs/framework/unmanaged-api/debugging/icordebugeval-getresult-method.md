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
ms.openlocfilehash: 7e160eddf667b542929c8dd3790de666a8e8bb77
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33413057"
---
# <a name="icordebugevalgetresult-method"></a>ICorDebugEval::GetResult, méthode
Obtient les résultats de cette évaluation.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetResult (  
    [out] ICorDebugValue    **ppResult  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `ppResult`  
 [out] Pointeur vers l’adresse d’un objet ICorDebugValue qui représente les résultats de cette évaluation, si l’évaluation s’exécute normalement.  
  
## <a name="remarks"></a>Notes  
 Le `GetResult` méthode est valide uniquement lorsque l’évaluation est terminée.  
  
 Si l’évaluation s’exécute normalement, `ppResult` spécifie les résultats. Si elle se termine avec une exception, le résultat est l’exception levée. Si l’évaluation a été d’un nouvel objet, le résultat est la référence au nouvel objet.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
