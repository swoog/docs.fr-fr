---
title: IHostSecurityManager::OpenThreadToken, méthode
ms.date: 03/30/2017
api_name:
- IHostSecurityManager.OpenThreadToken
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSecurityManager::OpenThreadToken
helpviewer_keywords:
- IHostSecurityManager::OpenThreadToken method [.NET Framework hosting]
- OpenThreadToken method [.NET Framework hosting]
ms.assetid: d5999052-8bf0-4a9e-8621-da6284406b18
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 68ebfdcd0ef34edec724a044791d05dd48580b12
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59144558"
---
# <a name="ihostsecuritymanageropenthreadtoken-method"></a>IHostSecurityManager::OpenThreadToken, méthode
Ouvre le jeton d’accès discrétionnaire associé au thread en cours d’exécution.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT OpenThreadToken (  
    [in]  DWORD    dwDesiredAccess,   
    [in]  BOOL     bOpenAsSelf,   
    [out] HANDLE   *phThreadToken  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `dwDesiredAccess`  
 [in] Masque des valeurs d’accès qui spécifient les types demandés d’accès au jeton de thread. Ces valeurs sont définies dans Win32 `OpenThreadToken` (fonction). Les types d’accès demandés sont rapprochées par rapport à la liste de contrôle d’accès discrétionnaire (DACL) pour déterminer quels types d’accès à accorder ou refuser du jeton.  
  
 `bOpenAsSelf`  
 [in] `true` pour spécifier que la vérification d’accès doit être effectuée à l’aide du contexte de sécurité du processus pour le thread appelant ; `false` pour spécifier que la vérification d’accès doit être effectuée à l’aide du contexte de sécurité pour le thread appelant lui-même. Si le thread emprunte un client, le contexte de sécurité peut être celui d’un processus client.  
  
 `phThreadToken`  
 [out] Pointeur vers le jeton d’accès qui vient d’être ouvert.  
  
## <a name="return-value"></a>Valeur de retour  
  
|HRESULT|Description|  
|-------------|-----------------|  
|S_OK|`OpenThreadToken` retourné avec succès.|  
|HOST_E_CLRNOTAVAILABLE|Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.|  
|HOST_E_TIMEOUT|L’appel a expiré.|  
|HOST_E_NOT_OWNER|L’appelant ne possède pas le verrou.|  
|HOST_E_ABANDONED|Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.|  
|E_FAIL|Une défaillance catastrophique inconnue s’est produite. Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus. Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.|  
  
## <a name="remarks"></a>Notes  
 `IHostSecurityManager::OpenThreadToken` se comporte de la même façon pour la fonction Win32 correspondante du même nom, sauf que la fonction Win32 permet à l’appelant de passer un handle à un thread arbitraire, alors que `IHostSecurityManager::OpenThreadToken` s’ouvre uniquement le jeton associé au thread appelant.  
  
 Le `HANDLE` type n’est pas conforme à COM, autrement dit, sa taille est spécifique au système d’exploitation et il requiert le marshaling personnalisé. Par conséquent, ce jeton est utilisé que dans le processus, entre le CLR et l’hôte.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [IHostSecurityContext, interface](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritycontext-interface.md)
- [IHostSecurityManager, interface](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-interface.md)
