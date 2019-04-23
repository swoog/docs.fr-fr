---
title: <clientCertificate> de <serviceCredentials>
ms.date: 03/30/2017
ms.assetid: 90ad03aa-2317-43dd-8a72-6d24cdcad15c
ms.openlocfilehash: 26ebac6439a90959e3a926e6a36c9044251a4aae
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59107982"
---
# <a name="clientcertificate-of-servicecredentials"></a>\<clientCertificate> of \<serviceCredentials>
Définit un certificat X.509 permettant de signer et de chiffrer des messages destinés à un client et envoyés à partir d'un service selon un modèle de communication duplex.  
  
 \<system.ServiceModel>  
\<behaviors>  
\<serviceBehaviors>  
\<serviceBehaviors>  
\<behavior>  
\<serviceCredentials>  
\<clientCertificate>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<clientCertificate>
  <certificate />
  <authentication />
</clientCertificate>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<authentication>](../../../../../docs/framework/configure-apps/file-schema/wcf/authentication-of-clientcertificate-element.md)|Spécifie des options d'authentification pour le certificat client.|  
|[\<certificate>](../../../../../docs/framework/configure-apps/file-schema/wcf/certificate-of-clientcertificate-element.md)|Spécifie le certificat à utiliser.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<serviceCredentials>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecredentials.md)|Spécifie les informations d’identification à utiliser pour authentifier le service, ainsi que les paramètres liés à la validation des informations d’identification du client.|  
  
## <a name="remarks"></a>Notes  
 Cet élément est utilisé lorsque le service doit disposer du certificat du client à l'avance afin de communiquer de manière sécurisée avec le client. Cela se produit lors de l'utilisation du modèle de communication duplex. Dans le modèle demande-réponse classique, le client inclut son certificat dans la demande que le service utilise pour sécuriser à nouveau sa réponse au client. Dans le modèle de communication duplex, toutefois, le service ne dispose pas de demande du client et, par conséquent, requiert le certificat du client à l'avance pour sécuriser l'envoi du message au client. C'est pourquoi vous devez obtenir le certificat du client dans une négociation hors bande et l'indiquer à l'aide de cet élément. Pour plus d’informations sur les services duplex, consultez [Comment : Créer un contrat Duplex](../../../../../docs/framework/wcf/feature-details/how-to-create-a-duplex-contract.md).  
  
 Le certificat défini dans cet élément est utilisé pour chiffrer les messages au client uniquement pour les liaisons configurées avec le mode d’authentification de sécurité des messages `MutualCertificateDuplex`.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Configuration.X509InitiatorCertificateServiceElement>
- <xref:System.ServiceModel.Configuration.ServiceCredentialsElement.ClientCertificate%2A>
- <xref:System.ServiceModel.Configuration.X509InitiatorCertificateServiceElement>
- <xref:System.ServiceModel.Description.ServiceCredentials.ClientCertificate%2A>
- <xref:System.ServiceModel.Security.X509CertificateInitiatorServiceCredential>
- [Guide pratique pour Créer un contrat Duplex](../../../../../docs/framework/wcf/feature-details/how-to-create-a-duplex-contract.md)
- [Comportements de sécurité](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [Utilisation des certificats](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)
