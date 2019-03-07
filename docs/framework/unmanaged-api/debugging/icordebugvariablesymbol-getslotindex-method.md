---
title: Méthode ICorDebugVariableSymbol::GetSlotIndex
ms.date: 03/30/2017
ms.assetid: 09c19f5f-afc4-4e0c-bffe-cd7147bc7a43
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8c7b70638b963968fb3ed7e294f1767718f9bc34
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57501290"
---
# <a name="icordebugvariablesymbolgetslotindex-method"></a>Méthode ICorDebugVariableSymbol::GetSlotIndex
Obtient l'index d'emplacement géré d'une variable locale.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetSlotIndex(  
   [out] ULONG32 *pSlotIndex  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pSlotIndex`  
 [out] Pointeur vers l'index d'emplacement de la variable locale.  
  
## <a name="return-value"></a>Valeur de retour  
 `S_OK` si l'opération a réussi. `E_FAIL` si la variable est un argument de fonction.  
  
## <a name="remarks"></a>Notes  
 L'index emplacement managé d'une variable locale peut être utilisé pour récupérer des informations de métadonnées de la variable.  
  
> [!NOTE]
>  Cette méthode est uniquement disponible avec .NET Native.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICorDebugVariableSymbol, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-interface.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
