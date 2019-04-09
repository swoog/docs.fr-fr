---
title: Icordebugmemorybuffer::getstartaddress, méthode
ms.date: 03/30/2017
ms.assetid: f804d9ab-8c88-44f0-b278-5fcca7f87726
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 58649a0fc12ce63a1307af5d831dbf5e0d5a776a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59136979"
---
# <a name="icordebugmemorybuffergetstartaddress-method"></a>Icordebugmemorybuffer::getstartaddress, méthode
Obtient l'adresse de départ de la mémoire tampon.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetStartAddress(  
   [out] LPCVOID *address  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `address`  
 [out] Pointeur vers l'adresse de départ de la mémoire tampon.  
  
## <a name="remarks"></a>Notes  
  
> [!WARNING]
>  Cette méthode est uniquement disponible avec .NET Native.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorDebugMemoryBuffer, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-interface.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
