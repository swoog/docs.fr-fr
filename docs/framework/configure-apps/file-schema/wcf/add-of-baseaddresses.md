---
title: '&lt;add&gt; de &lt;baseAddress&gt;'
ms.date: 03/30/2017
ms.assetid: 1bd7426f-5f4f-43fc-b8e9-de842219aa32
ms.openlocfilehash: 3f1b7e8f1f4ab8542270d459ce5020ce4320eea9
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltaddgt-of-ltbaseaddressesgt"></a>&lt;add&gt; de &lt;baseAddress&gt;
Représente un élément de configuration qui spécifie les adresses de base utilisées par l'hôte de service.  
  
 \<system.ServiceModel>  
\<client>  
\<point de terminaison >  
\<hôte >  
\<baseAddresses >  
\<baseAddress >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<add baseAddress="string" />  
```  
  
## <a name="type"></a>Type  
 `Type`  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`baseAddress`|Chaîne indiquant une adresse de base utilisée par l'hôte de service.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<baseAddresses >](../../../../../docs/framework/configure-apps/file-schema/wcf/baseaddresses.md)|Collection d'éléments `baseAddress`.|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Configuration.HostElement>  
 <xref:System.ServiceModel.ServiceHost>  
 <xref:System.ServiceModel.ServiceHostBase.BaseAddresses%2A>  
 [Hébergement](../../../../../docs/framework/wcf/feature-details/hosting.md)
