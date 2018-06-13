---
title: ICorProfilerInfo::BeginInprocDebugging, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.BeginInprocDebugging
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::BeginInprocDebugging
helpviewer_keywords:
- BeginInprocDebugging method [.NET Framework profiling]
- ICorProfilerInfo::BeginInprocDebugging method [.NET Framework profiling]
ms.assetid: c5c82c69-99f8-4447-aee0-42cca0a5eb5c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 82e798e1a31f771c63e71f2a85f8cbb684b237bd
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33462388"
---
# <a name="icorprofilerinfobegininprocdebugging-method"></a>ICorProfilerInfo::BeginInprocDebugging, méthode
Initialise intra-processus prise en charge de débogage. Cette méthode est obsolète dans le .NET Framework version 2.0.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT BeginInprocDebugging(  
    [in]  BOOL   fThisThreadOnly,  
    [out] DWORD *pdwProfilerContext);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `fThisThreadOnly`  
 [in] Définissez cette valeur sur `true` pour initialiser la prise en charge du débogage pour le thread actuel uniquement ; lui affectez la valeur `false` pour initialiser la prise en charge du débogage pour tous les threads.  
  
 `pdwProfilerContext`  
 [out] Pointeur vers une valeur retournée qui identifie la session de débogage.  
  
## <a name="remarks"></a>Notes  
 Les services de débogage CLR pris en charge limitée dans le processus de débogage dans les versions du .NET Framework 1.0 et 1.1. Dans le processus de débogage activé un profileur d’utiliser les parties de l’inspection de l’API de débogage. Toutefois, en raison des commentaires des clients, dans le processus de débogage ont été supprimé du .NET Framework version 2.0 et remplacé par un ensemble de fonctionnalités qui sont plus adaptées à l’API de profilage.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Version du .NET framework :** 1.0  
  
## <a name="see-also"></a>Voir aussi  
 [ICorProfilerInfo, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
