---
title: ICorProfilerCallback7::ModuleInMemorySymbolsUpdated (méthode)
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback7.ModuleInMemorySymbolsUpdated
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
ms.assetid: f362a896-3247-4894-9727-e48dbbcd2c78
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9aa690378a32ffee2def672f02dc8b5582647a5e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33455812"
---
# <a name="icorprofilercallback7moduleinmemorysymbolsupdated-method"></a>ICorProfilerCallback7::ModuleInMemorySymbolsUpdated (méthode)
[Prise en charge dans le .NET Framework 4.6.1 et versions ultérieures]  
  
 Notifie le profileur chaque fois que le flux de symbole associé à un module en mémoire est mise à jour.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT ModuleInMemorySymbolsUpdated(  
     ModuleID moduleId  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 [in] `moduleId`  
 Identificateur du module en mémoire dont flux de symbole est mis à jour.  
  
## <a name="remarks"></a>Notes  
 Ce rappel est contrôlé en définissant le [COR_PRF_HIGH_IN_MEMORY_SYMBOLS_UPDATED](../../../../docs/framework/unmanaged-api/profiling/cor-prf-high-monitor-enumeration.md) indicateur de masque d’événement lors de l’appel du [ICorProfilerCallback5::SetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md) (méthode).  
  
> [!NOTE]
>  Cet événement n’est pas déclenché actuellement des symboles implicitement créé ou modifié <xref:System.Reflection.Emit> API.  
  
 Même lorsque les symboles sont prévues au préalable un appel à une des surcharges de la <xref:System.Reflection.Assembly.Load*?displayProperty=nameWithType> méthodes qui inclut un `rawSymbolStore` argument afin de spécifier les symboles pour l’assembly, le runtime peut associer pas réellement les données symboliques avec le module jusqu'à ce qu’une fois la [ModuleLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md) rappel s’est produite. Cet événement fournit une opportunité ultérieure pour collecter des symboles pour ces modules.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [ModuleLoadFinished, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-moduleloadfinished-method.md)  
 [SetEventMask2, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md)  
 [ICorProfilerCallback7, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback7-interface.md)
