---
title: ICorProfilerCallback3::InitializeForAttach, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback3.InitializeForAttach Method
api_location:
- Mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback3::InitializeForAttach
helpviewer_keywords:
- InitializeForAttach method [.NET Framework profiling]
- ICorProfilerCallback3::InitializeForAttach method [.NET Framework profiling]
ms.assetid: bed097b3-6d52-46c9-bee7-ac7910b6fc3f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a8590a40ca74296bab618d6c0ba95f1683cf33cd
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57466256"
---
# <a name="icorprofilercallback3initializeforattach-method"></a>ICorProfilerCallback3::InitializeForAttach, méthode
Appelée par le Common Language Runtime (CLR) pour permettre au profileur d’initialiser son état après une opération d’attachement.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT InitializeForAttach(  
            [in] IUnknown * pCorProfilerInfoUnk,  
            [in] void * pvClientData,  
            [in] UINT cbClientData);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pCorProfilerInfoUnk`  
 [in] Pointeur d'interface pour l'interface `ICorProfilerInfo*`.  
  
 `pvClientData`  
 [in] Un pointeur vers les données passées à la [IClrProfiling::AttachProfiler](../../../../docs/framework/unmanaged-api/profiling/iclrprofiling-attachprofiler-method.md) méthode dans son `pvClientData` paramètre. Si ce paramètre est null, `cbClientData` est égal à 0 (zéro). Le CLR libère cette mémoire au retour de `InitializeForAttach`.  
  
 `cbClientData`  
 [in] Taille, en octets, des données vers lesquelles `pvClientData` pointe.  
  
## <a name="remarks"></a>Notes  
 Le CLR appelle `InitializeForAttach` pour permettre au profileur de demander des rappels.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICorProfilerCallback, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
- [ICorProfilerInfo3, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-interface.md)
- [Interfaces de profilage](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [Profilage](../../../../docs/framework/unmanaged-api/profiling/index.md)
