---
title: '&lt;host&gt;'
ms.date: 03/30/2017
ms.assetid: be566d55-9d50-4b2e-985d-52a5cc26cbbb
ms.openlocfilehash: 1fb35058d407d0fbae78092bb4ccd45b0aaa40e6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54702026"
---
# <a name="lthostgt"></a>&lt;host&gt;
Spécifie les paramètres d'un hôte de service.  
  
 \<system.ServiceModel>  
\<services>  
\<service>  
\<host>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<host>
  <baseAddresses>
    <add baseAddress="string" />
  </baseAddresses>
  <timeOuts closeTimeout="TimeSpan"
            openTimeout="TimeSpan" />
</host>
```  
  
## <a name="type"></a>Type  
 `Type`  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<baseAddresses>](../../../../../docs/framework/configure-apps/file-schema/wcf/baseaddresses.md)|Collection d’éléments `baseAddress` qui spécifie les adresses de base utilisées par l’hôte de service.|  
|[\<timeOuts>](../../../../../docs/framework/configure-apps/file-schema/wcf/timeouts.md)|Élément de configuration qui spécifie la durée d'ouverture ou de fermeture autorisée de l'hôte de service.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<service>](../../../../../docs/framework/configure-apps/file-schema/wcf/service.md)|Spécifie les paramètres pour un service Windows Communication Foundation (WCF).|  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.Configuration.HostElement>
- <xref:System.ServiceModel.ServiceHost>
- [Hébergement](../../../../../docs/framework/wcf/feature-details/hosting.md)
