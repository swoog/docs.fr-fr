---
title: ICorDebugFrame, interface
ms.date: 03/30/2017
api_name:
- ICorDebugFrame
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame
helpviewer_keywords:
- ICorDebugFrame interface [.NET Framework debugging]
ms.assetid: 0c48f764-3c64-4602-b2f4-4ffc60eb2c65
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a15d7f16676b8b9d66f8d1ba7484f3fec5735a44
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61988752"
---
# <a name="icordebugframe-interface"></a>ICorDebugFrame, interface

Représente un frame sur la pile en cours.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[CreateStepper, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-createstepper-method.md)|Obtient un ICorDebugStepper pour effectuer des opérations pas à pas concernant ce `ICorDebugFrame`.|  
|[GetCallee, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getcallee-method.md)|Obtient un pointeur vers le `ICorDebugFrame` dans la chaîne actuelle que ce frame est appelé, ou retourne null si c’est le frame plus profond dans la chaîne.|  
|[GetCaller, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getcaller-method.md)|Obtient un pointeur vers le `ICorDebugFrame` dans la chaîne actuelle qui appelé ce frame, ou retourne null si c’est le frame le plus extérieur dans la chaîne.|  
|[GetChain, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getchain-method.md)|Obtient un pointeur vers ICorDebugChain ce `ICorDebugFrame` fait partie de.|  
|[GetCode, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getcode-method.md)|Obtient un pointeur vers ICorDebugCode associé à ce frame de pile.|  
|[GetFunction, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getfunction-method.md)|Obtient un pointeur vers ICorDebugFunction qui contient le code associé à ce frame de pile.|  
|[GetFunctionToken, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getfunctiontoken-method.md)|Obtient le jeton de métadonnées pour la fonction qui contient le code associé à ce frame de pile.|  
|[GetStackRange, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getstackrange-method.md)|Obtient la plage d’adresses absolues du frame de pile représenté par cet `ICorDebugFrame`.|  
  
## <a name="remarks"></a>Notes  
  
> [!NOTE]
>  Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
