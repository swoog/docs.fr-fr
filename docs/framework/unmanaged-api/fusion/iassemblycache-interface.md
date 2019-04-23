---
title: IAssemblyCache, interface
ms.date: 03/30/2017
api_name:
- IAssemblyCache
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyCache
helpviewer_keywords:
- IAssemblyCache interface [.NET Framework fusion]
ms.assetid: 71ea170f-872d-4fc5-81b6-27da1dec9b19
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9fc5f3a3d5bc5699a596bcc648a7153190c130f0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59075630"
---
# <a name="iassemblycache-interface"></a>IAssemblyCache, interface
Représente le global assembly cache pour une utilisation par la technologie de fusion.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[CreateAssemblyCacheItem, méthode](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-createassemblycacheitem-method.md)|Obtient une référence à un nouveau [IAssemblyCacheItem](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-interface.md).|  
|[CreateAssemblyScavenger, méthode](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-createassemblyscavenger-method.md)|Réservé à un usage interne par la technologie de fusion.|  
|[InstallAssembly, méthode](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-installassembly-method.md)|Installe l’assembly spécifié dans le global assembly cache.|  
|[QueryAssemblyInfo, méthode](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-queryassemblyinfo-method.md)|Obtient les données demandées sur l’assembly spécifié.|  
|[UninstallAssembly, méthode](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-uninstallassembly-method.md)|Désinstalle l’assembly spécifié du global assembly cache.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Fusion.h  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
- [Global Assembly Cache](../../../../docs/framework/app-domains/gac.md)
