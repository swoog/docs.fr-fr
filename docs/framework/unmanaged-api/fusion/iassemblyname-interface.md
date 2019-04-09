---
title: IAssemblyName, interface
ms.date: 03/30/2017
api_name:
- IAssemblyName
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName
helpviewer_keywords:
- IAssemblyName interface [.NET Framework fusion]
ms.assetid: f7f8e605-6b67-4151-936f-f04ecd671d90
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0d8d59ef282818dd9852d0ff8d2ec2abd40986d0
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59097133"
---
# <a name="iassemblyname-interface"></a>IAssemblyName, interface
Fournit des méthodes pour décrire et travailler avec l’identité unique d’un assembly.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[Clone, méthode](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-clone-method.md)|Crée une copie superficielle de cet `IAssemblyName` objet.|  
|[Finalize, méthode](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-finalize-method.md)|Cela permet `IAssemblyName` objet pour libérer des ressources et effectuer d’autres opérations de nettoyage avant que son destructeur est appelé.|  
|[GetDisplayName, méthode](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-getdisplayname-method.md)|Obtient le nom lisible de l’assembly référencé par ce `IAssemblyName` objet.|  
|[GetName, méthode](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-getname-method.md)|Obtient le nom simple, non chiffré de l’assembly référencé par ce `IAssemblyName` objet.|  
|[GetProperty, méthode](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-getproperty-method.md)|Obtient un pointeur vers la propriété référencée par le `PropertyId`.|  
|[GetVersion, méthode](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-getversion-method.md)|Obtient les informations de version pour l’assembly référencé par ce `IAssemblyName` objet.|  
|[IsEqual, méthode](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-isequal-method.md)|Détermine si une certaine `IAssemblyName` objet est égal à ce `IAssemblyName`, selon les indicateurs de comparaison spécifié.|  
|[SetProperty, méthode](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-setproperty-method.md)|Définit la valeur de la propriété référencée par le `PropertyId`.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Fusion.h  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
- [IAssemblyEnum, interface](../../../../docs/framework/unmanaged-api/fusion/iassemblyenum-interface.md)
