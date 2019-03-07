---
title: IGCHost::SetGCStartupLimits, méthode
ms.date: 03/30/2017
api_name:
- IGCHost.SetGCStartupLimits
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- SetGCStartupLimits
helpviewer_keywords:
- SetGCStartupLimits method, IGCHost interface [.NET Framework hosting]
- IGCHost::SetGCStartupLimits method [.NET Framework hosting]
ms.assetid: cae53926-82ac-4d1d-b297-0bde0bd1bebb
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6962b52925ab5b70a8b34c6d3720bb45c85b24c0
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57473888"
---
# <a name="igchostsetgcstartuplimits-method"></a>IGCHost::SetGCStartupLimits, méthode
Définit la taille du segment et la taille maximale pour la génération 0.  
  
> [!IMPORTANT]
>  En commençant par le [!INCLUDE[net_v45](../../../../includes/net-v45-md.md)], vous pouvez définir la taille des segments de taille maximale de génération 0 aux valeurs et supérieur à `DWORD` à l’aide de la [IGCHost2::SetGCStartupLimitsEx](../../../../docs/framework/unmanaged-api/hosting/igchost2-setgcstartuplimitsex-method.md) (méthode).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT SetGCStartupLimits (  
    [in] DWORD SegmentSize,  
    [in] DWORD MaxGen0Size  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `SegmentSize`  
 [in] La taille du segment utilisé par le système de garbage collection.  
  
 `MaxGen0Size`  
 [in] La taille maximale pour la génération 0.  
  
## <a name="remarks"></a>Notes  
 Le `SetGCStartupLimits` méthode peut être appelée qu’une seule fois. Ces valeurs ne peuvent pas être modifiées ultérieurement.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** GCHost.idl, GCHost.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [IGCHost, interface](../../../../docs/framework/unmanaged-api/hosting/igchost-interface.md)
