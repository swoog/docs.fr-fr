---
title: EContextType, énumération
ms.date: 03/30/2017
api_name:
- EContextType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EContextType
helpviewer_keywords:
- EContextType enumeration [.NET Framework hosting]
ms.assetid: 92b926a9-b87e-408a-9036-df7b752c9492
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7a261d9164e8714531eab1fe9fc8148304e6d5bb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33432880"
---
# <a name="econtexttype-enumeration"></a>EContextType, énumération
Décrit le contexte de sécurité du thread en cours d’exécution.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum {  
    eCurrentContext    = 0x00,  
    eRestrictedContext = 0x01  
} EContextType;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`eCurrentContext`|Indique le contexte du thread actuel au moment où le common language runtime (CLR) appelle la [IHostSecurityManager::GetSecurityContext](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-getsecuritycontext-method.md) (méthode), ou le contexte demandé par le CLR dans un appel à la [ IHostSecurityManager::SetSecurityContext](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-setsecuritycontext-method.md) (méthode).|  
|`eRestrictedContext`|Indique un contexte sur lequel l’ordinateur hôte possède des privilèges inférieurs, tels que le garbage collector, ou les constructeurs de classe ou module.|  
  
## <a name="remarks"></a>Notes  
 Le CLR fournit l’une de le `EContextType` valeurs comme valeur de paramètre dans les appels à la `IHostSecurityManager::GetSecurityContext` et `IHostSecurityManager::SetSecurityContext` méthodes.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [IHostSecurityContext, interface](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritycontext-interface.md)  
 [IHostSecurityManager, interface](../../../../docs/framework/unmanaged-api/hosting/ihostsecuritymanager-interface.md)  
 [Énumérations d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
