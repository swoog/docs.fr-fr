---
title: IDebuggerThreadControl::ReleaseAllRuntimeThreads, méthode
ms.date: 03/30/2017
api_name:
- IDebuggerThreadControl.ReleaseAllRuntimeThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ReleaseAllRuntimeThreads
helpviewer_keywords:
- ReleaseAllRuntimeThreads method [.NET Framework hosting]
- IDebuggerThreadControl::ReleaseAllRuntimeThreads method [.NET Framework hosting]
ms.assetid: 1a2995ff-5f02-4b49-84dc-3a5f9cfd7d55
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5b3623c886a48cc938be017f955fbdac1df3f10f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33437633"
---
# <a name="idebuggerthreadcontrolreleaseallruntimethreads-method"></a>IDebuggerThreadControl::ReleaseAllRuntimeThreads, méthode
Avertit l’hôte que les services de débogage sont sur le point de libérer tous les threads qui sont bloqués.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT ReleaseAllRuntimeThreads ( );  
```  
  
## <a name="remarks"></a>Notes  
 Le `ReleaseAllRuntimeThreads` méthode ne sera jamais appelée sur un thread d’exécution. Si l’hôte a un thread du runtime bloqué, il doit maintenant le libérer.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [IDebuggerThreadControl, interface](../../../../docs/framework/unmanaged-api/hosting/idebuggerthreadcontrol-interface.md)
