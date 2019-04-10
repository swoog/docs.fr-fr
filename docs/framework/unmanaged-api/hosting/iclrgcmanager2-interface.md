---
title: ICLRGCManager2, interface
ms.date: 03/30/2017
api_name:
- ICLRGCManager2
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRGCManager2
helpviewer_keywords:
- ICLRGCManager2 interface [.NET Framework hosting]
ms.assetid: 4b5ffd7b-9ad7-41cd-9bba-34030ae3da7e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a89a7ef34418163d790fd055de681c1cdf989e57
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59226909"
---
# <a name="iclrgcmanager2-interface"></a>ICLRGCManager2, interface
Fournit des méthodes qui permettent à un hôte d’interagir avec le système de garbage collection du common language runtime.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[SetGCStartupLimitsEx, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrgcmanager2-setgcstartuplimitsex-method.md)|Définit la taille d’un segment de garbage collection et la taille maximale de la génération du système de nettoyage 0. Permet la génération 0 et les tailles de segment supérieures à `DWORD`.|  
  
## <a name="remarks"></a>Notes  
 Cette interface hérite le [ICLRGCManager, Interface](../../../../docs/framework/unmanaged-api/hosting/iclrgcmanager-interface.md).  
  
 Le common language runtime (CLR) implémente son mécanisme de garbage collection avec managé <xref:System.GC> type. Pour plus d’informations sur le système de garbage collection, consultez [Garbage Collection](../../../../docs/standard/garbage-collection/index.md).  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Automatic Memory Management](../../../../docs/standard/automatic-memory-management.md)
- [COR_GC_STATS, structure](../../../../docs/framework/unmanaged-api/hosting/cor-gc-stats-structure.md)
- [ICLRControl, interface](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)
- [Interfaces d'hébergement du CLR ajoutées dans .NET Framework 4 et 4.5](../../../../docs/framework/unmanaged-api/hosting/clr-hosting-interfaces-added-in-the-net-framework-4-and-4-5.md)
- [Interfaces d'hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [Hébergement](../../../../docs/framework/unmanaged-api/hosting/index.md)
