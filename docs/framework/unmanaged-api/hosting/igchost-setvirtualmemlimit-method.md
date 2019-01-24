---
title: IGCHost::SetVirtualMemLimit, méthode
ms.date: 03/30/2017
api_name:
- IGCHost.SetVirtualMemLimit
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- SetVirtualMemLimit
helpviewer_keywords:
- IGCHost::SetVirtualMemLimit method [.NET Framework hosting]
- SetVirtualMemLimit method [.NET Framework hosting]
ms.assetid: c7e7c2d0-e58c-4650-b40c-47b2be2cda45
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d38b174a7e959647a9c1f5287b8acbbcdaf5ca7b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54564277"
---
# <a name="igchostsetvirtualmemlimit-method"></a>IGCHost::SetVirtualMemLimit, méthode
Définit la taille maximale de mémoire virtuelle du runtime.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT SetVirtualMemLimit (  
    [in] SIZE_T sztMaxVirtualMemMB  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `sztMaxVirtualMemMB`  
 [in] La taille maximale, en mégaoctets, de mémoire virtuelle du runtime.  
  
## <a name="remarks"></a>Notes  
 La taille maximale de mémoire virtuelle du runtime peut être modifiée dynamiquement.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** GCHost.idl, GCHost.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [IGCHost, interface](../../../../docs/framework/unmanaged-api/hosting/igchost-interface.md)
