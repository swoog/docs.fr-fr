---
title: ICorDebugRegisterSet::GetRegistersAvailable, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet.GetRegistersAvailable
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet::GetRegistersAvailable
helpviewer_keywords:
- ICorDebugRegisterSet::GetRegistersAvailable method [.NET Framework debugging]
- GetRegistersAvailable method, ICorDebugRegisterSet interface [.NET Framework debugging]
ms.assetid: 4ba08ffa-55a2-4662-9d6d-4738f1db60c9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f341098268f735a576bdbc5f0cea52f1a7e14f90
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59156037"
---
# <a name="icordebugregistersetgetregistersavailable-method"></a>ICorDebugRegisterSet::GetRegistersAvailable, méthode
Obtient un masque de bits indiquant les registres dans ce [ICorDebugRegisterSet](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md) sont actuellement disponibles.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetRegistersAvailable (  
    [out] ULONG64   *pAvailable  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pAvailable`  
 [out] Un masque de bits qui indique quels registres sont actuellement disponibles.  
  
## <a name="remarks"></a>Notes  
 Un Registre est peut-être indisponible si sa valeur ne peut pas être déterminée pour la situation donnée.  
  
 Le masque retourné contient un bit pour chaque registre (1 << l’index du Registre). La valeur de bit est 1 si le Registre est disponible, ou 0 s’il n’est pas disponible.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorDebugRegisterSet, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md)
- [ICorDebugRegisterSet2, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-interface.md)
