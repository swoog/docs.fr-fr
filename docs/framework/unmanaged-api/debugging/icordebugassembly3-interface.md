---
title: ICorDebugAssembly3, interface
ms.date: 03/30/2017
ms.assetid: 17fc5d76-75a9-4933-83f0-594de7f973f3
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: eecb135e034c3565e805ea776115579488b2a4d5
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59210306"
---
# <a name="icordebugassembly3-interface"></a>ICorDebugAssembly3, interface
Étend logiquement l’interface ICorDebugAssembly pour prendre en charge pour les assemblys conteneurs et leurs assemblys de relation contenant-contenus.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[EnumerateContainedAssemblies, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly3-enumeratecontainedassemblies-method.md)|Obtient un énumérateur pour les assemblys contenus dans cet assembly.|  
|[GetContainerAssembly, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugassembly3-getcontainerassembly-method.md)|Retourne l'assembly conteneur de cet objet `ICorDebugAssembly3`.|  
  
## <a name="remarks"></a>Notes  
  
> [!NOTE]
>  L'interface est uniquement disponible avec .NET Native. Une tentative d'appel à `QueryInterface` pour récupérer un pointeur d'interface retourne `E_NOINTERFACE` pour les scénarios ICorDebug en dehors de .NET Native.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
