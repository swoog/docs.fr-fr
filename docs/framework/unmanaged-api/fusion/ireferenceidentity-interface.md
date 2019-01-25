---
title: IReferenceIdentity, interface
ms.date: 03/30/2017
api_name:
- IReferenceIdentity
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IReferenceIdentity
helpviewer_keywords:
- IReferenceIdentity interface [.NET Framework fusion]
ms.assetid: 9180ac5a-7019-4716-9f83-8a91d157239a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bb8686342b20bd6afe0a4c4803d64428ed95c98b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54665771"
---
# <a name="ireferenceidentity-interface"></a>IReferenceIdentity, interface
Représente une référence à la signature unique d’un objet de code.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|`IReferenceIdentity::Clone`|Obtient un pointeur d’interface vers un nouveau `IReferenceIdentity` instance qui est identique à ce `IReferenceIdentity`, sauf pour les modifications de l’attribut spécifié.|  
|`IReferenceIdentity::EnumAttributes`|Obtient un pointeur d’interface vers un `IEnumIDENTITY_ATTRIBUTE` instance qui contient les attributs associés à ce `IReferenceIdentity`.|  
|`IReferenceIdentity::GetAttribute`|Obtient la valeur de l’attribut dans l’espace de noms spécifié, avec le nom spécifié.|  
|`IReferenceIdentity::SetAttribute`|Définit l’attribut qui a l’espace de noms spécifié et le nom spécifié à la valeur spécifiée.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Isolation.h  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [Interfaces de fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
- [IEnumIDENTITY_ATTRIBUTE, interface](../../../../docs/framework/unmanaged-api/fusion/ienumidentity-attribute-interface.md)
