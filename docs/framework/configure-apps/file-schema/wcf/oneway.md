---
title: '&lt;oneWay&gt;'
ms.date: 03/30/2017
ms.assetid: 00e67e0e-77c0-4695-9138-c0997b0e5f3c
ms.openlocfilehash: f9a5631501b3879463606f526485314efd5eff2b
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltonewaygt"></a>&lt;oneWay&gt;
Active le routage de paquets et l’utilisation de méthodes unidirectionnelles pour une liaison personnalisée.  
  
 \<system.serviceModel>  
\<liaisons >  
\<customBinding >  
\<liaison >  
\<oneWay >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<oneWay packetRoutable="Boolean">  
        <channelPoolSettings  
           idleTimeout"TimeSpan"  
          leaseTimeout"TimeSpan"  
          maxOutboundConnectionsPerEndpopint="Integer" />  
```  
  
```xml  
</oneWay>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`packetRoutable`|Valeur booléenne qui spécifie si le routage de paquets est activé. La valeur par défaut est `false`.|  
|`MaxAcceptedChannels`|Entier qui spécifie le nombre maximal de canaux qui peuvent être acceptés.|  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<channelPoolSettings >](../../../../../docs/framework/configure-apps/file-schema/wcf/channelpoolsettings.md)|Objet <xref:System.ServiceModel.Configuration.ChannelPoolSettingsElement> qui contient des propriétés du pool de canaux pour le canal actuel.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<liaison >](../../../../../docs/framework/misc/binding.md)|Définit toutes les fonctions de liaison d’une liaison personnalisée.|  
  
## <a name="remarks"></a>Notes  
 Pour activer le routage de paquets, une couche de conversion unidirectionnelle est nécessaire (fournie par cet élément). Un utilisateur peut créer une liaison personnalisée qui crée une couche pour cette liaison via un transport prenant en charge la session ou de type demande/réponse pour qu'elle puisse router les paquets. Cet élément s'avère également utile lorsque vous souhaitez exposer des méthodes unidirectionnelles de façon plus native. D'autres transformations peuvent être appliquées sur cette couche, comme le duplex composite et la messagerie fiable.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Channels.OneWayBindingElement>  
 <xref:System.ServiceModel.Configuration.OneWayElement>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 [Liaisons](../../../../../docs/framework/wcf/bindings.md)  
 [Extension de liaisons](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [Liaisons personnalisées](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [\<customBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
