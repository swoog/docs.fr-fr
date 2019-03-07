---
title: IGCThreadControl::SuspensionEnding, méthode
ms.date: 03/30/2017
api_name:
- IGCThreadControl.SuspensionEnding
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- SuspensionEnding
helpviewer_keywords:
- IGCThreadControl::SuspensionEnding method [.NET Framework hosting]
- SuspensionEnding method, IGCThreadControl interface [.NET Framework hosting]
ms.assetid: 70814265-c734-4ddc-9502-fe8b28d2b414
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ffee1550c64f1ce7c438580ce78a497aeeb99f3a
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57468765"
---
# <a name="igcthreadcontrolsuspensionending-method"></a>IGCThreadControl::SuspensionEnding, méthode
Avertit l’hôte que le runtime est reprise des threads après un garbage collection ou une suspension.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT SuspensionEnding (  
    [in] DWORD Generation  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `Generation`  
 [in] La génération sur lequel un garbage collection a été effectué.  
  
## <a name="remarks"></a>Notes  
 Ne replanifiez pas de threads pendant le `SuspensionEnding` rappel.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [IGCThreadControl, interface](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-interface.md)
