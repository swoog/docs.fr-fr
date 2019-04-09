---
title: ICorDebugController::EnumerateThreads, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugController.EnumerateThreads
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController::EnumerateThreads
helpviewer_keywords:
- ICorDebugController::EnumerateThreads method [.NET Framework debugging]
- EnumerateThreads method [.NET Framework debugging]
ms.assetid: 73f536f6-4668-4a4a-b3e4-ac7df862d5be
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 17ba15553d2e7dcd2090870eaab54b4c680631f1
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59163083"
---
# <a name="icordebugcontrollerenumeratethreads-method"></a>ICorDebugController::EnumerateThreads, méthode
Obtient un énumérateur pour les threads managés actives dans le processus.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT EnumerateThreads (  
    [out] ICorDebugThreadEnum **ppThreads  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `ppThreads`  
 [out] Pointeur vers l’adresse d’un objet « ICorDebugThreadEnum » qui représente un énumérateur pour tous les threads managés qui sont actifs dans le processus.  
  
## <a name="remarks"></a>Notes  
 Un thread est considéré comme actif une fois la [ICorDebugManagedCallback::CreateThread](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-createthread-method.md) du rappel et avant le [ICorDebugManagedCallback::ExitThread](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-exitthread-method.md) du rappel . Un thread managé ne peut pas nécessairement des frames managés sur sa pile. Les threads peuvent être énumérés avant même que le [ICorDebugManagedCallback::CreateProcess](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-createprocess-method.md) rappel. L’énumération sera naturellement vide.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
