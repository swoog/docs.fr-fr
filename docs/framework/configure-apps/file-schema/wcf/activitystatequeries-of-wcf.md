---
title: '&lt;activityStateQueries&gt; de WCF'
ms.date: 10/08/2018
ms.assetid: 9e45db49-ed85-4fdf-bd65-0d5477e31823
ms.openlocfilehash: 081dc297912ed5735dd51111936b85b61f463d2d
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49123239"
---
# <a name="ltactivitystatequeriesgt-of-wcf"></a>&lt;activityStateQueries&gt; de WCF

Représente une collection de requêtes qui permettent d’effectuer le suivi des changements dans le cycle de vie des activités qui composent une instance de workflow. Par exemple, vous souhaiterez effectuer le suivi de chaque fois que l’activité « Envoyer un message électronique » se termine dans une instance de workflow. Cette requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des objets d'enregistrement d'état d'activité. Les états disponibles auxquels s'abonner sont spécifiés dans ActivityStates.

Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).

\<system.serviceModel>  
\<suivi >  
\<profils >  
\<trackingProfile >  
\<flux de travail >  
\<activityStateQueries >  

## <a name="syntax"></a>Syntaxe  
  
```xml
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <activityStateQueries>
          <activityStateQuery activityName="String">
            <arguments>
              <argument name="String"/>
            </arguments>
            <states>
              <state name="String"/>
            </states>
            <variables>
              <variable name="String"/>
            </variables>
          </activityStateQuery>
        </activityStateQueries>
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
|[\<activityStateQuery >](activitystatequery-of-wcf.md)|Requête utilisée pour effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.  Cet événement se produit chaque fois qu'un FaultHandler traite une erreur.|

### <a name="parent-elements"></a>Éléments parents

|Élément|Description|
|-------------|-----------------|
|[\<flux de travail >](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|Élément de configuration qui contient toutes les requêtes d'un flux de travail spécifique identifié par la propriété `activityDefinitionId`.|

## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityStateQueryElementCollection>    
- <xref:System.Activities.Tracking.ActivityStateQuery>    
- [Suivi et traçage de workflow](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
- [Profils de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
