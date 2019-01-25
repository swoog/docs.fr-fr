---
title: '&lt;serviceActivations&gt;'
ms.date: 03/30/2017
ms.assetid: 97e665b6-1c51-410b-928a-9bb42c954ddb
ms.openlocfilehash: 5da05c7b6a9685b9e34b3181ce8e0bd31ccd052b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54704954"
---
# <a name="ltserviceactivationsgt"></a>&lt;serviceActivations&gt;
Un élément de configuration qui vous permet d’ajouter des paramètres qui définissent les paramètres d’activation de service virtuel qui correspondent à vos types de service Windows Communication Foundation (WCF). Cela permet d'activer des services hébergés dans WAS/IIS sans utiliser de fichier .svc.  
  
 \<system.ServiceModel>  
\<serviceHostingEnvironment>  
\<serviceActivations>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<serviceHostingEnvironment>
  <serviceActivations>
    <add factory="String"
         service="String" />
  </serviceActivations>
</serviceHostingEnvironment>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<add>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-serviceactivations.md)|Ajoute un élément de configuration qui spécifie l'activation d'une application de service.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<serviceHostingEnvironment>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicehostingenvironment.md)|Définit le type instancié par l'environnement d'hébergement du service pour un transport particulier.|  
  
## <a name="remarks"></a>Notes  
 L'exemple suivant indique comment configurer des paramètres d'activation dans le fichier web.config.  
  
```xml  
<configuration>
  <system.serviceModel>
    <serviceHostingEnvironment>
      <serviceActivations>
        <add service="GreetingService" />
      </serviceActivations>
    </serviceHostingEnvironment>
  </system.serviceModel>
</configuration>
```  
  
 Cette configuration vous permet d'activer GreetingService sans utiliser de fichier .svc.  
  
 Notez que `<serviceHostingEnvironment>` est une configuration au niveau de l'application. Vous devez placer le `web.config` qui contient la configuration sous la racine de l'application virtuelle. De plus, `serviceHostingEnvironment` est une section machinetoApplication qui peut être héritée. Si vous inscrivez un seul service à la racine de l'ordinateur, chaque service dans l'application hérite de celui-ci.  
  
 L'activation basée sur la configuration prend en charge l'activation via un protocole HTTP ou non-HTTP. Elle requiert des extensions dans relativeAddress, par exemple .svc, .xoml ou .xamlx. Vous pouvez mapper vos propres extensions au buildProviders connu, qui vous permet ensuite d’activer le service sur n’importe quelle extension. En cas de conflit, la section `<serviceActivations>` remplace les inscriptions .svc.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.Configuration.ServiceActivationElementCollection>
- <xref:System.ServiceModel.Configuration.ServiceHostingEnvironmentSection>
- <xref:System.ServiceModel.ServiceHostingEnvironment>
