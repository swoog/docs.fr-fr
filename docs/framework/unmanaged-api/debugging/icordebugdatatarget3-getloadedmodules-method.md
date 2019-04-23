---
title: ICorDebugDataTarget3::GetLoadedModules (méthode)
ms.date: 03/30/2017
ms.assetid: 9a48c05b-1949-416e-933c-52549b6fcf5e
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 464fd9ac44d6ba5717dbc4ecfbe03b6e6ad52276
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59138656"
---
# <a name="icordebugdatatarget3getloadedmodules-method"></a>ICorDebugDataTarget3::GetLoadedModules (méthode)
Obtient la liste des modules qui ont été chargés jusqu'à présent.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetLoadedModules(  
   [in] ULONG32 cRequestedModules,  
   [out] ULONG32 *pcFetchedModules,  
   [out, size_is(cRequestedModules), length_is(*pcFetchedModules)] ICorDebugLoadedModule *pLoadedModules[]  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `cRequestedModules`  
 [in] Nombre de modules pour lesquels des informations sont demandées.  
  
 `pcFetchedModules`  
 [out] Pointeur vers le nombre de modules à propos desquels des informations ont été retournées.  
  
 `pLoadedModules`  
 [out] Un pointeur vers un tableau de [ICorDebugLoadedModule](../../../../docs/framework/unmanaged-api/debugging/icordebugloadedmodule-interface.md) objets qui fournissent des informations sur les modules chargement.  
  
## <a name="remarks"></a>Notes  
  
> [!NOTE]
>  Cette méthode est uniquement disponible avec .NET Native.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorDebugDataTarget3, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget3-interface.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
