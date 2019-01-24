---
title: ICorProfilerCallback::ModuleLoadStarted, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ModuleLoadStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ModuleLoadStarted
helpviewer_keywords:
- ModuleLoadStarted method [.NET Framework profiling]
- ICorProfilerCallback::ModuleLoadStarted method [.NET Framework profiling]
ms.assetid: 9cd2fe75-408a-400f-a6b1-9979624a2fe2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: aa5ca8871ab284d2a46e6777b226f5a9b155e566
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54502467"
---
# <a name="icorprofilercallbackmoduleloadstarted-method"></a>ICorProfilerCallback::ModuleLoadStarted, méthode
Informe le profileur qu’un module est chargé.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT ModuleLoadStarted(  
    [in] ModuleID moduleId);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `moduleId`  
 [in] L’ID du module qui est en cours de chargement.  
  
## <a name="remarks"></a>Notes  
 La valeur de `moduleId` n’est pas valide pour une demande d’informations jusqu'à ce que le [ICorProfilerCallback::ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md) méthode est appelée.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICorProfilerCallback, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
