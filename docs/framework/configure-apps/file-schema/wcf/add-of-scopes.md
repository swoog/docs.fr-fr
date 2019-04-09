---
title: <add> de <scopes>
ms.date: 03/30/2017
ms.assetid: 0563a7d8-fc84-4c85-9066-af32665857c2
ms.openlocfilehash: c29e47f688118e34fbdb4deb396c930d478f0582
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59187082"
---
# <a name="add-of-scopes"></a>\<Ajouter > de \<étendues >
Ajoute un URI de portée personnalisé qui permet de filtrer les points de terminaison de service pendant la requête.  
  
\<system.ServiceModel>  
\<behaviors>  
\<endpointBehaviors>  
\<behavior>  
\<endpointDiscovery>  
\<scopes>  
\<add>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<behaviors>
  <endpointBehaviors>
    <behavior name="String">
      <endpointDiscovery enable="Boolean">
        <scopes>
          <add scope="URI" />
        </scopes>
      </endpointDiscovery>
    </behavior>
  </endpointBehaviors>
</behaviors>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|portée|URI qui contient les informations de portée du point de terminaison à utiliser lors de la mise en correspondance des critères de recherche des services.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<scopes>](../../../../../docs/framework/configure-apps/file-schema/wcf/scopes.md)|Contient une collection d’éléments de configuration qui spécifient des URI de portée personnalisés à utiliser pour filtrer des points de terminaison de service pendant la requête.|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Discovery.EndpointDiscoveryBehavior>
