---
title: Méthode ICoreClrDebugTarget::EnumRuntimes
ms.date: 03/30/2017
api_name:
- ICoreClrDebugTarget.EnumRuntimes
api_location:
- mscordbi_macx86.dll
api_type:
- COM
f1_keywords:
- ICoreClrDebugTarget::EnumRuntimes
helpviewer_keywords:
- remote debugging API [Silverlight]
- ICorClrDebugTarget::EnumRuntimes method [Silverlight debugging]
- EnumRuntimes method, ICoreClrDebugTarget interface [Silverlight debugging]
- Silverlight, remote debugging
ms.assetid: 316df866-442d-40cc-b049-45e8adcb65d1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: afb31646d21ec7e15f79601f5fe83ea6ce44fa90
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59134674"
---
# <a name="icoreclrdebugtargetenumruntimes-method"></a>Méthode ICoreClrDebugTarget::EnumRuntimes
Énumère les CLR (Common Language Runtime) dans le processus spécifié en cours d'exécution sur un ordinateur distant.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT EnumRuntimes (  
      [in] DWORD       dwInternalProcessID,  
      [out] DWORD*     pcRuntimes,  
      [out] CoreClrDebugRuntimeInfo**    ppRuntimes  
    );  
```  
  
## <a name="parameters"></a>Paramètres  
 `dwInternalProcessID`  
 [in] ID de processus interne du processus pour lequel vous souhaitez énumérer les runtimes. Il s’agit de `m_dwInternalID` correspondants [CoreClrDebugProcInfo](../../../../docs/framework/unmanaged-api/debugging/coreclrdebugprocinfo-structure.md).  
  
 `pcRuntimes`  
 [out] Nombre de runtimes retournés dans `ppRuntimes`. Cette valeur peut être égale à 0 (zéro).  
  
 `ppRuntimes`  
 [out] Un tableau de [CoreClrDebugRuntimeInfo](../../../../docs/framework/unmanaged-api/debugging/coreclrdebugruntimeinfo-structure.md) structures qui représentent les runtimes chargement dans le processus distant cible.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK  
 Opération réussie.  
  
 S_FALSE  
 `dwInternalProcessID` ne correspond pas à n’importe quel processus est en cours d’exécution sur l’ordinateur, probablement parce que le processus a été arrêté. `pcRuntimes` et `ppRuntimes` sera null.  
  
 E_OUTOFMEMORY  
 Impossible d'allouer suffisamment de mémoire pour `ppRuntimes`.  
  
 E_FAIL (ou autres codes de retour E_)  
 Autres échecs.  
  
## <a name="remarks"></a>Notes  
 Pour libérer la mémoire allouée par cette méthode, appelez le [ICoreClrDebugTarget::FreeMemory](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-freememory-method.md) (méthode).  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CoreClrRemoteDebuggingInterfaces.h  
  
 **Bibliothèque :** mscordbi_macx86.dll  
  
 **Versions du .NET framework :** 3.5 SP1  
  
## <a name="see-also"></a>Voir aussi

- [Interface ICorDebugDataTarget](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-interface.md)
