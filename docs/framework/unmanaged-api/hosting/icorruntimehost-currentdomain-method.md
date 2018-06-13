---
title: ICorRuntimeHost::CurrentDomain, méthode
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.CurrentDomain
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::CurrentDomain
helpviewer_keywords:
- ICorRuntimeHost::CreateDomain method [.NET Framework hosting]
- CurrentDomain method [.NET Framework hosting]
ms.assetid: dd2afb38-675b-4c3c-a9f3-8ab3b133eb02
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 96cda3f504910d8fb70905f66b45f417158c505d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33436843"
---
# <a name="icorruntimehostcurrentdomain-method"></a>ICorRuntimeHost::CurrentDomain, méthode
Obtient un pointeur d’interface de type <xref:System.AppDomain?displayProperty=nameWithType> qui représente le domaine chargé sur le thread actuel.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT CurrentDomain (  
    [out] IUnknown** pAppDomain  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `pAppDomain`  
 [out] Un pointeur de type <xref:System.AppDomain?displayProperty=nameWithType> qui représente le domaine d’application actuel du thread. Ce pointeur est tapé `IUnknown`, de sorte que les appelants doivent généralement appeler `QueryInterface` pour obtenir un pointeur de type <xref:System._AppDomain>.  
  
## <a name="return-value"></a>Valeur de retour  
  
|HRESULT|Description|  
|-------------|-----------------|  
|S_OK|L’opération a réussi.|  
|S_FALSE|L’opération a échoué.|  
|E_FAIL|Une défaillance grave et inconnue s’est produite. Si une méthode retourne E_FAIL, le common language runtime (CLR) n’est plus utilisable dans le processus. Les appels suivants à toute API d’hébergement retournent HOST_E_CLRNOTAVAILABLE.|  
|HOST_E_CLRNOTAVAILABLE|Le CLR n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter du code managé ou traiter l’appel avec succès.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** 1.0, 1.1  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System._AppDomain>  
 <xref:System.AppDomain>  
 [ICorRuntimeHost, interface](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)
