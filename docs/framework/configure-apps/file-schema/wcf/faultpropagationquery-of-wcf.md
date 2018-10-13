---
title: '&lt;faultPropagationQuery&gt; de WCF'
ms.date: 03/30/2017
ms.assetid: fabafbc8-3e45-4feb-8321-0725e9f4079c
ms.openlocfilehash: c3853c470a9243835e071d35008dfff5b885591d
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49123317"
---
# <a name="ltfaultpropagationquerygt-of-wcf"></a><span data-ttu-id="24a93-102">&lt;faultPropagationQuery&gt; de WCF</span><span class="sxs-lookup"><span data-stu-id="24a93-102">&lt;faultPropagationQuery&gt; of WCF</span></span>

<span data-ttu-id="24a93-103">Représente une requête qui permet d'effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="24a93-103">Represents a query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="24a93-104">Cet événement se produit chaque fois qu'un FaultHandler traite une erreur.</span><span class="sxs-lookup"><span data-stu-id="24a93-104">This event occurs each time a FaultHandler processes a fault.</span></span> <span data-ttu-id="24a93-105">Vous devez utiliser cette requête pour effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="24a93-105">You should use such query to track the handling of faults that occur within an activity.</span></span> <span data-ttu-id="24a93-106">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner aux enregistrements de propagation d'erreur.</span><span class="sxs-lookup"><span data-stu-id="24a93-106">The query is necessary for a  tracking participant to subscribe to fault propagation records.</span></span>  
  
<span data-ttu-id="24a93-107">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="24a93-107">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="24a93-108">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="24a93-108">\<system.serviceModel></span></span>  
<span data-ttu-id="24a93-109">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="24a93-109">\<tracking></span></span>  
<span data-ttu-id="24a93-110">\<profils ></span><span class="sxs-lookup"><span data-stu-id="24a93-110">\<profiles></span></span>  
<span data-ttu-id="24a93-111">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="24a93-111">\<trackingProfile></span></span>  
<span data-ttu-id="24a93-112">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="24a93-112">\<workflow></span></span>  
<span data-ttu-id="24a93-113">\<faultPropagationQueries ></span><span class="sxs-lookup"><span data-stu-id="24a93-113">\<faultPropagationQueries></span></span>  
<span data-ttu-id="24a93-114">\<faultPropagationQuery ></span><span class="sxs-lookup"><span data-stu-id="24a93-114">\<faultPropagationQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="24a93-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24a93-115">Syntax</span></span>  
  
```xml
<tracking>
  <profiles>
    <trackingProfile name="Name">
      <workflow>
        <faultPropagationQueries>
          <faultPropagationQuery faultSourceActivityName="String"
                                 faultHandlerActivityName="String"/>
        </faultPropagationQueries>
      </workflow>
    </trackingProfile>
  </profiles>
</tracking>
```
  
## <a name="attributes-and-elements"></a><span data-ttu-id="24a93-116">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="24a93-116">Attributes and elements</span></span>

<span data-ttu-id="24a93-117">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="24a93-117">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="24a93-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="24a93-118">Attributes</span></span>  
  
|<span data-ttu-id="24a93-119">Attribut</span><span class="sxs-lookup"><span data-stu-id="24a93-119">Attribute</span></span>|<span data-ttu-id="24a93-120">Description</span><span class="sxs-lookup"><span data-stu-id="24a93-120">Description</span></span>|  
|---------------|-----------------|  
|`faultSourceActivityName`|<span data-ttu-id="24a93-121">Chaîne qui spécifie le nom de l'activité de gestionnaire d'erreur qui a propagé l'erreur.</span><span class="sxs-lookup"><span data-stu-id="24a93-121">A string that specifies the name of the fault hander activity that propagated the fault.</span></span> <span data-ttu-id="24a93-122">La valeur par défaut est \*, ce qui indique que les enregistrements de propagation d’erreur sont retournés pour toutes les activités.</span><span class="sxs-lookup"><span data-stu-id="24a93-122">The default is \*, which indicates that fault propagation records are returned for all activities.</span></span>|  
|`faultHandlerActivityName`|<span data-ttu-id="24a93-123">Chaîne qui spécifie le nom de l'activité à l'origine de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="24a93-123">A string that specifies the name of the activity that was the source of the fault.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="24a93-124">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="24a93-124">Child elements</span></span>

<span data-ttu-id="24a93-125">Aucun.</span><span class="sxs-lookup"><span data-stu-id="24a93-125">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="24a93-126">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="24a93-126">Parent elements</span></span>  
  
|<span data-ttu-id="24a93-127">Élément</span><span class="sxs-lookup"><span data-stu-id="24a93-127">Element</span></span>|<span data-ttu-id="24a93-128">Description</span><span class="sxs-lookup"><span data-stu-id="24a93-128">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="24a93-129">\<faultPropagationQueries></span><span class="sxs-lookup"><span data-stu-id="24a93-129">\<faultPropagationQueries></span></span>](faultpropagationqueries-of-wcf.md)|<span data-ttu-id="24a93-130">Représente une liste des éléments de configuration qui permettent d'effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="24a93-130">Represents a list of configuration elements that are used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="24a93-131">Cet événement se produit chaque fois qu'un FaultHandler traite une erreur.</span><span class="sxs-lookup"><span data-stu-id="24a93-131">This event occurs each time a FaultHandler processes a fault.</span></span>|
  
## <a name="see-also"></a><span data-ttu-id="24a93-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24a93-132">See also</span></span>  
 
- <xref:System.ServiceModel.Activities.Tracking.Configuration.FaultPropagationQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.FaultPropagationQuery?displayProperty=nameWithType>
- [<span data-ttu-id="24a93-133">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="24a93-133">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="24a93-134">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="24a93-134">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
