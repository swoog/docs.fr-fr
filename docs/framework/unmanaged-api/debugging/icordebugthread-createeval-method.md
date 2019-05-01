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
ms.openlocfilehash: 2016795e7b2c0588e2bd69e764fb96f7f90b24d0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61994069"
---
# <a name="icordebugthreadcreateeval-method"></a>ICorDebugThread::CreateEval, méthode
Crée un objet ICorDebugEval qui recueille et expose les fonctionnalités de ICorDebugThread.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT CreateEval (  
    [out] ICorDebugEval   **ppEval  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `ppEval`  
 [out] Un pointeur vers l’adresse d’un `ICorDebugEval` objet qui recueille et expose les fonctionnalités de ce thread.  
  
## <a name="remarks"></a>Notes  
 L’objet d’évaluation envoie une nouvelle chaîne sur le thread avant de procéder à son calcul. Cela interrompt le calcul en cours d’exécution sur le thread jusqu'à ce que la version d’évaluation se termine.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
