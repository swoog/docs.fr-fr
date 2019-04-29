---
title: Élément <issuerChannelBehaviors>
ms.date: 03/30/2017
ms.assetid: f7378673-8e9b-45b2-98d1-cf5dccdd8c40
ms.openlocfilehash: 7cbd50daa82b0ca937a1bba93786545898b03c8b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61760725"
---
# <a name="issuerchannelbehaviors-element"></a>\<issuerChannelBehaviors > élément

Contient une collection de comportements de point de terminaison de client Windows Communication Foundation (WCF) (défini dans la configuration) à utiliser lors de la communication avec les Services de jeton spécifiés. Les comportements définis ne peut pas inclure les [ \<clientCredentials >](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md) éléments.

```xml
<system.ServiceModel>
  <behaviors>
    <endpointBehaviors>
      <behavior>
        <clientCredentials>
          <issuedToken>
            <issuerChannelBehaviors>
```

## <a name="syntax"></a>Syntaxe

```xml
<issuerChannelBehaviors>
  <add behaviorConfiguration="string"
       issuerAddress="string" />
</issuerChannelBehaviors>
```

## <a name="attributes-and-elements"></a>Attributs et éléments

Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.

### <a name="attributes"></a>Attributs

Aucun.

### <a name="child-elements"></a>Éléments enfants

|Élément|Description|
|-------------|-----------------|
|[\<add>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-issuerchannelbehaviors.md)|Ajoute un comportement à la collection.|

### <a name="parent-elements"></a>Éléments parents

|Élément|Description|
|-------------|-----------------|
|[\<issuedToken>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtoken.md)|Spécifie un jeton personnalisé utilisé pour authentifier un client auprès d'un service.|

## <a name="remarks"></a>Notes

Utilisez cet élément lorsque des comportements (autres que ceux qui contiennent des éléments `<clientCredentials>`) doivent être utilisés pour communiquer avec un service. Par exemple, si un [ \<dataContractSerializer >](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) élément de comportement doit être inclus.

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
