---
title: ICorProfilerCallback8::DynamicMethodJITCompilationStarted (méthode)
ms.date: 04/10/2018
api_name:
- ICorProfilerCallback8.DynamicMethodJITCompilationStarted
api_location:
- mscorwks.dll
- corprof.idl
api_type:
- COM
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c4b8bffeb71497a7dd8e2ed25b833f9216d8017e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59142244"
---
# <a name="icorprofilercallback8dynamicmethodjitcompilationstarted-method"></a>ICorProfilerCallback8::DynamicMethodJITCompilationStarted (méthode)
[Pris en charge dans le .NET Framework 4.7 et versions ultérieures]  
  
Notifie le profileur chaque fois que la compilation JIT d’une méthode dynamique a démarré.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT DynamicMethodJITCompilationStarted(  
     [in]  FunctionID  functionId,   
     [in]  BOOL        fIsSafeToBlock,   
     [in]  LPCBYTE     pILHeader,   
     [in]  LONG        cbILHeader   
);  
```  
  
## <a name="parameters"></a>Paramètres  
[in] `functionId`  
L’identificateur de la fonction en mémoire pour le JIT démarrage de la compilation.   

[in] `fIsSafeToBlock`   
`true` pour indiquer que le blocage peut entraîner l’exécution pour attendre que le thread appelant retourner à partir de ce rappel ; `false` pour indiquer que le blocage n’affecte pas l’opération du runtime.  

[in] `pILHeader`    
Pointeur vers le premier octet d’en-tête de langage intermédiaire de la méthode.   

[in] `cbILHeader`    
Le nombre d’octets dans l’en-tête de langage intermédiaire. 

## <a name="remarks"></a>Notes  

Ce rappel est déclenché chaque fois qu’une méthode dynamique est compilé par JIT. Cela inclut diverses de stubs de langage intermédiaire et de méthodes LCG. Son objectif est de fournir les enregistreurs de profileur avec suffisamment d’informations pour identifier la méthode compilée pour les utilisateurs.

> [!NOTE]
> `functionId` les valeurs ne peut pas être permet de résoudre à leurs jetons de métadonnées, car les méthodes dynamiques ont pas de métadonnées.

Le `pILHeader` pointeur est uniquement valid pendant le rappel.

## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  
  
## <a name="see-also"></a>Voir aussi

- [DynamicMethodJITCompilationFinished, méthode](icorprofilercallback8-dynamicmethodjitcompilationfinished-method.md)
- [ICorProfilerCallback8, interface](icorprofilercallback8-interface.md)
