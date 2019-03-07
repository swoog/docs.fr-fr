---
title: ICorProfilerInfo2::GetRVAStaticAddress, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.GetRVAStaticAddress
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::GetRVAStaticAddress
helpviewer_keywords:
- GetRVAStaticAddress method [.NET Framework profiling]
- ICorProfilerInfo2::GetRVAStaticAddress method [.NET Framework profiling]
ms.assetid: a25a8f8b-5cfa-440d-9376-a1a1c3a9fc11
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 8d0d0982ab7249e88c48c7734c09043031a8d0d3
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57482416"
---
# <a name="icorprofilerinfo2getrvastaticaddress-method"></a>ICorProfilerInfo2::GetRVAStaticAddress, méthode
Obtient l’adresse du champ statique d’adresse virtuelle relative (RVA) spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetRVAStaticAddress(  
    [in] ClassID classId,  
    [in] mdFieldDef fieldToken,  
    [out] void **ppAddress);  
```  
  
## <a name="parameters"></a>Paramètres  
 `classId`  
 [in] ID de la classe qui contient le champ statique RVA demandé.  
  
 `fieldToken`  
 [in] Jeton de métadonnées pour le champ statique RVA demandé.  
  
 `ppAddress`  
 [out] Pointeur vers l’adresse du champ statique RVA.  
  
## <a name="remarks"></a>Notes  
 Le `GetRVAStaticAddress` méthode peut retourner l’une des opérations suivantes :  
  
-   Un HRESULT CORPROF_E_DATAINCOMPLETE si le champ statique donné n’a pas été assigné une adresse dans le contexte spécifié.  
  
-   Les adresses des objets qui peuvent être dans le tas de garbage collection. Ces adresses peuvent devenir non valides après le garbage collection, donc après le garbage collection, les profileurs ne doivent pas supposer qu’ils sont valides.  
  
 Avant la fin de constructeur de classe d’une classe, `GetRVAStaticAddress` retournera CORPROF_E_DATAINCOMPLETE pour tous ses champs statiques, bien que certains des champs statiques peuvent déjà être initialisés et utiliser des objets de garbage collection à la racine.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICorProfilerInfo, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
- [ICorProfilerInfo2, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-interface.md)
