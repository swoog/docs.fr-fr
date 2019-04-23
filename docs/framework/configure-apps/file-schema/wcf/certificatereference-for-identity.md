---
title: <certificateReference> pour <identity>
ms.date: 03/30/2017
ms.assetid: ac359c65-c22d-42d2-97de-db53b77cebdb
ms.openlocfilehash: 3b7779ac00c2fca6300c12ac18ff2d5f6b868424
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59138812"
---
# <a name="certificatereference-for-identity"></a>\<certificateReference > pour \<identité >
Spécifie les paramètres de validation du certificat X.509. Un client Windows Communication Foundation (WCF) sécurisé qui se connecte à un point de terminaison avec cette identité vérifie que les revendications présentées par le serveur contiennent la revendication d’identité utilisée pour construire cette identité.  
  
 \<identity>  
\<certificateReference>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<certificateReference findValue="String"
                      isChainIncluded="Boolean"
                      storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"
                      storeLocation="LocalMachine/CurrentUser"
                      X509FindType="FindByThumbPrint/FindBySubjectName/FindBySubjectDistinguishedName/FindByIssuerName/FindByIssuerDistinguishedName/FindBySerialNumber/FindByTimeValid/FindByTimeNotYetValid/FindByTemplateName/FindByApplicationPolicy/FindByCertificatePolicy/FindByExtension/FindByKeyUsage/FindBySubjectKeyIdentifier">
</certificateReference>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|findValue|Indique la valeur à rechercher dans le magasin de certificats X.509. Le type contenu dans cet attribut doit répondre aux exigences de la valeur `X509FindType` spécifiée. La valeur par défaut est une chaîne vide.|  
|isChainIncluded|Valeur booléenne indiquant si la validation est effectuée à l’aide d’une chaîne de certificats.|  
|storeLocation|Indique l'emplacement du magasin de certificats pouvant être utilisé par le client pour valider le certificat du serveur.<br /><br /> Les valeurs valides sont les suivantes :<br /><br /> -   LocalMachine: Magasin de certificats assigné à l’ordinateur local.<br />-CurrentUser : Magasin de certificats assigné à l’utilisateur actuel.<br /><br /> La valeur par défaut est LocalMachine.<br /><br /> Cet attribut est de type <xref:System.Security.Cryptography.X509Certificates.StoreLocation>.|  
|storeName|Spécifie le nom du magasin de certificats X.509 à ouvrir.<br /><br /> Les valeurs valides sont les suivantes :<br /><br /> -Carnet d’adresses : Magasin de certificats pour d’autres utilisateurs.<br />-   AuthRoot: Magasin de certificats Autorités de certification tierce (CA).<br />-   CertificateAuthority: Magasin de certificats Autorités de certification intermédiaires.<br />-Interdit : Magasin de certificats pour les certificats révoqués.<br />-Mon : Magasin de certificats pour les certificats personnels.<br />-Racine : Magasin de certificats Autorités de certification racines de confiance.<br />-   TrustedPeople: Magasin de certificats pour les personnes et ressources directement approuvées.<br />-TrustedPublisher : Magasin de certificats pour les éditeurs directement approuvés.<br /><br /> La valeur par défaut est My.<br /><br /> Cet attribut est de type <xref:System.Security.Cryptography.X509Certificates.StoreName>.|  
|X509FindType|Indique le type de recherche X.509 à exécuter. Le type contenu dans l'attribut `findValue` doit satisfaire les spécifications du X509FindType spécifié.<br /><br /> Les valeurs valides sont les suivantes :<br /><br /> -   FindByThumbPrint<br />-   FindBySubjectName<br />-   FindBySubjectDistinguishedName<br />-   FindByIssuerName<br />-   FindByIssuerDistinguishedName<br />-   FindBySerialNumber<br />-   FindByTimeValid<br />-   FindByTimeNotYetValid<br />-   FindByTemplateName<br />-   FindByApplicationPolicy<br />-   FindByCertificatePolicy<br />-   FindByExtension<br />-   FindByKeyUsage<br />-   FindBySubjectKeyIdentifier<br /><br /> La valeur par défaut est FindBySubjectDistinguishedName.<br /><br /> Cet attribut est de type <xref:System.Security.Cryptography.X509Certificates.X509FindType>.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<identity>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|Indique les paramètres permettant l'authentification d'un point de terminaison par les autres points de terminaison qui échangent des messages avec lui.|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Configuration.CertificateReferenceElement>
- <xref:System.ServiceModel.Configuration.IdentityElement>
- <xref:System.ServiceModel.EndpointAddress>
- <xref:System.ServiceModel.EndpointAddress.Identity%2A>
