---
title: Méthode ICorDebugSymbolProvider2::GetFrameProps
ms.date: 03/30/2017
ms.assetid: f07b73f3-188d-43a9-8f7d-44dce2f1ddb7
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cd8cc461519b01a9bf62a28610386e51630060d4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54646195"
---
# <a name="icordebugsymbolprovider2getframeprops-method"></a>Méthode ICorDebugSymbolProvider2::GetFrameProps
Retourne l'adresse virtuelle relative de départ d'une méthode et le frame parent en fonction d'une adresse virtuelle relative de code.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetFrameProps(  
   [in] ULONG32 codeRva,  
   [out] ULONG32 *pCodeStartRva,  
   [out] ULONG32 *pParentFrameStartRva  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `codeRva`  
 [in] Adresse virtuelle relative du code.  
  
 `pCodeStartRva`  
 [out] Pointeur vers l'adresse virtuelle relative de départ de la méthode.  
  
 `pParentFrameStartRva`  
 [out] Pointeur vers l'adresse virtuelle relative de départ du frame.  
  
## <a name="remarks"></a>Notes  
  
> [!NOTE]
>  Cette méthode est uniquement disponible avec .NET Native.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICorDebugSymbolProvider2, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider2-interface.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
