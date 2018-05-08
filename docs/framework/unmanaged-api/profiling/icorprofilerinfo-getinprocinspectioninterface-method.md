---
title: ICorProfilerInfo::GetInprocInspectionInterface, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetInprocInspectionInterface
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetInprocInspectionInterface
helpviewer_keywords:
- GetInprocInspectionInterface method [.NET Framework profiling]
- ICorProfilerInfo::GetInprocInspectionInterface method [.NET Framework profiling]
ms.assetid: 22a92d1d-8849-4af6-8304-ecc53dd1d289
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 761dd55d2ae48739f24a03b8ce81c571fb211a5a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="icorprofilerinfogetinprocinspectioninterface-method"></a>ICorProfilerInfo::GetInprocInspectionInterface, méthode
Obtient un objet qui peut être interrogé pour une interface « ICorDebugProcess ». Cette méthode est obsolète dans le .NET Framework version 2.0.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetInprocInspectionInterface(  
    [out] IUnknown **ppicd);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `ppicd`  
 [out](/cpp/atl/iunknown) objet qui peut être interrogé pour une `ICorDebugProcess` interface.  
  
## <a name="remarks"></a>Notes  
 L’API de débogage du common language runtime (CLR) prise en charge limitée dans le processus de débogage dans le .NET Framework version 1.0. Dans le processus de débogage activé un profileur d’utiliser les parties de l’inspection de l’API de débogage. Suite à des commentaires client, dans le processus de débogage ont été supprimé du .NET Framework version 2.0 et remplacé par un ensemble de fonctionnalités qui sont plus adaptées à l’API de profilage.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Version du .NET framework :** 1.0  
  
## <a name="see-also"></a>Voir aussi  
 [ICorProfilerInfo, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
