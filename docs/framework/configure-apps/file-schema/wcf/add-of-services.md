---
title: '&lt;add&gt; de &lt;services&gt;'
ms.date: 03/30/2017
ms.assetid: 6bdc4590-aa9c-4ec8-9345-879d780cd141
ms.openlocfilehash: 9a86b7549e0efef10cbeb16dcc427d04065e43d3
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145534"
---
# <a name="ltaddgt-of-ltservicesgt"></a><span data-ttu-id="0998e-102">&lt;add&gt; de &lt;services&gt;</span><span class="sxs-lookup"><span data-stu-id="0998e-102">&lt;add&gt; of &lt;services&gt;</span></span>
<span data-ttu-id="0998e-103">Spécifie les paramètres d’une instance de <xref:System.Workflow.Runtime.WorkflowRuntime> pour l’hébergement de services de Windows Communication Foundation (WCF) basés sur les flux de travail.</span><span class="sxs-lookup"><span data-stu-id="0998e-103">Specifies settings for an instance of <xref:System.Workflow.Runtime.WorkflowRuntime> for hosting workflow-based Windows Communication Foundation (WCF) services.</span></span> <span data-ttu-id="0998e-104">Cet élément est de type <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="0998e-104">This element is of type <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span></span>  
  
 <span data-ttu-id="0998e-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="0998e-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="0998e-106">\<comportements ></span><span class="sxs-lookup"><span data-stu-id="0998e-106">\<behaviors></span></span>  
<span data-ttu-id="0998e-107">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="0998e-107">\<serviceBehaviors></span></span>  
<span data-ttu-id="0998e-108">\<comportement ></span><span class="sxs-lookup"><span data-stu-id="0998e-108">\<behavior></span></span>  
<span data-ttu-id="0998e-109">\<services></span><span class="sxs-lookup"><span data-stu-id="0998e-109">\<services></span></span>  
<span data-ttu-id="0998e-110">\<add></span><span class="sxs-lookup"><span data-stu-id="0998e-110">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0998e-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0998e-111">Syntax</span></span>  
  
```xml  
<workflowRuntime>
  <services>
    <add type="String" />
  </services>
</workflowRuntime>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0998e-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="0998e-112">Attributes and Elements</span></span>  
 <span data-ttu-id="0998e-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="0998e-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0998e-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="0998e-114">Attributes</span></span>  
  
|<span data-ttu-id="0998e-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="0998e-115">Attribute</span></span>|<span data-ttu-id="0998e-116">Description</span><span class="sxs-lookup"><span data-stu-id="0998e-116">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="0998e-117">type</span><span class="sxs-lookup"><span data-stu-id="0998e-117">type</span></span>|<span data-ttu-id="0998e-118">Chaîne indiquant le nom qualifié du type d'assembly correspondant au service à initialiser.</span><span class="sxs-lookup"><span data-stu-id="0998e-118">A string that specifies the assembly-qualified type name of the service to be initialized.</span></span> <span data-ttu-id="0998e-119">Les services spécifiés doivent suivre certaines règles en ce qui concerne les signatures de leurs constructeurs.</span><span class="sxs-lookup"><span data-stu-id="0998e-119">The service specified must follow certain rules about the signatures of their constructors.</span></span> <span data-ttu-id="0998e-120">Pour plus d'informations, voir <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="0998e-120">See <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement> for more information.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0998e-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0998e-121">Child Elements</span></span>  
 <span data-ttu-id="0998e-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0998e-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="0998e-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0998e-123">Parent Elements</span></span>  
  
|<span data-ttu-id="0998e-124">Élément</span><span class="sxs-lookup"><span data-stu-id="0998e-124">Element</span></span>|<span data-ttu-id="0998e-125">Description</span><span class="sxs-lookup"><span data-stu-id="0998e-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0998e-126">\<services></span><span class="sxs-lookup"><span data-stu-id="0998e-126">\<services></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/services-of-workflowruntime.md)|<span data-ttu-id="0998e-127">Collection de services qui sera ajoutée au moteur de <xref:System.Workflow.Runtime.WorkflowRuntime>.</span><span class="sxs-lookup"><span data-stu-id="0998e-127">A collection of services that will be added to the <xref:System.Workflow.Runtime.WorkflowRuntime> engine.</span></span> <span data-ttu-id="0998e-128">Les éléments sont de type <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="0998e-128">The elements are of type <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span></span>  <span data-ttu-id="0998e-129">Les services spécifiés dans la collection sont initialisés par le moteur d'exécution de workflow et ajoutés à ses services lorsque le constructeur <xref:System.Workflow.Runtime.WorkflowRuntime> approprié est appelé.</span><span class="sxs-lookup"><span data-stu-id="0998e-129">The services specified in the collection will be initialized by the workflow runtime engine and added to its services when the appropriate <xref:System.Workflow.Runtime.WorkflowRuntime> constructor is called.</span></span> <span data-ttu-id="0998e-130">Par conséquent, les services spécifiés dans la collection doivent suivre certaines règles en ce qui concerne les signatures de leurs constructeurs.</span><span class="sxs-lookup"><span data-stu-id="0998e-130">Therefore, the services specified in the collection must follow certain rules about the signatures of their constructors.</span></span> <span data-ttu-id="0998e-131">Pour plus d'informations, voir <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="0998e-131">See <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement> for more information.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0998e-132">Notes</span><span class="sxs-lookup"><span data-stu-id="0998e-132">Remarks</span></span>  
 <span data-ttu-id="0998e-133">Le service spécifié dans cet élément est initialisé par le moteur d'exécution de workflow et ajouté à ses services lorsque le constructeur <xref:System.Workflow.Runtime.WorkflowRuntime> approprié est appelé.</span><span class="sxs-lookup"><span data-stu-id="0998e-133">The service specified in this element will be initialized by the workflow runtime engine and added to its services when the appropriate <xref:System.Workflow.Runtime.WorkflowRuntime> constructor is called.</span></span> <span data-ttu-id="0998e-134">Par conséquent, le service spécifié doit suivre certaines règles en ce qui concerne les signatures de son constructeur.</span><span class="sxs-lookup"><span data-stu-id="0998e-134">Therefore, the service specified must follow certain rules about the signatures of their constructors.</span></span> <span data-ttu-id="0998e-135">Pour plus d'informations, voir <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>.</span><span class="sxs-lookup"><span data-stu-id="0998e-135">See <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement> for more information.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0998e-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="0998e-136">Example</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="0998e-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0998e-137">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.WorkflowRuntimeElement>  
 <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>  
 <xref:System.Workflow.Runtime.WorkflowRuntime>  
 <span data-ttu-id="0998e-138">[Fichiers de Configuration de flux de travail](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="0998e-138">[Workflow Configuration Files](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90))</span></span>
