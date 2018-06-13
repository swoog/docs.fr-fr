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
ms.openlocfilehash: 13f60730fedef4876f81f078f811104777050175
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33440253"
---
# <a name="ihostsecuritymanager-interface"></a>IHostSecurityManager, interface
Fournit des méthodes qui permettent l’accès et le contrôle sur le contexte de sécurité du thread en cours d’exécution.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[GetSecurityContext, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-getsecuritycontext-method.md)|Obtient l’élément demandé [IHostSecurityContext](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritycontext-interface.md) à partir de l’ordinateur hôte.|  
|[ImpersonateLoggedOnUser, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-impersonateloggedonuser-method.md)|Les demandes que le code exécuté à l’aide des informations d’identification de l’utilisateur actuel.|  
|[OpenThreadToken, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-openthreadtoken-method.md)|Ouvre le jeton d’accès discrétionnaire associé au thread actuel.|  
|[RevertToSelf, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-reverttoself-method.md)|Met fin à l’emprunt d’identité de l’utilisateur actuel et retourne le jeton de thread d’origine.|  
|[SetSecurityContext, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-setsecuritycontext-method.md)|Définit le contexte de sécurité pour le thread en cours d’exécution.|  
|[SetThreadToken, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-setthreadtoken-method.md)|Définit un handle pour le thread en cours d’exécution.|  
  
## <a name="remarks"></a>Notes  
 Un hôte peut contrôler tous les accès du code aux jetons de threads par le common language runtime (CLR) et le code utilisateur. Il peut également garantir que la sécurité complète les informations de contexte sont passées aux opérations asynchrones ou des points de code avec accès restreint au code. `IHostSecurityContext` encapsule ces informations de contexte de sécurité, qui sont opaques pour le CLR.  
  
 Le CLR gère le contexte de thread managé en interne. Il interroge les processus spécifiques `IHostSecurityManager` dans les situations suivantes :  
  
-   Sur le thread finaliseur, pendant l’exécution du finaliseur.  
  
-   Pendant l’exécution de constructeur de classe et le module.  
  
-   Aux points asynchrones sur le thread de travail, dans les appels à la [IHostThreadPoolManager::QueueUserWorkItem](../../../../docs/framework/unmanaged-api/hosting/ihostthreadpoolmanager-queueuserworkitem-method.md) (méthode).  
  
-   Prise en charge des ports de terminaison d’e/s.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [IHostSecurityContext, interface](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritycontext-interface.md)  
 [Interfaces d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
