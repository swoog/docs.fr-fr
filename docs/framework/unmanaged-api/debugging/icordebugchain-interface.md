---
title: ICorDebugChain Interface1
ms.date: 03/30/2017
api_name:
- ICorDebugChain
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain
helpviewer_keywords:
- ICorDebugChain interface [.NET Framework debugging]
ms.assetid: f671f519-1cb3-4ae5-b9f1-abc5e783459f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 32889a8e8867fc42b48413463095dda423f26b85
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33409839"
---
# <a name="icordebugchain-interface1"></a>ICorDebugChain Interface1
Représente un segment d'une pile des appels physique ou logique.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[EnumerateFrames, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-enumerateframes-method.md)|Obtient un énumérateur qui contient tous les frames de pile managés dans la chaîne, en commençant par le frame le plus récent.|  
|[GetActiveFrame, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getactiveframe-method.md)|Obtient l’active (autrement dit, la plus récente) frame sur la chaîne.|  
|[GetCallee, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getcallee-method.md)|Obtient la chaîne qui a été appelée par cette chaîne.|  
|[GetCaller, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getcaller-method.md)|Obtient la chaîne qui a appelé cette chaîne.|  
|[GetContext, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getcontext-method.md)|Non implémenté.|  
|[GetNext, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getnext-method.md)|Obtient la chaîne suivante de frames pour le thread.|  
|[GetPrevious, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getprevious-method.md)|Obtient la précédente chaîne de frames pour le thread.|  
|[GetReason, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getreason-method.md)|Obtient la raison pour la genèse de cette chaîne appelante.|  
|[GetRegisterSet, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getregisterset-method.md)|Obtient le jeu de registres pour la partie active de cette chaîne.|  
|[GetStackRange, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getstackrange-method.md)|Obtient la plage d’adresses du segment de pile pour cette chaîne.|  
|[GetThread, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-getthread-method.md)|Obtient le thread physique que cette chaîne d’appel est partie.|  
|[IsManaged, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugchain-ismanaged-method.md)|Obtient une valeur qui indique si cette chaîne est en cours d’exécution du code managé.|  
  
## <a name="remarks"></a>Notes  
 Les frames de pile dans une chaîne occupent l’espace de pile contigu et partagent les mêmes thread et contexte. Une chaîne peut représenter soit chaînes en code managé ou non managé. Vide `ICorDebugChain` instance représente une chaîne de code non managé.  
  
> [!NOTE]
>  Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
