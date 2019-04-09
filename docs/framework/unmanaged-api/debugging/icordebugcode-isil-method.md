---
title: ICorDebugCode::IsIL, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugCode.IsIL
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::IsIL
helpviewer_keywords:
- ICorDebugCode::IsIL method [.NET Framework debugging]
- IsIL method [.NET Framework debugging]
ms.assetid: 132ef8cc-d938-43f3-b8f2-e3b97c0ceb33
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a82606d90444c2d543065287780e42da4f8b4943
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59180685"
---
# <a name="icordebugcodeisil-method"></a>ICorDebugCode::IsIL, méthode
Obtient une valeur qui indique si ce « ICorDebugCode » représente le code qui a été compilé en langage intermédiaire Microsoft (MSIL).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT IsIL (  
    [out] BOOL       *pbIL  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pbIL`  
 [out] `true` si ce `ICorDebugCode` représente le code qui a été compilé dans le langage MSIL ; sinon, `false`.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
