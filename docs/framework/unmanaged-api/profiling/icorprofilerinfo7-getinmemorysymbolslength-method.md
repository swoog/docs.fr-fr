---
title: ICorProfilerInfo7::GetInMemorySymbolsLength (méthode)
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo7.GetInMemorySymbolsLength
api_location:
- mscorwks.dll
- icorprof.idl
api_type:
- COM
ms.assetid: d62c4a4c-8a62-45aa-8f01-a8387cf36159
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 550acc8d696cbd9e82d05e09c48a8c929af23673
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57487473"
---
# <a name="icorprofilerinfo7getinmemorysymbolslength-method"></a>ICorProfilerInfo7::GetInMemorySymbolsLength (méthode)
[Prise en charge dans le .NET Framework 4.6.1 et versions ultérieures]  
  
 Retourne la longueur d’un flux de symbole d’en mémoire.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetInMemorySymbolsLength(  
        [in] ModuleID moduleId,  
        [out] DWORD* pCountSymbolBytes  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `moduleId`  
 [in] L’identificateur du module qui contient le flux en mémoire.  
  
 pCountSymbolBytes  
 [out] Un pointeur vers un `DWORD` valeur qui, lorsque la méthode est retournée, contient la longueur du flux en octets.  
  
## <a name="return-value"></a>Valeur de retour  
 La méthode retourne `S_OK` si la longueur du flux de mémoire peut être déterminée, même si elle est zéro (0).  
  
 La méthode retourne `CORPROF_E_MODULE_IS_DYNAMIC` si la méthode a été créée à l’aide de <xref:System.Reflection.Emit?displayProperty=nameWithType>.  
  
## <a name="remarks"></a>Notes  
 Si le module a de symboles en mémoire, la longueur du flux de données est placée dans `pCountSymbolBytes`. Si le module n’a pas les symboles en mémoire, `*pCountSymbolBytes = 0`.  
  
> [!NOTE]
>  L’implémentation actuelle ne prend pas en charge de Reflection.Emit. Si le module a été créé à l’aide de Reflection.Emit, la méthode retourne `CORPROF_E_MODULE_IS_DYNAMIC`.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICorProfilerInfo7, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-interface.md)
