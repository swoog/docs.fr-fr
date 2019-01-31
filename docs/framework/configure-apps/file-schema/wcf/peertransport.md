---
title: <peerTransport>
ms.date: 03/30/2017
ms.assetid: c1a5013a-9dd4-4a27-b114-795b8b323177
ms.openlocfilehash: 8962a0c018442ed590b62e53ea8323d80e334df7
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55290093"
---
# <a name="peertransport"></a>\<peerTransport>
Définit un transport d’homologue pour une liaison personnalisée.  
  
 \<system.serviceModel>  
\<bindings>  
\<customBinding>  
\<binding>  
\<peerTransport>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<peerTransport listenIpAddress="String"
               maxBufferPoolSize="Integer"
               maxReceivedMessageSize="Integer"
               port="Integer">
  <security>
  </security>
</peerTransport>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|listenIpAddress|Chaîne indiquant une adresse IP utilisée par le nœud homologue pour écouter les messages TCP. La valeur par défaut est `null`.|  
|maxBufferPoolSize|Entier positif indiquant la taille maximale du pool de mémoires tampons. La valeur par défaut est 524288.<br /><br /> De nombreux éléments de WCF utilisent des mémoires tampons. La création et la destruction des mémoires tampons à chaque utilisation sont chères, tout comme leur nettoyage. Avec les pools de mémoires tampons, vous pouvez prendre une mémoire tampon du pool, l'utiliser et la retourner au pool une fois que vous avez terminé. Ainsi, la surcharge de la création et de la destruction des mémoires tampons est évitée.|  
|maxReceivedMessageSize|Entier positif définissant la taille maximale du message (en octets, en-têtes compris). L'expéditeur d'un message reçoit une erreur SOAP si ce message est trop volumineux pour le récepteur. Ce dernier abandonne le message et crée une entrée d'événement dans le journal de suivi. La valeur par défaut est 65536.|  
|port|Entier indiquant le port d'interface réseau utilisé par cette liaison pour traiter les messages TCP du canal homologue. Cette valeur doit être comprise entre <xref:System.Net.IPEndPoint.MinPort> et <xref:System.Net.IPEndPoint.MaxPort>. La valeur par défaut est 0.|  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<security>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-peertransport.md)|Définit les paramètres de sécurité correspondant à ce transport. Cet élément est de type <xref:System.ServiceModel.Configuration.PeerSecurityElement>.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<binding>](../../../../../docs/framework/misc/binding.md)|Définit toutes les fonctions de liaison d’une liaison personnalisée.|  
  
## <a name="remarks"></a>Notes  
 Ce transport ne peut pas être utilisé avec les contrats comportant des opérations de demande/réponse.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.Configuration.PeerTransportElement>
- <xref:System.ServiceModel.Channels.PeerTransportBindingElement>
- <xref:System.ServiceModel.Channels.TransportBindingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [Transports](../../../../../docs/framework/wcf/feature-details/transports.md)
- [Choix d’un transport](../../../../../docs/framework/wcf/feature-details/choosing-a-transport.md)
- [Liaisons](../../../../../docs/framework/wcf/bindings.md)
- [Extension de liaisons](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [Liaisons personnalisées](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [\<customBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
