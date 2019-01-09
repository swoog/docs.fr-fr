---
title: '&lt;add&gt; de &lt;transportConfigurationType&gt;'
ms.date: 03/30/2017
ms.assetid: 03d79db9-571d-4534-acef-d05e5467b257
ms.openlocfilehash: 1079b25ce137dc89fc31f46a11f3720486462021
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54149135"
---
# <a name="ltaddgt-of-lttransportconfigurationtypegt"></a>&lt;add&gt; de &lt;transportConfigurationType&gt;
Cet élément est une paire clé/valeur, qui identifie le type d'un transport particulier.  
  
 \<system.ServiceModel>  
\<serviceHostingEnvironment >  
\<transportConfigurationTypes >  
\<add>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<serviceHostingEnvironment>
  <transportConfigurationTypes>
    <add name="String"
         transportConfigurationType="String" />
  </transportConfigurationTypes>
</serviceHostingEnvironment>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|name|Attribut de chaîne requis.<br /><br /> Contient une clé définie par l'utilisateur qui identifie uniquement le type de transport.|  
|transportConfigurationType|Chaîne contenant le type qui implémente le transport spécifique.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<transportConfigurationTypes >](../../../../../docs/framework/configure-apps/file-schema/wcf/transportconfigurationtypes.md)|Collection de types implémentant le transport spécifique.|  
  
## <a name="example"></a>Exemple  
  
```xml  
<serviceHostingEnvironment>
  <transportConfigurationTypes>
    <add name="net.udp"
         transportConfigurationType="Microsoft.ServiceModel.Samples.Hosting.HostedUdpTransportConfiguration, UdpActivation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=6fa904d2da1848d6" />
  </transportConfigurationTypes>
</serviceHostingEnvironment>
```  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Configuration.TransportConfigurationTypeElement>  
 <xref:System.ServiceModel.Configuration.ServiceHostingEnvironmentSection>  
 <xref:System.ServiceModel.ServiceHostingEnvironment>  
 [Hébergement](../../../../../docs/framework/wcf/feature-details/hosting.md)
