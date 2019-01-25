---
title: ICorDebugDataTarget2::GetImageFromPointer, méthode
ms.date: 03/30/2017
ms.assetid: 939cabe1-b647-4090-b662-eeec23c6c58d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 64affd9b262934316fc904b10f1a9c4a7e7657bb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54539972"
---
# <a name="icordebugdatatarget2getimagefrompointer-method"></a>ICorDebugDataTarget2::GetImageFromPointer, méthode
Retourne l'adresse de base et la taille d'un module à partir d'une adresse présente dans ce module.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetImageFromPointer(  
   [in] CORDB_ADDRESS addr,   
   [out] CORDB_ADDRESS *pImageBase,   
   [out] ULONG32 *pSize  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `addr`  
 Un [CORDB_ADDRESS](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md) valeur qui représente une adresse dans un module.  
  
 `pImageBase`  
 [out] Un [CORDB_ADDRESS](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md) valeur qui représente l’adresse de base du module.  
  
 `pSize`  
 Pointeur vers la taille du module.  
  
## <a name="remarks"></a>Notes  
  
> [!NOTE]
>  Cette méthode est uniquement disponible avec .NET Native.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICorDebugDataTarget2, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget2-interface.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
