---
title: EClrUnhandledException, énumération
ms.date: 03/30/2017
api_name:
- EClrUnhandledException
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EClrUnhandledException
helpviewer_keywords:
- EClrUnhandledException enumeration [.NET Framework hosting]
ms.assetid: d231044e-2b53-4836-93f9-8117ff0e5c3a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7e5fb3ab1d2dedb220fd4a486409512414233021
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59176668"
---
# <a name="eclrunhandledexception-enumeration"></a>EClrUnhandledException, énumération
Décrit les options disponibles pour la gestion des exceptions qui ne sont pas gérées dans le code utilisateur.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum {  
    eRuntimeDeterminedPolicy,  
    eHostDeterminedPolicy  
} EClrUnhandledException;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`eRuntimeDeterminedPolicy`|Spécifie que le comportement par défaut se produit. Le processus est détruit.|  
|`eHostDeterminedPolicy`|Spécifie que le common language runtime (CLR) ignore les exceptions non gérées et permet à l’hôte de déterminer toute action supplémentaire.|  
  
## <a name="remarks"></a>Notes  
 Pour spécifier que le CLR se comportent comme les versions antérieures, utilisez le `eHostDeterminedPolicy` membre.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** MSCorEE.dll  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [EClrFailure, énumération](../../../../docs/framework/unmanaged-api/hosting/eclrfailure-enumeration.md)
- [EClrOperation, énumération](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md)
- [ICLRPolicyManager, interface](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md)
- [SetUnhandledExceptionPolicy, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setunhandledexceptionpolicy-method.md)
- [IHostPolicyManager, interface](../../../../docs/framework/unmanaged-api/hosting/ihostpolicymanager-interface.md)
- [Énumérations d'hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
