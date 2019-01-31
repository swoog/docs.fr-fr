---
title: <add> de <services>
ms.date: 03/30/2017
ms.assetid: 6bdc4590-aa9c-4ec8-9345-879d780cd141
ms.openlocfilehash: 4e1a9c67fa82262ab49be196b2e4fd31a69e688f
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55264529"
---
# <a name="add-of-services"></a><span data-ttu-id="f3584-102">\<Ajouter > de \<services ></span><span class="sxs-lookup"><span data-stu-id="f3584-102">\<add> of \<services></span></span>
<span data-ttu-id="f3584-103">Spécifie les paramètres d’une instance de <xref:System.Workflow.Runtime.WorkflowRuntime> pour l’hébergement de services de Windows Communication Foundation (WCF) basés sur les flux de travail.</span><span class="sxs-lookup"><span data-stu-id="f3584-103">Specifies settings for an instance of <xref:System.Workflow.Runtime.WorkflowRuntime> for hosting workflow-based Windows Communication Foundation (WCF) services.</span></span> <span data-ttu-id="f3584-104">Cet élément est de type <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="f3584-104">This element is of type <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span></span>  
  
 <span data-ttu-id="f3584-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="f3584-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="f3584-106">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="f3584-106">\<behaviors></span></span>  
<span data-ttu-id="f3584-107">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="f3584-107">\<serviceBehaviors></span></span>  
<span data-ttu-id="f3584-108">\<behavior></span><span class="sxs-lookup"><span data-stu-id="f3584-108">\<behavior></span></span>  
<span data-ttu-id="f3584-109">\<services></span><span class="sxs-lookup"><span data-stu-id="f3584-109">\<services></span></span>  
<span data-ttu-id="f3584-110">\<add></span><span class="sxs-lookup"><span data-stu-id="f3584-110">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f3584-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3584-111">Syntax</span></span>  
  
```xml  
<workflowRuntime>
  <services>
    <add type="String" />
  </services>
</workflowRuntime>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f3584-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="f3584-112">Attributes and Elements</span></span>  
 <span data-ttu-id="f3584-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="f3584-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f3584-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="f3584-114">Attributes</span></span>  
  
|<span data-ttu-id="f3584-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="f3584-115">Attribute</span></span>|<span data-ttu-id="f3584-116">Description</span><span class="sxs-lookup"><span data-stu-id="f3584-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f3584-117">type</span><span class="sxs-lookup"><span data-stu-id="f3584-117">type</span></span>|<span data-ttu-id="f3584-118">Chaîne indiquant le nom qualifié du type d'assembly correspondant au service à initialiser.</span><span class="sxs-lookup"><span data-stu-id="f3584-118">A string that specifies the assembly-qualified type name of the service to be initialized.</span></span> <span data-ttu-id="f3584-119">Les services spécifiés doivent suivre certaines règles en ce qui concerne les signatures de leurs constructeurs.</span><span class="sxs-lookup"><span data-stu-id="f3584-119">The service specified must follow certain rules about the signatures of their constructors.</span></span> <span data-ttu-id="f3584-120">Pour plus d'informations, voir <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="f3584-120">See <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement> for more information.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f3584-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f3584-121">Child Elements</span></span>  
 <span data-ttu-id="f3584-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f3584-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="f3584-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f3584-123">Parent Elements</span></span>  
  
|<span data-ttu-id="f3584-124">Élément</span><span class="sxs-lookup"><span data-stu-id="f3584-124">Element</span></span>|<span data-ttu-id="f3584-125">Description</span><span class="sxs-lookup"><span data-stu-id="f3584-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f3584-126">\<services></span><span class="sxs-lookup"><span data-stu-id="f3584-126">\<services></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/services-of-workflowruntime.md)|<span data-ttu-id="f3584-127">Collection de services qui sera ajoutée au moteur de <xref:System.Workflow.Runtime.WorkflowRuntime>.</span><span class="sxs-lookup"><span data-stu-id="f3584-127">A collection of services that will be added to the <xref:System.Workflow.Runtime.WorkflowRuntime> engine.</span></span> <span data-ttu-id="f3584-128">Les éléments sont de type <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="f3584-128">The elements are of type <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span></span>  <span data-ttu-id="f3584-129">Les services spécifiés dans la collection sont initialisés par le moteur d'exécution de workflow et ajoutés à ses services lorsque le constructeur <xref:System.Workflow.Runtime.WorkflowRuntime> approprié est appelé.</span><span class="sxs-lookup"><span data-stu-id="f3584-129">The services specified in the collection will be initialized by the workflow runtime engine and added to its services when the appropriate <xref:System.Workflow.Runtime.WorkflowRuntime> constructor is called.</span></span> <span data-ttu-id="f3584-130">Par conséquent, les services spécifiés dans la collection doivent suivre certaines règles en ce qui concerne les signatures de leurs constructeurs.</span><span class="sxs-lookup"><span data-stu-id="f3584-130">Therefore, the services specified in the collection must follow certain rules about the signatures of their constructors.</span></span> <span data-ttu-id="f3584-131">Pour plus d'informations, voir <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="f3584-131">See <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement> for more information.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f3584-132">Notes</span><span class="sxs-lookup"><span data-stu-id="f3584-132">Remarks</span></span>  
 <span data-ttu-id="f3584-133">Le service spécifié dans cet élément est initialisé par le moteur d'exécution de workflow et ajouté à ses services lorsque le constructeur <xref:System.Workflow.Runtime.WorkflowRuntime> approprié est appelé.</span><span class="sxs-lookup"><span data-stu-id="f3584-133">The service specified in this element will be initialized by the workflow runtime engine and added to its services when the appropriate <xref:System.Workflow.Runtime.WorkflowRuntime> constructor is called.</span></span> <span data-ttu-id="f3584-134">Par conséquent, le service spécifié doit suivre certaines règles en ce qui concerne les signatures de son constructeur.</span><span class="sxs-lookup"><span data-stu-id="f3584-134">Therefore, the service specified must follow certain rules about the signatures of their constructors.</span></span> <span data-ttu-id="f3584-135">Pour plus d'informations, voir <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="f3584-135">See <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement> for more information.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f3584-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="f3584-136">Example</span></span>  
  
```xml  
<serviceBehaviors>
  <behavior name="ServiceBehavior">
    <workflowRuntime name="WorkflowServiceHostRuntime"
                     validateOnCreate="true"
                     enablePerformanceCounters="true">
      <services>
        <add type="NetFx.Checkin.Scenario.WorkflowServices.WorkflowBasedServices.Common.TestPersistenceService.FilePersistenceService, NetFx.Checkin.Scenario.WorkflowServices.WorkflowBasedServices.Common" />
      </services>
    </workflowRuntime>
  </behavior>
</serviceBehaviors>
```  
  
## <a name="see-also"></a><span data-ttu-id="f3584-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3584-137">See also</span></span>
- <xref:System.ServiceModel.Configuration.WorkflowRuntimeElement>
- <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>
- <xref:System.Workflow.Runtime.WorkflowRuntime>
- <span data-ttu-id="f3584-138">[Fichiers de Configuration de flux de travail](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="f3584-138">[Workflow Configuration Files](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90))</span></span>
