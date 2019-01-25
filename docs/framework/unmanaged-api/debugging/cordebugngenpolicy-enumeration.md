---
title: CorDebugNGenPolicy, énumération
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- CorDebugNGenPolicy
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugNGenPolicy
helpviewer_keywords:
- CorDebugNgenPolicy enumeration [.NET Framework debugging]
ms.assetid: edb4e4d2-3166-44d4-8b17-bf302f7ea093
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1ae40916807a86d1c9828080a6cb9e5c1d14c2ec
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54671224"
---
# <a name="cordebugngenpolicy-enumeration"></a>CorDebugNGenPolicy, énumération
Fournit une valeur qui détermine si un débogueur charge les images natives (NGen) depuis le cache d'images natives.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp
enum CorDebugNGENPolicy {  
    DISABLE_LOCAL_NIC = 1  
} CorDebugNGENPolicy;  
```  
  
## <a name="members"></a>Membres  
  
|Nom de membre|Description|  
|-----------------|-----------------|  
|`DISABLE_LOCAL_NIC`|Dans un [!INCLUDE[win8_appname_long](../../../../includes/win8-appname-long-md.md)] application, l’utilisation d’images à partir du cache d’images natives locales est désactivée. Dans une application de bureau, ce paramètre n’a aucun effet.|  
  
## <a name="remarks"></a>Notes  
 Le `CorDebugNGENPolicy` énumération est utilisée par le [ICorDebugProcess5::EnableNGENPolicy](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-enablengenpolicy-method.md) (méthode). La désactivation de l’utilisation d’images à partir du cache d’images natives locales fournit une expérience de débogage cohérente en veillant à ce que le débogueur charge des images pouvant être débogués compilé par JIT au lieu des images natives optimisées.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [Énumérations de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
