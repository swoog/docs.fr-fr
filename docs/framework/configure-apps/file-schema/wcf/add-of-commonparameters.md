---
title: <add> de <commonParameters>
ms.date: 03/30/2017
ms.assetid: 3713bf25-20c8-455f-bb85-de46b6487932
ms.openlocfilehash: 6aaba3f82966ad4496e6edaae06b5d7a8aef3863
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61673652"
---
# <a name="add-of-commonparameters"></a><span data-ttu-id="fdc6e-102">\<Ajouter > de \<Paramètres_courants ></span><span class="sxs-lookup"><span data-stu-id="fdc6e-102">\<add> of \<commonParameters></span></span>
<span data-ttu-id="fdc6e-103">Spécifie une paire nom-valeur de paramètres utilisés globalement dans plusieurs services.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-103">Specifies a name-value pair of parameters that are used globally across multiple services.</span></span> <span data-ttu-id="fdc6e-104">Ce paramètre inclut généralement la chaîne de connexion de base de données pouvant être partagée par les services fiables.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-104">Typically this parameter includes the database connection string that might be shared by durable services.</span></span>  
  
 <span data-ttu-id="fdc6e-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="fdc6e-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="fdc6e-106">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="fdc6e-106">\<behaviors></span></span>  
<span data-ttu-id="fdc6e-107">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="fdc6e-107">\<serviceBehaviors></span></span>  
<span data-ttu-id="fdc6e-108">\<behavior></span><span class="sxs-lookup"><span data-stu-id="fdc6e-108">\<behavior></span></span>  
<span data-ttu-id="fdc6e-109">\<workflowRuntime></span><span class="sxs-lookup"><span data-stu-id="fdc6e-109">\<workflowRuntime></span></span>  
<span data-ttu-id="fdc6e-110">\<commonParameters></span><span class="sxs-lookup"><span data-stu-id="fdc6e-110">\<commonParameters></span></span>  
<span data-ttu-id="fdc6e-111">\<add></span><span class="sxs-lookup"><span data-stu-id="fdc6e-111">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fdc6e-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fdc6e-112">Syntax</span></span>  
  
```xml  
<workflowRuntime>
  <commonParameters>
    <add name="String" value="String" />
  </commonParameters>
</workflowRuntime>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="fdc6e-113">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="fdc6e-113">Attributes and Elements</span></span>  
 <span data-ttu-id="fdc6e-114">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-114">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="fdc6e-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="fdc6e-115">Attributes</span></span>  
  
|<span data-ttu-id="fdc6e-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="fdc6e-116">Attribute</span></span>|<span data-ttu-id="fdc6e-117">Description</span><span class="sxs-lookup"><span data-stu-id="fdc6e-117">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="fdc6e-118">name</span><span class="sxs-lookup"><span data-stu-id="fdc6e-118">name</span></span>|<span data-ttu-id="fdc6e-119">Nom du paramètre spécifié pour un service.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-119">The name of the parameter specified for a service.</span></span>|  
|<span data-ttu-id="fdc6e-120">par défaut</span><span class="sxs-lookup"><span data-stu-id="fdc6e-120">value</span></span>|<span data-ttu-id="fdc6e-121">Valeur du paramètre spécifié pour un service.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-121">The value of the parameter specified for a service.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="fdc6e-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fdc6e-122">Child Elements</span></span>  
 <span data-ttu-id="fdc6e-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-123">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="fdc6e-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fdc6e-124">Parent Elements</span></span>  
  
|<span data-ttu-id="fdc6e-125">Élément</span><span class="sxs-lookup"><span data-stu-id="fdc6e-125">Element</span></span>|<span data-ttu-id="fdc6e-126">Description</span><span class="sxs-lookup"><span data-stu-id="fdc6e-126">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="fdc6e-127">\<commonParameters></span><span class="sxs-lookup"><span data-stu-id="fdc6e-127">\<commonParameters></span></span>](commonparameters.md)|<span data-ttu-id="fdc6e-128">Collection de paramètres communs utilisée par les services.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-128">A collection of common parameters used by services.</span></span> <span data-ttu-id="fdc6e-129">Cette collection inclut généralement la chaîne de connexion de base de données pouvant être partagée par les services fiables.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-129">This collection will typically include the database connection string that might be shared by durable services.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fdc6e-130">Notes</span><span class="sxs-lookup"><span data-stu-id="fdc6e-130">Remarks</span></span>  
 <span data-ttu-id="fdc6e-131">L'élément `<commonParameters>` définit tous les paramètres utilisés globalement dans plusieurs services, par exemple `ConnectionString` lors de l'utilisation de <xref:System.Workflow.Runtime.Hosting.SharedConnectionWorkflowCommitWorkBatchService>.</span><span class="sxs-lookup"><span data-stu-id="fdc6e-131">The `<commonParameters>` element defines any parameters that are used globally across multiple services, for example `ConnectionString` when using the <xref:System.Workflow.Runtime.Hosting.SharedConnectionWorkflowCommitWorkBatchService>.</span></span>  
  
 <span data-ttu-id="fdc6e-132">Pour les services qui valident des lots de travail dans des magasins de persistance, comme <xref:System.Workflow.Runtime.Hosting.DefaultWorkflowCommitWorkBatchService> et <xref:System.Workflow.Runtime.Hosting.SqlWorkflowPersistenceService>, vous pouvez les activer pour effectuer de nouvelles tentatives de transaction à l'aide du paramètre `EnableRetries` tel qu'indiqué dans l'exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="fdc6e-132">For services that commit work batches to persistence stores, such as <xref:System.Workflow.Runtime.Hosting.DefaultWorkflowCommitWorkBatchService> and <xref:System.Workflow.Runtime.Hosting.SqlWorkflowPersistenceService>, you can enable them to retry their transaction by using the `EnableRetries` parameter as shown in the following example:</span></span>  
  
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
    <add type="System.Workflow.Runtime.Hosting.SqlWorkflowPersistenceService, System.Workflow.Runtime, Version=3.0.00000.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"
         enableRetries="False" />
  </services>
</workflowRuntime>
```  
  
 <span data-ttu-id="fdc6e-133">Notez que le `EnableRetries` paramètre peut être défini à un niveau global (comme indiqué dans le *Paramètres_courants* section) ou pour des services individuels qui prennent en charge `EnableRetries` (comme indiqué dans le *Services*section).</span><span class="sxs-lookup"><span data-stu-id="fdc6e-133">Notice that the `EnableRetries` parameter can be set at either a global level (as shown in the *CommonParameters* section) or for individual services that support `EnableRetries` (as shown in the *Services* section).</span></span>  
  
 <span data-ttu-id="fdc6e-134">Pour plus d’informations sur l’utilisation d’un fichier de configuration pour contrôler le comportement d’un <xref:System.Workflow.Runtime.WorkflowRuntime> objet d’une application hôte Windows Workflow Foundation, consultez [les fichiers de Configuration de flux de travail](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90)).</span><span class="sxs-lookup"><span data-stu-id="fdc6e-134">For more information on using a configuration file to control the behavior of a <xref:System.Workflow.Runtime.WorkflowRuntime> object of a Windows Workflow Foundation host application, see [Workflow Configuration Files](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="fdc6e-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="fdc6e-135">Example</span></span>  
  
```xml  
<commonParameters>
  <add name="ConnectionString"
       value="Initial Catalog=WorkflowStore;Data Source=localhost;Integrated Security=SSPI;" />
  <add name="EnableRetries"
       value="true" />
</commonParameters>
```  
  
## <a name="see-also"></a><span data-ttu-id="fdc6e-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fdc6e-136">See also</span></span>

- <xref:System.ServiceModel.Configuration.WorkflowRuntimeElement>
- <xref:System.Workflow.Runtime.Configuration.WorkflowRuntimeServiceElement>
- <xref:System.Workflow.Runtime.WorkflowRuntime>
- <xref:System.Workflow.Runtime.Hosting.DefaultWorkflowCommitWorkBatchService>
- <xref:System.Workflow.Runtime.Hosting.SqlWorkflowPersistenceService>
- <span data-ttu-id="fdc6e-137">[Fichiers de Configuration de flux de travail](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="fdc6e-137">[Workflow Configuration Files](https://docs.microsoft.com/previous-versions/dotnet/netframework-3.5/ms732240(v=vs.90))</span></span>
- [<span data-ttu-id="fdc6e-138">\<commonParameters></span><span class="sxs-lookup"><span data-stu-id="fdc6e-138">\<commonParameters></span></span>](commonparameters.md)
