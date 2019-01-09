---
title: '&lt;add&gt; de &lt;namespaceTable&gt;'
ms.date: 03/30/2017
ms.assetid: cf7b5b75-63bd-49a6-abac-4bfdab377e36
ms.openlocfilehash: ef4f1c46a0ee3b94e5548b752e4e0a6a759fd45b
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54149512"
---
# <a name="ltaddgt-of-ltnamespacetablegt"></a>&lt;add&gt; de &lt;namespaceTable&gt;
Représente un élément de configuration qui contient un mappage espace de noms-préfixe à utiliser dans des filtres XPath pour le routage.  
  
 \<system.serviceModel>  
\<routage >  
\<namespaceTable >  
\<add>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<routing>
  <namespaceTable>
    <add namespace="String"
         prefix="String" />
  </namespaceTable>
</routing>
```  
  
```csharp  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|namespace|Chaîne qui contient l'espace de noms.|  
|prefix|Chaîne qui contient le préfixe de cet espace de noms.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<namespaceTable >](../../../../../docs/framework/configure-apps/file-schema/wcf/namespacetable.md)|Représente une section de configuration qui permet de définir un ensemble d’éléments contenant des mappages espace de noms-préfixe qui peuvent ensuite être utilisés dans des filtres XPath pour le routage.|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Routing.Configuration.NamespaceElement?displayProperty=nameWithType>    
