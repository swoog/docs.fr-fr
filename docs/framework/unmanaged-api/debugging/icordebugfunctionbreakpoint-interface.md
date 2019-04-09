---
title: ICorDebugFunctionBreakpoint, interface
ms.date: 03/30/2017
api_name:
- ICorDebugFunctionBreakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunctionBreakpoint
helpviewer_keywords:
- ICorDebugFunctionBreakpoint interface [.NET Framework debugging]
ms.assetid: 9c149303-14b1-4138-83d7-e8c3e0fcd332
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0f15b9f5961699f905e765426576bdf6f3416793
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59141152"
---
# <a name="icordebugfunctionbreakpoint-interface"></a>ICorDebugFunctionBreakpoint, interface

Étend l’interface ICorDebugBreakpoint pour prendre en charge des points d’arrêt dans les fonctions.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[GetFunction, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugfunctionbreakpoint-getfunction-method.md)|Obtient un pointeur d’interface ICorDebugFunction qui référence la fonction dans laquelle le point d’arrêt est défini.|  
|[GetOffset, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugfunctionbreakpoint-getoffset-method.md)|Obtient l’offset du point d’arrêt dans la fonction.|  
  
## <a name="remarks"></a>Notes  
  
> [!NOTE]
>  Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
