---
title: ICorDebugVariableHomeEnum Interface
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHomeEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHomeEnum
helpviewer_keywords:
- ICorDebugVariableHomeEnum interface [.NET Framework debugging]
ms.assetid: c312ae6d-c8dc-48d6-9f1e-ead515c88fdf
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4e67e4685320f56a4a6a8be2e3eb2e6c8065ce59
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61769003"
---
# <a name="icordebugvariablehomeenum-interface"></a>ICorDebugVariableHomeEnum Interface
Fournit un énumérateur pour les variables locales et les arguments dans une fonction.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[Next, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehomeenum-next-method.md)|Obtient le nombre spécifié de [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) instances qui contiennent des informations sur les variables locales et les arguments dans une fonction.|  
  
## <a name="remarks"></a>Notes  
 Le `ICorDebugVariableHomeEnum` interface implémente l’interface ICorDebugEnum.  
  
 Un `ICorDebugVariableHomeEnum` instance est remplie avec [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) instances en appelant le [ICorDebugCode4::EnumerateVariableHomes](../../../../docs/framework/unmanaged-api/debugging/icordebugcode4-enumeratevariablehomes-method.md) (méthode). Chaque [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) instance dans la collection représente une variable locale ou un argument dans une fonction. Le [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) objets dans la collection peuvent être énumérés en appelant le [ICorDebugVariableHomeEnum::Next](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehomeenum-next-method.md) (méthode).  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorDebugVariableHome, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
