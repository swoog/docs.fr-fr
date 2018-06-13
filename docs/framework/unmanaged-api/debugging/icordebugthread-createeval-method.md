---
title: ICorDebugThread::CreateEval, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugThread.CreateEval
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::CreateEval
helpviewer_keywords:
- CreateEval method [.NET Framework debugging]
- ICorDebugThread::CreateEval method [.NET Framework debugging]
ms.assetid: 36605067-33d3-4579-9c72-fb0e551ab0f1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5e2d99d85a6e6b09558e5941d08a7f522aaf66cb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33421815"
---
# <a name="icordebugthreadcreateeval-method"></a>ICorDebugThread::CreateEval, méthode
Crée un objet ICorDebugEval qui rassemble et expose les fonctionnalités de ICorDebugThread.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT CreateEval (  
    [out] ICorDebugEval   **ppEval  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `ppEval`  
 [out] Un pointeur vers l’adresse d’un `ICorDebugEval` objet qui rassemble et expose les fonctionnalités de ce thread.  
  
## <a name="remarks"></a>Notes  
 L’objet d’évaluation envoie une nouvelle chaîne sur le thread avant de procéder à son calcul. Cela interrompt le calcul en cours d’exécution sur le thread jusqu'à ce que l’évaluation s’exécute.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
