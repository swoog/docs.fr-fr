---
title: ICorProfilerCallback2::GarbageCollectionStarted, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback2.GarbageCollectionStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback2::GarbageCollectionStarted
helpviewer_keywords:
- GarbageCollectionStarted method [.NET Framework profiling]
- ICorProfilerCallback2::GarbageCollectionStarted method [.NET Framework profiling]
ms.assetid: 44eef087-f21f-4fe2-b481-f8a0ee022e7d
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9a447dca98e5010163d5cc5f4f3da4333f4cdf7d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="icorprofilercallback2garbagecollectionstarted-method"></a>ICorProfilerCallback2::GarbageCollectionStarted, méthode
Notifie le profileur de code que le garbage collection a démarré.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GarbageCollectionStarted(  
    [in] int cGenerations,  
    [in, size_is(cGenerations), length_is(cGenerations)] BOOL generationCollected[],  
    [in] COR_PRF_GC_REASON reason);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `cGenerations`  
 [in] Le nombre total d’entrées dans le `generationCollected` tableau.  
  
 `generationCollected`  
 [in] Un tableau de valeurs booléennes, qui sont `true` si la génération qui correspond à l’index de tableau sont collectées par ce garbage collection ; sinon, `false`.  
  
 Le tableau est indexé par une valeur de la [COR_PRF_GC_GENERATION](../../../../docs/framework/unmanaged-api/profiling/cor-prf-gc-generation-enumeration.md) énumération qui indique la génération.  
  
 `reason`  
 [in] Une valeur de la [COR_PRF_GC_REASON](../../../../docs/framework/unmanaged-api/profiling/cor-prf-gc-reason-enumeration.md) énumération qui indique la raison pour laquelle le garbage collection a été INDUITE.  
  
## <a name="remarks"></a>Notes  
 Tous les rappels relatifs à ce garbage collection seront produit entre le `GarbageCollectionStarted` rappel et correspondants [ICorProfilerCallback2::GarbageCollectionFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-garbagecollectionfinished-method.md) rappel. Ces rappels ne doivent pas avoir lieu sur le même thread.  
  
 Il est possible pour le profileur d’inspecter des objets dans leurs emplacements d’origine pendant la `GarbageCollectionStarted` rappel. Le garbage collector commencera à déplacer les objets après le retour de `GarbageCollectionStarted`. Une fois que le profileur a retourné à partir de ce rappel, le profileur doit considérer tous les ID d’objet est non valide jusqu'à ce qu’il reçoive une `ICorProfilerCallback2::GarbageCollectionFinished` rappel.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [ICorProfilerCallback, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [ICorProfilerCallback2, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback2-interface.md)
