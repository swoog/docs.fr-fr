---
title: ICorDebugVariableHomeEnum::Next (méthode)
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHomeEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHomeEnum::Next
helpviewer_keywords:
- ICorDebugVariableHomeEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugVariableHomeEnum interface [.NET Framework debugging]
ms.assetid: eb9ea96c-5b58-4655-8104-094fc8b393b8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d5ab18d6c2ae8bbf47a3bcd7cb892530be4f8f4e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="icordebugvariablehomeenumnext-method"></a>ICorDebugVariableHomeEnum::Next (méthode)
Obtient le nombre spécifié de [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) instances qui contiennent des informations sur les variables locales et les arguments dans une fonction.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT Next(  
    [in] ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched)] ICorDebugVariableHome *homes[],  
    [out] ULONG *pceltFetched  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `celt`  
 [in] Nombre d'objets à récupérer.  
  
 `homes`  
 Un tableau de pointeurs, chacun pointant vers un [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) objet qui fournit des informations sur une variable locale ou un argument d’une fonction.  
  
 `pceltFetched`  
 [out] Le nombre d’instances réellement retournés dans les objets.  
  
## <a name="return-value"></a>Valeur de retour  
 La méthode retourne les valeurs suivantes.  
  
|HRESULT|Description|  
|-------------|-----------------|  
|`S_OK`|La commande s'est correctement terminée.|  
|`S_FALSE`|Le nombre réel d’instances est récupéré, comme indiqué dans `pceltFetched`, est inférieur au nombre d’instances demandées.|  
  
## <a name="remarks"></a>Notes  
 Le [ICorDebugVariableHomeEnum::Next](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehomeenum-next-method.md) méthode extrait un maximum de `celt` objets commençant à la position actuelle de l’énumérateur. Lorsque la méthode retourne, `pceltFetched` contient le nombre réel d’objets récupérés.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [ICorDebugVariableHomeEnum, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehomeenum-interface.md)  
 [ICorDebugVariableHome, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md)
