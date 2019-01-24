---
title: '&lt;parameter&gt;'
ms.date: 03/30/2017
ms.assetid: 0fb41e2d-64f7-44ab-993e-05892eac6d82
ms.openlocfilehash: a68fdecaba6ad4e64e4d3a4161d9fef6c099d60a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54690733"
---
# <a name="ltparametergt"></a>&lt;parameter&gt;
Indique le paramètre générique lorsqu'un type déclaré est générique.  
  
 \<system.runtime.serialization>  
\<dataContractSerializer>  
\<declaredTypes > élément  
\<Ajouter > élément pour \<declaredTypes >  
\<knownType > élément  
\<paramètre > élément  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<parameter index="Integer"
           type="String" />
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|index|Lorsque le type déclaré est générique, spécifie le paramètre générique qui renverra le type connu.|  
|type|Chaîne décrivant le type connu utilisé pour la sérialisation et la désérialisation.|  
  
## <a name="index-attribute"></a>Indexer l'Attribut  
  
|Valeur|Description|  
|-----------|-----------------|  
|"0"|Premier paramètre du type générique. Par exemple, <xref:System.Collections.Generic.List%601> dispose d'un seul paramètre. S'il est utilisé comme type déclaré, l'index a la valeur « 0 ».|  
|"1"|Second paramètre d'un type générique. Par exemple, <xref:System.Collections.Generic.Dictionary%602> dispose de deux paramètres. Si le type connu est renvoyé par le second paramètre, affectez à l'attribut d'index la valeur « 1 ».|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<knownType>](../../../../../docs/framework/configure-apps/file-schema/wcf/knowntype.md)|Spécifie un type connu pouvant être renvoyé par un champ ou une propriété du type déclaré.|  
  
## <a name="remarks"></a>Notes  
 Pour plus d’informations sur les types connus, consultez [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) et <xref:System.Runtime.Serialization.DataContractSerializer>.  
  
 Consultez le [ \<dataContractSerializer >](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) pour obtenir un exemple d’utilisation de cet élément.  
  
 Cet élément de configuration ne peut pas contenir les deux attributs simultanément. Si c'est le cas, un <xref:System.Configuration.ConfigurationErrorsException> survient.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Runtime.Serialization.DataContractSerializer>
- [Types connus de contrats de données](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)
- [\<dataContractSerializer>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)
- [\<add>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)
