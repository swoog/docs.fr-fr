---
title: '&lt;activityScheduledQuery&gt; de WCF'
ms.date: 03/30/2017
ms.assetid: 25f6eee1-3d98-4c39-b517-c0813f03f106
ms.openlocfilehash: a3c4c8b338921c9d949edd83deb4d6073eb26b55
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49123369"
---
# <a name="ltactivityscheduledquerygt-of-wcf"></a>&lt;activityScheduledQuery&gt; de WCF

Représente une collection de requêtes qui permettent d’effectuer le suivi d’une activité dont l’exécution par une activité parent est planifiée. La requête est nécessaire pour qu'un participant au suivi puisse s'abonner aux enregistrements d'une activité planifiée.  
  
Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)  
  
\<system.serviceModel>  
\<suivi >  
\<profils >  
\<trackingProfile >  
\<flux de travail >  
\<activityScheduledQueries >  
\<activityScheduledQuery >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <activityScheduledQueries>
          <activityScheduledQuery activityName="String"   
                                  childActivityName="String"/>
        </activityScheduledQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking> 
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  

Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`activityName`|Chaîne qui spécifie le nom de l'activité demandant l'annulation.|  
|`childActivityName`|Chaîne qui spécifie le nom de l'activité enfant pour laquelle l'annulation a été demandée.|  
  
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<activityScheduledQueries>](activityscheduledqueries-of-wcf.md)|Une collection de requêtes qui sont utilisés pour suivre une activité planifiée pour l’exécution d’une activité parente.|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElement>
- <xref:System.Activities.Tracking.ActivityScheduledQuery>
- [Suivi et traçage de workflow](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [Profils de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
