---
title: ModuleBindInfo, structure
ms.date: 03/30/2017
api_name:
- ModuleBindInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ModuleBindInfo
helpviewer_keywords:
- ModuleBindInfo structure [.NET Framework hosting]
ms.assetid: 632d4adc-dbc9-4ce8-9397-abc3285c1c69
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f14d3dcaad1cc8cac11599b1647d61df3a793301
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61765178"
---
# <a name="modulebindinfo-structure"></a>ModuleBindInfo, structure
Fournit des informations détaillées sur le module référencé et l’assembly qui le contient.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
typedef struct _ModuleBindInfo {  
    DWORD    dwAppDomainId;  
    LPCWSTR  lpAssemblyIdentity;  
    LPCWSTR  lpModuleName  
} ModuleBindInfo;  
```  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|`dwAppDomainId`|Un identificateur unique pour le `IStream` qui est retourné par un appel à la [IHostAssemblyStore::ProvideModule](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-providemodule-method.md) (méthode) à partir duquel le module référencé doit être chargé.|  
|`lpAssemblyIdentity`|Un identificateur unique pour l’assembly qui contient le module référencé.|  
|`lpModuleName`|Le nom du module référencé.|  
  
## <a name="remarks"></a>Notes  
 `ModuleBindInfo` est passé en tant que paramètre à `IHostAssemblyStore::ProvideModule`. L’hôte fournit l’identificateur unique `dwAppDomainId` pour le common language runtime (CLR). Après un appel à la [IHostAssemblyStore::ProvideAssembly](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-provideassembly-method.md) méthode est retournée, le runtime utilise l’identificateur pour déterminer si le contenu de la `IStream` ont été mappés. Dans ce cas, le runtime charge la copie existante plutôt que de remapper le flux. Le runtime utilise également cet identificateur en tant que clé de recherche pour les flux qui sont retournées à partir des appels à la `IHostAssemblyStore::ProvideAssembly` (méthode). Par conséquent, l’identificateur doit être unique pour les demandes de module, ainsi que pour les demandes de l’assembly.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.idl  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Structures d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-structures.md)
- [AssemblyBindInfo, structure](../../../../docs/framework/unmanaged-api/hosting/assemblybindinfo-structure.md)
- [ICLRAssemblyIdentityManager, interface](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md)
- [ICLRAssemblyReferenceList, interface](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)
- [IHostAssemblyManager, interface](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-interface.md)
