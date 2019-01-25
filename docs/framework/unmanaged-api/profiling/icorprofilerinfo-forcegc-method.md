---
title: ICorProfilerInfo::ForceGC, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.ForceGC
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::ForceGC
helpviewer_keywords:
- ICorProfilerInfo::ForceGC method [.NET Framework profiling]
- ForceGC method [.NET Framework profiling]
ms.assetid: 0da1ef80-d242-4636-87d0-43e0470b342a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c30a666dcbac553d05cc5f54d5dbb326eb6a10e5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54706694"
---
# <a name="icorprofilerinfoforcegc-method"></a>ICorProfilerInfo::ForceGC, méthode
Force le garbage collection se produisent dans le common language runtime (CLR).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT ForceGC();  
```  
  
## <a name="remarks"></a>Notes  
 Le `ForceGC` méthode doit être appelée uniquement à partir d’un thread qui n’a jamais exécuté du code managé et n’a pas de rappels de profileur sur sa pile. L’implémentation la plus commode consiste à créer un thread séparé dans le profileur appelle `ForceGC` quand il est signalé.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICorProfilerInfo, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
