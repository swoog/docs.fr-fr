---
title: Élément <certificate>
ms.date: 03/30/2017
ms.assetid: 9b3d9233-ef35-477a-bf5d-efd1e80a52f4
ms.openlocfilehash: b53a0328ed1fcbae03e8844ccca64e949db44e7e
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55254546"
---
# <a name="certificate-element"></a>\<certificat > élément
Spécifie un certificat X.509 à utiliser pour signer et chiffrer des messages pour les clients de réseau pair à pair.  
  
 \<system.ServiceModel>  
\<behaviors>  
\<endpointBehaviors>  
\<behavior>  
\<clientCredentials>  
\<peer>  
\<certificate>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<certificate findValue="String"
             storeLocation="LocalMachine/CurrentUser"
             storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"
             X509FindType="FindByThumbPrint/FindBySubjectName/FindBySubjectDistinguishedName/FindByIssuerName/FindByIssuerDistinguishedName/FindBySerialNumber/FindByTimeValid/FindByTimeNotYetValid/FindByTemplateName/FindByApplicationPolicy/FindByCertificatePolicy/FindByExtension/FindByKeyUsage/FindBySubjectKeyIdentifier" />
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`findValue`|Chaîne qui contient la valeur à rechercher dans le magasin de certificats X.509. Le type contenu dans l'attribut doit répondre aux spécifications du `x509FindType` spécifié. La valeur par défaut est une chaîne vide.|  
|`storeLocation`|Indique l'emplacement du magasin de certificats X.509 utilisé par le client pour valider le certificat de l'homologue. Les valeurs valides sont les suivantes :<br /><br /> -LocalMachine : magasin de certificats assigné à l’ordinateur local.<br />-CurrentUser : magasin de certificats assigné à l’utilisateur actuel.<br /><br /> La valeur par défaut est LocalMachine.|  
|`storeName`|Spécifie le nom du magasin de certificats X.509 à ouvrir. Les valeurs valides sont les suivantes :<br /><br /> -Carnet d’adresses : Magasin de certificats pour d’autres utilisateurs.<br />-   AuthRoot: Magasin de certificats Autorités de certification tierce (CA).<br />-   CertificateAuthority: Magasin de certificats Autorités de certification intermédiaires (CA).<br />-Interdit : Magasin de certificats pour les certificats révoqués.<br />-Mon : Magasin de certificats pour les certificats personnels.<br />-Racine : Magasin de certificats Autorités de certification racine approuvée (CA).<br />-   TrustedPeople: Magasin de certificats pour les personnes directement approuvés et des ressources.<br />-TrustedPublisher : Magasin de certificats pour les éditeurs directement approuvés.<br /><br /> La valeur par défaut est My.|  
|`X509FindType`|Définit le type de recherche X.509 à exécuter. Les valeurs valides sont les suivantes :<br /><br /> -   FindByThumbPrint<br />-   FindBySubjectName<br />-   FindBySubjectDistinguishedName<br />-   FindByIssuerName<br />-   FindByIssuerDistinguishedName<br />-   FindBySerialNumber<br />-   FindByTimeValid<br />-   FindByTimeNotYetValid<br />-   FindByTemplateName<br />-   FindByApplicationPolicy<br />-   FindByCertificatePolicy<br />-   FindByExtension<br />-   FindByKeyUsage<br />-   FindBySubjectKeyIdentifier<br /><br /> Le type contenu dans l’attribut `findValue` doit répondre aux exigences du `X509FindType` spécifié.<br /><br /> La valeur par défaut est FindBySubjectDistinguishedName.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<peer>](../../../../../docs/framework/configure-apps/file-schema/wcf/peer-of-clientcredentials-element.md)|Spécifie les informations d'identification utilisées lors de l'authentification de clients de réseau pair à pair.|  
  
## <a name="remarks"></a>Notes  
 Cet élément de configuration contient une instance de X509Certificate2 utilisée lors de l'authentification de voisins dans la maille d'homologues.  
  
 Pour plus d’informations sur la programmation de peer-to-peer, consultez [mise en réseau Peer-to-Peer](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md).  
  
## <a name="example"></a>Exemple  
 Le code suivant spécifie comment rechercher le certificat utilisé dans un scénario de réseau pair à pair.  
  
```xml  
<behaviors>
  <endpointBehaviors>
    <behavior name="MyEndpointBehavior">
      <clientCredentials>
        <peer>
          <certificate findValue="www.contoso.com"
                       storeLocation="LocalMachine"
                       x509FindType="FindByIssuerName" />
        </peer>
      </clientCredentials>
    </behavior>
  </endpointBehaviors>
</behaviors>
```  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.Configuration.PeerCredentialElement>
- <xref:System.ServiceModel.Configuration.PeerCredentialElement.Certificate%2A>
- <xref:System.ServiceModel.Configuration.X509PeerCertificateElement>
- <xref:System.ServiceModel.Security.PeerCredential.Certificate%2A>
- [Utilisation des certificats](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)
- [Réseaux homologues](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md)
- [Authentification de Message de canal homologue](https://msdn.microsoft.com/library/80e73386-514e-4c30-9e4a-b9ca8c173a95)
- [Authentification personnalisée de canal homologue](https://msdn.microsoft.com/library/4aa8a82e-41a8-48e2-8621-7e1cbabdca7c)
- [Sécurisation des applications de canal homologue](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md)
