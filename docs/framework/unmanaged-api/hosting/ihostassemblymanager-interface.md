---
title: IHostAssemblyManager, interface
ms.date: 03/30/2017
api_name:
- IHostAssemblyManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostAssemblyManager
helpviewer_keywords:
- IHostAssemblyManager interface [.NET Framework hosting]
ms.assetid: dfec05bb-3cd7-4bd5-b396-a4f097c3a636
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c8c8d17723481fc5b41fe5f3006fe8db2c53d1ea
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="ihostassemblymanager-interface"></a>IHostAssemblyManager, interface
Fournit des méthodes qui permettent à un hôte spécifier des ensembles d’assemblys qui doivent être chargés par le common language runtime (CLR) ou par l’hôte.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[GetAssemblyStore, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-getassemblystore-method.md)|Obtient un pointeur d’interface vers un [IHostAssemblyStore](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md) qui représente la liste des assemblys chargés par l’hôte.|  
|[GetNonHostStoreAssemblies, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-getnonhoststoreassemblies-method.md)|Obtient un pointeur d’interface vers un [ICLRAssemblyReferenceList](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md) qui représente la liste des assemblys que l’hôte attend le CLR à charger.|  
  
## <a name="remarks"></a>Notes  
 L’ordinateur hôte n’est pas requis pour implémenter `IHostAssemblyManager` ou `IHostAssemblyStore`. Si l’hôte n’implémente pas `IHostAssemblyManager`, il doit également implémenter `IHostAssemblyStore`.  
  
 L’exécution des requêtes pour un `IHostAssemblyManager` en appelant [IHostControl::GetHostManager](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-gethostmanager-method.md) lors de l’initialisation avec un `IID` d’IID_IHostAssemblyManager.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [ICLRAssemblyReferenceList, interface](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)  
 [IHostAssemblyStore, interface](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-interface.md)  
 [IHostControl, interface](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md)  
 [Interfaces d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
