---
title: '&lt;add&gt; de &lt;serviceActivations&gt;'
ms.date: 03/30/2017
ms.assetid: e5b01fc8-ee84-48b7-95fd-95ab54fa871f
ms.openlocfilehash: b40127d531926f103f3e367c8721e8f5ff8e1a99
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54151538"
---
# <a name="ltaddgt-of-ltserviceactivationsgt"></a>&lt;add&gt; de &lt;serviceActivations&gt;
Un élément de configuration qui vous permet de définir les paramètres d’activation de service virtuel qui correspondent à vos types de service Windows Communication Foundation (WCF). Cela permet d'activer des services hébergés dans WAS/IIS sans utiliser de fichier .svc.  
  
 \<system.ServiceModel>  
\<serviceHostingEnvironment >  
  
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
  
|Attribut|Description|  
|---------------|-----------------|  
|factory|Chaîne qui spécifie le nom de type CLR de la fabrique qui génère un élément d'activation de service.|  
|service|Le ServiceType qui implémente le service (Typename qualifié complet ou Typename court (s'il est placé dans le dossier App_Code).|  
|relativeAddress|L'adresse relative dans l'application IIS active (par exemple « Service.svc ». Dans WCF 4.0 cette adresse relative doit contenir une des extensions de fichiers connues (.svc, .xamlx,…). Aucun fichier physique ne doit exister pour relativeUrl.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<serviceHostingEnvironment >](../../../../../docs/framework/configure-apps/file-schema/wcf/servicehostingenvironment.md)|Section de configuration qui décrit les paramètres d'activation.|  
  
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
 <xref:System.ServiceModel.Configuration.ServiceActivationElement>  
 <xref:System.ServiceModel.Configuration.ServiceHostingEnvironmentSection>  
 <xref:System.ServiceModel.ServiceHostingEnvironment>
