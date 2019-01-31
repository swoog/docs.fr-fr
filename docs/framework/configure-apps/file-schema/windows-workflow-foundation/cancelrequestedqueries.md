---
title: <cancelRequestedQueries>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: eab5af7e-76fa-434d-9d36-873e995cee05
ms.openlocfilehash: 989d6e99457108336c38fb1eece4c9ac2444c974
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271497"
---
# <a name="cancelrequestedqueries"></a>\<cancelRequestedQueries>
Représente une collection de requêtes qui permettent d’effectuer le suivi des demandes d’annulation d’une activité enfant par l’activité parent. La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement de demande d'annulation.  
  
 Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)  
  
\<system.serviceModel>  
\<tracking>  
\<trackingProfile>  
\<workflow>  
\<cancelRequestedQueries>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <cancelRequestQueries>
        <cancelRequestQuery activityName="String" 
                            childActivityName="String"/>
      </cancelRequestQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
 Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<cancelRequestedQuery>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/cancelrequestedquery.md)|Requête qui permet d'effectuer le suivi des demande d'annulation d'une activité enfant par l'activité parent.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<workflow>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|Un élément de configuration qui contient toutes les requêtes pour un flux de travail spécifique identifié par le **activityDefinitionId** propriété.|  
  
## <a name="see-also"></a>Voir aussi
- [Suivi et traçage de workflow](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [Profils de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
