---
title: ICorProfilerModuleEnum::Next, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerModuleEnum.Next Method
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerModuleEnum::Next
helpviewer_keywords:
- ICorProfilerModuleEnum::Next method [.NET Framework profiling]
- Next method, ICorProfilerModuleEnum interface [.NET Framework profiling]
ms.assetid: a3cea59d-7622-4323-897a-0a464c40f77f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 974879b854f7a4c18aa4625ea88abb4953123f3e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33456146"
---
# <a name="icorprofilermoduleenumnext-method"></a>ICorProfilerModuleEnum::Next, méthode
Obtient le nombre spécifié de modules contigus dans une collection séquentielle de modules, à commencer par la position actuelle de l’énumérateur dans la séquence.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT Next([in]  ULONG      celt,  
             [out, size_is(celt), length_is(*pceltFetched)]  
                    ModuleID ids[],  
             [out] ULONG *   pceltFetched);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `celt`  
 [in] Nombre de modules à récupérer.  
  
 `ids`  
 [out] Tableau de valeurs `ModuleID` qui représentent chacune un module récupéré.  
  
 `pceltFetched`  
 [out] Pointeur vers le nombre d'éléments réellement retournés dans le tableau `ids`.  
  
## <a name="return-value"></a>Valeur de retour  
 Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.  
  
|HRESULT|Description|  
|-------------|-----------------|  
|S_OK|`celt` éléments ont été retournés.|  
|S_FALSE|Moins de `celt` éléments ont été retournés, ce qui indique que l'énumération est terminée.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [ICorProfilerModuleEnum, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilermoduleenum-interface.md)  
 [Interfaces de profilage](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
