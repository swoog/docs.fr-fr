---
title: <timeOuts>
ms.date: 03/30/2017
ms.assetid: 7fccd436-b326-48ec-8de1-c16817a09e0d
ms.openlocfilehash: b6ae5faa2dd2ffef9669a0245a75227b0f669cf7
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59118064"
---
# <a name="timeouts"></a>\<timeOuts>
Représente un élément de configuration qui spécifie l'intervalle de temps pendant lequel l'ouverture ou la fermeture de l'hôte de service est autorisée.  
  
 \<system.ServiceModel>  
\<client>  
\<endpoint>  
\<host>  
\<timeOuts>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<timeOuts closeTimeout="TimeSpan"
          openTimeout="TimeSpan" />
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`closeTimeout`|Valeur de type <xref:System.TimeSpan> qui spécifie l'intervalle de temps pendant lequel la fermeture de l'hôte de service est autorisée.|  
|`openTimeout`|Valeur de type <xref:System.TimeSpan> qui spécifie l'intervalle de temps pendant lequel l'ouverture de l'hôte de service est autorisée.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<host>](../../../../../docs/framework/configure-apps/file-schema/wcf/host.md)|Élément de configuration qui spécifie des paramètres pour un hôte de service.|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Configuration.HostElement>
- <xref:System.ServiceModel.ServiceHost>
- [Hébergement](../../../../../docs/framework/wcf/feature-details/hosting.md)
