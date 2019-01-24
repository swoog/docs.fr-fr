---
title: IHostAssemblyStore, interface
ms.date: 03/30/2017
api_name:
- IHostAssemblyStore
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostAssemblyStore
helpviewer_keywords:
- IHostAssemblyStore interface [.NET Framework hosting]
ms.assetid: cccb650f-abe0-41e2-9fd1-b383788eb1f6
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d3714f31d0ab58584a8671055cf4c607f04a832c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54611057"
---
# <a name="ihostassemblystore-interface"></a>IHostAssemblyStore, interface
Fournit des méthodes qui permettent à un hôte charger des assemblys et des modules indépendamment le common language runtime (CLR).  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[ProvideAssembly, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-provideassembly-method.md)|Obtient une référence à un assembly qui n’est pas référencé par le [ICLRAssemblyReferenceList](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md) retourné par un appel à [IHostAssemblyManager::GetNonHostStoreAssemblies](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-getnonhoststoreassemblies-method.md).|  
|[ProvideModule, méthode](../../../../docs/framework/unmanaged-api/hosting/ihostassemblystore-providemodule-method.md)|Résout un module dans un assembly ou un fichier de ressources (non incorporé) lié.|  
  
## <a name="remarks"></a>Notes  
 `IHostAssemblyStore` fournit un moyen pour un hôte de charger des assemblys efficacement en fonction de l’identité d’assembly. L’hôte charge les assemblys en retournant `IStream` instances qui pointent directement vers les octets.  
  
 Le CLR détermine si un hôte a implémenté `IHostAssemblyStore` en appelant `IHostAssemblyManager::GetNonHostAssemblyStores` lors de l’initialisation. Cela permet à l’hôte, par exemple, pour contrôler la liaison aux assemblys d’utilisateur, mais s’appuyer sur le runtime pour la liaison aux assemblys .NET Framework.  
  
> [!NOTE]
>  Fournir une implémentation de `IHostAssemblyStore`, l’hôte spécifie son intention de résoudre tous les assemblys qui ne sont pas référencés par le `ICLRAssemblyReferenceList` retourné à partir de `IHostAssemblyManager::GetNonHostStoreAssemblies`.  
  
> [!NOTE]
>  La version 2.0 du .NET Framework ne fournit pas un moyen pour l’hôte de charger l’image native d’un assembly, tel que fourni par le [Native Image Generator (Ngen.exe)](../../../../docs/framework/tools/ngen-exe-native-image-generator.md) utilitaire.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** MSCorEE.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [ICLRAssemblyReferenceList, interface](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)
- [IHostAssemblyManager, interface](../../../../docs/framework/unmanaged-api/hosting/ihostassemblymanager-interface.md)
- [Interfaces d’hébergement](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
