---
title: ICorDebugILFrame4::GetCodeEx, méthode
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICorDebugILFrame4.GetLocalVariableEx
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: aeda0e42-29ee-4ca8-9f21-ac4641677a62
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 24be4507e8ad6cde1e9c50582e352f0fc9b12ed3
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44201762"
---
# <a name="icordebugilframe4getcodeex-method"></a>ICorDebugILFrame4::GetCodeEx, méthode
[Pris en charge dans .NET Framework 4.5.2 et ultérieur]  
  
 Obtient un pointeur vers le code exécuté par ce frame de pile.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp
HRESULT GetCodeEx(  
   [in] ILCodeKind flags,   
   [out] ICorDebugCode **ppCode  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `flags`  
 [in] Un [ILCodeKind](../../../../docs/framework/unmanaged-api/debugging/ilcodekind-enumeration.md) membre d’énumération qui spécifie si le langage intermédiaire (IL) défini par la demande ReJIT du profileur est inclus dans le frame.  
  
 `ppCode`  
 [out] Pointeur vers l’adresse d’un objet « ICorDebugCode » qui représente le code en cours d’exécution de ce frame de pile.  
  
## <a name="remarks"></a>Notes  
 Cette méthode est similaire à la [ICorDebugFrame::GetCode](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getcode-method.md) (méthode), à ceci près qu’elle peut éventuellement accéder au code défini par la demande ReJIT du profileur. Appel de cette méthode avec un `flags` valeur `ILCODE_ORIGINAL_IL` équivaut à appeler [GetCode](../../../../docs/framework/unmanaged-api/debugging/icordebugframe-getcode-method.md); si la méthode est instrumentée, son langage intermédiaire ne sera pas accessible. `ILCODE_REJIT_IL` permet au débogueur d'accéder au langage intermédiaire défini par la demande ReJIT du profileur. Si le langage intermédiaire n’est pas instrumenté, `ppCode` est **null**, et la méthode retourne `S_OK`.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [ICorDebugILFrame4, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe4-interface.md)  
 [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [ReJIT : Un Guide de procédure](https://blogs.msdn.com/b/davbr/archive/2011/10/12/rejit-a-how-to-guide.aspx)
