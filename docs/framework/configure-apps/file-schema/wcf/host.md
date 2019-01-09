---
title: '&lt;Hôte&gt;'
ms.date: 03/30/2017
ms.assetid: be566d55-9d50-4b2e-985d-52a5cc26cbbb
ms.openlocfilehash: afa9d65223ab3a7730a55bc41ed98458707b32db
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145222"
---
# <a name="lthostgt"></a>&lt;Hôte&gt;
Spécifie les paramètres d'un hôte de service.  
  
 \<system.ServiceModel>  
\<services>  
\<service >  
\<hôte >  
  
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
|[\<BaseAddress >](../../../../../docs/framework/configure-apps/file-schema/wcf/baseaddresses.md)|Collection d’éléments `baseAddress` qui spécifie les adresses de base utilisées par l’hôte de service.|  
|[\<délais d’attente >](../../../../../docs/framework/configure-apps/file-schema/wcf/timeouts.md)|Élément de configuration qui spécifie la durée d'ouverture ou de fermeture autorisée de l'hôte de service.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<service>](../../../../../docs/framework/configure-apps/file-schema/wcf/service.md)|Spécifie les paramètres pour un service Windows Communication Foundation (WCF).|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Configuration.HostElement>  
 <xref:System.ServiceModel.ServiceHost>  
 [Hébergement](../../../../../docs/framework/wcf/feature-details/hosting.md)
