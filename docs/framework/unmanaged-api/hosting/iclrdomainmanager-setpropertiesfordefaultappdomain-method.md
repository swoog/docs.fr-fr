---
title: ICLRDomainManager::SetPropertiesForDefaultAppDomain, méthode
ms.date: 03/30/2017
api_name:
- ICLRDomainManager.SetPropertiesForDefaultAppDomain
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRDomainManager::SetPropertiesForDefaultAppDomain
helpviewer_keywords:
- ICLRDomainManager::SetPropertiesForDefaultAppDomain method [.NET Framework hosting]
- SetPropertiesForDefaultAppDomain method [.NET Framework hosting]
ms.assetid: 43e61c4b-c435-45ec-9ef6-c68403aa4200
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 18db77b42af47b76bf1b3b66748d586c4c41dbd7
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33433552"
---
# <a name="iclrdomainmanagersetpropertiesfordefaultappdomain-method"></a>ICLRDomainManager::SetPropertiesForDefaultAppDomain, méthode
Définit les propriétés qui servira à initialiser le domaine d’application par défaut.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT SetPropertiesForDefaultAppDomain(  
    [in] DWORD nProperties,  
    [in] LPCWSTR *pwszPropertyNames,  
    [in] LPCWSTR *pwszPropertyValues  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `nProperties`  
 [in] Le nombre d’entrées dans `pwszPropertyNames` et `pwszPropertyValues`.  
  
 `pwszPropertyNames`  
 [in] Un tableau de noms de propriété, ou null si aucune propriété. Actuellement, le seul nom de propriété reconnu par cette méthode est « PARTIAL_TRUST_VISIBLE_ASSEMBLIES ».  
  
 `pwszPropertyValues`  
 [in] Un tableau de valeurs de propriété, ou null si aucune propriété.  
  
## <a name="return-value"></a>Valeur de retour  
 Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.  
  
|HRESULT|Description|  
|-------------|-----------------|  
|S_OK|La commande s'est correctement terminée.|  
|HRESULT_FROM_WIN32(ERROR_UNKNOWN_PROPERTY)|`pwszPropertyNames` inclut un nom de propriété qui n’est pas reconnu par cette méthode.|  
  
## <a name="remarks"></a>Notes  
 La valeur de propriété pour « PARTIAL_TRUST_VISIBLE_ASSEMBLIES » est une liste d’assemblys qui ont l’attribut conditional <xref:System.Security.AllowPartiallyTrustedCallersAttribute> ) l’attribut APTCA (avec le <xref:System.Security.PartialTrustVisibilityLevel.NotVisibleByDefault?displayProperty=nameWithType> indicateur, qui est rendues visibles aux appelants partiellement approuvés dans l’application par défaut domaine.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MetaHost.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [Hébergement](../../../../docs/framework/unmanaged-api/hosting/index.md)  
 [ICLRDomainManager, interface](../../../../docs/framework/unmanaged-api/hosting/iclrdomainmanager-interface.md)
