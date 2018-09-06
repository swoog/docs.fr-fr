---
title: 'Comment : configurer un client Windows Communication Foundation de base'
ms.date: 03/30/2017
helpviewer_keywords:
- WCF clients [WCF], configuring
ms.assetid: d067b86d-afb0-47bf-94f6-45180a3d8d78
ms.openlocfilehash: 2866cbd5862bf55286fc771823488cf913863de2
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43855853"
---
# <a name="how-to-configure-a-basic-windows-communication-foundation-client"></a>Comment : configurer un client Windows Communication Foundation de base
Il s’agit de la cinquième des six tâches requises pour créer une application Windows Communication Foundation (WCF) de base. Pour une vue d’ensemble des six tâches, consultez la rubrique [Tutoriel Bien démarrer](../../../docs/framework/wcf/getting-started-tutorial.md).  
  
 Cette rubrique décrit le fichier de configuration de client qui a été généré à l’aide de la fonctionnalité Ajouter une référence de Service de [!INCLUDE[vs_current_long](../../../includes/vs-current-long-md.md)] ou [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md). La configuration du client consiste à spécifier le point de terminaison que le client utilise pour accéder au service. Un point de terminaison a une adresse, une liaison et un contrat et chacun de ces éléments doit être spécifié dans le processus de configuration du client.  
  
### <a name="to-configure-a-windows-communication-foundation-client"></a>Pour configurer un client Windows Communication Foundation  
  
1.  Ouvrez le fichier de configuration généré (App.config) du projet GettingStartedClient. L'exemple suivant est une vue du fichier de configuration généré. Sous le [ \<system.serviceModel >](../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md) section, recherchez le [ \<point de terminaison >](https://msdn.microsoft.com/library/13aa23b7-2f08-4add-8dbf-a99f8127c017) élément.  
  
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
  
     Cet exemple configure le point de terminaison que le client utilise pour accéder au service qui se trouve à l’adresse suivante : http://localhost:8000/ServiceModelSamples/Service/CalculatorService  
  
     L'élément de point de terminaison spécifie que le contrat de service `ServiceReference1.ICalculator` est utilisé pour la communication entre le client et le service WCF. Le canal WCF est configuré avec <xref:System.ServiceModel.WSHttpBinding> fourni par le système. Ce contrat a été généré à l'aide de la fonctionnalité Ajouter une référence de service dans Visual Studio. Il s'agit essentiellement d'une copie du contrat défini dans le projet GettingStartedLib. La liaison <xref:System.ServiceModel.WSHttpBinding> spécifie le protocole HTTP pour le transport, la sécurité interopérable et d'autres détails de configuration.  
  
2.  Pour plus d’informations sur l’utilisation du client généré avec cette configuration, consultez [Comment : utiliser un Client](../../../docs/framework/wcf/how-to-use-a-wcf-client.md).  
  
## <a name="see-also"></a>Voir aussi  
 [Utilisation de liaisons pour configurer des services et des clients](../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
 [Outil ServiceModel Metadata Utility (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)  
 [Guide pratique pour créer un client](../../../docs/framework/wcf/how-to-create-a-wcf-client.md)  
 [Prise en main](../../../docs/framework/wcf/samples/getting-started-sample.md)  
 [Auto-hébergement](../../../docs/framework/wcf/samples/self-host.md)
