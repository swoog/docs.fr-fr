---
title: '&lt;faultPropagationQuery&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 4fb5c2b1-3dad-4eca-9c7f-3efb51899813
ms.openlocfilehash: 3c8038c133eb7f7a8d47c950037332fa68aa065e
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltfaultpropagationquerygt"></a><span data-ttu-id="0dd36-102">&lt;faultPropagationQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="0dd36-102">&lt;faultPropagationQuery&gt;</span></span>
<span data-ttu-id="0dd36-103">Représente une requête qui permet d'effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="0dd36-103">Represents a query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="0dd36-104">Cet événement se produit chaque fois qu'un FaultHandler traite une erreur.</span><span class="sxs-lookup"><span data-stu-id="0dd36-104">This event occurs each time a FaultHandler processes a fault.</span></span> <span data-ttu-id="0dd36-105">Vous devez utiliser cette requête pour effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="0dd36-105">You should use such query to track the handling of faults that occur within an activity.</span></span> <span data-ttu-id="0dd36-106">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner aux enregistrements de propagation d'erreur.</span><span class="sxs-lookup"><span data-stu-id="0dd36-106">The query is necessary for a  tracking participant to subscribe to fault propagation records.</span></span>  
  
 <span data-ttu-id="0dd36-107">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="0dd36-107">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="0dd36-108">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="0dd36-108">\<system.serviceModel></span></span>  
<span data-ttu-id="0dd36-109">\<suivi ></span><span class="sxs-lookup"><span data-stu-id="0dd36-109">\<tracking></span></span>  
<span data-ttu-id="0dd36-110">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="0dd36-110">\<trackingProfile></span></span>  
<span data-ttu-id="0dd36-111">\<flux de travail ></span><span class="sxs-lookup"><span data-stu-id="0dd36-111">\<workflow></span></span>  
<span data-ttu-id="0dd36-112">\<faultPropagationQueries ></span><span class="sxs-lookup"><span data-stu-id="0dd36-112">\<faultPropagationQueries></span></span>  
<span data-ttu-id="0dd36-113">\<faultPropagationQuery ></span><span class="sxs-lookup"><span data-stu-id="0dd36-113">\<faultPropagationQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0dd36-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0dd36-114">Syntax</span></span>  
  
```xml  
<tracking>
  <trackingProfile name="Name">
    <workflow>
      <faultPropagationQueries>
        <faultPropagationQuery activityName="String" 
                               faultHandlerActivityName="String" />
      </faultPropagationQueries>
    </workflow>
  </trackingProfile>
</tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0dd36-115">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="0dd36-115">Attributes and Elements</span></span>  
 <span data-ttu-id="0dd36-116">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="0dd36-116">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0dd36-117">Attributs</span><span class="sxs-lookup"><span data-stu-id="0dd36-117">Attributes</span></span>  
  
|<span data-ttu-id="0dd36-118">Attribut</span><span class="sxs-lookup"><span data-stu-id="0dd36-118">Attribute</span></span>|<span data-ttu-id="0dd36-119">Description</span><span class="sxs-lookup"><span data-stu-id="0dd36-119">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="0dd36-120">activityName</span><span class="sxs-lookup"><span data-stu-id="0dd36-120">activityName</span></span>|<span data-ttu-id="0dd36-121">Chaîne qui spécifie le nom de l'activité de gestionnaire d'erreur qui a propagé l'erreur.</span><span class="sxs-lookup"><span data-stu-id="0dd36-121">A string that specifies the name of the fault hander activity that propagated the fault.</span></span> <span data-ttu-id="0dd36-122">La valeur par défaut est \*, qui indique que des enregistrements de propagation d'erreur sont retournés pour toutes les activités.</span><span class="sxs-lookup"><span data-stu-id="0dd36-122">The default is \*, which indicates that fault propagation records are returned for all activities.</span></span>|  
|<span data-ttu-id="0dd36-123">faultHandlerActivityName</span><span class="sxs-lookup"><span data-stu-id="0dd36-123">faultHandlerActivityName</span></span>|<span data-ttu-id="0dd36-124">Chaîne qui spécifie le nom de l'activité à l'origine de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="0dd36-124">A string that specifies the name of the activity that was the source of the fault.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0dd36-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0dd36-125">Child Elements</span></span>  
 <span data-ttu-id="0dd36-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0dd36-126">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="0dd36-127">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0dd36-127">Parent Elements</span></span>  
  
|<span data-ttu-id="0dd36-128">Élément</span><span class="sxs-lookup"><span data-stu-id="0dd36-128">Element</span></span>|<span data-ttu-id="0dd36-129">Description</span><span class="sxs-lookup"><span data-stu-id="0dd36-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0dd36-130">\<faultPropagationQueries></span><span class="sxs-lookup"><span data-stu-id="0dd36-130">\<faultPropagationQueries></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/faultpropagationqueries.md)|<span data-ttu-id="0dd36-131">Représente une liste des éléments de configuration qui permettent d'effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="0dd36-131">Represents a list of configuration elements that are used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="0dd36-132">Cet événement se produit chaque fois qu'un FaultHandler traite une erreur.</span><span class="sxs-lookup"><span data-stu-id="0dd36-132">This event occurs each time a FaultHandler processes a fault.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0dd36-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0dd36-133">See Also</span></span>  
 <xref:System.ServiceModel.Activities.Tracking.Configuration.FaultPropagationQueryElement?displayProperty=nameWithType>       
 <xref:System.Activities.Tracking.FaultPropagationQuery?displayProperty=nameWithType>       
 [<span data-ttu-id="0dd36-134">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="0dd36-134">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="0dd36-135">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="0dd36-135">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
