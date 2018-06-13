---
title: '&lt;callbackTimeouts&gt;'
ms.date: 03/30/2017
ms.assetid: d7fcfc5f-6d35-491e-8fa6-2f964c1e792f
ms.openlocfilehash: 48da0351d162a2143a26cc5b9eaa05b731358639
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32749564"
---
# <a name="ltcallbacktimeoutsgt"></a>&lt;callbackTimeouts&gt;
Spécifie la valeur du délai d’attente lors du transfert de transactions du serveur vers un client dans un scénario de contrat de rappel duplex.  
  
 \<system.ServiceModel>  
\<comportements >  
\<endpointBehaviors >  
\<comportement >  
\<callbackTimeOuts >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<callbackTimeOuts transactionTimeout="TimeSpan" />  
```  
  
## <a name="type"></a>Type  
 `Type`  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`transactionTimeout`|Valeur <xref:System.TimeSpan> qui spécifie l'intervalle au cours duquel les transactions doivent être automatiquement effectuées ou arrêtées. La valeur par défaut est « 00 : 00:00 ».|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<behavior>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|Spécifie un comportement de point de terminaison.|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Configuration.CallbackTimeoutsElement>
