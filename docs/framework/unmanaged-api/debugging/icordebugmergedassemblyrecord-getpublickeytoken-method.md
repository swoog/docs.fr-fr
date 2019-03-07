---
title: ICorDebugMergedAssemblyRecord::GetPublicKeyToken, méthode
ms.date: 03/30/2017
ms.assetid: 72020b72-9611-4bc3-b1e7-5a16b023bfa3
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 726ded615fb6d1bcd0a3a4b92e93f3675d9ce8fa
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57484561"
---
# <a name="icordebugmergedassemblyrecordgetpublickeytoken-method"></a>ICorDebugMergedAssemblyRecord::GetPublicKeyToken, méthode
Obtient le jeton de clé publique de l'assembly.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetPublicKeyToken(  
   [in] ULONG32 cbPublicKeyToken,   
   [out] ULONG32 *pcbPublicKeyToken,   
   [out, size_is(cbPublicKeyToken), length_is(*pcbPublicKeyToken)] BYTE pbPublicKeyToken[]  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `cbPublicKeyToken`  
 [in] Nombre maximal d'octets dans le tableau `pbPublicKeyToken`.  
  
 `pcbPublicKeyToken`  
 [out] Pointeur vers le nombre réel d'octets écrits dans le tableau `pbPublicKeyToken`.  
  
 `pbPublicKeyToken`  
 [in] Pointeur vers un tableau d'octets contenant le jeton de clé publique de l'assembly.  
  
## <a name="remarks"></a>Notes  
 Le jeton de clé publique d'un assembly se compose des huit derniers octets d'un hachage SHA1 de sa clé publique.  
  
> [!NOTE]
>  Cette méthode est uniquement disponible avec .NET Native.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICorDebugMergedAssemblyRecord, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugmergedassemblyrecord-interface.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
