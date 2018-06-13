---
title: COR_GC_THREAD_STATS, structure
ms.date: 03/30/2017
api_name:
- COR_GC_THREAD_STATS
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- COR_GC_THREAD_STATS
helpviewer_keywords:
- COR_GC_THREAD_STATS structure [.NET Framework hosting]
ms.assetid: 01f9a59b-7679-4d42-9ced-4a8981625c3d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 24a386fe82bbd004954924a573c090af7f58824a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33431826"
---
# <a name="corgcthreadstats-structure"></a>COR_GC_THREAD_STATS, structure
Contient des statistiques par thread concernant le garbage collection.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef struct _COR_GC_THREAD_STATS {  
    ULONGLONG  PerThreadAllocation;   
    ULONG      Flags;   
} COR_GC_THREAD_STATS;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`PerThreadAllocation`|Le nombre d’octets de mémoire alloués sur le thread qui est associé à l’actuel `COR_GC_THREAD_STATS` instance. Ce nombre est remis à zéro chaque fois qu'un nettoyage de la génération zéro se produit.|  
|`Flags`|Le nombre d’octets promus à une génération supérieure garbage collection le plus récent.|  
  
## <a name="remarks"></a>Notes  
 [ICLRTask::GetMemStats](../../../../docs/framework/unmanaged-api/hosting/iclrtask-getmemstats-method.md) prend un paramètre de sortie de type `COR_GC_THREAD_STATS`.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** GCHost.idl  
  
 **Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Structures d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-structures.md)  
 [IHostTask, interface](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
