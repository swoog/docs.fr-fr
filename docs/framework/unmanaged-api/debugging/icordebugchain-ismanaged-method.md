---
title: ICorDebugChain::IsManaged, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugChain.IsManaged
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain::IsManaged
helpviewer_keywords:
- ICorDebugChain::IsManaged method [.NET Framework debugging]
- IsManaged method, ICorDebugChain interface [.NET Framework debugging]
ms.assetid: 17b389a0-1a4d-4e8a-8613-9bc1769930f9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a27ea95ca78f7db8f67ec2a13f02767e67619e97
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57488056"
---
# <a name="icordebugchainismanaged-method"></a>ICorDebugChain::IsManaged, méthode
Obtient une valeur qui indique si cette chaîne est en cours d’exécution du code managé.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT IsManaged (  
    [out] BOOL               *pManaged  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pManaged`  
 [out] `true` si cette chaîne est en cours d’exécution du code managé ; sinon, `false`.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
