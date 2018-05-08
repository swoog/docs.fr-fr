---
title: Méthode ICoreClrDebugTarget::EnumProcesses
ms.date: 03/30/2017
api_name:
- ICoreClrDebugTarget.EnumProcesses
api_location:
- mscordbi_macx86.dll
api_type:
- COM
f1_keywords:
- ICoreClrDebugTarget::EnumProcesses
helpviewer_keywords:
- remote debugging API [Silverlight]
- EnumProcesses method, ICorClrDebugTarget interface [Silverlight debugging]
- ICorClrDebugTarget::EnumProcesses method [Silverlight debugging]
- Silverlight, remote debugging
ms.assetid: e00fd477-4f49-43d3-bd0e-3094824b1136
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c09b70b5afb0561d32e55dd89df6cac083abc068
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="icoreclrdebugtargetenumprocesses-method"></a>Méthode ICoreClrDebugTarget::EnumProcesses
Énumère les processus en cours d'exécution sur un ordinateur distant.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT EnumProcesses (  
       [out]  DWORD*                  pcProcs,   
       [out]  CoreClrDebugProcInfo**  ppProcs  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `pcProcs`  
 [out] Nombre de processus retournés dans `ppProcs`. Cette valeur peut être égale à 0 (zéro).  
  
 `ppProcs`  
 [out] Un tableau de [CoreClrDebugProcInfo](../../../../docs/framework/unmanaged-api/debugging/coreclrdebugprocinfo-structure.md) des structures qui représentent les processus en cours d’exécution sur l’ordinateur distant.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK  
 Opération réussie.  
  
 E_OUTOFMEMORY  
 Impossible d'allouer suffisamment de mémoire pour `ppProcs`.  
  
 E_FAIL (ou autres codes de retour E_)  
 Autres échecs.  
  
## <a name="remarks"></a>Notes  
 Pour libérer la mémoire allouée par cette méthode, appelez le [ICoreClrDebugTarget::FreeMemory](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-freememory-method.md) (méthode).  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CoreClrRemoteDebuggingInterfaces.h  
  
 **Bibliothèque :** mscordbi_macx86.dll  
  
 **Versions du .NET framework :** 3.5 SP1  
  
## <a name="see-also"></a>Voir aussi  
 [ICoreClrDebugTarget, interface](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-interface.md)
