---
title: <serviceCertificate> de <serviceCredentials>
ms.date: 03/30/2017
ms.assetid: 597ae6d5-4938-4950-9f5e-b2280e816182
ms.openlocfilehash: 086b700b94198aa36e61289178ebbed75d33da98
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59173561"
---
# <a name="servicecertificate-of-servicecredentials"></a>\<serviceCertificate > de \<serviceCredentials >
Spécifiez un certificat X.509 qui sera utilisé pour authentifier le service auprès des clients à l'aide du mode de sécurité Message.  
  
 \<system.ServiceModel>  
\<behaviors>  
\<serviceBehaviors>  
\<behavior>  
\<serviceCredentials>  
\<serviceCertificate>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<serviceCertificate findValue="String"
                    storeLocation="LocalMachine/CurrentUser"
                    storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"
                    x509FindType="FindByThumbprint/FindBySubjectName/FindBySubjectDistinguishedName/FindByIssuerName/FindByIssuerDistinguishedName/FindBySerialNumber/FindByTimeValid/FindByTimeNotYetValid/FindByTemplateName/FindByApplicationPolicy/FindByCertificatePolicy/FindByExtension/FindByKeyUsage/FindBySubjectKeyIdentifier" />
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`findValue`|Chaîne qui contient la valeur à rechercher dans le magasin de certificats X.509. Le type contenu dans l'attribut doit satisfaire les spécifications du X509FindType spécifié. La valeur par défaut est une chaîne vide.|  
|`storeLocation`|Spécifie l'emplacement du magasin de certificats X.509 que le client utilise pour valider le certificat du serveur. Les valeurs valides sont les suivantes :<br /><br /> -LocalMachine : magasin de certificats assigné à l’ordinateur local.<br />-CurrentUser : magasin de certificats assigné à l’utilisateur actuel.<br /><br /> La valeur par défaut est LocalMachine.|  
|`storeName`|Spécifie le nom du magasin de certificats X.509 à ouvrir. Les valeurs valides sont les suivantes :<br /><br /> -Carnet d’adresses : Magasin de certificats pour d’autres utilisateurs.<br />-   AuthRoot: Magasin de certificats Autorités de certification tierce (CA).<br />-   CertificatAuthority: Magasin de certificats Autorités de certification intermédiaires (CA).<br />-Interdit : Magasin de certificats pour les certificats révoqués.<br />-Mon : Magasin de certificats pour les certificats personnels.<br />-Racine : Magasin de certificats Autorités de certification racine approuvée (CA).<br />-   TrustedPeople: Magasin de certificats pour les personnes et ressources directement approuvées.<br />-TrustedPublisher : Magasin de certificats pour les éditeurs directement approuvés.<br /><br /> La valeur par défaut est My.|  
|`x509FindType`|Définit le type de recherche X.509 à exécuter. Les valeurs valides sont les suivantes :<br /><br /> -   FindByThumbprint<br />-   FindBySubjectName<br />-   FindBySubjectDistinguishedName<br />-   FindByIssuerName<br />-   FindByIssuerDistinguishedName<br />-   FindBySerialNumber<br />-   FindByTimeValid<br />-   FindByTimeNotYetValid<br />-   FindByTemplateName<br />-   FindByApplicationPolicy<br />-   FindByCertificatePolicy<br />-   FindByExtension<br />-   FindByKeyUsage<br />-   FindBySubjectKeyIdentifier<br /><br /> Le type contenu dans l'attribut `findValue` doit satisfaire les spécifications du X509FindType spécifié.<br /><br /> La valeur par défaut est FindBySubjectDistinguishedName.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<serviceCredentials>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecredentials.md)|Spécifie l’information d’identification à utiliser pour authentifier le service, ainsi que les paramètres liés à la validation de l’information d’identification du client.|  
  
## <a name="remarks"></a>Notes  
 Cet élément vous permet de spécifier un certificat X.509 qui sera utilisé pour authentifier le service auprès des clients à l'aide du mode de sécurité Message. Si vous utilisez un certificat qui sera périodiquement renouvelé, son empreinte numérique changera. Dans ce cas, utilisez le nom du sujet comme `x509FindType` car le certificat peut être réémis avec le même nom du sujet.  
  
 Pour plus d’informations sur l’utilisation de l’élément, consultez [Comment : Renseignez les informations d’identification Client](../../../../../docs/framework/wcf/how-to-specify-client-credential-values.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Configuration.X509RecipientCertificateServiceElement>
- <xref:System.ServiceModel.Configuration.ServiceCredentialsElement.ServiceCertificate%2A>
- <xref:System.ServiceModel.Security.X509CertificateRecipientServiceCredential>
- <xref:System.ServiceModel.Description.ServiceCredentials.ServiceCertificate%2A>
- [Guide pratique pour Renseignez les informations d’identification Client](../../../../../docs/framework/wcf/how-to-specify-client-credential-values.md)
- [Comportements de sécurité](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
