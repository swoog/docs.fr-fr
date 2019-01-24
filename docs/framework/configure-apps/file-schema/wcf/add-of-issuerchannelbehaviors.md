---
title: '&lt;add&gt; de &lt;issuerChannelBehaviors&gt;'
ms.date: 03/30/2017
ms.assetid: 50710506-e28f-45dd-ab7e-bff6f44173db
ms.openlocfilehash: e0f49f71a3f9649492b3ad7ccf263114957ee4e3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54729929"
---
# <a name="ltaddgt-of-ltissuerchannelbehaviorsgt"></a>&lt;add&gt; de &lt;issuerChannelBehaviors&gt;
Ajoute un comportement de point de terminaison à utiliser lors de la communication avec un service STS.  
  
> [!NOTE]
>  Si un comportement de point de terminaison contient un [ \<clientCredentials >](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md) élément, une exception sera levée.  
  
 \<system.ServiceModel>  
\<behaviors>  
section d’endpointBehaviors  
\<behavior>  
\<clientCredentials>  
\<issuedToken>  
\<issuerChannelBehaviors > élément  
\<add>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<add issuerAddress="string"
     behaviorConfiguraton="string" />
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|issuerAddress|URI de l'émetteur de jeton de sécurité avec lequel communiquer.|  
|behaviorConfiguration|Nom d'un comportement de point de terminaison défini dans le même fichier de configuration.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<issuerChannelBehaviors>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuerchannelbehaviors-element.md)|Contient une collection de comportements de point de terminaison de client Windows Communication Foundation (WCF) à utiliser lors de la communication avec les Services de jeton spécifiés.|  
  
## <a name="remarks"></a>Notes  
 `issuerAddress` contient l'URI du service d'émission de jeton de sécurité avec lequel le client souhaite communiquer. `behaviorConfiguration` pointe vers un comportement de point de terminaison que l’application utilise dans les canaux créés par Windows Communication Foundation (WCF) pour obtenir les jetons émis à partir des Services de jeton de sécurité.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.Configuration.IssuedTokenClientElement.IssuerChannelBehaviors%2A>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientBehaviorsElement>
- <xref:System.ServiceModel.Configuration.IssuedTokenClientBehaviorsElementCollection>
- <xref:System.ServiceModel.Security.IssuedTokenClientCredential.IssuerChannelBehaviors%2A>
- [Identité du service et authentification](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [Comportements de sécurité](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)
- [Fédération et jetons émis](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [Sécurisation des services et des clients](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
- [Sécurisation des clients](../../../../../docs/framework/wcf/securing-clients.md)
- [Guide pratique pour Créer un Client fédéré](../../../../../docs/framework/wcf/feature-details/how-to-create-a-federated-client.md)
- [Guide pratique pour Configurer un émetteur Local](../../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md)
- [Fédération et jetons émis](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [\<issuerChannelBehaviors>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuerchannelbehaviors-element.md)
