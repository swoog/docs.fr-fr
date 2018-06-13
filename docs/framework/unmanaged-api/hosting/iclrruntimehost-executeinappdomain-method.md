---
title: ICLRRuntimeHost::ExecuteInAppDomain, méthode
ms.date: 03/30/2017
api_name:
- ICLRRuntimeHost.ExecuteInAppDomain
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeHost::ExecuteInAppDomain
helpviewer_keywords:
- ICLRRuntimeHost::ExecuteInAppDomain method [.NET Framework hosting]
- ExecuteInAppDomain method [.NET Framework hosting]
ms.assetid: e2b0e2db-3fae-4b56-844e-d30a125a660c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 96352ec5eaba67489dbef999925c56475611746c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33435966"
---
# <a name="iclrruntimehostexecuteinappdomain-method"></a>ICLRRuntimeHost::ExecuteInAppDomain, méthode
Spécifie le <xref:System.AppDomain> dans lequel exécuter le code managé spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT ExecuteInAppDomain(  
    [in] DWORD AppDomainId,   
    [in] FExecuteInDomainCallback pCallback,   
    [in] void* cookie  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `AppDomainId`  
 [in] ID numérique de la <xref:System.AppDomain> dans lequel exécuter la méthode spécifiée.  
  
 `pCallback`  
 [in] Un pointeur vers la fonction à exécuter dans le texte spécifié <xref:System.AppDomain>.  
  
 `cookie`  
 [in] Pointeur vers la mémoire allouée par l’appelant opaque. Ce paramètre est passé par le common language runtime (CLR) au rappel de domaine. Il n’est pas mémoire du segment de mémoire gérée par le runtime ; l’allocation et la durée de vie de cette mémoire sont contrôlées par l’appelant.  
  
## <a name="return-value"></a>Valeur de retour  
  
|HRESULT|Description|  
|-------------|-----------------|  
|S_OK|`ExecuteInAppDomain` retourné avec succès.|  
|HOST_E_CLRNOTAVAILABLE|Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.|  
|HOST_E_TIMEOUT|L’appel a expiré.|  
|HOST_E_NOT_OWNER|L’appelant ne possède pas le verrou.|  
|HOST_E_ABANDONED|Un événement a été annulé alors qu’un thread bloqué ou une fibre l’attendait.|  
|E_FAIL|Une défaillance grave et inconnue s’est produite. Si une méthode retourne E_FAIL, le CLR n’est plus utilisable dans le processus. Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.|  
  
## <a name="remarks"></a>Notes  
 `ExecuteInAppDomain` permet à l’hôte d’exercer un contrôle sur lequel gérés <xref:System.AppDomain> la méthode managée spécifiée doit être exécutée dans. Vous pouvez obtenir la valeur d’identificateur d’un domaine d’application, qui correspond à la valeur de la <xref:System.AppDomain.Id%2A> propriété, en appelant [GetCurrentAppDomainId, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-getcurrentappdomainid-method.md).  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [ICLRRuntimeHost, interface](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md)
