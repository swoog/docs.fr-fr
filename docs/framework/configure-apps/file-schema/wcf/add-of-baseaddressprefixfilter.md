---
title: '&lt;add&gt; de &lt;baseAddressPrefixFilter&gt;'
ms.date: 03/30/2017
ms.assetid: b226bede-8459-4de9-b2ac-3d39604ce2bc
ms.openlocfilehash: e4408488036be210e3a8b9cf8b8f8f8c2e669a1d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33365187"
---
# <a name="ltaddgt-of-ltbaseaddressprefixfiltergt"></a>&lt;add&gt; de &lt;baseAddressPrefixFilter&gt;
Représente un élément de configuration qui spécifie un filtre direct qui fournit un mécanisme permettant de sélectionner les liaisons de Internet Information Services (IIS) appropriées lors de l’hébergement d’une application Windows Communication Foundation (WCF) dans IIS.  
  
 \<system.ServiceModel>  
\<ServiceHostingEnvironment >  
\<baseAddressPrefixFilters >  
\<add>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<serviceHostingEnvironment>  
     <baseAddressPrefixFilters>  
        <add prefix="string"/>  
     </baseAddressPrefixFilters>  
</serviceHostingEnvironment>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|prefix|URI utilisé pour correspondre à une partie d'une adresse de base.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<baseAddressPrefixFilters >](../../../../../docs/framework/configure-apps/file-schema/wcf/baseaddressprefixfilters.md)|Une collection d’éléments de configuration qui spécifient des filtres directs qui fournissent un mécanisme permettant de sélectionner les liaisons IIS appropriées lors de l’hébergement d’une application Windows Communication Foundation (WCF) dans IIS.|  
  
## <a name="remarks"></a>Notes  
 Un filtre de préfixe permet aux fournisseurs d'hébergement partagé de spécifier les URI que le service doit utiliser. Il permet aux hôtes partagés d'héberger plusieurs applications avec différentes adresses de base pour la même méthode sur le même site.  
  
 Les sites Web IIS sont des conteneurs d'applications virtuelles qui contiennent des répertoires virtuels. L'application dans un site est accessible par le biais d'une ou de plusieurs liaisons IIS. Les liaisons IIS fournissent deux informations : un protocole de liaison et des informations de liaison. Le protocole de liaison (par exemple, HTTP) définit le modèle sur lequel la communication se produit, tandis que les informations de liaison (par exemple, adresse IP, port, en-tête de l'hôte) contiennent les données servant à accéder au site.  
  
 IIS prend en charge la spécification de plusieurs liaisons IIS pour chaque site, ce qui génère plusieurs adresses de base pour chaque méthode. Un service WCF hébergé sur un site autorise la liaison à une seule adresse de base pour chaque modèle, vous pouvez utiliser la fonctionnalité de filtre de préfixe pour choisir l’adresse de base requise du service hébergé. Les adresses de base entrantes, fournies par IIS, sont filtrées selon le filtre de la liste de préfixes facultative.  
  
 Par exemple, votre site peut contenir les adresses de base suivantes.  
  
```  
http://testl.fabrikam.com/Service.svc  
http://test2.fabrikam.com/Service.svc  
```  
  
 Vous pouvez utiliser le fichier de configuration suivant pour spécifier un filtre de préfixe au niveau AppDomain.  
  
```xml  
<system.serviceModel>  
  <serviceHostingEnvironment>  
     <baseAddressPrefixFilters>  
        <add prefix="net.tcp://test1.fabrikam.com:8000"/>  
        <add prefix="http://test2.fabrikam.com:9000"/>  
    </baseAddressPrefixFilters>  
  </serviceHostingEnvironment>  
</system.serviceModel>  
```  
  
 Dans cet exemple, `net.tcp://test1.fabrikam.com:8000` et `http://test2.fabrikam.com:9000` sont les seules adresses de base pouvant être transmises pour leur modèle respectif.  
  
 Par défaut, si aucun préfixe n'est spécifié, toutes les adresses sont transmises. La spécification du préfixe autorise uniquement la transmission de l'adresse de base correspondante pour ce modèle.  
  
> [!NOTE]
>  Le filtre ne prend pas en charge les caractères génériques. En outre, les adresses de base fournies par IIS peuvent avoir des adresses liées à d'autres modèles non présents dans la liste `baseAddressPrefixFilters`. Ces adresses ne sont pas éliminées par filtrage.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Configuration.BaseAddressPrefixFilterElement>  
 <xref:System.ServiceModel.Configuration.ServiceHostingEnvironmentSection>  
 <xref:System.ServiceModel.ServiceHostingEnvironment>  
 [Hébergement](../../../../../docs/framework/wcf/feature-details/hosting.md)
