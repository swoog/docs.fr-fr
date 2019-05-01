---
title: ICorDebugModule2, interface
ms.date: 03/30/2017
api_name:
- ICorDebugModule2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule2
helpviewer_keywords:
- ICorDebugModule2 interface [.NET Framework debugging]
ms.assetid: 0847e64f-fdbe-4c96-8168-da20fdc84d80
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d3fb1bf3f61c78f4eb157b93363b1c06b25bee04
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61987946"
---
# <a name="icordebugmodule2-interface"></a>ICorDebugModule2, interface

Sert d’extension logique à l’interface ICorDebugModule.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[ApplyChanges, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-applychanges-method.md)|Applique les modifications dans les métadonnées et les modifications dans le code de Microsoft intermediate language (MSIL) pour le processus en cours d’exécution.|  
|[GetJITCompilerFlags, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-getjitcompilerflags-method.md)|Obtient les indicateurs qui contrôlent la compilation juste-à-temps (JIT) pour ce `ICorDebugModule2`.|  
|[ResolveAssembly, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-resolveassembly-method.md)|Résout l’assembly référencé par le jeton de métadonnées spécifié.|  
|[SetJITCompilerFlags, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-setjitcompilerflags-method.md)|Définit les indicateurs qui contrôlent la compilation JIT pour ce `ICorDebugModule2`.|  
|[SetJMCStatus, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-setjmcstatus-method.md)|Définit l’état uniquement mon Code (JMC) de toutes les méthodes de toutes les classes dans ce `ICorDebugModule2` à la valeur spécifiée, à l’exception de celles figurant dans le `pTokens` tableau, il définit la valeur opposée.|  
  
## <a name="remarks"></a>Notes  
  
> [!NOTE]
>  Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
