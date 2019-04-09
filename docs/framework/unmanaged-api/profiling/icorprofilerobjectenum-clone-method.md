---
title: ICorProfilerObjectEnum::Clone, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerObjectEnum.Clone
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerObjectEnum::Clone
helpviewer_keywords:
- Clone method, ICorProfilerObjectEnum interface [.NET Framework profiling]
- ICorProfilerObjectEnum::Clone method [.NET Framework profiling]
ms.assetid: b0b2facd-5991-4f4c-932d-c4937f45cef9
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 14e8086532eff5dba6883575cc2daf447a32343a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59182362"
---
# <a name="icorprofilerobjectenumclone-method"></a>ICorProfilerObjectEnum::Clone, méthode
Obtient un pointeur d’interface vers une copie de ce [ICorProfilerObjectEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilerobjectenum-interface.md) interface.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT Clone (  
    [out] ICorProfilerObjectEnum   **ppEnum);  
```  
  
## <a name="parameters"></a>Paramètres  
 `ppEnum`  
 [out] Un pointeur vers le pointeur d’interface qui pointe à son tour vers la copie de ce `ICorProfilerObjectEnum` interface. La copie conserve son propre état d’énumération séparément à partir de celui-ci. Toutefois, position du curseur initiale de la copie sera identique à la position actuelle du curseur de cet énumérateur.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorProfilerObjectEnum, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerobjectenum-interface.md)
