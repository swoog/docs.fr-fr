---
title: '&lt;add&gt; de &lt;backupList&gt;'
ms.date: 03/30/2017
ms.assetid: bc5939fc-314a-4ea4-a533-c96958da7173
ms.openlocfilehash: 7e7361b24c0444b5f3d51a6f5bf079d5eb2dee18
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltaddgt-of-ltbackuplistgt"></a>&lt;add&gt; de &lt;backupList&gt;
Représente un élément de configuration qui définit un élément de point de terminaison de sauvegarde.  
  
 \<system.serviceModel>  
\<routage >  
\<backupLists >  
\<backupList >  
\<add>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
   <routing>  <backupLists>    <backupList name="String">      <add endpointName="String" />    </backupList>    </backupLists></routing>  
```  
  
```csharp  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|name|Chaîne qui spécifie le nom du point de terminaison de sauvegarde.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<routage >](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|Contient une liste de points de terminaison que vous souhaitez que le Service de routage à utiliser au cas où le point de terminaison principal ne peut pas être atteint.|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Routing.Configuration.BackupEndpointElement?displayProperty=nameWithType> 
