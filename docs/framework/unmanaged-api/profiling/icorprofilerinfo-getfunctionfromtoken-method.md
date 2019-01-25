---
title: ICorProfilerInfo::GetFunctionFromToken, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetFunctionFromToken
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetFunctionFromToken
helpviewer_keywords:
- ICorProfilerInfo::GetFunctionFromToken method [.NET Framework profiling]
- GetFunctionFromToken method, ICorProfilerInfo interface [.NET Framework profiling]
ms.assetid: 0eed759f-cce8-405d-88dc-9ee293a38928
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 12f76059387f00316888cbe6d839bece33e3eef9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54520264"
---
# <a name="icorprofilerinfogetfunctionfromtoken-method"></a>ICorProfilerInfo::GetFunctionFromToken, méthode
Obtient l’ID d’une fonction. Cette méthode est obsolète dans le .NET Framework version 2.0. Utilisez le [ICorProfilerInfo2::GetFunctionFromTokenAndTypeArgs](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getfunctionfromtokenandtypeargs-method.md) méthode à la place.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetFunctionFromToken(  
    [in]  ModuleID   moduleId,  
    [in]  mdToken    token,  
    [out] FunctionID *pFunctionId);  
```  
  
## <a name="remarks"></a>Notes  
 Le `GetFunctionFromToken` méthode ne fonctionne pas pour les fonctions génériques ou des fonctions dans des types génériques ; il est désormais obsolète. Utilisez `ICorProfilerInfo2::GetFunctionFromTokenAndTypeArgs` pour toutes les fonctions.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** 1.1, 1.0  
  
## <a name="see-also"></a>Voir aussi
- [ICorProfilerInfo, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
