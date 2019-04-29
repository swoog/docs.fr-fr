---
title: <scopes>
ms.date: 03/30/2017
ms.assetid: 9a0dd3ce-e383-4ac3-b7be-7d604388304a
ms.openlocfilehash: 8bc720238ca3039106345783381cd26134fc46b5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61670623"
---
# <a name="scopes"></a>\<scopes>
Contient une collection d’éléments de configuration qui spécifient des URI de portée personnalisés à utiliser pour filtrer des points de terminaison de service pendant la requête.  
  
\<system.ServiceModel>  
\<behaviors>  
\<endpointBehaviors>  
\<behavior>  
\<endpointDiscovery>  
\<scopes>  
  
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
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Attribut|Description|  
|---------------|-----------------|  
|[\<add>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-scopes.md)|Ajoute les informations de portée du point de terminaison à utiliser lors de la mise en correspondance des critères de recherche des services.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<endpointDiscovery>](../../../../../docs/framework/configure-apps/file-schema/wcf/endpointdiscovery.md)|Spécifie les différents paramètres de découverte d’un point de terminaison, tels que la fonctionnalité de découverte, les portées et toutes les extensions personnalisées de ses métadonnées.|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Discovery.EndpointDiscoveryBehavior>
