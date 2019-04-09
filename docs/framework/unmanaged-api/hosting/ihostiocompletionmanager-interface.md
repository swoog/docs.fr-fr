---
title: IHostIoCompletionManager, interface
ms.date: 03/30/2017
api_name:
- IHostIoCompletionManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostIoCompletionManager
helpviewer_keywords:
- IHostIoCompletionManager interface [.NET Framework hosting]
ms.assetid: c28d1983-83f7-46e2-990f-dbb9dc07c818
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3c3bebe8eabd4d5fd5faec21e0b0efc408353bc2
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59197267"
---
# <a name="ihostiocompletionmanager-interface"></a>IHostIoCompletionManager, interface
Fournit des méthodes qui permettent le common language runtime (CLR) pour interagir avec les ports de terminaison d’e/s fournis par l’hôte.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[Bind, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-bind-method.md)|Lie un handle à un port de terminaison d’e/s.|  
|[CloseIoCompletionPort, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-closeiocompletionport-method.md)|Ferme un port qui a été créé via un appel antérieur à `CreateIoCompletionPort`.|  
|[CreateIoCompletionPort, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-createiocompletionport-method.md)|Demande que l’hôte crée un nouveau port de terminaison d’e/s.|  
|[GetAvailableThreads, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-getavailablethreads-method.md)|Obtient le nombre de threads de terminaison d’e/s qui ne traitent pas actuellement des demandes.|  
|[GetHostOverlappedSize, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-gethostoverlappedsize-method.md)|Obtient la taille des données personnalisées que l’hôte projette d’ajouter aux demandes d’e/s.|  
|[GetMaxThreads, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-getmaxthreads-method.md)|Obtient le nombre maximal de threads que l’hôte peut allouer pour traiter les demandes d’e/s.|  
|[GetMinThreads, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-getminthreads-method.md)|Obtient le nombre minimal de threads que l’hôte fournit pour traiter les demandes d’e/s.|  
|[InitializeHostOverlapped, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-initializehostoverlapped-method.md)|Fournit à l’hôte d’initialiser des données personnalisées relatives à une demande d’e/s.|  
|[SetCLRIoCompletionManager, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-setclriocompletionmanager-method.md)|Fournit à l’hôte avec un pointeur d’interface vers un [ICLRIoCompletionManager](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-interface.md) instance implémentée par le CLR.|  
|[SetMaxThreads, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-setmaxthreads-method.md)|Définit le nombre maximal de threads plus alloue de l’hôte pour traiter les demandes d’e/s.|  
|[SetMinThreads, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-setminthreads-method.md)|Définit le nombre minimal de threads que l’hôte doit allouer jusqu'à son achèvement d’e/s.|  
  
## <a name="remarks"></a>Notes  
 `IHostIoCompletionManager` correspond à la `ICLRIoCompletionManager` interface implémentée par le CLR. Le CLR appelle les méthodes de `IHostIoCompletionManager` pour lier des handles aux ports qui fournit de l’hôte et l’hôte appelle les méthodes de `ICLRIoCompletionManager` pour signaler l’achèvement de demandes d’e/s.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces d'hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
