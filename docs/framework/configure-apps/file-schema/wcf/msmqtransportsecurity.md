---
title: '&lt;msmqTransportSecurity&gt;'
ms.date: 03/30/2017
ms.assetid: 092e911b-ab1b-4069-a26e-6134c3299e06
ms.openlocfilehash: 2a4daea50e1b6c24d923e01a6bc7ae913c241001
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54593483"
---
# <a name="ltmsmqtransportsecuritygt"></a>&lt;msmqTransportSecurity&gt;
Spécifie des paramètres de sécurité de transport MSMQ pour une liaison personnalisée.  
  
 \<system.serviceModel>  
\<bindings>  
\<customBinding>  
\<binding>  
\<msmqIntegration>  
\<msmqTransportSecurity>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<msmqTransportSecurity msmqAuthenticationMode="None/Windows/Certificate"
                       msmqEncryptionAlgorithm="RC4Stream/AES"
                       msmqProtectionLevel="None/Sign/EncryptAndSign"
                       msmqSecureHashAlgorithm="MD5/SHA1/SHA256/SHA512" />
</msmqTransportSecurity>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`msmqAuthenticationMode`|Spécifie comment le message doit être authentifié par le transport MSMQ. S'il a la valeur `None`, la valeur de l'attribut `msmqProtectionLevel` doit également être `None`.<br /><br /> Les valeurs valides sont les suivantes :<br /><br /> -None : Aucune authentification.<br />-Windows : Le mécanisme d’authentification utilise Active Directory pour obtenir le certificat X.509 pour le SID associé au message. Il est ensuite utilisé pour vérifier l'ACL de la file d'attente afin de s'assurer que l'utilisateur a l'autorisation d'écrire dans la file d'attente.<br />-Certificat : Le canal Obtient le certificat du magasin de certificats.<br /><br /> La valeur par défaut est Windows. Cet attribut est de type <xref:System.ServiceModel.MsmqAuthenticationMode>.|  
|`msmqEncryptionAlgorithm`|Spécifie l'algorithme à utiliser pour le chiffrement des messages sur le câble lors du transfert de messages entre des gestionnaires de file d'attente de messages. Les valeurs valides sont les suivantes :<br /><br /> -   RC4Stream<br />-   AES<br /><br /> La valeur par défaut est RC4Stream. Cet attribut est de type <xref:System.ServiceModel.MsmqEncryptionAlgorithm>.|  
|`msmqProtectionLevel`|Spécifie le mode de sécurisation du message au niveau du transport MSMQ. Le chiffrement garantit l'intégrité des messages tandis que EncryptAndSign garantit à la fois l'intégrité des messages et leur non-rejet ; autrement dit, le message vient en effet de l'expéditeur et c'est celui-ci qui se déclare lui-même. Les valeurs valides sont les suivantes :<br /><br /> -None : Aucune protection.<br />-Signe : Les messages sont signés.<br />-   EncryptAndSign: Les messages sont chiffrés et signés.<br /><br /> La valeur par défaut est Sign. Cet attribut est de type <xref:System.Net.Security.ProtectionLevel>.|  
|`msmqSecureHashAlgorithm`|Spécifie l'algorithme à utiliser pour calculer le message condensé dans le cadre des signatures. Les valeurs valides sont les suivantes :<br /><br /> -   MD5<br />-   SHA1<br />-   SHA256<br />-   SHA512<br /><br /> La valeur par défaut est SHA1. Cet attribut est de type <xref:System.ServiceModel.MsmqSecureHashAlgorithm>.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<msmqIntegration>](../../../../../docs/framework/configure-apps/file-schema/wcf/msmqintegration.md)|Spécifie des paramètres requis pour l'interaction avec un expéditeur ou un récepteur MSMQ.|  
|[\<msmqTransport>](../../../../../docs/framework/configure-apps/file-schema/wcf/msmqtransport.md)|Spécifie les propriétés de communication mises en file d'attente pour un service Windows Communication Foundation (WCF) qui utilise le protocole MSMQ natif.|  
  
## <a name="remarks"></a>Notes  
 Pour plus d’informations sur la sécurité de transport, consultez [sécurité du Transport](../../../../../docs/framework/wcf/feature-details/transport-security.md).  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationSecurity>
- <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [Files d’attente dans WCF](../../../../../docs/framework/wcf/feature-details/queues-in-wcf.md)
- [Transports](../../../../../docs/framework/wcf/feature-details/transports.md)
- [Choix d’un transport](../../../../../docs/framework/wcf/feature-details/choosing-a-transport.md)
- [Liaisons](../../../../../docs/framework/wcf/bindings.md)
- [Extension de liaisons](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [Liaisons personnalisées](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [\<customBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
- [Sécurité de transport](../../../../../docs/framework/wcf/feature-details/transport-security.md)
