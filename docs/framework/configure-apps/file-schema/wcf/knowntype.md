---
title: '&lt;knownType&gt;'
ms.date: 03/30/2017
ms.assetid: ee2b7be3-7148-4a3a-b861-48e7330615e5
ms.openlocfilehash: cb36a0d1d1ceb13a6db902904783ee15b14e673b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54541064"
---
# <a name="ltknowntypegt"></a>&lt;knownType&gt;
Indique un type devant être utilisé par le <xref:System.Runtime.Serialization.DataContractSerializer> pendant la désérialisation. L'élément indique un « type connu » renvoyé par un champ ou une propriété d'un « type déclaré ». Pour plus d’informations, consultez [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).  
  
 \<system.runtime.serialization>  
\<dataContractSerializer>  
\<declaredTypes > élément  
\<add> of \<declaredTypes>  
\<knownType > élément  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<knownType type="String">
  <parameter index="Integer"
             type="String" />
</knownType>
```  
  
## <a name="type"></a>Type  
 `string`  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|type|Indique le type (espace de noms compris), le nom de l'assembly, la version, la culture et le jeton de clé publique.|  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<parameter>](../../../../../docs/framework/configure-apps/file-schema/wcf/parameter.md)|Indique un index de paramètre lorsque le type déclaré est générique.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<add>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)|Ajoute un type déclaré à la collection de types déclarés.|  
  
## <a name="remarks"></a>Notes  
 Pour plus d’informations sur les types connus, consultez [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) et <xref:System.Runtime.Serialization.DataContractSerializer>.  
  
 Consultez le [ \<dataContractSerializer >](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) pour obtenir un exemple d’utilisation de cet élément.  
  
## <a name="example"></a>Exemple  
  
```xml  
<add type="MyCompany.Library.Shape,
           MyAssembly, Version=2.0.0.0, Culture=neutral,
           PublicKeyToken=XXXXXX, processorArchitecture=MSIL">
  <knownType type="MyCompany.Library.Circle,
                   MyAssembly, Version=2.0.0.0, Culture=neutral,
                   PublicKeyToken=XXXXXX,
                   processorArchitecture=MSIL"/>
</add>
```  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Runtime.Serialization.DataContractSerializer>
- [Types connus de contrats de données](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)
- [\<dataContractSerializer>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)
- [\<add>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)
