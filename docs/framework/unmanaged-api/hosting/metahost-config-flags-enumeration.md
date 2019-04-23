---
title: METAHOST_CONFIG_FLAGS, énumération
ms.date: 03/30/2017
api_name:
- METAHOST_CONFIG_FLAGS
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- METAHOST_CONFIG_FLAGS
helpviewer_keywords:
- METAHOST_CONFIG_FLAGS enumeration [.NET Framework hosting]
ms.assetid: 6f1e389f-ed99-4d6a-a0ba-72d7d869a01d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6e322f5c7119d13c8a872bd87d00c1e55324b581
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59135772"
---
# <a name="metahostconfigflags-enumeration"></a>METAHOST_CONFIG_FLAGS, énumération
Décrit les indicateurs possibles retournés dans le `pdwConfigFlags` paramètre de la [ICLRMetaHostPolicy::GetRequestedRuntime](../../../../docs/framework/unmanaged-api/hosting/iclrmetahostpolicy-getrequestedruntime-method.md) (méthode), indiquant la présence et le paramètre de la `useLegacyV2RuntimeActivationPolicy` d’attribut dans le [ \<démarrage > élément](../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md) du fichier de configuration.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef enum {  
    METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_UNSET  = 0x00,  
    METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_TRUE   = 0x01,  
    METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_FALSE  = 0x02,  
    METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_MASK   = 0x03  
} METAHOST_CONFIG_FLAGS;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_UNSET`|Le `useLegacyV2RuntimeActivationPolicy` attribut n’était pas présent dans le [ \<démarrage > élément](../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md).|  
|`METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_TRUE`|Le `useLegacyV2RuntimeActivationPolicy` attribut était présent et défini à `true`.|  
|`METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_FALSE`|Le `useLegacyV2RuntimeActivationPolicy` attribut était présent et défini à `false`.|  
|`METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_MASK`|Appliquez ce masque à la valeur retournée dans `pdwConfigFlags` pour obtenir les valeurs pertinentes à `useLegacyV2RuntimeActivationPolicy`.|  
  
## <a name="remarks"></a>Notes  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Metahost.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Énumérations d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
- [GetRequestedRuntime, méthode](../../../../docs/framework/unmanaged-api/hosting/iclrmetahostpolicy-getrequestedruntime-method.md)
- [\<startup>, élément](../../../../docs/framework/configure-apps/file-schema/startup/startup-element.md)
