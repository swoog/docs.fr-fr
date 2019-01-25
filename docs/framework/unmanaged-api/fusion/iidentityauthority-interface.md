---
title: IIdentityAuthority, interface
ms.date: 03/30/2017
api_name:
- IIdentityAuthority
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IIdentityAuthority
helpviewer_keywords:
- IIdentityAuthority interface [.NET Framework fusion]
ms.assetid: 6277f914-51a8-49be-bec6-52d6d648527d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ab8965ca5d6c9c96cea5f5b351547ce2d4dfacc7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54546278"
---
# <a name="iidentityauthority-interface"></a>IIdentityAuthority, interface
Gère les clés d’identité pour les objets de code.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|`IIdentityAuthority::AreDefinitionsEqual`|Obtient une valeur qui indique si les deux spécifié [IDefinitionIdentity](../../../../docs/framework/unmanaged-api/fusion/idefinitionidentity-interface.md) instances sont égales.|  
|`IIdentityAuthority::AreReferencesEqual`|Obtient une valeur qui indique si les deux spécifié [IReferenceIdentity](../../../../docs/framework/unmanaged-api/fusion/ireferenceidentity-interface.md) instances sont égales.|  
|`IIdentityAuthority::AreTextualDefinitionsEqual`|Obtient une valeur qui indique si les deux représentations sous forme de chaîne spécifiée définition identity sont égaux.|  
|`IIdentityAuthority::AreTextualReferencesEqual`|Obtient une valeur qui indique si les deux représentations d’identité de référence de chaîne spécifié sont égale.|  
|`IIdentityAuthority::CreateDefinition`|Obtient un pointeur vers un nouveau `IDefinitionIdentity` instance qui représente l’objet de code dans la portée actuelle.|  
|`IIdentityAuthority::CreateReference`|Obtient un pointeur vers un nouveau `IReferenceIdentity` instance qui représente l’objet de code dans la portée actuelle.|  
|`IIdentityAuthority::DefinitionToText`|Obtient une version de la chaîne mise en forme de l’objet `IDefinitionIdentity`.|  
|`IIdentityAuthority::DefinitionToTextBuffer`|Remplit la mémoire tampon de caractères larges spécifié avec une version de chaîne de l’objet `IDefinitionIdentity`.|  
|`IIdentityAuthority::DoesDefinitionMatchReference`|Obtient une valeur qui indique si le texte spécifié `IDefinitionIdentity` et `IReferenceIdentity` instances font référence au même objet de code.|  
|`IIdentityAuthority::DoesTextualDefinitionMatchTextualReference`|Obtient une valeur qui indique si les chaînes spécifiées font référence au même objet de code.|  
|`IIdentityAuthority::GenerateDefinitionKey`|Obtient un pointeur vers une clé de chaîne qui vient d’être créée pour spécifié `IDefinitionIdentity`.|  
|`IIdentityAuthority::GenerateReferenceKey`|Obtient un pointeur vers une clé de chaîne qui vient d’être créée pour spécifié `IReferenceIdentity`.|  
|`IIdentityAuthority::HashDefinition`|Obtient une valeur de hachage spécifié `IDefinitionIdentity`.|  
|`IIdentityAuthority::HashReference`|Obtient une valeur de hachage spécifié `IreferenceIdentity`.|  
|`IIdentityAuthority::ReferenceToText`|Obtient une version de la chaîne mise en forme de l’objet `IReferenceIdentity`.|  
|`IIdentityAuthority::ReferenceToTextBuffer`|Remplit la mémoire tampon de caractères larges spécifié avec une version de chaîne de l’objet `IReferenceIdentity`.|  
|`IIdentityAuthority::TextToDefinition`|Obtient un pointeur d’interface vers un `IDefinitionIdentity` instance générée à partir du spécifié au format chaîne.|  
|`IIdentityAuthority::TextToReference`|Obtient un pointeur d’interface vers un `IReferenceIdentity` instance générée à partir du spécifié au format chaîne.|  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Isolation.h  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [Interfaces de fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
