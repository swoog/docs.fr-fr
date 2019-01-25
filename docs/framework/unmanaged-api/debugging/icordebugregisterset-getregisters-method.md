---
title: ICorDebugRegisterSet::GetRegisters, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet.GetRegisters
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet::GetRegisters
helpviewer_keywords:
- GetRegisters method, ICorDebugRegisterSet interface [.NET Framework debugging]
- ICorDebugRegisterSet::GetRegisters method [.NET Framework debugging]
ms.assetid: fdf91864-48ea-4aa6-b70c-361b7a3184c7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ee56a7f343de999d68a71d9eac04eed6e06b444e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54568892"
---
# <a name="icordebugregistersetgetregisters-method"></a>ICorDebugRegisterSet::GetRegisters, méthode
Obtient la valeur de chaque registre (sur l’ordinateur qui exécute actuellement le code) qui est spécifié par le masque de bits.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetRegisters (  
    [in] ULONG64       mask,   
    [in] ULONG32       regCount,  
    [out, size_is(regCount), length_is(regCount)]  
        CORDB_REGISTER regBuffer[]  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `mask`  
 [in] Un masque de bits qui spécifie les valeurs de registres à récupérer. Chaque bit correspond à un Registre. Si un bit est défini sur 1, la valeur de Registre est récupérée ; Sinon, la valeur de Registre n’est pas récupérée.  
  
 `regCount`  
 [in] Le nombre de valeurs de registres à récupérer.  
  
 `regBuffer`  
 [out] Un tableau de `CORDB_REGISTER` objets, chacun d’eux reçoit une valeur d’un Registre.  
  
## <a name="remarks"></a>Notes  
 La taille du tableau doit être égale au nombre de bits définis à l’autre dans le masque de bits. Le `regCount` paramètre spécifie le nombre d’éléments dans la mémoire tampon qui recevra les valeurs de Registre. Si le `regCount` valeur est trop petite pour le nombre de registres indiqué par le masque, les registres plus élevées seront tronquées à partir de l’ensemble. Si le `regCount` valeur est trop volumineux, l’inutilisé `regBuffer` éléments ne sont pas modifiés.  
  
 Si le masque de bits spécifie un Registre qui n’est pas disponible, `GetRegisters` retourne une valeur indéterminée pour ce Registre.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICorDebugRegisterSet, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md)
- [ICorDebugRegisterSet2, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-interface.md)
