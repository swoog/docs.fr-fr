---
title: ICorProfilerInfo::IsArrayClass, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.IsArrayClass
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::IsArrayClass
helpviewer_keywords:
- IsArrayClass method [.NET Framework profiling]
- ICorProfilerInfo::IsArrayClass method [.NET Framework profiling]
ms.assetid: 7f230961-23a6-4d56-ad2d-7a876d65705f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 350221ae205636cef82581f3fe11367006dd8b2b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59072170"
---
# <a name="icorprofilerinfoisarrayclass-method"></a>ICorProfilerInfo::IsArrayClass, méthode
Détermine si la classe spécifiée est une classe array.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT IsArrayClass(  
    [in]  ClassID        classId,  
    [out] CorElementType *pBaseElemType,  
    [out] ClassID        *pBaseClassId,  
    [out] ULONG          *pcRank);  
```  
  
## <a name="parameters"></a>Paramètres  
 `classId`  
 [in] L’ID de la classe doit être examinée.  
  
 `pBaseElemType`  
 [out] Pointeur vers une valeur de l’énumération CorElementType qui indique le type des éléments du tableau.  
  
 `pBaseClassId`  
 [out] Pointeur vers l’ID de classe des éléments du tableau, lorsqu’il est disponible.  
  
 `pcRank`  
 [out] Pointeur vers un entier qui indique le classement (autrement dit, le nombre de dimensions) du tableau.  
  
## <a name="remarks"></a>Notes  
 Si la classe spécifiée est une classe array, la `IsArrayClass` méthode retourne une valeur S_OK HRESULT et des valeurs des paramètres de sortie non null. Sinon, elle retourne S_FALSE.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorProfilerInfo, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
