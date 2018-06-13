---
title: '&lt;Entrées&gt;'
ms.date: 03/30/2017
ms.assetid: 202e430c-c1b9-4343-abe2-ac78c181a3b7
ms.openlocfilehash: b9cc7f7736ffefaca68a0f197bd064a99c4dca9a
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32746707"
---
# <a name="ltentriesgt"></a>&lt;Entrées&gt;
Entrée de routage qui contient des mappages entre les filtres de routage et les points de terminaison cibles vers lesquels envoyer des messages lorsque le filtre correspond.  
  
 \<system.serviceModel>  
\<routage >  
\<routingTables >  
\<table >  
\<entrées >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml
   <routing>      <filterTables>        <filterTable name="String">          <entries>            <add backupList="String"                 endpointName="String"                  filterName="String"                  priority="Integer" />          </entries>        </table>      </routingTables></routing>  
```

## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<filtres >](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md)|Mappe un filtre à un point de terminaison client précédemment défini. Les messages correspondant à ce filtre sont envoyés à cette destination.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<routage >](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|Section de configuration qui contient une table de routage.|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Routing.Configuration.RoutingSection?displayProperty=nameWithType>       
 <xref:System.ServiceModel.Routing.Configuration.FilterTableEntryElement?displayProperty=nameWithType>    
