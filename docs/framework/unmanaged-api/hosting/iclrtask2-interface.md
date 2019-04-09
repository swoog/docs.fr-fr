---
title: ICLRTask2, interface
ms.date: 03/30/2017
api_name:
- ICLRTask2
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTask2
helpviewer_keywords:
- ICLRTask2 interface [.NET Framework hosting]
ms.assetid: b5a22ebc-0582-49de-91f9-97a3d9789290
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 518248651de6d8afdf25692c5f48da52b11eb0f7
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59172469"
---
# <a name="iclrtask2-interface"></a>ICLRTask2, interface
Fournit toutes les fonctionnalités de la [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) interface ; en outre, fournit des méthodes qui permettent les abandons de thread pour être retardée sur le thread actuel.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[BeginPreventAsyncAbort, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrtask2-beginpreventasyncabort-method.md)|Nouveau thread de retards interrompre les requêtes sur le thread actuel.|  
|[BeginPreventAsyncAbort, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrtask2-endpreventasyncabort-method.md)|Permet à nouveau ou en attente de demandes d’abandon de thread pour le thread sur abandonnée sur le thread actuel.|  
  
## <a name="remarks"></a>Notes  
 Le `ICLRTask2` interface hérite le `ICLRTask` interface et ajoute des méthodes qui permettent à l’hôte de différer les abandons de thread, pour protéger une région de code qui ne doit pas échouer. Appel `BeginPreventAsyncAbort` incrémente le compteur de délai d’abandon de thread pour le thread actuel et l’appel `EndPreventAsyncAbort` décrémente il. Les appels à `BeginPreventAsyncAbort` et `EndPreventAsyncAbort` peuvent être imbriqués. Tant que le compteur est supérieur à zéro, pour le thread actuel abandons de thread.  
  
 Si les appels à `BeginPreventAsyncAbort` et `EndPreventAsyncAbort` sont ne pas jumelées, il est possible d’atteindre un état dans lequel thread abandons ne peut pas être remis au thread actuel.  
  
 Le délai n’est pas reconnue pour un thread qui abandonne lui-même.  
  
 La fonctionnalité exposée par cette fonctionnalité est utilisée en interne par la machine virtuelle (VM). Une mauvaise utilisation de ces méthodes peut-être provoquer un comportement non spécifié dans la machine virtuelle. Par exemple, l’appel `EndPreventAsyncAbort` sans appeler d’abord `BeginPreventAsyncAbort` Impossible de définir le compteur à zéro lors de la machine virtuelle a précédemment incrémenté. De même, le compteur interne n’est pas vérifié pour dépassement de capacité. S’il dépasse sa limite intégrale, car il est incrémenté par l’hôte et la machine virtuelle, le comportement résultant n’est pas spécifié.  
  
 Pour plus d’informations sur les membres hérités de `ICLRTask` et sur les autres utilisations de cette interface, consultez la [ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md) interface.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICLRTask, interface](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)
- [ICLRTaskManager, interface](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
- [IHostTask, interface](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)
- [IHostTaskManager, interface](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
- [Interfaces d'hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
