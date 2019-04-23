---
title: ICorProfilerCallback::ModuleAttachedToAssembly, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ModuleAttachedToAssembly
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ModuleAttachedToAssembly
helpviewer_keywords:
- ICorProfilerCallback::ModuleAttachedToAssembly method [.NET Framework profiling]
- ModuleAttachedToAssembly method [.NET Framework profiling]
ms.assetid: b595798a-5d40-4cac-ab4f-911c61d2c5d2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 791827b9c4b60cb2ee963881bc8e1a6131cd00fb
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59139917"
---
# <a name="icorprofilercallbackmoduleattachedtoassembly-method"></a>ICorProfilerCallback::ModuleAttachedToAssembly, méthode
Notifie le profileur qu’un module est attaché à son assembly parent.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT ModuleAttachedToAssembly(  
    [in] ModuleID   moduleId,  
    [in] AssemblyID AssemblyId);  
```  
  
## <a name="parameters"></a>Paramètres  
 `moduleId`  
 [in] L’ID du module qui est attaché.  
  
 `AssemblyId`  
 [in] L’ID de l’assembly parent auquel le module est attaché.  
  
## <a name="remarks"></a>Notes  
 Un module peut être chargé via une table d’adresse d’importation (IAT), via un appel à `LoadLibrary`, ou via une référence de métadonnées. Par conséquent, le chargeur du common language runtime (CLR) a plusieurs chemins de code pour déterminer l’assembly dans lequel réside un module. Par conséquent, il est possible qu’après [ICorProfilerCallback::ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md) est appelée, le module ne sait pas quel assembly il se trouve dans et obtenir l’ID d’assembly parent n’est pas possible. Le `ModuleAttachedToAssembly` méthode est appelée lorsque le module est attaché à son assembly parent et son parent ID peut être obtenu.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorProfilerCallback, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
