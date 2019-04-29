---
title: IEnumReferenceIdentity, interface
ms.date: 03/30/2017
api_name:
- IEnumReferenceIdentity
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IEnumReferenceIdentity
helpviewer_keywords:
- IEnumReferenceIdentity interface [.NET Framework fusion]
ms.assetid: a17b3155-7216-4e16-8c9f-abce21f549e7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 766b17bae0c58d9872ff9c118f330ebc3220257e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61697249"
---
# <a name="ienumreferenceidentity-interface"></a>IEnumReferenceIdentity, interface
Sert d’énumérateur pour une collection de `IReferenceIdentity` objets.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|`IEnumReferenceIdentity::Clone`|Obtient un pointeur d’interface vers un nouveau `IEnumReferenceIdentity` qui contient les mêmes membres que cela `IEnumReferenceIdentity`.|  
|`IEnumReferenceIdentity::Next`|Obtient le nombre spécifié de `IReferenceIdentity` objets, en commençant à la position actuelle.|  
|`IEnumReferenceIdentity::Reset`|Déplace le pointeur d’instruction au début de ce `IEnumReferenceIdentity`.|  
|`IEnumReferenceIdentity::Skip`|Déplace le pointeur d’instruction par le nombre spécifié d’éléments, en commençant à la position actuelle.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Isolation.h  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
- [IReferenceIdentity, interface](../../../../docs/framework/unmanaged-api/fusion/ireferenceidentity-interface.md)
