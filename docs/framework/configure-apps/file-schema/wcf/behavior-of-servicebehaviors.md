---
title: <behavior> de <serviceBehaviors>
ms.date: 03/30/2017
ms.assetid: 78fc0a08-55de-416a-ac12-a5e6ffc9a987
ms.openlocfilehash: 89ad23a801abce9b2fe409b7e7acb1f5e9c2ac55
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271124"
---
# <a name="behavior-of-servicebehaviors"></a>\<comportement > de \<serviceBehaviors >
L’élément `behavior` contient une collection de paramètres concernant le comportement d’un service. Chaque comportement est indexé en fonction de son `name`. Services peuvent être liés à chaque comportement via ce nom à l’aide de la `behaviorConfiguration` attribut de la [ \<point de terminaison >](../../../../../docs/framework/configure-apps/file-schema/wcf/endpoint-element.md) élément. Ceci permet aux points de terminaison de partager des configurations de comportement communes sans redéfinir les paramètres. Depuis [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], les liaisons et les comportements ne sont pas obligés d’avoir un nom. Pour plus d’informations sur la configuration par défaut et les liaisons sans nom et les comportements, consultez [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) et [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).  
  
> [!NOTE]
>  Éléments de comportement spécifiques aux activités de flux de travail Windows, telles que la [ \<sendMessageChannelCache >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/sendmessagechannelcache.md) élément, sont documentées dans le [ \<comportement > de \< serviceBehaviors >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/behavior-of-servicebehaviors-of-workflow.md) page.  
  
 \<system.ServiceModel>  
\<behaviors>  
\<serviceBehaviors>  
\<behavior>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<system.ServiceModel>
  <behaviors>
    <serviceBehaviors>
       <behavior name="String" />
    </serviceBehaviors>
  </behaviors>
</system.ServiceModel>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|name|Chaîne unique qui contient le nom de configuration du comportement. Cette valeur est une chaîne définie par l'utilisateur qui doit être unique, puisqu'elle sert de chaîne d'identification pour l'élément. Depuis [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], les liaisons et les comportements ne sont pas obligés d’avoir un nom. Pour plus d’informations sur la configuration par défaut et les liaisons sans nom et les comportements, consultez [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) et [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).|  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<dataContractSerializer>](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)|Contient les données de configuration pour DataContractSerializer.|  
|[\<persistenceProvider>](../../../../../docs/framework/configure-apps/file-schema/wcf/persistenceprovider.md)|Indique le type d'implémentation de fournisseur de persistance à utiliser, ainsi que le délai d'expiration à utiliser pour les opérations de persistance.|  
|[\<routing>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing-of-servicebehavior.md)|Fournit un accès au service de routage au moment de l'exécution afin d'autoriser une modification dynamique de la configuration de routage.|  
|[\<serviceAuthenticationManager>](../../../../../docs/framework/configure-apps/file-schema/wcf/serviceauthenticationmanager.md)|Fournit un élément de configuration de flux de travail qui établit au niveau du service la validité d'une transmission, d'un message ou d'un expéditeur.|  
|[\<serviceAuthorization>](../../../../../docs/framework/configure-apps/file-schema/wcf/serviceauthorization-element.md)|Spécifie les paramètres qui autorisent l'accès aux opérations de service.|  
|[\<serviceCredentials>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecredentials.md)|Spécifie l’information d’identification à utiliser pour authentifier le service, ainsi que les paramètres liés à la validation des informations d’identification du client.|  
|[\<serviceDebug>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicedebug.md)|Spécifie les fonctionnalités d’informations de débogage et d’aide pour un service Windows Communication Foundation (WCF).|  
|[\<serviceDiscovery>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicediscovery.md)|Spécifie la fonctionnalité de découverte des points de terminaison de service.|  
|[\<serviceMetadata>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicemetadata.md)|Spécifie la publication de métadonnées de service et des informations associées.|  
|[\<serviceSecurityAudit>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicesecurityaudit.md)|Spécifie des paramètres qui activent l'audit d'événements de sécurité pendant des opérations de service.|  
|[\<serviceThrottling>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicethrottling.md)|Spécifie le mécanisme de limitation d’un service WCF.|  
|[\<serviceTimeouts>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicetimeouts.md)|Spécifie le délai d'attente pour un service.|  
|[\<workflowRuntime>](../../../../../docs/framework/configure-apps/file-schema/wcf/workflowruntime.md)|Spécifie les paramètres d’une instance de WorkflowRuntime pour l’hébergement de services WCF basés sur les flux de travail.|  
|[\<useRequestHeadersForMetadataAddress>](../../../../../docs/framework/configure-apps/file-schema/wcf/userequestheadersformetadataaddress.md)|Active la récupération des informations d'adresse des métadonnées à partir des en-têtes de message de demande.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<serviceBehaviors>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicebehaviors.md)|Collection d’éléments de comportement de service.|
