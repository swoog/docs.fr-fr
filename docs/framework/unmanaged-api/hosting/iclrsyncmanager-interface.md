---
title: ICLRSyncManager, interface
ms.date: 03/30/2017
ms.prod: .net-framework
ms.technology:
- dotnet-clr
ms.topic: reference
api_name:
- ICLRSyncManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRSyncManager
helpviewer_keywords:
- ICLRSyncManager interface [.NET Framework hosting]
ms.assetid: a49f9d80-1c76-4ddd-8c49-34f913a5c596
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 17a1e3073713b54cb7a68e6ba3ef2562d4fbcaeb
ms.sourcegitcommit: 9a4fe1a1c37b26532654b4bbe22d702237950009
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2018
---
# <a name="iclrsyncmanager-interface"></a>ICLRSyncManager, interface
Définit des méthodes qui permettent à l’hôte pour obtenir des informations sur les tâches demandées et pour détecter les blocages dans son implémentation de synchronisation.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[CreateRWLockOwnerIterator, méthode](iclrsyncmanager-createrwlockowneriterator-method.md)|Demande que le common language runtime (CLR) crée un itérateur pour l’hôte à utiliser pour déterminer l’ensemble de tâches attendant un verrou de lecteur-writer.|  
|[DeleteRWLockOwnerIterator, méthode](iclrsyncmanager-deleterwlockowneriterator-method.md)|Demande que le CLR détruise un itérateur qui a été créé par un appel à `CreateRWLockOwnerIterator`.|  
|[GetMonitorOwner, méthode](iclrsyncmanager-getmonitorowner-method.md)|Obtient la tâche qui possède le moniteur spécifié.|  
|[GetRWLockOwnerNext, méthode](iclrsyncmanager-getrwlockownernext-method.md)|Obtient la tâche suivante qui attend le verrou de lecteur-writer actuelle.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Threading.Thread>  
 [IHostSyncManager, interface](ihostsyncmanager-interface.md)  
 [Threading managé et non managé](https://msdn.microsoft.com/library/db425c20-4b2f-4433-bf96-76071c7881e5(v=vs.100))  
 [Interfaces d’hébergement](hosting-interfaces.md)
