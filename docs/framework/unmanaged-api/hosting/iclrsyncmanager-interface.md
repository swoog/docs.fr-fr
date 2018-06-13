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
ms.openlocfilehash: 1b87ccc3d6c3e957d0384499048032e35247093a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33436479"
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
