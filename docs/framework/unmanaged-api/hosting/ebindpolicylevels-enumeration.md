---
title: EBindPolicyLevels, énumération
ms.date: 03/30/2017
api_name:
- EBindPolicyLevels
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EBindPolicyLevels
helpviewer_keywords:
- EBindPolicyLevels enumeration [.NET Framework hosting]
ms.assetid: a9e00b4f-b6d0-4257-bd88-4fe9af97b8fa
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1da1d368725ab0a2334080c1caa7d4e25f5f3bab
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="ebindpolicylevels-enumeration"></a>EBindPolicyLevels, énumération
Fournit des indicateurs pour spécifier le niveau auquel appliquer ou modifier une stratégie de l’assembly.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum {  
    ePolicyLevelNone         = 0x0,  
    ePolicyLevelRetargetable = 0x1,  
    ePolicyUnifiedToCLR      = 0x2,  
    ePolicyLevelApp          = 0x4,  
    ePolicyLevelPublisher    = 0x8,  
    ePolicyLevelHost         = 0x10,  
    ePolicyLevelAdmin        = 0x20  
    ePolicyPortability       = 0x40  
} EBindPolicyLevels;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`ePolicyLevelAdmin`|Spécifie que la stratégie doit être appliquée au niveau de l’administrateur.|  
|`ePolicyLevelApp`|Spécifie que la stratégie doit être appliquée au niveau de l’application.|  
|`ePolicyLevelHost`|Spécifie que la stratégie doit être appliquée au niveau de l’hôte.|  
|`ePolicyLevelNone`|Ne spécifie des indicateurs d’aucun niveau de stratégie.|  
|`ePolicyLevelPublisher`|Spécifie que la stratégie doit être appliquée au niveau du serveur de publication.|  
|`ePolicyLevelRetargetable`|Spécifie que la stratégie doit s’applique à des niveaux variables.|  
|`ePolicyPortability`|Spécifie que stratégie doit prendre en charge la portabilité entre les implémentations d’un assembly .NET Framework. Consultez le [ \<supportPortability >](../../../../docs/framework/configure-apps/file-schema/runtime/supportportability-element.md) élément de fichier de configuration.|  
|`ePolicyUnifiedToCLR`|Spécifie que la stratégie doit être unifiée à celui du common language runtime (CLR).|  
  
## <a name="remarks"></a>Notes  
 Cette énumération est passée aux méthodes de la [ICLRHostBindingPolicyManager](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-interface.md) interface afin de spécifier les modifications dans la stratégie d’application.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** MSCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [ICLRAssemblyIdentityManager, interface](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md)  
 [Énumérations d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
