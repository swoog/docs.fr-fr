---
title: '&lt;workflowUnhandledException&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 57adeab5-f06a-44b2-916b-0e177cf0f4a6
ms.openlocfilehash: 5c5dddc6d126811d7fd1eaae2f85df1e42c1cd41
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54700869"
---
# <a name="ltworkflowunhandledexceptiongt"></a><span data-ttu-id="e8792-102">&lt;workflowUnhandledException&gt;</span><span class="sxs-lookup"><span data-stu-id="e8792-102">&lt;workflowUnhandledException&gt;</span></span>
<span data-ttu-id="e8792-103">Comportement de service qui vous permet de spécifier l'action à exécuter lorsqu'une exception non prise en charge est levée dans un service de workflow.</span><span class="sxs-lookup"><span data-stu-id="e8792-103">A service behavior that enables you to specify the action to take when an unhandled exception occurs within a workflow service.</span></span>  
  
<span data-ttu-id="e8792-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="e8792-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="e8792-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="e8792-105">\<behaviors></span></span>  
<span data-ttu-id="e8792-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="e8792-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="e8792-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="e8792-107">\<behavior></span></span>  
<span data-ttu-id="e8792-108">\<workflowUnhandledException></span><span class="sxs-lookup"><span data-stu-id="e8792-108">\<workflowUnhandledException></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e8792-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8792-109">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <workflowUnhandledException action="Abandon/AbandonAndSuspend/Cancel/Terminate" />
    </behavior>
  </serviceBehaviors>
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e8792-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="e8792-110">Attributes and Elements</span></span>  
 <span data-ttu-id="e8792-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="e8792-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e8792-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="e8792-112">Attributes</span></span>  
  
|<span data-ttu-id="e8792-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="e8792-113">Attribute</span></span>|<span data-ttu-id="e8792-114">Description</span><span class="sxs-lookup"><span data-stu-id="e8792-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e8792-115">action</span><span class="sxs-lookup"><span data-stu-id="e8792-115">action</span></span>|<span data-ttu-id="e8792-116">Chaîne qui spécifie l'action à entreprendre lorsqu'une exception non gérée se produit.</span><span class="sxs-lookup"><span data-stu-id="e8792-116">A string that specifies the action to take when an unhandled exception occurs.</span></span> <span data-ttu-id="e8792-117">Cet attribut est de type <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionAction></span><span class="sxs-lookup"><span data-stu-id="e8792-117">This attribute is of type <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionAction></span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e8792-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e8792-118">Child Elements</span></span>  
 <span data-ttu-id="e8792-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e8792-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="e8792-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e8792-120">Parent Elements</span></span>  
  
|<span data-ttu-id="e8792-121">Élément</span><span class="sxs-lookup"><span data-stu-id="e8792-121">Element</span></span>|<span data-ttu-id="e8792-122">Description</span><span class="sxs-lookup"><span data-stu-id="e8792-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e8792-123">\<comportement > de \<serviceBehaviors ></span><span class="sxs-lookup"><span data-stu-id="e8792-123">\<behavior> of \<serviceBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/behavior-of-servicebehaviors-of-workflow.md)|<span data-ttu-id="e8792-124">Spécifie un élément de comportement.</span><span class="sxs-lookup"><span data-stu-id="e8792-124">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e8792-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8792-125">See also</span></span>
- <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionBehavior>
- <xref:System.ServiceModel.Activities.Configuration.WorkflowUnhandledExceptionElement>
