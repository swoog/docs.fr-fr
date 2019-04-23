---
title: IHostSecurityManager, interface
ms.date: 03/30/2017
api_name:
- IHostSecurityManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSecurityManager
helpviewer_keywords:
- IHostSecurityManager interface [.NET Framework hosting]
ms.assetid: c3be2cbd-2d93-438b-9888-9a0251b63c03
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f45379fe8640ef7e7b3917bac8d10ca956d75ffb
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59223756"
---
# <a name="ihostsecuritymanager-interface"></a>IHostSecurityManager, interface
Fournit des méthodes qui permettent l’accès et contrôle sur le contexte de sécurité du thread en cours d’exécution.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[GetSecurityContext, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-getsecuritycontext-method.md)|Obtient le texte demandé [IHostSecurityContext](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritycontext-interface.md) à partir de l’hôte.|  
|[ImpersonateLoggedOnUser, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-impersonateloggedonuser-method.md)|Les demandes qui code être exécutée en utilisant les informations d’identification de l’utilisateur actuel.|  
|[OpenThreadToken, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-openthreadtoken-method.md)|Ouvre le jeton d’accès discrétionnaire associé au thread actuel.|  
|[RevertToSelf, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-reverttoself-method.md)|Termine l’emprunt d’identité de l’utilisateur actuel et retourne le jeton de thread d’origine.|  
|[SetSecurityContext, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-setsecuritycontext-method.md)|Définit le contexte de sécurité pour le thread en cours d’exécution.|  
|[SetThreadToken, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-setthreadtoken-method.md)|Définit un handle pour le thread en cours d’exécution.|  
  
## <a name="remarks"></a>Notes  
 Un hôte peut contrôler tous les accès de code aux jetons de thread par le common language runtime (CLR) et le code utilisateur. Il peut également garantir que la sécurité complète des informations de contexte sont passées aux opérations asynchrones ou des points de code avec accès restreint au code. `IHostSecurityContext` encapsule ces informations de contexte de sécurité, qui sont opaques pour le CLR.  
  
 Le CLR gère le contexte de thread managé en interne. Elle interroge les processus spécifiques `IHostSecurityManager` dans les situations suivantes :  
  
-   Sur le thread finaliseur, pendant l’exécution du finaliseur.  
  
-   Pendant l’exécution de constructeur de classe et le module.  
  
-   Aux points asynchrones sur le thread de travail, dans les appels à la [IHostThreadPoolManager::QueueUserWorkItem](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-queueuserworkitem-method.md) (méthode).  
  
-   Prise en charge des ports de terminaison d’e/s.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IHostSecurityContext, interface](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritycontext-interface.md)
- [Interfaces d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
