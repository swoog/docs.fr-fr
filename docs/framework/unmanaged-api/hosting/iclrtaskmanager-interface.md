---
title: ICLRTaskManager, interface
ms.date: 03/30/2017
api_name:
- ICLRTaskManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTaskManager
helpviewer_keywords:
- ICLRTaskManager interface [.NET Framework hosting]
ms.assetid: 2bd55e0c-001b-41fd-b29d-f01670fe8216
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9012a38271afdef5e00e9e69eb9b2730834be2fa
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54656152"
---
# <a name="iclrtaskmanager-interface"></a>ICLRTaskManager, interface
Fournit des méthodes qui permettent à l’hôte à demander explicitement que le common language runtime (CLR) créer une nouvelle tâche, obtenir la tâche en cours d’exécution et définir le langage géographique et la culture pour la tâche.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[CreateTask, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-createtask-method.md)|Demande explicitement que le CLR crée un nouveau [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) instance.|  
|[GetCurrentTask, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-getcurrenttask-method.md)|Obtient le `ICLRTask` instance qui représente la tâche en cours d’exécution.|  
|[GetCurrentTaskType, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-getcurrenttasktype-method.md)|Obtient le type de la tâche en cours d’exécution.|  
|[SetLocale, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-setlocale-method.md)|Notifie le CLR que l’hôte a modifié l’identificateur de paramètres régionaux sur la tâche en cours d’exécution.|  
|[SetUILocale, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-setuilocale-method.md)|Notifie le common language runtime que l’hôte a modifié l’identificateur de paramètres régionaux d’interface utilisateur sur la tâche en cours d’exécution.|  
  
## <a name="remarks"></a>Notes  
 Chaque tâche qui s’exécute dans un environnement hébergé a des représentations à la fois du côté hôte (une instance de [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)) et sur le côté CLR (une instance de [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)). L’hôte ou le CLR peut lancer la création d’une tâche, mais la représentation côté hôte doit être associée à une représentation côté CLR correspondante pour garantir une communication réussie entre l’hôte et le CLR concernant la tâche. Les deux objets doivent être créées et instanciés avant que le code managé peut s’exécuter sur un thread de système d’exploitation.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICLRTask, interface](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [IHostTask, interface](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [IHostTaskManager, interface](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
- [Interfaces d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
