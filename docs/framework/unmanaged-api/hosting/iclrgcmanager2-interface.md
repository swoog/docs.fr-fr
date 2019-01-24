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
ms.openlocfilehash: 9897526882a8ae53410a7744f78c558dfa6981e1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54708582"
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
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [Gestion automatique de la mémoire](../../../../docs/standard/automatic-memory-management.md)
- [COR_GC_STATS, structure](../../../../docs/framework/unmanaged-api/hosting/cor-gc-stats-structure.md)
- [ICLRControl, interface](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)
- [Interfaces d’hébergement CLR ajoutées dans .NET Framework 4 et 4.5](../../../../docs/framework/unmanaged-api/hosting/clr-hosting-interfaces-added-in-the-net-framework-4-and-4-5.md)
- [Interfaces d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [Hébergement](../../../../docs/framework/unmanaged-api/hosting/index.md)
