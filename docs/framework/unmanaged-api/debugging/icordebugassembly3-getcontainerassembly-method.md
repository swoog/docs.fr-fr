---
title: ICorDebugAssembly3::GetContainerAssembly, méthode
ms.date: 03/30/2017
ms.assetid: f5fddeb6-b82e-4ebb-b432-849ce8513c77
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9c01898bcbd76f7e6de9445d5d1f511203c100ed
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54585183"
---
# <a name="icordebugassembly3getcontainerassembly-method"></a>ICorDebugAssembly3::GetContainerAssembly, méthode
Retourne l'assembly conteneur de cet objet `ICorDebugAssembly3`.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetContainerAssembly(  
    ICorDebugAssembly **ppAssembly  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `ppAssembly`  
 Un pointeur vers l’adresse d’un objet ICorDebugAssembly qui représente l’assembly conteneur, ou **null** si l’appel de méthode échoue.  
  
## <a name="return-value"></a>Valeur de retour  
 `S_OK` Si l’appel de méthode réussit ; Sinon, `S_FALSE`, et `ppAssembly` est **null**.  
  
## <a name="remarks"></a>Notes  
 Si cet assembly a été fusionné avec d’autres assemblys dans un seul assembly conteneur, cette méthode retourne l’assembly conteneur. Pour plus d’informations et de la terminologie, consultez le [ICorDebugProcess6::EnableVirtualModuleSplitting](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-enablevirtualmodulesplitting-method.md) rubrique.  
  
> [!NOTE]
>  Cette méthode est uniquement disponible avec .NET Native.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICorDebugAssembly3, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly3-interface.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
