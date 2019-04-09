---
title: ICorDebugExceptionDebugEvent::GetStackPointer, méthode
ms.date: 03/30/2017
ms.assetid: d8f66a1c-16be-4264-afc5-bc2dfbb4a682
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d9d4c0a1938edd3e2fe88ea6e418b3430f1b5cb8
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59163200"
---
# <a name="icordebugexceptiondebugeventgetstackpointer-method"></a>ICorDebugExceptionDebugEvent::GetStackPointer, méthode
Obtient le pointeur de pile de cet événement de débogage d'exception.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetStackPointer(  
   [out]CORDB_ADDRESS *pStackPointer  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pStackPointer`  
 [out] Pointeur vers l'adresse du pointeur de pile de cet événement de débogage d'exception. Pour plus d'informations, consultez la section Notes.  
  
## <a name="remarks"></a>Notes  
 La signification de ce pointeur de pile varie selon le type d'événement, comme indiqué dans le tableau suivant.  
  
|Type d'événement|Signification de la valeur `pStackPointer`|  
|----------------|--------------------------------------|  
|[MANAGED_EXCEPTION_FIRST_CHANCE](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)|Pointeur de pile du frame ayant levé l'exception.|  
|[MANAGED_EXCEPTION_USER_FIRST_CHANCE](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)|Pointeur de pile du frame de code utilisateur le plus proche du point de l'exception levée.|  
|[MANAGED_EXCEPTION_CATCH_HANDLER_FOUND](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)|Pointeur de pile du frame contenant le gestionnaire catch.|  
|[MANAGED_EXCEPTION_UNHANDLED](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)|`pStackPointer` est **null**.|  
  
> [!NOTE]
>  Cette méthode est uniquement disponible avec .NET Native.  
  
 Le type d’événement est disponible à partir de la [ICorDebugDebugEvent::GetEventKind](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-geteventkind-method.md) (méthode).  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorDebugExceptionDebugEvent, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptiondebugevent-interface.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
