---
title: <faultPropagationQuery> de WCF
ms.date: 03/30/2017
ms.assetid: fabafbc8-3e45-4feb-8321-0725e9f4079c
ms.openlocfilehash: 1670f8fdf72bc202a4a595034f3818ab43b11be6
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55276053"
---
# <a name="faultpropagationquery-of-wcf"></a>\<faultPropagationQuery> of WCF

Représente une requête qui permet d'effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.  Cet événement se produit chaque fois qu'un FaultHandler traite une erreur. Vous devez utiliser cette requête pour effectuer le suivi de la gestion des erreurs qui se produisent dans une activité. La requête est nécessaire pour qu'un participant au suivi puisse s'abonner aux enregistrements de propagation d'erreur.  
  
Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).  
  
\<system.serviceModel>  
\<tracking>  
\<profiles>  
\<trackingProfile>  
\<workflow>  
\<faultPropagationQueries>  
\<faultPropagationQuery>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <faultPropagationQueries>
          <faultPropagationQuery faultSourceActivityName="String"
                                 faultHandlerActivityName="String" />
        </faultPropagationQueries>
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
|`faultSourceActivityName`|Chaîne qui spécifie le nom de l'activité de gestionnaire d'erreur qui a propagé l'erreur. La valeur par défaut est \*, ce qui indique que les enregistrements de propagation d’erreur sont retournés pour toutes les activités.|  
|`faultHandlerActivityName`|Chaîne qui spécifie le nom de l'activité à l'origine de l'erreur.|  
  
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<faultPropagationQueries>](faultpropagationqueries-of-wcf.md)|Représente une liste des éléments de configuration qui permettent d'effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.  Cet événement se produit chaque fois qu'un FaultHandler traite une erreur.|
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Activities.Tracking.Configuration.FaultPropagationQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.FaultPropagationQuery?displayProperty=nameWithType>
- [Suivi et traçage de workflow](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [Profils de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
