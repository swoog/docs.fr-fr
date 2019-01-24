---
title: ICorProfilerFunctionControl, interface
ms.date: 03/30/2017
api_name:
- ICorProfilerFunctionControl
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerFunctionControl
helpviewer_keywords:
- ICorProfilerFunctionControl interface [.NET Framework profiling]
ms.assetid: 4e3d3141-4662-4166-8f05-bc857c1b4216
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 37e0c9dcbd8975338e7c64dbd9c44dd54508b4d6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54649711"
---
# <a name="icorprofilerfunctioncontrol-interface"></a>ICorProfilerFunctionControl, interface
Fournit des méthodes qui permettent à un profileur de code de communiquer avec le CLR (Common Language Runtime) pour contrôler comment le compilateur juste-à-temps doit générer du code lors de la recompilation d'une méthode spécifique.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[SetCodegenFlags, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-setcodegenflags-method.md)|Définit un ou plusieurs indicateurs à partir de la [COR_PRF_CODEGEN_FLAGS](../../../../docs/framework/unmanaged-api/profiling/cor-prf-codegen-flags-enumeration.md) fonction recompilée de l’énumération à la génération de code de contrôle pour un juste-à-temps (JIT).|  
|[SetILFunctionBody, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-setilfunctionbody-method.md)|Remplace le corps Common Intermediate Language (CIL) de la méthode.|  
|[SetILInstrumentedCodeMap, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-setilinstrumentedcodemap-method.md)|Définit une carte de code pour la fonction spécifiée à l’aide des entrées de mappage CIL (Common Intermediate Language) spécifiées.|  
  
## <a name="remarks"></a>Notes  
 L'interface `ICorProfilerFunctionControl` fournit des méthodes pour le contrôle de la génération de code pour une seule fonction recompilée. Le profileur obtient une instance de cette interface via la [ICorProfilerCallback4::GetReJITParameters](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-getrejitparameters-method.md) rappel. Chaque instance de `ICorProfilerFunctionControl` contrôle toutes les instances d'une seule fonction.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICorProfilerInfo4, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-interface.md)
- [Interfaces de profilage](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [EnumJITedFunctions2, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-enumjitedfunctions2-method.md)
