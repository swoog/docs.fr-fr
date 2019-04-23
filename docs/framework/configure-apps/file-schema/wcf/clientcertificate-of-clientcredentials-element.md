---
title: <clientCertificate> de <clientCredentials> élément
ms.date: 03/30/2017
ms.assetid: 3b3fa000-3434-4142-a178-11903bdd2c5d
ms.openlocfilehash: 5abf0a99beff1b9fb3655cb82d74484f3b88237f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59216455"
---
# <a name="clientcertificate-of-clientcredentials-element"></a>\<clientCertificate > de \<clientCredentials > élément
Définit un certificat X.509 utilisé pour authentifier un client à un service.  
  
 \<system.ServiceModel>  
\<behaviors>  
\<endpointBehaviors>  
\<behavior>  
\<clientCredentials>  
\<clientCertificate>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<clientCertificate findValue="String"
                   storeLocation="LocalMachine/CurrentUser"
                   storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"
                   X509FindType="FindByThumbPrint/FindBySubjectName/FindBySubjectDistinguishedName/FindByIssuerName/FindByIssuerDistinguishedName/FindBySerialNumber/FindByTimeValid/FindByTimeNotYetValid/FindByTemplateName/FindByApplicationPolicy/FindByCertificatePolicy/FindByExtension/FindByKeyUsage/FindBySubjectKeyIdentifier" />
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`findValue`|Chaîne qui contient la valeur à rechercher dans le magasin de certificats X.509. Le type contenu dans cet attribut doit répondre aux spécifications de l'attribut `X509FindType` spécifié. La valeur par défaut est une chaîne vide.|  
|`storeLocation`|Indique l'emplacement du certificat X.509 utilisé par le client pour s'authentifier auprès du service. Les valeurs valides sont les suivantes :<br /><br /> -LocalMachine : magasin de certificats assigné à l’ordinateur local.<br />-CurrentUser : magasin de certificats assigné à l’utilisateur actuel.<br /><br /> La valeur par défaut est LocalMachine. Cet attribut est de type <xref:System.Security.Cryptography.X509Certificates.StoreLocation>.|  
|`storeName`|Spécifie le nom du magasin de certificats X.509 dans lequel effectuer la recherche. Les valeurs valides sont les suivantes :<br /><br /> -Carnet d’adresses : Magasin de certificats pour d’autres utilisateurs.<br />-   AuthRoot: Magasin de certificats Autorités de certification (CA).<br />-   CertificateAuthority: Magasin de certificats Autorités de certification intermédiaires (CA).<br />-Interdit : Magasin de certificats pour les certificats révoqués.<br />-Mon : Magasin de certificats pour les certificats personnels.<br />-Racine : Magasin de certificats Autorités de certification racine approuvée (CA).<br />-   TrustedPeople: Magasin de certificats pour les personnes et ressources directement approuvées.<br />-TrustedPublisher : Magasin de certificats pour les éditeurs directement approuvés.<br /><br /> La valeur par défaut est My. Cet attribut est de type <xref:System.Security.Cryptography.X509Certificates.StoreName>.|  
|X509FindType|Définit le type de recherche X.509 à exécuter. Le type contenu dans l'attribut `findValue` doit répondre aux spécifications de cet attribut. Les valeurs valides sont les suivantes :<br /><br /> -   FindByThumbPrint<br />-   FindBySubjectName<br />-   FindBySubjectDistinguishedName<br />-   FindByIssuerName<br />-   FindByIssuerDistinguishedName<br />-   FindBySerialNumber<br />-   FindByTimeValid<br />-   FindByTimeNotYetValid<br />-   FindByTemplateName<br />-   FindByApplicationPolicy<br />-   FindByCertificatePolicy<br />-   FindByExtension<br />-   FindByKeyUsage<br />-   FindBySubjectKeyIdentifier<br /><br /> La valeur par défaut est FindBySubjectDistinguishedName. Cet attribut est de type <xref:System.Security.Cryptography.X509Certificates.X509FindType>.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<clientCredentials>](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md)|Indique les informations d'identification utilisées pour authentifier le client auprès d'un service.|  
  
## <a name="remarks"></a>Notes  
 Cet élément de configuration spécifie le certificat utilisé pour authentifier le client avec cet élément. Pour plus d'informations, voir [Procédure : Renseignez les informations d’identification Client](../../../../../docs/framework/wcf/how-to-specify-client-credential-values.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Configuration.ClientCredentialsElement>
- <xref:System.ServiceModel.Configuration.ClientCredentialsElement.ClientCertificate%2A>
- <xref:System.ServiceModel.Description.ClientCredentials>
- <xref:System.ServiceModel.Description.ClientCredentials.ClientCertificate%2A>
- <xref:System.ServiceModel.Configuration.X509InitiatorCertificateServiceElement>
- <xref:System.ServiceModel.Security.X509CertificateInitiatorClientCredential>
- [Comportements de sécurité](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [Guide pratique pour Renseignez les informations d’identification Client](../../../../../docs/framework/wcf/how-to-specify-client-credential-values.md)
- [Sécurisation des clients](../../../../../docs/framework/wcf/securing-clients.md)
- [Utilisation des certificats](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)
- [Sécurisation des services et des clients](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
