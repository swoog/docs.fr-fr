---
title: ICorDebugManagedCallback2::FunctionRemapOpportunity, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback2.FunctionRemapOpportunity
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback2::FunctionRemapOpportunity
helpviewer_keywords:
- FunctionRemapOpportunity method [.NET Framework debugging]
- ICorDebugManagedCallback2::FunctionRemapOpportunity method [.NET Framework debugging]
ms.assetid: 0d6471bc-ad9b-4b1d-a307-c10443918863
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: dc900ca20ac87ddecfd8f7adf0894af21ca5d2f0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33418088"
---
# <a name="icordebugmanagedcallback2functionremapopportunity-method"></a>ICorDebugManagedCallback2::FunctionRemapOpportunity, méthode
Notifie le débogueur que l’exécution du code a atteint un point de séquence dans une version antérieure d’une fonction modifiée.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT FunctionRemapOpportunity (  
    [in] ICorDebugAppDomain   *pAppDomain,  
    [in] ICorDebugThread      *pThread,  
    [in] ICorDebugFunction    *pOldFunction,  
    [in] ICorDebugFunction    *pNewFunction,  
    [in] ULONG32              oldILOffset  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `pAppDomain`  
 [in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application contenant la fonction modifiée.  
  
 `pThread`  
 [in] Pointeur vers un objet ICorDebugThread qui représente le thread sur lequel le point d’arrêt de remappage a été rencontrée.  
  
 `pOldFunction`  
 [in] Pointeur vers un objet ICorDebugFunction qui représente la version de la fonction en cours d’exécution sur le thread.  
  
 `pNewFunction`  
 [in] Pointeur vers un objet ICorDebugFunction qui représente la version la plus récente de la fonction.  
  
 `oldILOffset`  
 [in] L’offset Microsoft intermediate language (MSIL), du pointeur d’instruction dans l’ancienne version de la fonction.  
  
## <a name="remarks"></a>Notes  
 Ce rappel permet au débogueur de remapper le pointeur d’instruction à son emplacement approprié dans la nouvelle version de la fonction spécifiée en appelant le [ICorDebugILFrame2::RemapFunction](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe2-remapfunction-method.md) (méthode). Si le débogueur n’appelle pas `RemapFunction` avant d’appeler le [ICorDebugController::Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md) (méthode), le runtime continue à exécuter l’ancien code et déclenchera un autre `FunctionRemapOpportunity` rappel au point de séquence suivant.  
  
 Ce rappel est appelé pour chaque frame qui exécute une ancienne version de la fonction donnée jusqu'à ce que le débogueur retourne S_OK.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [ICorDebugManagedCallback2, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-interface.md)  
 [ICorDebugManagedCallback, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
