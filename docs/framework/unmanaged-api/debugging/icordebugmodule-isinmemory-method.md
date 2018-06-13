---
title: ICorDebugModule::IsInMemory, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugModule.IsInMemory
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::IsInMemory
helpviewer_keywords:
- IsInMemory method [.NET Framework debugging]
- ICorDebugModule::IsInMemory method [.NET Framework debugging]
ms.assetid: 89940711-98e7-4aa6-bffc-5e39e91e1b7d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9ae5c16f9f508511e4a15b2eae2c28d68238f1d7
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33415891"
---
# <a name="icordebugmoduleisinmemory-method"></a>ICorDebugModule::IsInMemory, méthode
Obtient une valeur qui indique si ce module existe uniquement en mémoire.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT IsInMemory(  
    [out] BOOL *pInMemory  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `pInMemory`  
 [out] `true` si ce module existe uniquement en mémoire ; sinon, `false`.  
  
## <a name="remarks"></a>Notes  
 Le common language runtime (CLR) prend en charge le chargement de modules à partir de flux bruts d’octets. Ces modules sont appelés *en mémoire modules* et n’existent pas sur le disque.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
    
 
