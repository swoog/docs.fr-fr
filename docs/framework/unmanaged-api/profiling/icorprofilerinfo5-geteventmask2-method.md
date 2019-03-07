---
title: ICorProfilerInfo5::GetEventMask2, méthode
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICorProfilerInfo5.GetEventMask2
api_location:
- mscorwks.dll
api_type:
- COM
ms.assetid: f854b68f-009c-4ffb-89cd-ca874d1c0fb7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c68668c1d591a8fb53d04d632027b0d8effb0c42
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57474799"
---
# <a name="icorprofilerinfo5geteventmask2-method"></a>ICorProfilerInfo5::GetEventMask2, méthode
[Pris en charge dans .NET Framework 4.5.2 et ultérieur]  
  
 Obtient les catégories des événements actifs pour lesquelles le profileur veut recevoir des notifications du CLR.  Il fournit des fonctionnalités non fournies par le [ICorProfilerInfo::GetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-geteventmask-method.md) (méthode).  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp
HRESULT GetEventMask2(  
        [out] DWORD* pdwEventsLow,  
        [out] DWORD* pdwEventsHigh  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pdwEventsLow`  
 [en sortie] Un pointeur vers une valeur de 4 octets qui spécifie les catégories des événements. Chaque bit contrôle une fonctionnalité, un comportement ou un type d'événement différents. Les bits sont décrits dans le [COR_PRF_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-monitor-enumeration.md) énumération.  
  
 `pdwEventsHigh`  
 [en sortie] Un pointeur vers une valeur de 4 octets qui spécifie les catégories des événements.  Chaque bit contrôle une fonctionnalité, un comportement ou un type d'événement différents. Les bits sont décrits dans le [COR_PRF_HIGH_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-high-monitor-enumeration.md) énumération.  
  
## <a name="remarks"></a>Notes  
 La méthode `GetEventMask2` est utilisée pour déterminer les rappels auxquels le profileur s'est abonné. En général, vous effectuez une opération OR logique de la `pdwEventsLow` et `pdwEventsHigh` valeurs et des nouveaux bits que vous souhaitez définir, puis appelez le [SetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md) (méthode).  
  
 Cette méthode est l’alternative recommandée à la [GetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-geteventmask-method.md) (méthode).  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorProf.idl, CorProf.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICorProfilerInfo5, interface](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-interface.md)
- [SetEventMask2, méthode](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md)
