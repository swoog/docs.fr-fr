---
title: ICorProfilerInfo::SetEnterLeaveFunctionHooks, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.SetEnterLeaveFunctionHooks
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::SetEnterLeaveFunctionHooks
helpviewer_keywords:
- SetEnterLeaveFunctionHooks method [.NET Framework profiling]
- ICorProfilerInfo::SetEnterLeaveFunctionHooks method [.NET Framework profiling]
ms.assetid: 72399636-c219-4ffd-8ac8-39432c9d4641
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a2d45e98f3e7b71375b14c43c4bff4929bc79494
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59142530"
---
# <a name="icorprofilerinfosetenterleavefunctionhooks-method"></a>ICorProfilerInfo::SetEnterLeaveFunctionHooks, méthode
Spécifie les fonctions implémentées par le profileur à être appelée sur « entrée », « quitter » et « tailcall » de fonctions managées.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT SetEnterLeaveFunctionHooks(  
    [in] FunctionEnter    *pFuncEnter,  
    [in] FunctionLeave    *pFuncLeave,  
    [in] FunctionTailcall *pFuncTailcall);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pFuncEnter`  
 [in] Un pointeur vers l’implémentation à utiliser comme la [FunctionEnter](../../../../docs/framework/unmanaged-api/profiling/functionenter-function.md) rappel.  
  
 `pFuncLeave`  
 [in] Un pointeur vers l’implémentation à utiliser comme la [FunctionLeave](../../../../docs/framework/unmanaged-api/profiling/functionleave-function.md) rappel.  
  
 `pFuncTailcall`  
 [in] Un pointeur vers l’implémentation à utiliser comme la [FunctionTailcall](../../../../docs/framework/unmanaged-api/profiling/functiontailcall-function.md) rappel.  
  
## <a name="remarks"></a>Notes  
 Dans le .NET Framework version 1.0, chaque pointeur fonction peut être null pour désactiver ce rappel correspondant.  
  
 Qu’un seul jeu de rappels peut être actif à la fois. Par conséquent, si un profileur appelle `SetEnterLeaveFunctionHooks` et [ICorProfilerInfo2::SetEnterLeaveFunctionHooks2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-setenterleavefunctionhooks2-method.md), puis `SetEnterLeaveFunctionHooks2` est prioritaire.  
  
 Le `SetEnterLeaveFunctionHooks` méthode peut être appelée uniquement à partir du profileur [ICorProfilerCallback::Initialize](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-initialize-method.md) rappel.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorProfilerInfo, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
