---
title: IEnumIDENTITY_ATTRIBUTE, interface
ms.date: 03/30/2017
api_name:
- IEnumIDENTITY_ATTRIBUTE
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IEnumIDENTITY_ATTRIBUTE
helpviewer_keywords:
- IEnumIDENTITY_ATTRIBUTE interface [.NET Framework fusion]
ms.assetid: c2ec2748-e9ae-4e1b-80db-6fcec5cb81a1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d725228f2a7359d415673fdcb90d0cabae1a40be
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59175524"
---
# <a name="ienumidentityattribute-interface"></a>IEnumIDENTITY_ATTRIBUTE, interface
Sert d’énumérateur pour les attributs de l’objet de code dans la portée actuelle.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|`IEnumIDENTITY_ATTRIBUTE::Clone`|Obtient un pointeur d’interface vers un nouveau `IEnumIDENTITY_ATTRIBUTE` qui contient les mêmes membres que cela `IEnumIDENTITY_ATTRIBUTE`.|  
|`IEnumIDENTITY_ATTRIBUTE::CurrentIntoBuffer`|Écrit les données contenues dans les éléments de ce `IEnumIDENTITY_ATTRIBUTE` vers la mémoire tampon de données spécifié.|  
|`IEnumIDENTITY_ATTRIBUTE::Next`|Obtient le nombre spécifié d’attributs, en commençant à la position actuelle.|  
|`IEnumIDENTITY_ATTRIBUTE::Reset`|Déplace le pointeur d’instruction au début de ce `IEnumIDENTITY_ATTRIBUTE`.|  
|`IEnumIDENTITY_ATTRIBUTE::Skip`|Déplace le pointeur d’instruction par le nombre spécifié d’éléments, en commençant à la position actuelle.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Isolation.h  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
