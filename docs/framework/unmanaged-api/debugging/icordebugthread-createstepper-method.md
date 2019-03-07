---
title: ICorDebugThread::CreateStepper, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugThread.CreateStepper
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::CreateStepper
helpviewer_keywords:
- ICorDebugThread::CreateStepper method [.NET Framework debugging]
- CreateStepper method, ICorDebugThread interface [.NET Framework debugging]
ms.assetid: 4657443f-dd12-431b-a648-175c23f13c83
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 89182739633984011aaab3d7900d376b6db5ef99
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57476202"
---
# <a name="icordebugthreadcreatestepper-method"></a>ICorDebugThread::CreateStepper, méthode
Crée un objet ICorDebugStepper qui permet l’exécution pas à pas via le frame actif de ICorDebugThread.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT CreateStepper (  
    [out] ICorDebugStepper **ppStepper  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `ppStepper`  
 [out] Un pointeur vers l’adresse d’un `ICorDebugStepper` objet qui permet l’exécution pas à pas via le frame actif de ce thread.  
  
## <a name="remarks"></a>Notes  
 Le frame actif peut être le code non managé.  
  
 Le `ICorDebugStepper` interface doit être utilisée pour effectuer l’exécution pas à pas réelle.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
