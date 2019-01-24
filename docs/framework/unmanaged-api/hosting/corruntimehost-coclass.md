---
title: CorRuntimeHost, coclasse
ms.date: 03/30/2017
api_name:
- CorRuntimeHost Coclass
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorRuntimeHost
helpviewer_keywords:
- CoRuntimeHost coclass [.NET Framework hosting]
ms.assetid: 5833740b-7d67-44b4-865c-b5bf45e291e3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7c81a39acee31986421c810e2814a4f7e6c4d970
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54597526"
---
# <a name="corruntimehost-coclass"></a>CorRuntimeHost, coclasse
Fournit des interfaces pour la gestion des applications qui sont en cours d’exécution par le common language runtime.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
coclass CorRuntimeHost {  
    [default] interface ICorRuntimeHost;  
    interface IGCHost;  
    interface ICorConfiguration;  
    interface IValidator;  
    interface IDebuggerInfo;  
};  
```  
  
## <a name="interfaces"></a>Interfaces  
  
|Interface|Description|  
|---------------|-----------------|  
|[ICorConfiguration, interface](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-interface.md)|Fournit des méthodes pour configurer le common language runtime (CLR).|  
|[ICorRuntimeHost, interface](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)|Fournit des méthodes qui permettent à l’hôte démarrer et arrêter le common language runtime explicitement, pour créer et configurer des domaines d’application, pour accéder au domaine par défaut et d’énumérer tous les domaines en cours d’exécution dans le processus.|  
|[IDebuggerInfo, interface](../../../../docs/framework/unmanaged-api/hosting/idebuggerinfo-interface.md)|Fournit des méthodes pour obtenir des informations sur l’état des services de débogage.|  
|[IGCHost, interface](../../../../docs/framework/unmanaged-api/hosting/igchost-interface.md)|Fournit des méthodes pour obtenir des informations sur le système de garbage collection et contrôler certains aspects du garbage collection.|  
|« IValidator »|Fournit des méthodes pour la validation d’images exécutables portables et des rapports détaillés d’erreurs de validation.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.idl  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [Coclasses d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-coclasses.md)
