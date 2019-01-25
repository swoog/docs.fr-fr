---
title: '&lt;faultPropagationQuery&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 4fb5c2b1-3dad-4eca-9c7f-3efb51899813
ms.openlocfilehash: a91a6f61b39a780ed48ad8d5f5e0dfb9ef60da39
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54538334"
---
# <a name="ltfaultpropagationquerygt"></a><span data-ttu-id="70342-102">&lt;faultPropagationQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="70342-102">&lt;faultPropagationQuery&gt;</span></span>
<span data-ttu-id="70342-103">Représente une requête qui permet d'effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="70342-103">Represents a query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="70342-104">Cet événement se produit chaque fois qu'un FaultHandler traite une erreur.</span><span class="sxs-lookup"><span data-stu-id="70342-104">This event occurs each time a FaultHandler processes a fault.</span></span> <span data-ttu-id="70342-105">Vous devez utiliser cette requête pour effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="70342-105">You should use such query to track the handling of faults that occur within an activity.</span></span> <span data-ttu-id="70342-106">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner aux enregistrements de propagation d'erreur.</span><span class="sxs-lookup"><span data-stu-id="70342-106">The query is necessary for a  tracking participant to subscribe to fault propagation records.</span></span>  
  
 <span data-ttu-id="70342-107">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="70342-107">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>  
  
<span data-ttu-id="70342-108">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="70342-108">\<system.serviceModel></span></span>  
<span data-ttu-id="70342-109">\<tracking></span><span class="sxs-lookup"><span data-stu-id="70342-109">\<tracking></span></span>  
<span data-ttu-id="70342-110">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="70342-110">\<trackingProfile></span></span>  
<span data-ttu-id="70342-111">\<workflow></span><span class="sxs-lookup"><span data-stu-id="70342-111">\<workflow></span></span>  
<span data-ttu-id="70342-112">\<faultPropagationQueries></span><span class="sxs-lookup"><span data-stu-id="70342-112">\<faultPropagationQueries></span></span>  
<span data-ttu-id="70342-113">\<faultPropagationQuery></span><span class="sxs-lookup"><span data-stu-id="70342-113">\<faultPropagationQuery></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="70342-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70342-114">Syntax</span></span>  
  
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
  
## <a name="attributes-and-elements"></a><span data-ttu-id="70342-115">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="70342-115">Attributes and Elements</span></span>  
 <span data-ttu-id="70342-116">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="70342-116">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="70342-117">Attributs</span><span class="sxs-lookup"><span data-stu-id="70342-117">Attributes</span></span>  
  
|<span data-ttu-id="70342-118">Attribut</span><span class="sxs-lookup"><span data-stu-id="70342-118">Attribute</span></span>|<span data-ttu-id="70342-119">Description</span><span class="sxs-lookup"><span data-stu-id="70342-119">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="70342-120">activityName</span><span class="sxs-lookup"><span data-stu-id="70342-120">activityName</span></span>|<span data-ttu-id="70342-121">Chaîne qui spécifie le nom de l'activité de gestionnaire d'erreur qui a propagé l'erreur.</span><span class="sxs-lookup"><span data-stu-id="70342-121">A string that specifies the name of the fault hander activity that propagated the fault.</span></span> <span data-ttu-id="70342-122">La valeur par défaut est \*, qui indique que des enregistrements de propagation d'erreur sont retournés pour toutes les activités.</span><span class="sxs-lookup"><span data-stu-id="70342-122">The default is \*, which indicates that fault propagation records are returned for all activities.</span></span>|  
|<span data-ttu-id="70342-123">faultHandlerActivityName</span><span class="sxs-lookup"><span data-stu-id="70342-123">faultHandlerActivityName</span></span>|<span data-ttu-id="70342-124">Chaîne qui spécifie le nom de l'activité à l'origine de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="70342-124">A string that specifies the name of the activity that was the source of the fault.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="70342-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="70342-125">Child Elements</span></span>  
 <span data-ttu-id="70342-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="70342-126">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="70342-127">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="70342-127">Parent Elements</span></span>  
  
|<span data-ttu-id="70342-128">Élément</span><span class="sxs-lookup"><span data-stu-id="70342-128">Element</span></span>|<span data-ttu-id="70342-129">Description</span><span class="sxs-lookup"><span data-stu-id="70342-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="70342-130">\<faultPropagationQueries></span><span class="sxs-lookup"><span data-stu-id="70342-130">\<faultPropagationQueries></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/faultpropagationqueries.md)|<span data-ttu-id="70342-131">Représente une liste des éléments de configuration qui permettent d'effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="70342-131">Represents a list of configuration elements that are used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="70342-132">Cet événement se produit chaque fois qu'un FaultHandler traite une erreur.</span><span class="sxs-lookup"><span data-stu-id="70342-132">This event occurs each time a FaultHandler processes a fault.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="70342-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70342-133">See also</span></span>
- <xref:System.ServiceModel.Activities.Tracking.Configuration.FaultPropagationQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.FaultPropagationQuery?displayProperty=nameWithType>
- [<span data-ttu-id="70342-134">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="70342-134">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="70342-135">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="70342-135">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
