---
title: ICorRuntimeHost::GetConfiguration, méthode
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.GetConfiguration
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::GetConfiguration
helpviewer_keywords:
- ICorRuntimeHost::GetConfiguration method [.NET Framework hosting]
- GetConfiguration method [.NET Framework hosting]
ms.assetid: c431617a-b055-44a0-8730-48b7a86d9610
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f435fc71c3b1eb610b57b60a71819a0f835d4189
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57466438"
---
# <a name="icorruntimehostgetconfiguration-method"></a>ICorRuntimeHost::GetConfiguration, méthode
Obtient un objet qui permet à l’hôte spécifier la configuration de rappel du common language runtime (CLR).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetConfiguration(  
    [out] ICorConfiguration** pConfiguration  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pConfiguration`  
 [out] Un pointeur vers l’adresse d’un [ICorConfiguration](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-interface.md) objet qui peut être utilisé pour configurer le CLR.  
  
## <a name="remarks"></a>Notes  
 Le CLR doit être configuré avant son initialisation ; Sinon, le `GetConfiguration` méthode retourne une valeur HRESULT indiquant une erreur.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET framework :** 1.0, 1.1  
  
## <a name="see-also"></a>Voir aussi
- [ICorRuntimeHost, interface](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)
