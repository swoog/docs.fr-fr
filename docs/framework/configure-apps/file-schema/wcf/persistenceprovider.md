---
title: <persistenceProvider>
ms.date: 03/30/2017
ms.assetid: a37049c5-a7ea-4519-94f2-912eeb010380
ms.openlocfilehash: 054991687a54ecbf95cc18f58717a4ed3e36f050
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55260799"
---
# <a name="persistenceprovider"></a>\<persistenceProvider>
Indique le type d'implémentation de fournisseur de persistance à utiliser, ainsi que le délai d'expiration à utiliser pour les opérations de persistance.  
  
 \<system.ServiceModel>  
\<behaviors>  
\<serviceBehaviors>  
\<behavior>  
\<persistenceProvider>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<persistenceProvider persistenceOperationTimeout="TimeSpan"
                     type="String" />
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|persistenceOperationTimeout|Valeur <xref:System.TimeSpan> indiquant le délai d'expiration utilisé pour les opérations de persistance. La valeur par défaut est « 00 : 00:30 ».|  
|type|Chaîne indiquant le type à utiliser pour la fabrique de fournisseurs de persistance.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<behavior>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|Spécifie un élément de comportement.|  
  
## <a name="remarks"></a>Notes  
 Cet élément spécifie le fournisseur de persistance à utiliser pour sérialiser l'état d'un service WCF. Il doit être utilisé avec le `wsHttpContextBinding` qui transmet les informations d'état dans les en-têtes HTTP.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.Configuration.PersistenceProviderElement>
- <xref:System.ServiceModel.Persistence.PersistenceProvider>
