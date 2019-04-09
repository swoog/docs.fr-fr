---
title: ICorProfilerInfo2::GetStaticFieldInfo, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.GetStaticFieldInfo
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::GetStaticFieldInfo
helpviewer_keywords:
- ICorProfilerInfo2::GetStaticFieldInfo method [.NET Framework profiling]
- GetStaticFieldInfo method [.NET Framework profiling]
ms.assetid: fc663e76-e23f-49a8-bdd5-52cdf1a3b2b3
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c0106b2dd1151e302c0082b306d999ab5a1c4322
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59177747"
---
# <a name="icorprofilerinfo2getstaticfieldinfo-method"></a>ICorProfilerInfo2::GetStaticFieldInfo, méthode
Obtient une valeur qui indique le type de champ statique qui s’applique au champ spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetStaticFieldInfo (  
    [in] ClassID               classId,  
    [in] mdFieldDef            fieldToken,  
    [out] COR_PRF_STATIC_TYPE  *pFieldInfo);  
```  
  
## <a name="parameters"></a>Paramètres  
 `classId`  
 [in] L’ID de la classe dans laquelle le champ statique est défini.  
  
 `fieldToken`  
 [in] Le jeton de métadonnées pour le champ statique.  
  
 `pFieldInfo`  
 [out] Un pointeur vers une valeur de la [COR_PRF_STATIC_TYPE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-static-type-enumeration.md) énumération qui indique si le champ spécifié est statique, et si, par conséquent, le type de champ statique qui s’applique au champ.  
  
## <a name="remarks"></a>Notes  
 Ces informations peuvent être utilisées pour déterminer la fonction à appeler pour obtenir l’adresse du champ statique.  
  
 Le code du profileur doit toujours vérifier les métadonnées pour un champ statique pour vous assurer qu’il a réellement une adresse. Littéraux statiques (autrement dit, les constantes) existent uniquement dans les métadonnées et n’ont pas d’adresse.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorProfilerInfo, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
- [ICorProfilerInfo2, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-interface.md)
