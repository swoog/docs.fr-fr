---
title: <identity>
ms.date: 03/30/2017
ms.assetid: c1d2ae56-e231-4a07-9c3f-9f13381dc0d8
ms.openlocfilehash: 0f5eace346fd0ed2c0532fb602585c4593d97291
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61756687"
---
# <a name="identity"></a>\<identity>
L'élément d'identité autorise un développeur client à spécifier au moment de la conception l'identité attendue du service. Dans le processus de négociation entre le client et le service, l’infrastructure Windows Communication Foundation (WCF) permet de garantir que l’identité du service attendu correspond aux valeurs de cet élément et peut donc être authentifiée. Pour plus d’informations, consultez [identité de Service et d’authentification](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).  
  
 \<system.ServiceModel>  
\<client>  
\<endpoint>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<identity>
  <certificate encodedValue="String" />
  <certificateReference findValue="String"
                        isChainIncluded="Boolean"
                        storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"
                        storeLocation="LocalMachine/CurrentUser"
                        X509FindType="Enumeration" />
  <dns value="String" />
  <rsa value="String" />
  <servicePrincipalName value="String" />
  <usePrincipalName value="String" />
</identity>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|certificat|Spécifie les paramètres d'un certificat X.509. Cet élément est de type <xref:System.ServiceModel.Configuration.CertificateElement>. Il contient un `encodedValue` d'attribut qui est une chaîne indiquant la valeur encodée par ce certificat.|  
|certificateReference|Spécifie les paramètres de validation du certificat X.509. Cet élément est de type <xref:System.ServiceModel.Configuration.CertificateReferenceElement>.|  
|dns|Spécifie le système DNS d'un certificat X.509 utilisé pour authentifier un service. Cet élément contient un attribut `value` qui est une chaîne et qui contient l'identité réelle.|  
|rsa|Indique la valeur du champ RSA d'un certificat X.509 utilisée pour authentifier un service au niveau d'un client. Cet élément contient un attribut `value` qui est une chaîne et qui contient l'identité réelle.|  
|servicePrincipalName|Indique le nom SPN correspondant au nom principal utilisé par un client pour identifier de manière unique l'instance d'un service. Cet élément contient un `value` d'attribut qui est une chaîne contenant le nom principal réel. Cet élément est de type <xref:System.ServiceModel.Configuration.ServicePrincipalNameElement>.|  
|userPrincipalName|Spécifie une identité UPN correspondant au type de nom de connexion d'un utilisateur sur un réseau. Le nom d’utilisateur principal se compose du nom d’objet utilisateur utilisé dans Active Directory, suivi par le symbole at (\@) et puis, en règle générale, le système de nom de domaine parent. Par exemple, Jeff dans l’arborescence de domaine Fabrikam.com peut avoir le nom d’utilisateur principal [ jeff@fabrikam.com ](mailto:jeffsmith@fabrikam.com).  Cet élément contient un `value` d'attribut qui est une chaîne contenant le nom principal réel. Cet élément est de type <xref:System.ServiceModel.Configuration.UserPrincipalNameElement>.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<custom>](../../../../../docs/framework/configure-apps/file-schema/wcf/custom.md)|Indique le programme de résolution d'homologue personnalisé pour un netPeerTcpBinding.|  
|[\<endpoint>](endpoint-element.md)|Configure les points de terminaison de service.|  
|[\<point de terminaison > de \<client >](endpoint-of-client.md)|Configure les points de terminaison de canal.|  
|[\<issuer>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuer.md)|Spécifie le service STS pour le service fédéré.|  
|[\<issuerMetadata>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuermetadata.md)|Spécifie le point de terminaison de métadonnées pour le service STS d'un service fédéré.|  
|[\<issuedTokenParameters>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtokenparameters.md)|Définit des paramètres correspondant à un jeton émis dans une liaison personnalisée.|  
|[\<localIssuer>](../../../../../docs/framework/configure-apps/file-schema/wcf/localissuer.md)|Spécifie un service STS local.|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Configuration.IdentityElement>
- <xref:System.ServiceModel.EndpointAddress>
- <xref:System.ServiceModel.EndpointAddress.Identity%2A>
- [Identité du service et authentification](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [Points de terminaison : Adresses, liaisons et contrats](../../../../../docs/framework/wcf/feature-details/endpoints-addresses-bindings-and-contracts.md)
