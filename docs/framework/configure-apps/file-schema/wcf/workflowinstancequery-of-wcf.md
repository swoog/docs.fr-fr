---
title: <workflowInstanceQuery> de WCF
ms.date: 03/30/2017
ms.assetid: 35c73f9d-474e-42eb-874d-ddc04b1987f3
ms.openlocfilehash: 726d4db3bad9f57663790e2bb4e081faba28f1ef
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61672963"
---
# <a name="workflowinstancequery-of-wcf"></a>\<workflowInstanceQuery > de WCF

Représente une requête qui effectue le suivi des changements dans le cycle de vie d'une instance de flux de travail, tels que le début et la fin d'un événement.  
  
Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)  
  
\<system.serviceModel>  
\<tracking>  
\<profiles>  
\<trackingProfile>  
\<workflow>  
\<workflowInstanceQueries>  
\<workflowInstanceQuery>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <workflowInstanceQueries>
          <workflowInstanceQuery>
            <states>
              <state name="Name" />
            </states>
          </workflowInstanceQuery>
        </workflowInstanceQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  

Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  

Aucun.  
  
### <a name="child-elements"></a>Éléments enfants  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<states>](states-of-wcf-workflowinstancequery.md)|Collection d'états faisant l'objet d'un abonnement dans l'instance de flux de travail suivie lors de la création des enregistrements de suivi.|  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<workflowInstanceQueries>](workflowinstancequeries-of-wcf.md)|Représente une collection d'éléments de configuration qui effectuent le suivi des changements dans le cycle de vie d'une instance de flux de travail, tels que le début ou la fin d'un événement.|  
  
## <a name="remarks"></a>Notes  

L'objet <xref:System.Activities.Tracking.WorkflowInstanceQuery> sert à s'abonner aux objets <xref:System.Activities.Tracking.TrackingRecord> suivants :  
  
- <xref:System.Activities.Tracking.WorkflowInstanceRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceAbortedRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceUnhandledExceptionRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceTerminatedRecord>  
  
- <xref:System.Activities.Tracking.WorkflowInstanceSuspendedRecord>  
  
## <a name="example"></a>Exemple  

La configuration suivante permet de s'abonner aux enregistrements de suivi au niveau de l'instance de flux de travail pour l'état de l'instance `Started` à l'aide de cette requête.  
  
```xml  
<workflowInstanceQueries>
  <workflowInstanceQuery>
    <states>
      <state name="Started" />
    </states>
  </workflowInstanceQuery>
</workflowInstanceQueries>
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Activities.Tracking.Configuration.WorkflowInstanceQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.WorkflowInstanceQuery?displayProperty=nameWithType>
- [Suivi et traçage de workflow](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [Profils de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
