---
title: IReferenceAppId, interface
ms.date: 03/30/2017
api_name:
- IReferenceAppId
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IReferenceAppId
helpviewer_keywords:
- IReferenceAppId interface [.NET Framework fusion]
ms.assetid: 8eb9e565-f358-43ce-900e-a8f8a5aa6cfb
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2289a9a75311c9642a764844ee466adcc5838655
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54744347"
---
# <a name="ireferenceappid-interface"></a>IReferenceAppId, interface
Représente une référence à l’identificateur unique pour l’application dans la portée actuelle.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|`IReferenceAppId::get_CodeBase`|Obtient un pointeur vers une représentation sous forme de chaîne de l’identificateur de code de l’application référencée par ce `IReferenceAppId`.|  
|`IReferenceAppId::put_CodeBase`|Définit l’identificateur de code de l’application référencée par ce `IReferenceAppId`.|  
|`IReferenceAppId::EnumAppPath`|Obtient un pointeur d’interface vers un `IEnumReferenceIdentity` instance contenant le `IReferenceIdentity` instances qui représentent les membres de ce `IReferenceAppId`.|  
|`IReferenceAppId::get_SubscriptionId`|Obtient un pointeur vers une représentation sous forme de chaîne de l’identificateur de jeton pour un abonnement à ce `IReferenceAppId`.|  
|`IReferenceAppId::put_SubscriptionId`|Définit l’identificateur de jeton pour un abonnement à ce `IReferenceAppId` à la valeur de chaîne spécifiée.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Isolation.h  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [Interfaces de fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
- [IEnumReferenceIdentity, interface](../../../../docs/framework/unmanaged-api/fusion/ienumreferenceidentity-interface.md)
- [IReferenceIdentity, interface](../../../../docs/framework/unmanaged-api/fusion/ireferenceidentity-interface.md)
