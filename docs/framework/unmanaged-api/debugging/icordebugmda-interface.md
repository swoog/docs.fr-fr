---
title: ICorDebugMDA, interface
ms.date: 03/30/2017
api_name:
- ICorDebugMDA
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugMDA
helpviewer_keywords:
- ICorDebugMDA interface [.NET Framework debugging]
ms.assetid: 8ecbb854-295c-4dd4-b9fc-01ebeac46e06
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cea8f6827d3e361b3f6498e6612d8b11a2357285
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61916667"
---
# <a name="icordebugmda-interface"></a>ICorDebugMDA, interface
Représente un message d'Assistant Débogage managé (MDA).  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[GetDescription, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-getdescription-method.md)|Obtient une chaîne contenant une description de cet Assistant Débogage MANAGÉ.|  
|[GetFlags, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-getflags-method.md)|Obtient les indicateurs associés à cet Assistant Débogage MANAGÉ.|  
|[GetName, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-getname-method.md)|Obtient une chaîne contenant le nom de cet Assistant Débogage MANAGÉ.|  
|[GetOSThreadId, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-getosthreadid-method.md)|Obtient l’identificateur de thread de système d’exploitation sur lequel cet Assistant Débogage MANAGÉ s’exécute.|  
|[GetXML, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-getxml-method.md)|Obtient le flux XML complet associé à cet Assistant Débogage MANAGÉ.|  
  
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
- [Diagnostic d’erreurs avec les Assistants Débogage managé](../../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
