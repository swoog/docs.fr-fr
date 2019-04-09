---
title: IGCHost2, interface
ms.date: 03/30/2017
api_name:
- IGCHost2
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IGCHost2
helpviewer_keywords:
- IGCHost2 interface [.NET Framework hosting]
ms.assetid: e5323fa4-18ac-424d-859d-a65a550d08d9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 75bef91eb70c8109653741452362cd2e85f625ce
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59138136"
---
# <a name="igchost2-interface"></a>IGCHost2, interface
Fournit des méthodes pour obtenir des informations sur le système de garbage collection et contrôler certains aspects du garbage collection.  
  
> [!NOTE]
>  Pour tout nouveau développement, nous vous recommandons d’utiliser le [ICLRGCManager2](../../../../docs/framework/unmanaged-api/hosting/iclrgcmanager2-interface.md) à la place de l’interface.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[SetGCStartupLimitsEx, méthode](../../../../docs/framework/unmanaged-api/hosting/igchost2-setgcstartuplimitsex-method.md)|Définit la taille du segment et la taille maximale pour la génération 0. Permet la génération 0 et les tailles de segment supérieures à `DWORD`.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** GCHost.idl, GCHost.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces d'hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [Interfaces d'hébergement du CLR](../../../../docs/framework/unmanaged-api/hosting/clr-hosting-interfaces.md)
- [CorRuntimeHost, coclasse](../../../../docs/framework/unmanaged-api/hosting/corruntimehost-coclass.md)
