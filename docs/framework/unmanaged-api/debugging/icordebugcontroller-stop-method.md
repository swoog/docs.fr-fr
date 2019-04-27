---
title: ICorDebugController::Stop, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugController.Stop
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController::Stop
helpviewer_keywords:
- Stop method, ICorDebugController interface [.NET Framework debugging]
- ICorDebugController::Stop method [.NET Framework debugging]
ms.assetid: c34e79be-a7fb-479e-8dec-d126a4c330e5
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 724db8c5c8dbb5bf3ff8bc7202a60397180b7b38
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61749061"
---
# <a name="icordebugcontrollerstop-method"></a>ICorDebugController::Stop, méthode
Effectue un arrêt coopératif sur tous les threads qui exécutent du code managé dans le processus.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT Stop (  
    [in] DWORD dwTimeoutIgnored  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `dwTimeoutIgnored`  
 Non utilisé.  
  
## <a name="remarks"></a>Notes  
 `Stop` effectue un arrêt coopératif sur tous les threads en cours d’exécution code managé dans le processus. Pendant une session de débogage managé uniquement, les threads non managés peuvent continuer à exécuter (mais sera bloqué lorsque vous tentez d’appeler du code managé). Pendant une session de débogage d’interopérabilité, les threads non managés seront également arrêtés. Le `dwTimeoutIgnored` valeur est actuellement ignorée et traitée en tant que « Infinite » (-1). Si l’arrêt coopératif échoue en raison d’un blocage, tous les threads sont suspendus et E_TIMEOUT est retourné.  
  
> [!NOTE]
>  `Stop` est la seule méthode synchrone dans l’API de débogage. Lorsque `Stop` retourne S_OK, le processus est arrêté. Aucun rappel n’est donné à informer les écouteurs de l’arrêt. Le débogueur doit appeler [ICorDebugController::Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md) pour permettre la reprise du processus.  
  
 Le débogueur gère un compteur de mots vides. Lorsque le compteur atteint zéro, le contrôleur est repris. Chaque appel à `Stop` ou chaque rappel distribué incrémente le compteur. Chaque appel à `ICorDebugController::Continue` décrémente le compteur.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
