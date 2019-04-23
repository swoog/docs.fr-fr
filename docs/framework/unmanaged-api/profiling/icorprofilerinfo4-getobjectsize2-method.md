---
title: ICorProfilerInfo4::GetObjectSize2, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo4.GetObjectSize2
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo4::GetObjectSize2
helpviewer_keywords:
- GetObjectSize2 method, ICorProfilerInfo4 interface [.NET Framework profiling]
- ICorProfilerInfo4::GetObjectSize2 method [.NET Framework profiling]
ms.assetid: 4a3e43ed-3ee3-4395-ab14-f78b903be13e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 15829e08a755b91ff91ca939b92a5a87bd377e8b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59176291"
---
# <a name="icorprofilerinfo4getobjectsize2-method"></a>ICorProfilerInfo4::GetObjectSize2, méthode
Retourne la taille d’un objet spécifié. Remplace le [ICorProfilerInfo::GetObjectSize](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-getobjectsize-method.md) méthode en signalant les tailles des objets supérieurs à ce qui peut être exprimé dans un `ULONG`.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetObjectSize2(  
    [in]  ObjectID objectId,  
    [out] SIZE_T *pcSize);  
```  
  
## <a name="parameters"></a>Paramètres  
 `objectId`  
 [in] L’ID de l’objet.  
  
 `pcSize`  
 [out] Pointeur vers la taille de l’objet, en octets.  
  
## <a name="remarks"></a>Notes  
 Différents objets des mêmes types ont souvent la même taille. Toutefois, certains types, tels que des tableaux ou des chaînes, peuvent avoir une taille différente pour chaque objet.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorProfilerInfo4, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-interface.md)
