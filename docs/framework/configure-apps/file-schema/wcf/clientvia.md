---
title: '&lt;clientVia&gt;'
ms.date: 03/30/2017
ms.assetid: c27ee94e-babd-459b-9574-2a6d67d11314
ms.openlocfilehash: 6218bb3f205f2825eb3f10fabf834cfd0396ac87
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltclientviagt"></a>&lt;clientVia&gt;
Spécifie l'URI pour lequel le canal de transport doit être créé. Pour plus d'informations, consultez <xref:System.ServiceModel.Description.ClientViaBehavior>.  
  
 \<system.ServiceModel>  
\<comportements >  
\<endpointBehaviors >  
\<comportement >  
\<clientVia >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<clientVia viaUri="String"/>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`viaUri`|Chaîne qui spécifie un URI indiquant l'itinéraire d'un message.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<behavior>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|Spécifie un comportement de point de terminaison.|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Configuration.ClientViaElement>  
 <xref:System.ServiceModel.Description.ClientViaBehavior>
