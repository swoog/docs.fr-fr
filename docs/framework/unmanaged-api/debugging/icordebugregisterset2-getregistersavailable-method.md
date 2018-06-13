---
title: ICorDebugRegisterSet2::GetRegistersAvailable, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet2.GetRegistersAvailable
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet2::GetRegistersAvailable
helpviewer_keywords:
- GetRegistersAvailable method, ICorDebugRegisterSet2 interface [.NET Framework debugging]
- ICorDebugRegisterSet2::GetRegistersAvailable method [.NET Framework debugging]
ms.assetid: f3ed344b-0d3a-44e8-8000-2a97e0805a2c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d3a9cdb49c1a44dbc68cd4b7ccf4d4781ce5c539
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33421890"
---
# <a name="icordebugregisterset2getregistersavailable-method"></a>ICorDebugRegisterSet2::GetRegistersAvailable, méthode
Obtient un tableau d’octets qui fournit une bitmap des registres disponibles.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetRegistersAvailable (  
    [in] ULONG32 numChunks,  
    [out, size_is(numChunks)] BYTE availableRegChunks[]  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `numChunks`  
 [in] Taille du tableau `availableRegChunks`.  
  
 `availableRegChunks`  
 [out] Tableau d’octets, dont chaque bit correspond à un Registre. Si un Registre est disponible, le bit correspondant au Registre est défini.  
  
## <a name="remarks"></a>Notes  
 Les valeurs de l’énumération CorDebugRegister spécifient les registres de différents microprocesseurs. Les cinq derniers bits de chaque valeur sont des index dans le `availableRegChunks` tableau d’octets. Les trois bits inférieurs de chaque valeur identifier la position de bit dans l’octet indexé. Étant donné un `CorDebugRegister` valeur qui spécifie un registre particulier, la position du Registre dans le masque est déterminée comme suit :  
  
1.  Extrayez l’index nécessaire pour accéder à l’octet correct dans le `availableRegChunks` tableau :  
  
     `CorDebugRegister` valeur >> 3  
  
2.  Extrayez la position de bit dans l’octet indexé, où le bit zéro est le bit le moins significatif :  
  
     `CorDebugRegister` valeur & 7  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [ICorDebugRegisterSet2, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-interface.md)  
 [ICorDebugRegisterSet, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md)
