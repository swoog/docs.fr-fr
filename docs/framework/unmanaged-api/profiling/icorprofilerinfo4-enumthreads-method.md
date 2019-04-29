---
title: ICorProfilerInfo4::EnumThreads, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo4.EnumThreads
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo4::EnumThreads
helpviewer_keywords:
- ICorProfilerInfo4::EnumThreads method [.NET Framework profiling]
- EnumThreads method, ICorProfilerInfo4 interface [.NET Framework profiling]
ms.assetid: bca7a5b4-c207-4894-918c-0733926296dd
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: bd0a4149b6dc6023579e8bc5b40751d23416e3a6
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61683862"
---
# <a name="icorprofilerinfo4enumthreads-method"></a>ICorProfilerInfo4::EnumThreads, méthode
Retourne un énumérateur qui fournit des méthodes pour boucler séquentiellement dans la collection de tous les threads managés dans le processus profilé.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT EnumThreads([out]  
            ICorProfilerThreadEnum** ppEnum);  
```  
  
## <a name="parameters"></a>Paramètres  
 `ppEnum`  
 [out] Un pointeur vers un [ICorProfilerThreadEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilerthreadenum-interface.md) interface.  
  
## <a name="remarks"></a>Notes  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorProfilerThreadEnum, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerthreadenum-interface.md)
- [ICorProfilerInfo4, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-interface.md)
- [Interfaces de profilage](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [Profilage](../../../../docs/framework/unmanaged-api/profiling/index.md)
