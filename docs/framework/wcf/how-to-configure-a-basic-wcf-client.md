---
title: 'Comment : configurer un client Windows Communication Foundation de base'
ms.date: 09/14/2018
helpviewer_keywords:
- WCF clients [WCF], configuring
ms.assetid: d067b86d-afb0-47bf-94f6-45180a3d8d78
ms.openlocfilehash: 3f267edf87711de8a5969e3e0b577648008c5a75
ms.sourcegitcommit: dfb2a100cfb4d3902c042f17b3204f49bc7635e7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/21/2018
ms.locfileid: "46524861"
---
# <a name="how-to-configure-a-basic-windows-communication-foundation-client"></a>Comment : configurer un client Windows Communication Foundation de base

Il s’agit de la cinquième des six tâches requises pour créer une application Windows Communication Foundation (WCF) de base. Pour une vue d’ensemble des six tâches, consultez la rubrique [Tutoriel Bien démarrer](../../../docs/framework/wcf/getting-started-tutorial.md).

Cette rubrique décrit le fichier de configuration de client qui a été généré à l’aide de la **ajouter une référence de Service** des fonctionnalités de Visual Studio ou le [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md). La configuration du client consiste à spécifier le point de terminaison que le client utilise pour accéder au service. Un point de terminaison a une adresse, une liaison et un contrat, et chacun d'entre eux doit être spécifié en cours de la configuration du client.

## <a name="configure-a-windows-communication-foundation-client"></a>Configurer un client Windows Communication Foundation

Ouvrez le fichier de configuration généré (App.config) du projet GettingStartedClient. L'exemple suivant est une vue du fichier de configuration généré. Sous le [ \<system.serviceModel >](../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md) section, recherchez le [ \<point de terminaison >](https://msdn.microsoft.com/library/13aa23b7-2f08-4add-8dbf-a99f8127c017) élément.

```xml
    <?xml version="1.0" encoding="utf-8" ?>
    <configuration>
        <startup>
          <!-- specifies the version of WCF to use-->
            <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5,Profile=Client" />
        </startup>
        <system.serviceModel>
            <bindings>
                <!-- Uses wsHttpBinding-->
                <wsHttpBinding>
                    <binding name="WSHttpBinding_ICalculator" />
                </wsHttpBinding>
            </bindings>
            <client>
                <!-- specifies the endpoint to use when calling the service -->
                <endpoint address="http://localhost:8000/ServiceModelSamples/Service/CalculatorService"
                    binding="wsHttpBinding" bindingConfiguration="WSHttpBinding_ICalculator"
                    contract="ServiceReference1.ICalculator" name="WSHttpBinding_ICalculator">
                    <identity>
                        <userPrincipalName value="migree@redmond.corp.microsoft.com" />
                    </identity>
                </endpoint>
            </client>
        </system.serviceModel>
    </configuration>
```

Cet exemple configure le point de terminaison que le client utilise pour accéder au service qui se trouve à l’adresse suivante : `http://localhost:8000/ServiceModelSamples/Service/CalculatorService`.

L'élément de point de terminaison spécifie que le contrat de service `ServiceReference1.ICalculator` est utilisé pour la communication entre le client et le service WCF. Le canal WCF est configuré avec <xref:System.ServiceModel.WSHttpBinding> fourni par le système. Ce contrat a été généré à l’aide de **ajouter une référence de Service** dans Visual Studio. Il s'agit essentiellement d'une copie du contrat défini dans le projet GettingStartedLib. La liaison <xref:System.ServiceModel.WSHttpBinding> spécifie le protocole HTTP pour le transport, la sécurité interopérable et d'autres détails de configuration.

Pour plus d’informations sur l’utilisation du client généré avec cette configuration, consultez [Comment : utiliser un Client](../../../docs/framework/wcf/how-to-use-a-wcf-client.md).

## <a name="next-steps"></a>Étapes suivantes

> [!div class="nextstepaction"]
> [Comment : utiliser un client WCF](../../../docs/framework/wcf/how-to-use-a-wcf-client.md)

## <a name="see-also"></a>Voir aussi

- [Utilisation de liaisons pour configurer des services et des clients](../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [Outil ServiceModel Metadata Utility (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)
- [Guide pratique pour créer un client](../../../docs/framework/wcf/how-to-create-a-wcf-client.md)
- [Prise en main](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [Auto-hébergement](../../../docs/framework/wcf/samples/self-host.md)