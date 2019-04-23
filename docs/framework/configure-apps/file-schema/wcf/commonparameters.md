---
title: <commonParameters>
ms.date: 03/30/2017
ms.assetid: ffc20832-34d6-4622-8174-81924fd53514
ms.openlocfilehash: b9ab4e8ca5a71d54a80d17322b61c83d41af2b40
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59088351"
---
# <a name="commonparameters"></a><span data-ttu-id="80f50-101">\<commonParameters></span><span class="sxs-lookup"><span data-stu-id="80f50-101">\<commonParameters></span></span>
<span data-ttu-id="80f50-102">Représente une collection de paramètres utilisés globalement dans plusieurs services.</span><span class="sxs-lookup"><span data-stu-id="80f50-102">Represents a collection of parameters that are used globally across multiple services.</span></span> <span data-ttu-id="80f50-103">Cette collection inclut généralement la chaîne de connexion de base de données pouvant être partagée par les services fiables.</span><span class="sxs-lookup"><span data-stu-id="80f50-103">This collection will typically include the database connection string that might be shared by durable services.</span></span>  
  
 <span data-ttu-id="80f50-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="80f50-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="80f50-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="80f50-105">\<behaviors></span></span>  
<span data-ttu-id="80f50-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="80f50-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="80f50-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="80f50-107">\<behavior></span></span>  
<span data-ttu-id="80f50-108">\<workflowRuntime></span><span class="sxs-lookup"><span data-stu-id="80f50-108">\<workflowRuntime></span></span>  
<span data-ttu-id="80f50-109">\<commonParameters></span><span class="sxs-lookup"><span data-stu-id="80f50-109">\<commonParameters></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="80f50-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80f50-110">Syntax</span></span>  
  
```xml  
<workflowRuntime>
  <commonParameters>
    <add name="String"
         value="String" />
  </commonParameters>
</workflowRuntime>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="80f50-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="80f50-111">Attributes and Elements</span></span>  
 <span data-ttu-id="80f50-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="80f50-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="80f50-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="80f50-113">Attributes</span></span>  
 <span data-ttu-id="80f50-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="80f50-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="80f50-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="80f50-115">Child Elements</span></span>  
  
|<span data-ttu-id="80f50-116">Élément</span><span class="sxs-lookup"><span data-stu-id="80f50-116">Element</span></span>|<span data-ttu-id="80f50-117">Description</span><span class="sxs-lookup"><span data-stu-id="80f50-117">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="80f50-118">\<add></span><span class="sxs-lookup"><span data-stu-id="80f50-118">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-commonparameters.md)|<span data-ttu-id="80f50-119">Ajoute à la collection une paire nom-valeur de paramètres communs utilisés par les services.</span><span class="sxs-lookup"><span data-stu-id="80f50-119">Adds a name-value pair of common parameters used by services to the collection.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="80f50-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="80f50-120">Parent Elements</span></span>  
  
|<span data-ttu-id="80f50-121">Élément</span><span class="sxs-lookup"><span data-stu-id="80f50-121">Element</span></span>|<span data-ttu-id="80f50-122">Description</span><span class="sxs-lookup"><span data-stu-id="80f50-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="80f50-123">\<workflowRuntime></span><span class="sxs-lookup"><span data-stu-id="80f50-123">\<workflowRuntime></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/workflowruntime.md)|<span data-ttu-id="80f50-124">Spécifie les paramètres d’une instance de <xref:System.Workflow.Runtime.WorkflowRuntime> pour l’hébergement de services de Windows Communication Foundation (WCF) basés sur les flux de travail.</span><span class="sxs-lookup"><span data-stu-id="80f50-124">Specifies settings for an instance of <xref:System.Workflow.Runtime.WorkflowRuntime> for hosting workflow-based Windows Communication Foundation (WCF) services.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="80f50-125">Notes</span><span class="sxs-lookup"><span data-stu-id="80f50-125">Remarks</span></span>  
 <span data-ttu-id="80f50-126">L'élément `<commonParameters>` définit tous les paramètres utilisés globalement dans plusieurs services, par exemple `ConnectionString` lors de l'utilisation de <xref:System.Workflow.Runtime.Hosting.SharedConnectionWorkflowCommitWorkBatchService>.</span><span class="sxs-lookup"><span data-stu-id="80f50-126">The `<commonParameters>` element defines any parameters that are used globally across multiple services, for example `ConnectionString` when using the <xref:System.Workflow.Runtime.Hosting.SharedConnectionWorkflowCommitWorkBatchService>.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="80f50-127">Le service de suivi SQL n'utilise pas toujours la valeur `ConnectionString` si elle est spécifiée dans la section `<commonParameters>`.</span><span class="sxs-lookup"><span data-stu-id="80f50-127">SQL Tracking service does not consistently use the `ConnectionString` value if it is specified in the `<commonParameters>` section.</span></span> <span data-ttu-id="80f50-128">En effet, certaines de ses opérations, comme la récupération de la propriété `StateMachineWorkflowInstance.StateHistory`, peuvent échouer.</span><span class="sxs-lookup"><span data-stu-id="80f50-128">Some of its operations such as retrieving the `StateMachineWorkflowInstance.StateHistory` property may fail.</span></span> <span data-ttu-id="80f50-129">Pour résoudre ce problème, spécifiez l'attribut `ConnectionString` dans la section de configuration pour le fournisseur de suivi, comme indiqué dans l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="80f50-129">To workaround this, specify the `ConnectionString` attribute in the configuration section for tracking provider, as indicated in the following example.</span></span>  
  
 `<add`  
  
 `type="System.Workflow.Runtime.Tracking.SqlTrackingService, System.Workflow.Runtime, Version=3.0.00000.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"`  
  
 `ConnectionString="Data Source=localhost;Initial Catalog=Partner20WFTP;Integrated Security=True;" />`  
  
 <span data-ttu-id="80f50-130">Pour les services qui valident des lots de travail dans des magasins de persistance, comme <xref:System.Workflow.Runtime.Hosting.DefaultWorkflowCommitWorkBatchService> et <xref:System.Workflow.Runtime.Hosting.SqlWorkflowPersistenceService>, vous pouvez les activer pour effectuer de nouvelles tentatives de transaction à l'aide du paramètre `EnableRetries` tel qu'indiqué dans l'exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="80f50-130">For services that commit work batches to persistence stores, such as <xref:System.Workflow.Runtime.Hosting.DefaultWorkflowCommitWorkBatchService> and <xref:System.Workflow.Runtime.Hosting.SqlWorkflowPersistenceService>, you can enable them to retry their transaction by using the `EnableRetries` parameter as shown in the following example:</span></span>  
  
```xml  
<workflowRuntime name="SampleApplication"
                 unloadOnIdle="false">
  <commonParameters>
    <add name="ConnectionString"
         value="Initial Catalog=WorkflowStore;Data Source=localhost;Integrated Security=SSPI;" />
    <add name="EnableRetries"
         value="True" />
  </commonParameters>
  <services>
    <add type="System.Workflow.Runtime.Hosting.SqlWorkflowPersistenceService, System.Workflow.Runtime,
               Version=3.0.00000.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"
         enableRetries="False" />
  </services>
</workflowRuntime>
```  
  
 <span data-ttu-id="80f50-131">Notez que le `EnableRetries` paramètre peut être défini à un niveau global (comme indiqué dans le *Paramètres_courants* section) ou pour des services individuels qui prennent en charge `EnableRetries` (comme indiqué dans le *Services*section).</span><span class="sxs-lookup"><span data-stu-id="80f50-131">Notice that the `EnableRetries` parameter can be set either at a global level (as shown in the *CommonParameters* section) or for individual services that support `EnableRetries` (as shown in the *Services* section).</span></span>  
  
 <span data-ttu-id="80f50-132">L'exemple de code suivant indique comment modifier les paramètres communs par programme.</span><span class="sxs-lookup"><span data-stu-id="80f50-132">The following sample code shows how to change the common parameters programmatically.</span></span>  
  
```  
Configuration config=WebConfigurationManager.OpenWebConfiguration("/Workflow", "Default Web Site", null, "localhost");  
WorkflowRuntimeSection wfruntime=config.GetSection("WorkflowRuntime") as WorkflowRuntimeSection;  
NameValueConfigurationCollection commonParameters=wfruntime.CommonParameters;  
commonParameters["ConnectionString"].Value="another connection string";  
config.Save();  
```  
  
 <span data-ttu-id="80f50-133">Pour plus d’informations sur l’utilisation d’un fichier de configuration pour contrôler le comportement d’un <xref:System.Workflow.Runtime.WorkflowRuntime> objet d’une application hôte Windows Workflow Foundation, consultez [les fichiers de Configuration de flux de travail](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90)).</span><span class="sxs-lookup"><span data-stu-id="80f50-133">For more information about using a configuration file to control the behavior of a <xref:System.Workflow.Runtime.WorkflowRuntime> object of a Windows Workflow Foundation host application, see [Workflow Configuration Files](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="80f50-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="80f50-134">Example</span></span>  
  
```xml  
<commonParameters>
   <add name="ConnectionString"
        value="Initial Catalog=WorkflowStore;Data Source=localhost;Integrated Security=SSPI;" />
   <add name="EnableRetries"
        value="true" />
</commonParameters>
```  
  
## <a name="see-also"></a><span data-ttu-id="80f50-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80f50-135">See also</span></span>

- <xref:System.ServiceModel.Configuration.WorkflowRuntimeElement>
- <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>
- <xref:System.Workflow.Runtime.WorkflowRuntime>
- <xref:System.Workflow.Runtime.Hosting.DefaultWorkflowCommitWorkBatchService>
- <xref:System.Workflow.Runtime.Hosting.SqlWorkflowPersistenceService>
- <span data-ttu-id="80f50-136">[Fichiers de Configuration de flux de travail](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="80f50-136">[Workflow Configuration Files](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90))</span></span>
- [<span data-ttu-id="80f50-137">\<add></span><span class="sxs-lookup"><span data-stu-id="80f50-137">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-commonparameters.md)
