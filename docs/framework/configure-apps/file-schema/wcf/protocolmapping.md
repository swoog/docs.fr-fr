---
title: '&lt;protocolMapping&gt;'
ms.date: 03/30/2017
ms.assetid: 5076644b-1f33-4f26-9488-87de9fcda04c
ms.openlocfilehash: 4afdaaa62c1ac3241eb7382d0995bed51bde73e2
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltprotocolmappinggt"></a>&lt;protocolMapping&gt;
Représente une section de configuration pour définir un ensemble de mappage de protocole par défaut entre les schémas de protocole de transport (par exemple, http, net.tcp, net.pipe, etc.) et des liaisons WCF. Lors de la création de points de terminaison par défaut lors de l’exécution, Windows Communication Foundation (WCF) examine les mappages configurés et décide de liaison à utiliser en une adresse de base.  
  
 \<system.serviceModel>  
\<protocolMapping >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml
   <protocolMapping>    <add binding="String"         bindingConfiguration="String"         scheme="http/net.msmq/net.pipe/net.tcp"/></protocolMapping>  
```

## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<filtres >](../../../../../docs/framework/configure-apps/file-schema/wcf/filters-of-routing.md)|Contient un mappage de protocole par défaut entre un schéma de protocole de transport (par exemple, http, net.tcp, net.pipe, etc.) et une liaison WCF.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|system.ServiceModel|Élément racine de tous les éléments de configuration WCF.|  
  
## <a name="example"></a>Exemple  
 L'exemple de configuration suivant montre le mappage de protocole par défaut dans le fichier machine.config. Vous pouvez remplacer ce mappage par défaut au niveau de l'ordinateur en modifiant le fichier machine.config. Ou, si vous souhaitez uniquement le remplacer dans la portée d'une application, vous pouvez remplacer cette section dans le fichier de configuration de votre application et modifier le mappage pour les schémas de protocole individuels.  
  
```xml  
<protocolMapping>  
        <add scheme="http" binding="basicHttpBinding"/>  
        <add scheme="net.tcp" binding="netTcpBinding"/>  
        <add scheme="net.pipe" binding="netNamedPipeBinding"/>  
        <add scheme="net.msmq" binding="netMsmqBinding"/>  
</protocolMapping>  
```  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Configuration.ProtocolMappingSection?displayProperty=nameWithType>       
 <xref:System.ServiceModel.Configuration.ProtocolMappingElement?displayProperty=nameWithType>    
