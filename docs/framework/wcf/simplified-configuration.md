---
title: Configuration simplifiée
ms.date: 03/30/2017
ms.assetid: dcbe1f84-437c-495f-9324-2bc09fd79ea9
ms.openlocfilehash: 13cf8bd46ef3aabb011cb2ddd207963235468662
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59184052"
---
# <a name="simplified-configuration"></a>Configuration simplifiée
Configuration des services Windows Communication Foundation (WCF) peut être une tâche complexe. Il existe de nombreuses options différentes et il n'est pas toujours évident de déterminer les paramètres nécessaires. Bien que les fichiers de configuration augmentent la flexibilité des services WCF, ils sont également la source de nombreux problèmes difficiles à détecter. [!INCLUDE[netfx_current_long](../../../includes/netfx-current-long-md.md)] résout ces problèmes et fournit un moyen de réduire la taille et la complexité de configuration du service.  
  
## <a name="simplified-configuration"></a>Configuration simplifiée  
 Dans les fichiers de configuration de service WCF, le <`system.serviceModel`> section contient un <`service`>, élément pour chaque service hébergé. Le <`service`> élément contient une collection de <`endpoint`> éléments qui spécifient les points de terminaison exposés pour chaque service et éventuellement un ensemble de comportements de service. Le <`endpoint`> éléments spécifient l’adresse, liaison et contrat exposés par le point de terminaison et éventuellement une configuration de liaison et les comportements de point de terminaison. Le <`system.serviceModel`> section contient également un <`behaviors`> élément qui vous permet de spécifier des comportements de service ou de point de terminaison. L’exemple suivant montre le <`system.serviceModel`> section d’un fichier de configuration.  
  
```  
<system.serviceModel>  
  <behaviors>  
    <serviceBehaviors>  
      <behavior name="MyServiceBehavior">  
        <serviceMetadata httpGetEnabled="true">  
        <serviceDebug includeExceptionDetailInFaults="false">  
      </behavior>  
    </serviceBehaviors>  
  </behaviors>  
  <bindings>  
   <basicHttpBinding>  
      <binding name=MyBindingConfig"  
               maxBufferSize="100"  
               maxReceiveBufferSize="100" />  
   </basicHttpBinding>  
   </bindings>   <services>  
    <service behaviorConfiguration="MyServiceBehavior"  
             name="MyService">  
      <endpoint address=""  
                binding="basicHttpBinding"  
                contract="ICalculator"  
                bindingConfiguration="MyBindingConfig" />  
      <endpoint address="mex"  
                binding="mexHttpBinding"  
                contract="IMetadataExchange"/>  
    </service>  
  </services>  
</system.serviceModel>  
```  
  
 [!INCLUDE[netfx_current_short](../../../includes/netfx-current-short-md.md)] simplifie la configuration d’un service WCF plus facile en supprimant la nécessité pour le <`service`> élément. Si vous n’ajoutez pas un <`service`> section ou ajouter des points de terminaison dans un <`service`> section et votre service ne définit pas par programmation des points de terminaison, puis un ensemble de points de terminaison par défaut sont automatiquement ajoutés à votre service, une pour chaque adresse de base du service et pour chaque contrat implémenté par votre service. Dans chacun de ces points de terminaison, l’adresse du point de terminaison correspond à l’adresse de base, la liaison est déterminée par le schéma d’adresse de base et le contrat est celui implémenté par votre service. Si vous n’avez pas besoin de spécifier de comportements de point de terminaison ou de service, ni de modifier un paramètre de liaison, il est inutile de spécifier un fichier de configuration de service. Si un service implémente deux contrats et que l'hôte active à la fois les transports HTTP et TCP, l'hôte de service crée quatre points de terminaison par défaut, un pour chaque contrat utilisant chaque transport. Pour créer des points de terminaison par défaut, l'hôte de service doit savoir quelles liaisons utiliser. Ces paramètres sont spécifiés dans un <`protocolMappings`> section dans le <`system.serviceModel`> section. Le <`protocolMappings`> section contient une liste de schémas de protocole de transport mappés aux types de liaison. L’hôte du service utilise les adresses de base qui lui sont transmises pour déterminer quelle liaison utiliser. L’exemple suivant utilise le <`protocolMappings`> élément.  
  
> [!WARNING]
>  Le fait de modifier les éléments de configuration par défaut, comme les liaisons ou les comportements, peut affecter les services définis dans les niveaux inférieurs de la hiérarchie de configuration, car ces derniers peuvent utiliser ces liaisons et comportements par défaut. C’est pourquoi, la personne qui modifie les liaisons et comportements par défaut doit savoir que ces changements peuvent affecter d’autres services dans la hiérarchie.  
  
> [!NOTE]
>  Les services hébergés dans les services IIS (Internet Information Services) ou WAS (Windows Process Activation Service) utilisent le répertoire virtuel comme leur adresse de base.  
  
```xml  
<protocolMapping>  
  <add scheme="http"     binding="basicHttpBinding" bindingConfiguration="MyBindingConfiguration"/>  
  <add scheme="net.tcp"  binding="netTcpBinding"/>  
  <add scheme="net.pipe" binding="netNamedPipeBinding"/>  
  <add scheme="net.msmq" binding="netMSMQBinding"/>  
</protocolMapping>  
```  
  
 Dans l'exemple précédent, un point de terminaison avec une adresse de base commençant par le schéma « http » utilise la liaison <xref:System.ServiceModel.BasicHttpBinding>. Un point de terminaison avec une adresse de base commençant par le schéma « net.tcp » utilise la liaison <xref:System.ServiceModel.NetTcpBinding>. Vous pouvez remplacer des paramètres dans un fichier local App.config ou Web.config.  
  
 Chaque élément dans le <`protocolMappings`> section doit spécifier un schéma et une liaison. Il peut éventuellement spécifier un `bindingConfiguration` attribut qui spécifie une configuration de liaison dans le <`bindings`> section du fichier de configuration. Si aucun attribut `bindingConfiguration` n’est spécifié, la configuration de liaison anonyme du type de liaison approprié est utilisée.  
  
 Comportements de service sont configurés pour les points de terminaison par défaut à l’aide d’anonyme <`behavior`> intérieur des sections <`serviceBehaviors`> sections. Sans nom <`behavior`> éléments dans <`serviceBehaviors`> sont utilisés pour configurer les comportements de service. Par exemple, le fichier de configuration suivant permet la publication de métadonnées de service pour tous les services qui se trouvent dans l'hôte.  
  
```xml  
<system.serviceModel>  
    <behaviors>  
      <serviceBehaviors>  
        <behavior>  
          <serviceMetadata httpGetEnabled="True"/>  
        </behavior>  
      </serviceBehaviors>  
    </behaviors>    <!-- No <service> tag is necessary. Default endpoints are added to the service -->  
    <!-- The service behavior with name="" is picked up by the service -->  
 </system.serviceModel>  
```  
  
 Les comportements de point de terminaison sont configurés à l’aide d’anonyme <`behavior`> intérieur des sections <`serviceBehaviors`> sections.  
  
 L'exemple suivant est un fichier de configuration équivalent à celui qui se trouve au début de cette rubrique. Il utilise le modèle de configuration simplifié.  
  
```xml  
<system.serviceModel>
    <behaviors>
      <serviceBehaviors>
        <behavior>
          <serviceMetadata httpGetEnabled="true" />
          <serviceDebug includeExceptionDetailInFaults="false" />
        </behavior>
      </serviceBehaviors>
    </behaviors>
    <bindings>
       <basicHttpBinding>
          <binding maxBufferSize="100"
                   maxReceiveBufferSize="100" />
       </basicHttpBinding>
    </bindings>
    <!-- No <service> tag is necessary. Default endpoints will be added to the service -->
    <!-- The service behavior with name="" will be picked up by the service -->
    <protocolMapping>
      <add scheme="http" binding="basicHttpBinding" />
  </protocolMapping>
  </system.serviceModel>
```  
  
> [!IMPORTANT]
>  Cette fonctionnalité concerne uniquement la configuration du service WCF, non la configuration du client. La plupart de temps, la configuration cliente WCF est générée par un outil comme svcutil.exe ou en ajoutant une référence de service à partir de Visual Studio. Si vous configurez manuellement un client WCF, vous devrez ajouter un \<client > élément à la configuration et spécifier des points de terminaison que vous souhaitez appeler.  
  
## <a name="see-also"></a>Voir aussi

- [Configuration des services à l'aide de fichiers de configuration](../../../docs/framework/wcf/configuring-services-using-configuration-files.md)
- [Configuration de liaisons pour les services](../../../docs/framework/wcf/configuring-bindings-for-wcf-services.md)
- [Configuration des liaisons fournies par le système](../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)
- [Configuration des services](../../../docs/framework/wcf/configuring-services.md)
- [Configuration des services WCF](configuring-services.md)
- [Configuration de services WCF dans le code](../../../docs/framework/wcf/configuring-wcf-services-in-code.md)
