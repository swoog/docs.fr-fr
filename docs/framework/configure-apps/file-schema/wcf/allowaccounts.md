---
title: '&lt;allowAccounts&gt;'
ms.date: 03/30/2017
ms.assetid: 166923a9-a8ac-478f-92f9-529d9667f3a6
ms.openlocfilehash: bbfe0d5d531cf61c01f95d0e82ce0f894031d6f3
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltallowaccountsgt"></a>&lt;allowAccounts&gt;
Contient une collection d’éléments de configuration qui spécifient l’utilisateur des comptes pour les processus qui hébergent les services Windows Communication Foundation (WCF) et qui disposent d’accès à la connexion au service de partage.  
  
 \<system.serviceModel.activation>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<allowAccounts>  
   <add securityIdentifier="String"/>  
</allowAccounts>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Attribut|Description|  
|---------------|-----------------|  
|[\<add>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-allowaccounts.md)|Ajoute un compte d'utilisateur pour les processus qui hébergent des services [!INCLUDE[indigo2](../../../../../includes/indigo2-md.md)] et qui disposent d'un accès de connexion au service de partage|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<NET.PIPE >](../../../../../docs/framework/configure-apps/file-schema/wcf/net-pipe.md) ou [ \<net.tcp >](../../../../../docs/framework/configure-apps/file-schema/wcf/net-tcp.md)|Spécifie les paramètres de configuration pour le canal du réseau ou les services de partage TCP.|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Activation.Configuration.NetTcpSection.AllowAccounts%2A>  
 <xref:System.ServiceModel.Activation.Configuration.NetPipeSection.AllowAccounts%2A>  
 <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElementCollection>  
 <xref:System.ServiceModel.Activation.Configuration.SecurityIdentifierElement>
