---
title: <faultPropagationQuery>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 4fb5c2b1-3dad-4eca-9c7f-3efb51899813
ms.openlocfilehash: f3e281ff8a9de9be41dd6ad9d01ab52798d8e89e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61794548"
---
# <a name="faultpropagationquery"></a><span data-ttu-id="6fc81-101">\<faultPropagationQuery></span><span class="sxs-lookup"><span data-stu-id="6fc81-101">\<faultPropagationQuery></span></span>

<span data-ttu-id="6fc81-102">Représente une requête qui permet d'effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="6fc81-102">Represents a query that is used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="6fc81-103">Cet événement se produit chaque fois qu'un FaultHandler traite une erreur.</span><span class="sxs-lookup"><span data-stu-id="6fc81-103">This event occurs each time a FaultHandler processes a fault.</span></span> <span data-ttu-id="6fc81-104">Vous devez utiliser cette requête pour effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="6fc81-104">You should use such query to track the handling of faults that occur within an activity.</span></span> <span data-ttu-id="6fc81-105">La requête est nécessaire pour qu'un participant au suivi puisse s'abonner aux enregistrements de propagation d'erreur.</span><span class="sxs-lookup"><span data-stu-id="6fc81-105">The query is necessary for a  tracking participant to subscribe to fault propagation records.</span></span>

 <span data-ttu-id="6fc81-106">Pour plus d’informations sur les requêtes de modèle de suivi, consultez [modèles de suivi](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="6fc81-106">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).</span></span>

<span data-ttu-id="6fc81-107">\<system.serviceModel>\\</span><span class="sxs-lookup"><span data-stu-id="6fc81-107">\<system.serviceModel>\\</span></span>
<span data-ttu-id="6fc81-108">\<suivi > \\</span><span class="sxs-lookup"><span data-stu-id="6fc81-108">\<tracking>\\</span></span>
<span data-ttu-id="6fc81-109">\<trackingProfile>\\</span><span class="sxs-lookup"><span data-stu-id="6fc81-109">\<trackingProfile>\\</span></span>
<span data-ttu-id="6fc81-110">\<workflow>\\</span><span class="sxs-lookup"><span data-stu-id="6fc81-110">\<workflow>\\</span></span>
<span data-ttu-id="6fc81-111">\<faultPropagationQueries>\\</span><span class="sxs-lookup"><span data-stu-id="6fc81-111">\<faultPropagationQueries>\\</span></span>
<span data-ttu-id="6fc81-112">\<faultPropagationQuery></span><span class="sxs-lookup"><span data-stu-id="6fc81-112">\<faultPropagationQuery></span></span>

## <a name="syntax"></a><span data-ttu-id="6fc81-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6fc81-113">Syntax</span></span>

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

## <a name="attributes-and-elements"></a><span data-ttu-id="6fc81-114">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="6fc81-114">Attributes and Elements</span></span>

<span data-ttu-id="6fc81-115">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="6fc81-115">The following sections describe attributes, child elements, and parent elements.</span></span>

### <a name="attributes"></a><span data-ttu-id="6fc81-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="6fc81-116">Attributes</span></span>

|<span data-ttu-id="6fc81-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="6fc81-117">Attribute</span></span>|<span data-ttu-id="6fc81-118">Description</span><span class="sxs-lookup"><span data-stu-id="6fc81-118">Description</span></span>|
|---------------|-----------------|
|<span data-ttu-id="6fc81-119">activityName</span><span class="sxs-lookup"><span data-stu-id="6fc81-119">activityName</span></span>|<span data-ttu-id="6fc81-120">Chaîne qui spécifie le nom de l’activité de gestionnaire d’erreur qui a propagé l’erreur.</span><span class="sxs-lookup"><span data-stu-id="6fc81-120">A string that specifies the name of the fault handler activity that propagated the fault.</span></span> <span data-ttu-id="6fc81-121">La valeur par défaut est \*, qui indique que des enregistrements de propagation d'erreur sont retournés pour toutes les activités.</span><span class="sxs-lookup"><span data-stu-id="6fc81-121">The default is \*, which indicates that fault propagation records are returned for all activities.</span></span>|
|<span data-ttu-id="6fc81-122">faultHandlerActivityName</span><span class="sxs-lookup"><span data-stu-id="6fc81-122">faultHandlerActivityName</span></span>|<span data-ttu-id="6fc81-123">Chaîne qui spécifie le nom de l'activité à l'origine de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="6fc81-123">A string that specifies the name of the activity that was the source of the fault.</span></span>|

### <a name="child-elements"></a><span data-ttu-id="6fc81-124">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6fc81-124">Child Elements</span></span>

<span data-ttu-id="6fc81-125">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6fc81-125">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="6fc81-126">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="6fc81-126">Parent Elements</span></span>

|<span data-ttu-id="6fc81-127">Élément</span><span class="sxs-lookup"><span data-stu-id="6fc81-127">Element</span></span>|<span data-ttu-id="6fc81-128">Description</span><span class="sxs-lookup"><span data-stu-id="6fc81-128">Description</span></span>|
|-------------|-----------------|
|[<span data-ttu-id="6fc81-129">\<faultPropagationQueries></span><span class="sxs-lookup"><span data-stu-id="6fc81-129">\<faultPropagationQueries></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/faultpropagationqueries.md)|<span data-ttu-id="6fc81-130">Représente une liste des éléments de configuration qui permettent d'effectuer le suivi de la gestion des erreurs qui se produisent dans une activité.</span><span class="sxs-lookup"><span data-stu-id="6fc81-130">Represents a list of configuration elements that are used to track the handling of faults that occur within an activity.</span></span>  <span data-ttu-id="6fc81-131">Cet événement se produit chaque fois qu'un FaultHandler traite une erreur.</span><span class="sxs-lookup"><span data-stu-id="6fc81-131">This event occurs each time a FaultHandler processes a fault.</span></span>|

## <a name="see-also"></a><span data-ttu-id="6fc81-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fc81-132">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.FaultPropagationQueryElement?displayProperty=nameWithType>
- <xref:System.Activities.Tracking.FaultPropagationQuery?displayProperty=nameWithType>
- [<span data-ttu-id="6fc81-133">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="6fc81-133">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
- [<span data-ttu-id="6fc81-134">Profils de suivi</span><span class="sxs-lookup"><span data-stu-id="6fc81-134">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
