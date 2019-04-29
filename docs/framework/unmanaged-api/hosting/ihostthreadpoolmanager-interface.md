---
title: IHostThreadPoolManager, interface
ms.date: 03/30/2017
api_name:
- IHostThreadPoolManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostThreadPoolManager
helpviewer_keywords:
- IHostThreadPoolManager interface [.NET Framework hosting]
ms.assetid: c3a2cd90-7c4e-4374-bb87-b41befb8344f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2e7976740a79efda8e5ab569f2efb55444012c5d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61796567"
---
# <a name="ihostthreadpoolmanager-interface"></a>IHostThreadPoolManager, interface
Fournit des méthodes qui permettent le common language runtime (CLR) pour configurer le pool de threads et en file d’attente des éléments de travail au pool de threads.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[GetAvailableThreads, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-getavailablethreads-method.md)|Obtient le nombre de threads du pool de threads qui ne traitent pas actuellement des éléments de travail.|  
|[GetMaxThreads, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-getmaxthreads-method.md)|Obtient le nombre maximal de threads que l’hôte conserve simultanément dans le pool de threads.|  
|[GetMinThreads, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-getminthreads-method.md)|Obtient le nombre minimal de threads inactifs que l’hôte conserve en prévision des demandes.|  
|[QueueUserWorkItem, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-queueuserworkitem-method.md)|Files d’attente d’une fonction pour l’exécution et fournit un objet contenant les données à utiliser par la fonction.|  
|[SetMaxThreads, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-setmaxthreads-method.md)|Définit le nombre maximal de threads que l’hôte peut gérer dans le pool de threads.|  
|[SetMinThreads, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-setminthreads-method.md)|Définit le nombre minimal de threads inactifs que l’hôte doit gérer en prévision des demandes.|  
  
## <a name="remarks"></a>Notes  
 L’hôte n’est pas nécessaire de configurer le pool de threads en utilisant les valeurs spécifiées dans les appels à la `SetMaxThreads` et `SetMinThreads` méthodes. Dans ce cas, l’hôte doit retourner une valeur HRESULT d’E_NOTIMPL à partir de ces méthodes.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Threading>
- <xref:System.Threading.ThreadPool>
- [Interfaces d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
