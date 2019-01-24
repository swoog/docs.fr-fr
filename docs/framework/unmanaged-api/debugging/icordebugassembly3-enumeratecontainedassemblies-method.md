---
title: ICorDebugAssembly3::EnumerateContainedAssemblies, méthode
ms.date: 03/30/2017
ms.assetid: 98f15b05-afad-4616-9e2a-1a9af31948b6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: aa99e7289e0e86032f7bb85bbe209932f5c50d16
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54627575"
---
# <a name="icordebugassembly3enumeratecontainedassemblies-method"></a>ICorDebugAssembly3::EnumerateContainedAssemblies, méthode
Obtient un énumérateur pour les assemblys contenus dans cet assembly.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT EnumerateContainedAssemblies(  
    ICorDebugAssemblyEnum **ppAssemblies  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `ppAssemblies`  
 [out] Pointeur vers l’adresse d’un objet d’interface ICorDebugAssemblyEnum qui est l’énumérateur.  
  
## <a name="return-value"></a>Valeur de retour  
 `S_OK` si cet objet `ICorDebugAssembly3` est un conteneur ; sinon, `S_FALSE`, et l'énumération est vide.  
  
## <a name="remarks"></a>Notes  
 Des symboles doivent être utilisés pour énumérer les assemblys contenus dans l'assembly. S'ils ne sont pas présents, la méthode retourne `S_FALSE`, et aucun énumérateur valide n'est fourni.  
  
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
