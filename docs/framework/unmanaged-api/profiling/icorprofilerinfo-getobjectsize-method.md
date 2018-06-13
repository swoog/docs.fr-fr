---
title: ICorProfilerInfo::GetObjectSize, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetObjectSize
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetObjectSize
helpviewer_keywords:
- GetObjectSize method [.NET Framework profiling]
- ICorProfilerInfo::GetObjectSize method [.NET Framework profiling]
ms.assetid: 9f02e763-73f7-42cb-a41c-f78499d9482c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7ed27602dfa9090b46b842e4e65af8af373cc207
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33453907"
---
# <a name="icorprofilerinfogetobjectsize-method"></a>ICorProfilerInfo::GetObjectSize, méthode
Obtient la taille d’un objet spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetObjectSize(  
    [in]  ObjectID objectId,  
    [out] ULONG  *pcSize);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `objectId`  
 [in] L’ID de l’objet.  
  
 `pcSize`  
 [out] Pointeur vers la taille de l’objet, en octets.  
  
## <a name="remarks"></a>Notes  
  
> [!IMPORTANT]
>  Cette méthode est obsolète. Il renvoie COR_E_OVERFLOW pour les objets supérieurs à 4 Go sur les plateformes 64 bits. Utilisez le [ICorProfilerInfo4::GetObjectSize2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-getobjectsize2-method.md) méthode à la place.  
  
 Différents objets des mêmes types ont souvent la même taille. Toutefois, certains types, tels que des tableaux ou des chaînes, peuvent avoir une taille différente pour chaque objet.  
  
 La taille retournée par la `GetObjectSize` méthode n’inclut pas de tout remplissage d’alignement susceptibles d’apparaître une fois l’objet sur le tas de garbage collection. Si vous utilisez la `GetObjectSize` méthode pour passer d’un objet à l’objet sur le tas de garbage collection, ajouter alignement remplissage manuellement, si nécessaire.  
  
-   Sur Windows 32 bits, COR_PRF_GC_GEN_0, COR_PRF_GC_GEN_1 et COR_PRF_GC_GEN_2 utilisent alignement de 4 octets et COR_PRF_GC_LARGE_OBJECT_HEAP utilise l’alignement de 8 octets.  
  
-   Sur Windows 64 bits, l’alignement est toujours de 8 octets.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [ICorProfilerInfo, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
