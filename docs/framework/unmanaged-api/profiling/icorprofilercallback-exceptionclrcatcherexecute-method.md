---
title: ICorProfilerCallback::ExceptionCLRCatcherExecute, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionCLRCatcherExecute
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionCLRCatcherExecute
helpviewer_keywords:
- ExceptionCLRCatcherExecute method [.NET Framework profiling]
- ICorProfilerCallback::ExceptionCLRCatcherExecute method [.NET Framework profiling]
ms.assetid: aaac8f98-5cf4-42c7-b04b-556cce367e36
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b640a6dee9ae50278d6a844d20d21eae156e9dd7
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59200959"
---
# <a name="icorprofilercallbackexceptionclrcatcherexecute-method"></a>ICorProfilerCallback::ExceptionCLRCatcherExecute, méthode
Appelé lorsqu’un `catch` block pour une exception est exécutée dans le common language runtime (CLR) lui-même. Cette méthode est obsolète dans le .NET Framework version 2.0.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT ExceptionCLRCatcherExecute();  
```  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** 1.1, 1.0  
  
## <a name="see-also"></a>Voir aussi

- [ICorProfilerCallback, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [ExceptionCLRCatcherFound, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionclrcatcherfound-method.md)
