---
title: IGCHost::GetStats, méthode
ms.date: 03/30/2017
api_name:
- IGCHost.GetStats
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- GetStats
helpviewer_keywords:
- GetStats method, IGCHost interface [.NET Framework hosting]
- IGCHost::GetStats method [.NET Framework hosting]
ms.assetid: c4ae022c-46ac-4f19-9ddd-09b955f19412
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 14751b41809eeda5e6bd990fae368879d0f30492
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59227832"
---
# <a name="igchostgetstats-method"></a>IGCHost::GetStats, méthode
Obtient les statistiques pour l’état actuel du système garbage collection.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetStats (  
    [in, out] COR_GC_STATS *pStats  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pStats`  
 [in, out] Un pointeur vers un [COR_GC_STATS](../../../../docs/framework/unmanaged-api/hosting/cor-gc-stats-structure.md) structure qui contient les statistiques de l’état actuel du système garbage collection.  
  
## <a name="remarks"></a>Notes  
 Les statistiques peuvent être utilisées par un système intelligent d’allocation pour aider le système de garbage collection à fonctionner. Par exemple, le système d’allocation peut déterminer, après avoir examiné les statistiques dont il a besoin pour ajouter davantage de mémoire ou de forcer une collection.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** GCHost.idl, GCHost.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IGCHost, interface](../../../../docs/framework/unmanaged-api/hosting/igchost-interface.md)
