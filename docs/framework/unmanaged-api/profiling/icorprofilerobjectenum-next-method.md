---
title: ICorProfilerObjectEnum::Next, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerObjectEnum.Next
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerObjectEnum::Next
helpviewer_keywords:
- Next method, ICorProfilerObjectEnum interface [.NET Framework profiling]
- ICorProfilerObjectEnum::Next method [.NET Framework profiling]
ms.assetid: b420433c-5ebe-4986-bba1-97902e6db819
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4db788755febab9b21adb26caf74c8ea154c1493
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54653812"
---
# <a name="icorprofilerobjectenumnext-method"></a>ICorProfilerObjectEnum::Next, méthode
Obtient le nombre spécifié d’objets contigus dans une collection séquentielle d’objets, en commençant à la position actuelle de l’énumérateur dans la séquence.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT Next (  
    [in] ULONG                    celt,  
    [out, size_is(celt), length_is(*pceltFetched)]    
        ObjectID                  objects[],  
    [out] ULONG                   *pceltFetched  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `celt`  
 [in] Nombre d'objets à récupérer.  
  
 `objects`  
 [out] Un tableau de `ObjectID` valeurs, chacune représentant un objet récupéré.  
  
 `pceltFetched`  
 [out] Pointeur vers le nombre d'éléments réellement retournés dans le tableau `objects`.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICorProfilerObjectEnum, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerobjectenum-interface.md)
