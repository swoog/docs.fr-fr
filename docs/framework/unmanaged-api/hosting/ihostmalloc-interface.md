---
title: IHostMalloc, interface
ms.date: 03/30/2017
api_name:
- IHostMAlloc
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMAlloc
helpviewer_keywords:
- IHostMAlloc interface [.NET Framework hosting]
ms.assetid: e3c6643b-6fc7-4a99-959d-4b7b4e63fdee
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f2a7a29ef1dc85c2ad554995286e5137fcb104be
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59136407"
---
# <a name="ihostmalloc-interface"></a>IHostMalloc, interface
Fournit des méthodes qui permettent le common language runtime (CLR) pour demander des allocations fines à partir du tas via l’hôte.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[Alloc, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostmalloc-alloc-method.md)|Demande que l’hôte alloue la quantité de mémoire demandée à partir du tas.|  
|[DebugAlloc, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostmalloc-debugalloc-method.md)|Demande que l’hôte alloue la quantité de mémoire demandée à partir du tas et en outre suivre où la mémoire a été allouée.|  
|[Free, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostmalloc-free-method.md)|Libère la mémoire qui a été alloué à l’aide de la `Alloc` (méthode).|  
  
## <a name="remarks"></a>Notes  
 Le CLR obtient un pointeur d’interface vers un `IHostMalloc` instance en appelant le [IHostMemoryManager::CreateMalloc](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-createmalloc-method.md) (méthode).  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IHostMemoryManager, interface](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md)
- [Interfaces d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
