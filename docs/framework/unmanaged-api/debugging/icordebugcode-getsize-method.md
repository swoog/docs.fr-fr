---
title: ICorDebugCode::GetSize, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugCode.GetSize
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::GetSize
helpviewer_keywords:
- GetSize method, ICorDebugCode interface [.NET Framework debugging]
- ICorDebugCode::GetSize method [.NET Framework debugging]
ms.assetid: 115bc6de-f5e2-4e8e-bb38-c7cf54045434
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3bd21e43973d116e4383d88bd5ce90f0fbfeb1a6
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57471476"
---
# <a name="icordebugcodegetsize-method"></a>ICorDebugCode::GetSize, méthode
Obtient la taille, en octets, du code binaire représenté par « ICorDebugCode ».  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetSize (  
    [out] ULONG32    *pcBytes  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pcBytes`  
 [out] Un pointeur vers la taille, en octets, du fichier binaire de code que ce `ICorDebugCode` représente l’objet.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

