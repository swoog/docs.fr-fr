---
title: <transport> de <ws2007HttpBinding>
ms.date: 03/30/2017
ms.assetid: 692befa3-8b0b-4ec5-b601-755874e98eb0
ms.openlocfilehash: b8f84d0ed6c6248e72e3353675c9da96a0678ae6
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55273304"
---
# <a name="transport-of-ws2007httpbinding"></a>\<transport > de \<ws2007HttpBinding >
Définit les paramètres d'authentification correspondant au transport HTTP.  
  
 \<system.serviceModel>  
\<bindings>  
\<ws2007HttpBinding>  
\<binding>  
\<security>  
\<transport>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<transport clientCredentialType="Basic/Certificate/Digest/None/Ntlm/Windows"
           proxyCredentialType="Basic/Digest/None/Ntlm/Windows"
           realm="string" />
```  
  
## <a name="type"></a>Type  
 <xref:System.ServiceModel.HttpTransportSecurity>  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`clientCredentialType`|Spécifie les informations d'identification utilisées pour authentifier le client auprès du service. Cet attribut est de type <xref:System.ServiceModel.HttpClientCredentialType>.|  
|`proxyCredentialType`|Spécifie les informations d'identification utilisées pour authentifier le client auprès d'un proxy de domaine. Cet attribut est de type <xref:System.ServiceModel.HttpProxyCredentialType>.|  
|`realm`|Domaine d'authentification correspondant à l'authentification de base ou Digest. La valeur par défaut est une chaîne vide.<br /><br /> Un domaine d'authentification spécifie au moins le nom de l'hôte qui exécute l'authentification. Il peut également spécifier une collection d'utilisateurs disposant d'un accès. Un utilisateur peut interroger le domaine d'authentification afin de déterminer les noms d'utilisateur et les mots de passe pouvant être utilisés.|  
  
## <a name="clientcredentialtype-attribute"></a>Attribut clientCredentialType  
  
|Valeur|Description|  
|-----------|-----------------|  
|None|La sécurité est désactivée.|  
|Basic|Utilise l'authentification de base.|  
|Digest|Utilise l'authentification Digest.|  
|Ntlm|Utilise l'authentification NTLM comme solution de secours dans un domaine Windows.|  
|Windows|Utilise l'authentification intégrée Windows.|  
|Certificat|Utilise des certificats X.509 pour authentifier le client.|  
  
## <a name="proxycredentialtype-attribute"></a>Attribut proxyCredentialType  
  
|Valeur|Description|  
|-----------|-----------------|  
|None|La sécurité est désactivée.|  
|Basic|Utilise l'authentification de base.|  
|Digest|Utilise l'authentification Digest.|  
|Ntlm|Utilise l'authentification NTLM comme solution de secours dans un domaine Windows.|  
|Windows|Utilise l'authentification intégrée Windows.|  
|Certificat|Utilise des certificats X.509 pour authentifier le client.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<security>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-ws2007httpbinding.md)|Représente les fonctionnalités de sécurité de la [ \<ws2007HttpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/ws2007httpbinding.md) élément.|  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.HttpTransportSecurity>
- <xref:System.ServiceModel.Configuration.BasicHttpSecurityElement.Transport%2A>
- <xref:System.ServiceModel.WSHttpSecurity.Transport%2A>
- <xref:System.ServiceModel.Configuration.WSHttpTransportSecurityElement>
- [Sécurisation des services et des clients](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [Liaisons](../../../../../docs/framework/wcf/bindings.md)
- [Configuration des liaisons fournies par le système](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [Utilisation de liaisons pour configurer des services et des clients](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](../../../../../docs/framework/misc/binding.md)
