---
title: Configuration client
ms.date: 03/30/2017
ms.assetid: 5da5bd3b-65d9-43b7-91b9-cc9e989b1350
ms.openlocfilehash: b9975c6caeedc94bf4a7773e71a95eb0d8c7aed2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59144688"
---
# <a name="client-configuration"></a>Configuration client
Vous pouvez utiliser la configuration du client Windows Communication Foundation (WCF) pour spécifier l’adresse, liaison, comportement et contrat, les propriétés « ABC » du point de terminaison client, les clients utilisent pour se connecter aux points de terminaison de service. Le [ \<client >](../../configure-apps/file-schema/wcf/client.md) élément a un [ \<point de terminaison >](../../configure-apps/file-schema/wcf/endpoint-of-client.md) élément dont les attributs sont utilisés pour configurer l’ABC de point de terminaison. Ces attributs sont décrits dans le [configuration des points de terminaison de](#configuring-endpoints) section.  
  
 Le [ \<point de terminaison >](../../configure-apps/file-schema/wcf/endpoint-of-client.md) élément contient également un [ \<métadonnées >](../../configure-apps/file-schema/wcf/metadata.md) élément qui est utilisé pour spécifier les paramètres pour l’importation et exportation de métadonnées, un [ \<en-têtes >](../../configure-apps/file-schema/wcf/headers.md) élément qui constituée une collection d’en-têtes d’adresse personnalisés, et un [ \<identité >](../../configure-apps/file-schema/wcf/identity.md) élément qui permet l’authentification d’un point de terminaison par d’autres points de terminaison échange de messages avec lui. Le [ \<en-têtes >](../../configure-apps/file-schema/wcf/headers.md) et [ \<identité >](../../configure-apps/file-schema/wcf/identity.md) éléments font partie de la <xref:System.ServiceModel.EndpointAddress> et sont décrits dans le [adresses](../../wcf/feature-details/endpoint-addresses.md) article. Des liens vers des rubriques qui expliquent l’utilisation des extensions de métadonnées sont fournis dans le [configuration des métadonnées](#configuring-metadata) section.  
  
## <a name="configuring-endpoints"></a>Configuration des points de terminaison  
 La configuration du client est conçue pour permettre au client de spécifier un ou plusieurs points de terminaison, chacun avec son propre nom, adresse et contrat, et référençant chacun les [ \<liaisons >](../../../../docs/framework/configure-apps/file-schema/wcf/bindings.md) et [ \< comportements >](../../../../docs/framework/configure-apps/file-schema/wcf/behaviors.md) éléments dans la configuration du client à utiliser pour configurer ce point de terminaison. Le fichier de configuration client doit être nommé « App.config », car c’est le nom que le runtime WCF attend. L'exemple suivant illustre un fichier de configuration client.  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<configuration>  
  <system.serviceModel>  
        <client>  
          <endpoint  
            name="endpoint1"  
            address="http://localhost/ServiceModelSamples/service.svc"  
            binding="wsHttpBinding"  
            bindingConfiguration="WSHttpBinding_IHello"  
            behaviorConfiguration="IHello_Behavior"  
            contract="IHello" >  
  
            <metadata>  
              <wsdlImporters>  
                <extension  
                  type="Microsoft.ServiceModel.Samples.WsdlDocumentationImporter, WsdlDocumentation"/>  
              </wsdlImporters>  
            </metadata>  
  
            <identity>  
              <servicePrincipalName value="host/localhost" />  
            </identity>  
          </endpoint>  
// Add another endpoint by adding another <endpoint> element.  
          <endpoint  
            name="endpoint2">  
           //Configure another endpoint here.  
          </endpoint>  
        </client>  
  
//The bindings section references by the bindingConfiguration endpoint attribute.  
    <bindings>  
      <wsHttpBinding>  
        <binding name="WSHttpBinding_IHello"   
                 bypassProxyOnLocal="false"   
                 hostNameComparisonMode="StrongWildcard">  
          <readerQuotas maxDepth="32"/>  
          <reliableSession ordered="true"   
                           enabled="false" />  
          <security mode="Message">  
           //Security settings go here.  
          </security>  
        </binding>  
        <binding name="Another Binding"  
        //Configure this binding here.  
        </binding>  
          </wsHttpBinding>  
        </bindings>  
  
//The behavior section references by the behaviorConfiguration endpoint attribute.  
        <behaviors>  
            <endpointBehaviors>  
                <behavior name=" IHello_Behavior ">  
                    <clientVia />  
                </behavior>  
            </endpointBehaviors>  
        </behaviors>  
  
    </system.serviceModel>  
</configuration>  
```  
  
 L'attribut `name` facultatif identifie de manière unique un point de terminaison pour un contrat donné. Il est utilisé par le <xref:System.ServiceModel.ChannelFactory%601.%23ctor%2A> ou par le <xref:System.ServiceModel.ClientBase%601.%23ctor%2A> pour spécifier quel point de terminaison est visé dans la configuration client et doit être chargé lorsqu'un canal est créé pour le desservir. Un nom de configuration de point de terminaison générique «\*» est disponible et indique à la <xref:System.ServiceModel.ChannelFactory.ApplyConfiguration%2A> méthode qu’il doit charger toute configuration de point de terminaison dans le fichier, condition que précisément une disponible et sinon lève une exception. Si cet attribut est omis, le point de terminaison correspondant est utilisé comme point de terminaison par défaut associé au type de contrat spécifié. La valeur par défaut pour l'attribut `name` est une chaîne vide qui est mise en correspondance comme tout autre nom.  
  
 Chaque point de terminaison doit avoir une adresse qui lui est associée pour pouvoir être localisé et identifié. L'attribut `address` peut être utilisé pour spécifier l'URL qui fournit l'emplacement du point de terminaison. Mais l'adresse d'un point de terminaison de service peut également être spécifiée dans du code en créant un URI et en l'ajoutant à <xref:System.ServiceModel.ServiceHost> qui utilise l'une des méthodes <xref:System.ServiceModel.ServiceHost.AddServiceEndpoint%2A>. Pour plus d’informations, consultez [adresses](../../../../docs/framework/wcf/feature-details/endpoint-addresses.md). Comme indiqué dans l’introduction, le [ \<en-têtes >](../../../../docs/framework/configure-apps/file-schema/wcf/headers.md) et [ \<identité >](../../../../docs/framework/configure-apps/file-schema/wcf/identity.md) éléments font partie de la <xref:System.ServiceModel.EndpointAddress> et sont également traités dans le [ Adresses](../../../../docs/framework/wcf/feature-details/endpoint-addresses.md) rubrique.  
  
 L’attribut `binding` indique le type de liaison que le point de terminaison s’attend à utiliser lors de la connexion à un service. Ce type doit posséder une section de configuration inscrite s'il doit être référencé. Dans l’exemple précédent, il s’agit du [ \<wsHttpBinding >](../../../../docs/framework/configure-apps/file-schema/wcf/wshttpbinding.md) section, ce qui indique que le point de terminaison utilise un <xref:System.ServiceModel.WSHttpBinding>. Mais il peut y avoir plusieurs liaisons d’un type donné utilisables par le point de terminaison. Chacune de celles-ci a son propre [ \<liaison >](../../../../docs/framework/misc/binding.md) élément dans l’élément de type (binding). L’attribut `bindingconfiguration` est utilisé pour distinguer plusieurs liaisons du même type. Sa valeur est mise en correspondance avec la `name` attribut de la [ \<liaison >](../../../../docs/framework/misc/binding.md) élément. Pour plus d’informations sur la façon de configurer un client de liaison à l’aide de la configuration, consultez [Comment : Spécifier une liaison Client dans Configuration](../../../../docs/framework/wcf/how-to-specify-a-client-binding-in-configuration.md).  
  
 Le `behaviorConfiguration` attribut est utilisé pour spécifier quel [ \<comportement >](../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md) de la [ \<endpointBehaviors >](../../../../docs/framework/configure-apps/file-schema/wcf/endpointbehaviors.md) le point de terminaison doit utiliser. Sa valeur est mise en correspondance avec la `name` attribut de la [ \<comportement >](../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md) élément. Pour obtenir un exemple de configuration pour spécifier des comportements de client, consultez [configuration des comportements clients](../../../../docs/framework/wcf/configuring-client-behaviors.md).  
  
 L'attribut `contract` spécifie quel contrat le point de terminaison expose. Cette valeur correspond au <xref:System.ServiceModel.ServiceContractAttribute.ConfigurationName%2A> de <xref:System.ServiceModel.ServiceContractAttribute>. La valeur par défaut est le nom de type complet de la classe qui implémente le service.  
  
### <a name="configuring-metadata"></a>Configuration des métadonnées  
 Le [ \<métadonnées >](../../../../docs/framework/configure-apps/file-schema/wcf/metadata.md) élément est utilisé pour spécifier les paramètres utilisés pour enregistrer les métadonnées des extensions d’importation. Pour plus d’informations sur l’extension du système de métadonnées, consultez [extension du système de métadonnées](../../../../docs/framework/wcf/extending/extending-the-metadata-system.md).  
  
## <a name="see-also"></a>Voir aussi

- [Points de terminaison : Adresses, liaisons et contrats](../../../../docs/framework/wcf/feature-details/endpoints-addresses-bindings-and-contracts.md)
- [Configuration des comportements clients](../../../../docs/framework/wcf/configuring-client-behaviors.md)
