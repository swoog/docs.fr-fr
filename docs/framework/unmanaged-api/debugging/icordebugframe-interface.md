---
title: ICorDebugFrame Interface1
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
ms.openlocfilehash: f3d6c1a2bfd66e275b506d4465731c48cd7c6515
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33416629"
---
# <a name="icordebugframe-interface1"></a>ICorDebugFrame Interface1
Représente un frame sur la pile en cours.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[CreateStepper, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-createstepper-method.md)|Obtient un ICorDebugStepper pour effectuer des opérations pas à pas relatif à cette `ICorDebugFrame`.|  
|[GetCallee, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getcallee-method.md)|Obtient un pointeur vers le `ICorDebugFrame` dans la chaîne actuelle que ce frame a appelée ou retourne null s’il est le plus profond frame dans la chaîne.|  
|[GetCaller, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getcaller-method.md)|Obtient un pointeur vers le `ICorDebugFrame` dans la chaîne actuelle que ce frame a appelée ou retourne null s’il est le frame le plus extérieur de la chaîne.|  
|[GetChain, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getchain-method.md)|Obtient un pointeur vers ICorDebugChain ce `ICorDebugFrame` fait partie.|  
|[GetCode, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getcode-method.md)|Obtient un pointeur vers ICorDebugCode associé à ce frame de pile.|  
|[GetFunction, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getfunction-method.md)|Obtient un pointeur vers ICorDebugFunction qui contient le code associé à ce frame de pile.|  
|[GetFunctionToken, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getfunctiontoken-method.md)|Obtient le jeton de métadonnées pour la fonction qui contient le code associé à ce frame de pile.|  
|[GetStackRange, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getstackrange-method.md)|Obtient la plage d’adresses absolues du frame de pile représenté par ce `ICorDebugFrame`.|  
  
## <a name="remarks"></a>Notes  
  
> [!NOTE]
>  Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
