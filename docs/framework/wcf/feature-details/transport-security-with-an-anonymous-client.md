---
title: Sécurité de transport avec un client anonyme - WCF
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 056653a5-384e-4a02-ae3c-1b0157d2ccb4
ms.openlocfilehash: 20d7e59ba2b4b9dedc0b0daff1c1aa9c5210e61b
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55260383"
---
# <a name="transport-security-with-an-anonymous-client"></a>Sécurité de transport avec un client anonyme

Ce scénario de Windows Communication Foundation (WCF) utilise la sécurité du transport (HTTPS) pour garantir la confidentialité et l’intégrité. Le serveur doit être authentifié à l'aide d'un certificat SSL (Secure Sockets Layer). Les clients doivent ensuite faire confiance à ce certificat. Aucun mécanisme n'authentifie les clients, ceux-ci restent donc anonymes.

Pour un exemple d’application, consultez [sécurité du Transport WS](../samples/ws-transport-security.md). Pour plus d’informations sur la sécurité de transport, consultez [vue d’ensemble de sécurité de Transport](transport-security-overview.md).

Pour plus d’informations sur l’utilisation d’un certificat avec un service, consultez [Working with Certificates](working-with-certificates.md) et [Comment : Configurer un Port avec un certificat SSL](how-to-configure-a-port-with-an-ssl-certificate.md).

![Utilisation de la sécurité de transport avec un client anonyme](./media/8fa2e931-0cfb-4aaa-9272-91d652b85d8d.gif)

|Caractéristique|Description|
|--------------------|-----------------|
|Mode de sécurité|Transport|
|Interopérabilité|Avec les services Web et les clients existants|
|Authentification (serveur)<br /><br /> Authentification (client)|Oui<br /><br /> Niveau de l’application (aucune prise en charge WCF)|
|Intégrité|Oui|
|Confidentialité|Oui|
|Transport|HTTPS|
|Binding|<xref:System.ServiceModel.WSHttpBinding>|

## <a name="service"></a>Service

La configuration et le code ci-dessous sont conçus pour s'exécuter indépendamment. Effectuez l’une des opérations suivantes :

- Créez un service autonome à l'aide du code sans configuration.

- Créez un service à l'aide de la configuration fournie, mais ne définissez pas de point de terminaison.

### <a name="code"></a>Code

Le code suivant illustre comment créer un point de terminaison à l'aide de la sécurité de transport :

[!code-csharp[c_SecurityScenarios#5](~/samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#5)]
[!code-vb[c_SecurityScenarios#5](~/samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#5)]

### <a name="configuration"></a>Configuration

Le code ci-dessous configure le même point de terminaison en utilisant la configuration. Aucun mécanisme n'authentifie les clients, ceux-ci restent donc anonymes.

```xml
<?xml version="1.0" encoding="utf-8"?>
<configuration>
  <system.serviceModel>
    <services>
      <service name="ServiceModel.Calculator">
        <endpoint address="https://localhost/Calculator"
                  binding="wsHttpBinding"
                  bindingConfiguration="WSHttpBinding_ICalculator"
                  name="SecuredByTransportEndpoint"
                  contract="ServiceModel.ICalculator" />
      </service>
    </services>
    <bindings>
      <wsHttpBinding>
        <binding name="WSHttpBinding_ICalculator">
          <security mode="Transport">
            <transport clientCredentialType="None" />
          </security>
        </binding>
      </wsHttpBinding>
    </bindings>
    <client />
  </system.serviceModel>
</configuration>
```

## <a name="client"></a>Client

La configuration et le code ci-dessous sont conçus pour s'exécuter indépendamment. Effectuez l’une des opérations suivantes :

- Créez un client autonome à l'aide du code (et du code client).

- Créez un client qui ne définit pas d'adresse de point de terminaison. Au lieu de cela, utilisez le constructeur client qui accepte le nom de configuration comme argument. Par exemple :

     [!code-csharp[C_SecurityScenarios#0](~/samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#0)]
     [!code-vb[C_SecurityScenarios#0](~/samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#0)]

### <a name="code"></a>Code

[!code-csharp[c_SecurityScenarios#6](~/samples/snippets/csharp/VS_Snippets_CFX/c_securityscenarios/cs/source.cs#6)]
[!code-vb[c_SecurityScenarios#6](~/samples/snippets/visualbasic/VS_Snippets_CFX/c_securityscenarios/vb/source.vb#6)]

### <a name="configuration"></a>Configuration

La configuration suivante peut être utilisée à la place du code pour paramétrer le service :

```xml
<configuration>
  <system.serviceModel>
    <bindings>
      <wsHttpBinding>
        <binding name="WSHttpBinding_ICalculator" >
          <security mode="Transport">
            <transport clientCredentialType="None" />
          </security>
        </binding>
      </wsHttpBinding>
    </bindings>
    <client>
      <endpoint address="https://machineName/Calculator"
                binding="wsHttpBinding"
                bindingConfiguration="WSHttpBinding_ICalculator"
                contract="ICalculator"
                name="WSHttpBinding_ICalculator" />
    </client>
  </system.serviceModel>
</configuration>
```

## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de la sécurité](security-overview.md)
- [Sécurité de transport WS](../samples/ws-transport-security.md)
- [Vue d’ensemble de la sécurité de transport](transport-security-overview.md)
- [Modèle de sécurité pour Windows Server AppFabric](https://docs.microsoft.com/previous-versions/appfabric/ee677202(v=azure.10))