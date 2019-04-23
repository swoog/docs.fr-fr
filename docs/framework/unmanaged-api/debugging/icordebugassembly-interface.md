---
title: ICorDebugAssembly, interface
ms.date: 03/30/2017
api_name:
- ICorDebugAssembly
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAssembly
helpviewer_keywords:
- ICorDebugAssembly interface [.NET Framework debugging]
ms.assetid: 9d657a28-6984-4c5e-8a54-89d20080baff
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3dd60defc1c003fa4b235ddcb0a78b9a819b1b0c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59198021"
---
# <a name="icordebugassembly-interface"></a>ICorDebugAssembly, interface

Représente un assembly.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[EnumerateModules, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-enumeratemodules-method.md)|Obtient un énumérateur pour les modules contenus dans l’assembly.|  
|[GetAppDomain, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-getappdomain-method.md)|Obtient un pointeur d’interface vers le domaine d’application qui contient ce `ICorDebugAssembly` instance.|  
|[GetCodeBase, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-getcodebase-method.md)|Non implémenté dans la version actuelle du .NET Framework.|  
|[GetName, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-getname-method.md)|Obtient le nom de l'assembly.|  
|[GetProcess, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly-getprocess-method.md)|Obtient l’instance ICorDebugProcess dans lequel l’assembly est en cours d’exécution.|  
  
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
