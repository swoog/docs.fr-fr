---
title: IDebuggerInfo::IsDebuggerAttached, méthode
ms.date: 03/30/2017
api_name:
- IDebuggerInfo.IsDebuggerAttached
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IsDebuggerAttached
helpviewer_keywords:
- IDebuggerInfo::IsDebuggerAttached method [.NET Framework hosting]
- IsDebuggerAttached method, IDebuggerInfo interface [.NET Framework hosting]
ms.assetid: 6e21872f-602f-411a-a423-bff5cdf27000
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: aae7bc60abaedef8c3491a90eae01ebc02cff1ce
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57469051"
---
# <a name="idebuggerinfoisdebuggerattached-method"></a>IDebuggerInfo::IsDebuggerAttached, méthode
Obtient une valeur qui indique si un débogueur managé est attaché à ce processus.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT IsDebuggerAttached (  
    [out] BOOL *pbAttached  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pbAttached`  
 [out] Un pointeur vers une valeur qui est `true` si un débogueur managé est attaché au processus ; sinon, `false`.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [IDebuggerInfo, interface](../../../../docs/framework/unmanaged-api/hosting/idebuggerinfo-interface.md)
