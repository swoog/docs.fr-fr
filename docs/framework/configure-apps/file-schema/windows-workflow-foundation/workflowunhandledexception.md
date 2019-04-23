---
title: <workflowUnhandledException>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 57adeab5-f06a-44b2-916b-0e177cf0f4a6
ms.openlocfilehash: cfe3350ac42d1e0e837b79f25753f62dc2051dd2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59096249"
---
# <a name="workflowunhandledexception"></a><span data-ttu-id="7ba9c-101">\<workflowUnhandledException></span><span class="sxs-lookup"><span data-stu-id="7ba9c-101">\<workflowUnhandledException></span></span>
<span data-ttu-id="7ba9c-102">Comportement de service qui vous permet de spécifier l'action à exécuter lorsqu'une exception non prise en charge est levée dans un service de workflow.</span><span class="sxs-lookup"><span data-stu-id="7ba9c-102">A service behavior that enables you to specify the action to take when an unhandled exception occurs within a workflow service.</span></span>  
  
<span data-ttu-id="7ba9c-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="7ba9c-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="7ba9c-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="7ba9c-104">\<behaviors></span></span>  
<span data-ttu-id="7ba9c-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="7ba9c-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="7ba9c-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="7ba9c-106">\<behavior></span></span>  
<span data-ttu-id="7ba9c-107">\<workflowUnhandledException></span><span class="sxs-lookup"><span data-stu-id="7ba9c-107">\<workflowUnhandledException></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7ba9c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ba9c-108">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <workflowUnhandledException action="Abandon/AbandonAndSuspend/Cancel/Terminate" />
    </behavior>
  </serviceBehaviors>
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7ba9c-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="7ba9c-109">Attributes and Elements</span></span>  
 <span data-ttu-id="7ba9c-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="7ba9c-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7ba9c-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="7ba9c-111">Attributes</span></span>  
  
|<span data-ttu-id="7ba9c-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="7ba9c-112">Attribute</span></span>|<span data-ttu-id="7ba9c-113">Description</span><span class="sxs-lookup"><span data-stu-id="7ba9c-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="7ba9c-114">action</span><span class="sxs-lookup"><span data-stu-id="7ba9c-114">action</span></span>|<span data-ttu-id="7ba9c-115">Chaîne qui spécifie l'action à entreprendre lorsqu'une exception non gérée se produit.</span><span class="sxs-lookup"><span data-stu-id="7ba9c-115">A string that specifies the action to take when an unhandled exception occurs.</span></span> <span data-ttu-id="7ba9c-116">Cet attribut est de type <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionAction></span><span class="sxs-lookup"><span data-stu-id="7ba9c-116">This attribute is of type <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionAction></span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="7ba9c-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7ba9c-117">Child Elements</span></span>  
 <span data-ttu-id="7ba9c-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7ba9c-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="7ba9c-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="7ba9c-119">Parent Elements</span></span>  
  
|<span data-ttu-id="7ba9c-120">Élément</span><span class="sxs-lookup"><span data-stu-id="7ba9c-120">Element</span></span>|<span data-ttu-id="7ba9c-121">Description</span><span class="sxs-lookup"><span data-stu-id="7ba9c-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="7ba9c-122">\<comportement > de \<serviceBehaviors ></span><span class="sxs-lookup"><span data-stu-id="7ba9c-122">\<behavior> of \<serviceBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/behavior-of-servicebehaviors-of-workflow.md)|<span data-ttu-id="7ba9c-123">Spécifie un élément de comportement.</span><span class="sxs-lookup"><span data-stu-id="7ba9c-123">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="7ba9c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ba9c-124">See also</span></span>

- <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionBehavior>
- <xref:System.ServiceModel.Activities.Configuration.WorkflowUnhandledExceptionElement>
