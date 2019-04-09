---
title: ICorDebugGuidToTypeEnum::Next, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugGuidToTypeEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugGuidToTypeEnum::Next
helpviewer_keywords:
- ICorDebugGuidToTypeEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugGuidToTypeEnum interface [.NET Framework debugging]
ms.assetid: c9937666-8e18-484d-9fe0-b9ac95199530
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f48c142b2b3742d01a8f796f11d5c9174529a041
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59105817"
---
# <a name="icordebugguidtotypeenumnext-method"></a>ICorDebugGuidToTypeEnum::Next, méthode
Obtient le nombre spécifié de [CorDebugGuidToTypeMapping](../../../../docs/framework/unmanaged-api/debugging/cordebugguidtotypemapping-structure.md) instances qui mappent des GUID vers le type d’informations.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT Next(  
    [in] ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched] CorDebugGuidToTypeMapping values[  ],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `celt`  
 [in] Le nombre d’objets de mappage de type-GUID à récupérer.  
  
 `values`  
 [out] Un tableau de pointeurs, chacun d’eux pointe vers un [CorDebugGuidToTypeMapping](../../../../docs/framework/unmanaged-api/debugging/cordebugguidtotypemapping-structure.md) objet qui mappe un [!INCLUDE[wrt](../../../../includes/wrt-md.md)] GUID à son objet ICorDebugType correspondant.  
  
 `pceltFetched`  
 [out] Un pointeur vers le nombre de [CorDebugGuidToTypeMapping](../../../../docs/framework/unmanaged-api/debugging/cordebugguidtotypemapping-structure.md) réellement retournés dans des objets `values`.  
  
## <a name="remarks"></a>Notes  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** [!INCLUDE[wrt](../../../../includes/wrt-md.md)]  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorDebugGuidToTypeEnum, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugguidtotypeenum-interface.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
