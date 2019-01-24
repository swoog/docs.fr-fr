---
title: IAssemblyCacheItem, interface
ms.date: 03/30/2017
api_name:
- IAssemblyCacheItem
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyCacheItem
helpviewer_keywords:
- IAssemblyCacheItem interface [.NET Framework fusion]
ms.assetid: ccc9387a-9f44-4f4f-bf8f-0ea6d2afa21b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d89a531ad09e6865bd9c7dad00c1d8c1840fab8f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54662164"
---
# <a name="iassemblycacheitem-interface"></a>IAssemblyCacheItem, interface
Représente un seul assembly dans le global assembly cache.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[AbortItem, méthode](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-abortitem-method.md)|Permet à l’assembly dans le global assembly cache effectuer des opérations de nettoyage avant qu’il est libéré.|  
|[Commit, méthode](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-commit-method.md)|Valide la référence d’assembly mis en cache dans la mémoire.|  
|[CreateStream, méthode](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-createstream-method.md)|Crée un flux avec le format et le nom spécifié.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Fusion.h  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [Interfaces de fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
- [Global Assembly Cache](../../../../docs/framework/app-domains/gac.md)
- [IAssemblyCache, interface](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-interface.md)
