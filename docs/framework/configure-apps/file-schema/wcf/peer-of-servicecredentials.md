---
title: <peer> de <serviceCredentials>
ms.date: 03/30/2017
ms.assetid: b134e21d-e5b5-458e-9309-626dbf8db4ed
ms.openlocfilehash: 2090e79e6affe8ade6e2e52b94d2c4e1dafe8fa1
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55266024"
---
# <a name="peer-of-servicecredentials"></a>\<homologue > de \<serviceCredentials >
Spécifie les informations d'identification actuelles d'un nœud homologue.  
  
 \<system.ServiceModel>  
\<behaviors>  
\<serviceBehaviors>  
\<behavior>  
\<serviceCredentials>  
\<peer>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<peer>
  <certificate />
  <peerAuthentication />
  <messageSenderAuthentication />
</peer>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<certificate>](../../../../../docs/framework/configure-apps/file-schema/wcf/certificate-of-peer.md)|Spécifie un certificat X.509 à utiliser pour signer et chiffrer des messages pour les services de réseau pair à pair. .|  
|[\<messageSenderAuthentication>](../../../../../docs/framework/configure-apps/file-schema/wcf/messagesenderauthentication.md)|Spécifie les options d'authentification pour les expéditeurs de messages.|  
|[\<peerAuthentication>](../../../../../docs/framework/configure-apps/file-schema/wcf/peerauthentication.md)|Spécifie les options d'authentification pour les services du réseau pair à pair.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<serviceCredentials>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecredentials.md)|Spécifie les informations d’identification à utiliser pour authentifier le service, ainsi que les paramètres liés à la validation des informations d’identification du client.|  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.Configuration.PeerCredentialElement>
- <xref:System.ServiceModel.Configuration.ServiceCredentialsElement.Peer%2A>
- <xref:System.ServiceModel.Description.ServiceCredentials.Peer%2A>
- <xref:System.ServiceModel.Security.PeerCredential>
- [Réseaux homologues](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md)
- [Authentification de Message de canal homologue](https://msdn.microsoft.com/library/80e73386-514e-4c30-9e4a-b9ca8c173a95)
- [Authentification personnalisée de canal homologue](https://msdn.microsoft.com/library/4aa8a82e-41a8-48e2-8621-7e1cbabdca7c)
- [Sécurisation des applications de canal homologue](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md)
- [Sécurisation des services et des clients](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
