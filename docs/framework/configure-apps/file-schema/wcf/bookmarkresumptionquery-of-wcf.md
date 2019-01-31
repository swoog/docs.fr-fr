---
title: <bookmarkResumptionQuery> de WCF
ms.date: 03/30/2017
ms.assetid: 755a34f0-87c9-4a1e-ae4d-0fb8a6fbdc0e
ms.openlocfilehash: 38c87cefc49821b03d119299ef60e3fbbad21d7e
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55255114"
---
# <a name="bookmarkresumptionquery-of-wcf"></a>\<bookmarkResumptionQuery > de WCF

Représente une requête qui permet d'effectuer le suivi de la reprise d'un signet dans une instance de flux de travail. La requête est nécessaire pour qu'un participant au suivi puisse s'abonner à des enregistrements de reprise de signet.  
  
Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
  
\<system.serviceModel>  
\<tracking>  
\<profiles>  
\<trackingProfile>  
\<workflow>  
\<bookmarkResumptionQueries>  
\<bookmarkResumptionQuery>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <bookmarkResumptionQueries>
          <bookmarkResumptionQuery name="String" />
        </bookmarkResumptionQueries>
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
|`name`|Chaîne qui spécifie le nom de l'enregistrement de signet auquel s'abonner.|  
  
### <a name="child-elements"></a>Éléments enfants

Aucun.
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<bookmarkResumptionQueries>](bookmarkresumptionqueries-of-wcf.md)|Représente une collection de requêtes qui permettent d’effectuer le suivi de la reprise d’un signet dans une instance de flux de travail.|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.ServiceModel.Activities.Tracking.Configuration.BookmarkResumptionQueryElementCollection?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.BookmarkResumptionQuery?displayProperty=nameWithType>
- [Suivi et traçage de workflow](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [Profils de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
