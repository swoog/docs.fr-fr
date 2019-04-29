---
title: <tracking>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: fd9b50ed-98a1-4518-836d-e4e02c670822
ms.openlocfilehash: 31490c7425572909cc30fe4237af9309754b68e4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61768847"
---
# <a name="tracking"></a><span data-ttu-id="4c005-101">\<tracking></span><span class="sxs-lookup"><span data-stu-id="4c005-101">\<tracking></span></span>
<span data-ttu-id="4c005-102">Représente une section de configuration permettant de définir les paramètres de suivi d'un service de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="4c005-102">Represents a configuration section for defining tracking settings for a workflow service.</span></span>  
  
 <span data-ttu-id="4c005-103">Pour plus d’informations de suivi de workflow et sa configuration, consultez [suivi et traçage de Workflow](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md) et [configuration du suivi d’un flux de travail](../../../../../docs/framework/windows-workflow-foundation/configuring-tracking-for-a-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="4c005-103">For more information in workflow tracking and its configuration, see [Workflow Tracking and Tracing](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md) and [Configuring Tracking for a Workflow](../../../../../docs/framework/windows-workflow-foundation/configuring-tracking-for-a-workflow.md).</span></span>  
  
<span data-ttu-id="4c005-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="4c005-104">\<system.serviceModel></span></span>  
<span data-ttu-id="4c005-105">\<tracking></span><span class="sxs-lookup"><span data-stu-id="4c005-105">\<tracking></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4c005-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c005-106">Syntax</span></span>  
  
```xml  
<system.serviceModel>
  <tracking>
    <profiles>
      <participants>
        <add name="String" 
             profileName="String" 
             type="String" />
      </participants>
      <trackingProfile name="String">
        <workflow activityDefinitionId="String">
          <activityScheduledQueries>
            <activityScheduledQuery activityName="String" 
                                    childActivityName="String"/>
          </activityScheduledQueries>
          <activityStateQueries>
            <activityStateQuery activityName="String" />
            <arguments>
              <argument name="String" />
            </arguments>
            <states>
              <state name="String"  />
            </states>
            <variables>
              <variable name="String" />
            </variables>
          </activityStateQueries>
          <bookmarkResumptionQueries>
            <bookmarkResumptionQuery name="String" />
          </bookmarkResumptionQueries>
          <cancelRequestQueries>
            <cancelRequestQuery activityName="String" 
                                childActivityName="String"/>
          </cancelRequestQueries>
          <customTrackingQueries>
            <customTrackingQuery activityName="String" 
                                 name="String"/>
          </customTrackingQueries>
          <faultPropagationQueries>
            <faultPropagationQuery activityName="String" 
                                   faultHandlerActivityName="String" />
          </faultPropagationQueries>
          <workflowInstanceQueries>
            <workflowInstanceQuery>
              <states>
                <state name="String" />
              </states>
            </workflowInstanceQuery>
          </workflowInstanceQueries>
        </workflow>
      </trackingProfile>
    </profiles>
  </tracking>
</system.serviceModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4c005-107">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="4c005-107">Attributes and Elements</span></span>  
 <span data-ttu-id="4c005-108">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="4c005-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4c005-109">Attributs</span><span class="sxs-lookup"><span data-stu-id="4c005-109">Attributes</span></span>  
 <span data-ttu-id="4c005-110">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4c005-110">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="4c005-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4c005-111">Child Elements</span></span>  
  
|<span data-ttu-id="4c005-112">Élément</span><span class="sxs-lookup"><span data-stu-id="4c005-112">Element</span></span>|<span data-ttu-id="4c005-113">Description</span><span class="sxs-lookup"><span data-stu-id="4c005-113">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4c005-114">\<participants></span><span class="sxs-lookup"><span data-stu-id="4c005-114">\<participants></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/participants.md)|<span data-ttu-id="4c005-115">Une collection d’éléments de configuration définissent des participants qui s’abonner aux enregistrements de suivi.</span><span class="sxs-lookup"><span data-stu-id="4c005-115">A collection of configuration elements defining participants that subscribe to tracking records.</span></span> <span data-ttu-id="4c005-116">Les participants de suivi contiennent la logique nécessaire pour traiter la charge utile des enregistrements de suivi (par exemple, ils peuvent choisir d'écrire dans un fichier).</span><span class="sxs-lookup"><span data-stu-id="4c005-116">The tracking participants contain the logic to process the payload from the tracking records (for example, they could choose to write to a file).</span></span>|  
|[<span data-ttu-id="4c005-117">\<trackingProfile></span><span class="sxs-lookup"><span data-stu-id="4c005-117">\<trackingProfile></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/trackingprofile.md)|<span data-ttu-id="4c005-118">Modèle de suivi permettant de filtrer les enregistrements de suivi émis d'une instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="4c005-118">A tracking profile to filter tracking records emitted from a workflow instance.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="4c005-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4c005-119">Parent Elements</span></span>  
  
|<span data-ttu-id="4c005-120">Élément</span><span class="sxs-lookup"><span data-stu-id="4c005-120">Element</span></span>|<span data-ttu-id="4c005-121">Description</span><span class="sxs-lookup"><span data-stu-id="4c005-121">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="4c005-122">system.ServiceModel</span><span class="sxs-lookup"><span data-stu-id="4c005-122">system.ServiceModel</span></span>|<span data-ttu-id="4c005-123">Élément racine de tous les éléments de configuration de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="4c005-123">The root element of all workflow configuration elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4c005-124">Notes</span><span class="sxs-lookup"><span data-stu-id="4c005-124">Remarks</span></span>  
 <span data-ttu-id="4c005-125">Le suivi vous fournit la capacité d'examiner l'exécution d'un flux de travail.</span><span class="sxs-lookup"><span data-stu-id="4c005-125">Tracking provides you with the ability to examine the execution of a workflow.</span></span> <span data-ttu-id="4c005-126">L'infrastructure de suivi de flux de travail instrumente un flux de travail pour émettre des enregistrements qui reflètent les principaux événements pendant l'exécution.</span><span class="sxs-lookup"><span data-stu-id="4c005-126">The workflow tracking infrastructure instruments a workflow to emit records reflecting key events during the execution.</span></span> <span data-ttu-id="4c005-127">Par exemple, lorsqu'une instance de flux de travail démarre ou se termine, des enregistrements de suivi sont émis.</span><span class="sxs-lookup"><span data-stu-id="4c005-127">For example, when a workflow instance starts or completes tracking records are emitted.</span></span> <span data-ttu-id="4c005-128">Le suivi peut également extraire des données métier pertinentes associées aux variables de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="4c005-128">Tracking can also extract business relevant data associated with the workflow variables.</span></span> <span data-ttu-id="4c005-129">Par exemple, si le flux de travail représente un système de traitement des commandes, l'ID de commande peut être extrait avec l'enregistrement de suivi.</span><span class="sxs-lookup"><span data-stu-id="4c005-129">For example, if the workflow represents an order processing system the order id can be extracted along with the tracking record.</span></span> <span data-ttu-id="4c005-130">En général, l'activation du suivi WF facilite les diagnostics ou les analyses d'entreprise à partir d'une exécution de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="4c005-130">In general, enabling WF tracking facilitates diagnostics or business analytics over a workflow execution.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4c005-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c005-131">See also</span></span>

- <xref:System.ServiceModel.Activities.Tracking.Configuration.TrackingSection?displayProperty=nameWithType>
- [<span data-ttu-id="4c005-132">Suivi et traçage de workflow</span><span class="sxs-lookup"><span data-stu-id="4c005-132">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)
