---
title: Interface ICorDebugDataTarget
ms.date: 03/30/2017
api_name:
- ICoreClrDebugTarget
api_location:
- mscordbi_macx86.dll
api_type:
- COM
f1_keywords:
- ICoreClrDebugTarget
helpviewer_keywords:
- remote debugging API [Silverlight]
- ICorClrDebugTarget interface
- Silverlight, remote debugging
ms.assetid: 7cfaee76-e284-4a66-a431-8e33f0f60038
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 371768a8306c3751e7fc54b91a8583df41ad219b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33422280"
---
# <a name="icoreclrdebugtarget-interface"></a>Interface ICorDebugDataTarget
Fournit des méthodes qui contrôlent les nombres de références, énumérer des processus et libèrent la mémoire associée à un débogueur est attaché à une cible distante Macintosh Silverlight.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
class ICoreClrDebugTarget {  
      HRESULT EnumProcesses (  
          [out] DWORD*                    pcProcs,  
          [out] CoreClrDebugProcInfo**    ppProcs  
      );  
  
      HRESULT EnumRuntimes (  
      [in]  DWORD                      dwInternalProcessID,  
      [out] DWORD*                     pcRuntimes,  
      [out] CoreClrDebugRuntimeInfo**  ppRuntimes  
      );  
  
      void FreeMemory (  
      [in] void*      pMemory  
    );  
};  
```  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[ICoreClrDebugTarget::EnumProcesses, méthode](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-enumprocesses-method.md)|Énumère les processus en cours d'exécution sur un ordinateur distant.|  
|[ICoreClrDebugTarget::EnumRuntimes, méthode](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-enumruntimes-method.md)|Énumère le common language runtime (CLR) dans le processus spécifié sur un ordinateur distant.|  
|[ICoreClrDebugTarget::FreeMemory, méthode](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-freememory-method.md)|Libère la mémoire allouée par les méthodes d’énumération dans cette classe.|  
  
## <a name="remarks"></a>Notes  
 Actuellement, cette fonctionnalité est prise en charge uniquement pour le débogage d’une cible d’une application basée sur Silverlight qui s’exécute sur un ordinateur Macintosh distant.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CoreClrRemoteDebuggingInterfaces.h  
  
 **Bibliothèque :** mscordbi_macx86.dll  
  
 **Versions du .NET framework :** 3.5 SP1  
  
## <a name="see-also"></a>Voir aussi  
 [ICorDebugRemoteTarget, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugremotetarget-interface.md)  
 [ICorDebug, interface](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)  
    
 [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
