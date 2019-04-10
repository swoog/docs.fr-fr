---
title: ICorDebugValue, interface
ms.date: 03/30/2017
api_name:
- ICorDebugValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue
helpviewer_keywords:
- ICorDebugValue interface [.NET Framework debugging]
ms.assetid: b2f7007f-c446-4b18-aed1-a25cff8aee31
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bdc889dd6b2854654bfe43b24afbe4cc19863c80
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59227819"
---
# <a name="icordebugvalue-interface"></a>ICorDebugValue, interface
Représente une valeur dans le processus en cours de débogage. La valeur peut être une lecture ou une valeur de l’écriture.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[CreateBreakpoint, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-createbreakpoint-method.md)|Cette méthode n’est pas implémentée actuellement.|  
|[GetAddress, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-getaddress-method.md)|Obtient l’adresse de ce `ICorDebugValue` objet, qui est en cours de débogage.|  
|[GetSize, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-getsize-method.md)|Obtient la taille, en octets, de ce `ICorDebugValue` objet.|  
|[GetType, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue-gettype-method.md)|Obtient le type primitif de cet `ICorDebugValue` objet.|  
  
## <a name="remarks"></a>Notes  
 En règle générale, la propriété d’un objet de valeur est passée lorsqu’elle est retournée. Le destinataire est responsable de la suppression d’une référence à partir de l’objet lorsqu’il est terminé avec l’objet.  
  
 Selon où la valeur a été récupérée à partir de, la valeur restera ne peut-être pas valide une fois que le processus se poursuit. Par conséquent, en règle générale, la valeur ne doit pas être maintenue à travers un appel de la [ICorDebugController::Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md) (méthode).  
  
> [!NOTE]
>  Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorDebugValue3, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-interface.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
