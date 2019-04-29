---
title: IDefinitionIdentity, interface
ms.date: 03/30/2017
api_name:
- IDefinitionIdentity
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IDefinitionIdentity
helpviewer_keywords:
- IDefinitionIdentity interface [.NET Framework fusion]
ms.assetid: ce5ba888-5fbe-4efd-91cf-f0ff94d8428b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4ff23330f307c10eac134048de39a6e19a67c75b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61697535"
---
# <a name="idefinitionidentity-interface"></a>IDefinitionIdentity, interface
Représente la signature unique du code qui définit l’application dans la portée actuelle.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|`IDefinitionIdentity::Clone`|Obtient un pointeur d’interface vers un nouveau `IDefinitionIdentity` objet qui est identique à ce `IDefinitionIdentity`, sauf pour les modifications de l’attribut spécifié.|  
|`IDefinitionIdentity::EnumAttributes`|Obtient un pointeur d’interface vers un [IEnumIDENTITY_ATTRIBUTE](../../../../docs/framework/unmanaged-api/fusion/ienumidentity-attribute-interface.md) objet qui contient les attributs associés à ce `IDefinitionIdentity`.|  
|`IDefinitionIdentity::GetAttribute`|Obtient la valeur de l’attribut avec le nom spécifié dans l’espace de noms spécifié.|  
|`IDefinitionIdentity::SetAttribute`|Définit l’attribut ayant le nom spécifié dans l’espace de noms spécifié à la valeur spécifiée.|  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Isolation.h  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
