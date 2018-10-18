---
title: ICLRSyncManager, interface
ms.date: 03/30/2017
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
ms.openlocfilehash: 21295268ba5c230062fadddc9c61217f3574551b
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "49370982"
---
# <a name="iclrsyncmanager-interface"></a>ICLRSyncManager, interface
Définit des méthodes qui permettent à l’hôte pour obtenir des informations sur les tâches demandées et pour détecter les blocages dans son implémentation de synchronisation.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[CreateRWLockOwnerIterator, méthode](iclrsyncmanager-createrwlockowneriterator-method.md)|Demande que le common language runtime (CLR) crée un itérateur pour l’hôte à utiliser pour déterminer l’ensemble de tâches en attente sur un verrou de lecteur-writer.|  
|[DeleteRWLockOwnerIterator, méthode](iclrsyncmanager-deleterwlockowneriterator-method.md)|Demande que le CLR détruise un itérateur qui a été créé par un appel à `CreateRWLockOwnerIterator`.|  
|[GetMonitorOwner, méthode](iclrsyncmanager-getmonitorowner-method.md)|Obtient la tâche qui possède le moniteur spécifié.|  
|[GetRWLockOwnerNext, méthode](iclrsyncmanager-getrwlockownernext-method.md)|Obtient la tâche suivante qui attend le verrou de lecteur-writer actuel.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Threading.Thread>  
 [IHostSyncManager, interface](ihostsyncmanager-interface.md)  
 [Threading managé et non managé](/previous-versions/dotnet/netframework-4.0/5s8ee185(v=vs.100))  
 [Interfaces d’hébergement](hosting-interfaces.md)
