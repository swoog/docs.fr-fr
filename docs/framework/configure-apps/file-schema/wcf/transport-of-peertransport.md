---
title: '&lt;transport&gt; de &lt;peerTransport&gt;'
ms.date: 03/30/2017
ms.assetid: d7116240-845c-4b6f-b203-262de6b597ef
ms.openlocfilehash: d02bb1cb4c20ab7dc482001ea7ce21180394eee7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54716581"
---
# <a name="lttransportgt-of-ltpeertransportgt"></a>&lt;transport&gt; de &lt;peerTransport&gt;
Indique le type de transport correspondant aux messages sécurisés envoyés par des homologues configurés avec cette liaison.  
  
 \<system.serviceModel>  
\<bindings>  
\<customBinding>  
\<binding>  
\<peerTransport>  
\<security>  
\<transport>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<security>
  <transport credentialType="Certificate/Password" />
</security>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|credentialType|Facultatif. Spécifie le type d'informations d'identification utilisé pour vérifier les messages envoyés avec le transport d'homologues. Cet attribut est de type <xref:System.ServiceModel.PeerTransportCredentialType>.|  
  
## <a name="credentialtype-attribute"></a>Attribut credentialType  
  
|Valeur|Description|  
|-----------|-----------------|  
|Certificat|L'authentification du transport de canal homologue requiert un certificat X509.|  
|Mot de passe|L'authentification du transport de canal homologue requiert un mot de passe correct.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<security>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-peertransport.md)|Définit les paramètres de sécurité pour un transport d'homologue.|  
  
## <a name="remarks"></a>Notes  
 Cet élément est défini uniquement si l’attribut de mode de [ \<sécurité >](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-peertransport.md) a la valeur `Transport` ou `TransportWithMessageCredential`.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>
- <xref:System.ServiceModel.PeerSecuritySettings.Transport%2A>
- <xref:System.ServiceModel.PeerTransportSecuritySettings>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [Sécurité de transport](../../../../../docs/framework/wcf/feature-details/transport-security.md)
- [Transports](../../../../../docs/framework/wcf/feature-details/transports.md)
- [Choix d’un transport](../../../../../docs/framework/wcf/feature-details/choosing-a-transport.md)
- [Liaisons](../../../../../docs/framework/wcf/bindings.md)
- [Extension de liaisons](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [Liaisons personnalisées](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [\<customBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
