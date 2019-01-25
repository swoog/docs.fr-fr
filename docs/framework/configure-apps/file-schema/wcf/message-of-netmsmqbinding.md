---
title: '&lt;message&gt; de &lt;netMsmqBinding&gt;'
ms.date: 03/30/2017
ms.assetid: 6ebf0240-d7be-4493-b0fe-f00fd5989d77
ms.openlocfilehash: b636a22fe7c6bcfae5b8f81c1566ea39c9f8ced5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54683740"
---
# <a name="ltmessagegt-of-ltnetmsmqbindinggt"></a>&lt;message&gt; de &lt;netMsmqBinding&gt;
Définit les paramètres de sécurité des messages SOAP sur cette liaison `netMsmqBinding`.  
  
 \<system.ServiceModel>  
\<bindings>  
\<netMsmqBinding>  
\<binding>  
\<security>  
\<message>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<netMsmqBinding>
  <binding>
    <security>
      <message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
               clientCredentialType="None/Windows/UserName/Certificate/CardSpace" />
    </security>
  </binding>
</netMsmqBinding>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|algorithmSuite|Définit le chiffrement des messages et algorithmes de clé de type WRAP utilisés pour obtenir la sécurité basée sur des messages pour les messages envoyés via le transport MSMQ.<br /><br /> La valeur par défaut est `Aes256`. Cet attribut est de type <xref:System.ServiceModel.Security.SecurityAlgorithmSuite>.|  
|clientCredentialType|Spécifie le type d'information d'identification à utiliser lors de l'exécution de l'authentification du client pour les messages envoyés via le transport MSMQ. Les valeurs valides sont les suivantes :<br /><br /> -None : Permet au service d'interagir avec les clients anonymes. Ni le service ni le client n'exigent d'informations d'identification.<br />-Windows : Ainsi, les échanges SOAP d’être sous le contexte authentifié d’informations d’identification Windows. Exécute toujours une authentification basée sur Kerberos.<br />-   UserName: Cela permet au service d’exiger que le client soit authentifié à l’aide des informations d’identification de nom d’utilisateur. Les informations d’identification dans ce cas doivent être spécifiées à l’aide du `clientCredentials` comportement **attention :**  Windows Communication Foundation (WCF) ne prend pas en charge l’envoi d’un mot de passe digest ou de dérivation de clés à l’aide du mot de passe et à l’aide de ces clés pour la sécurité de message. WCF applique donc que l’échange est sécurisé lors de l’utilisation des informations d’identification UserName. Ce mode requiert que le certificat de service soit spécifié côté client à l'aide du comportement `clientCredential` et de `serviceCertificate`. <br /><br /> -Certificat : Cela permet au service d’exiger que le client soit authentifié à l’aide d’un certificat. Les informations d'identification du client dans ce cas doivent être spécifiées à l'aide du comportement `clientCredentials`. Les informations d'identification du service dans ce cas doivent être spécifiées à l'aide du comportement `clientCredentials` en spécifiant le `serviceCertificate`.<br />-   CardSpace: Cela permet au service d’exiger que le client soit authentifié à l’aide d’un CardSpace. Le `serviceCertiifcate` doit être configuré dans le comportement `clientCredential`.<br /><br /> La valeur par défaut est `Windows`. Cet attribut est de type <xref:System.ServiceModel.MessageCredentialType>.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<security>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-netmsmqbinding.md)|Définit les paramètres de sécurité d’une liaison.|  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.Configuration.MessageSecurityOverMsmqElement>
- <xref:System.ServiceModel.Configuration.NetMsmqSecurityElement.Message%2A>
- <xref:System.ServiceModel.NetMsmqSecurity.Message%2A>
- <xref:System.ServiceModel.MessageSecurityOverMsmq>
- [Files d’attente dans WCF](../../../../../docs/framework/wcf/feature-details/queues-in-wcf.md)
- [Sécurisation des services et des clients](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [Liaisons](../../../../../docs/framework/wcf/bindings.md)
- [Configuration des liaisons fournies par le système](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [Utilisation de liaisons pour configurer des services et des clients](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](../../../../../docs/framework/misc/binding.md)
