---
title: <workflowUnhandledException>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 57adeab5-f06a-44b2-916b-0e177cf0f4a6
ms.openlocfilehash: caf5be7aaff0df436be3a1d618a9f89bb32e6bb7
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55254845"
---
# <a name="workflowunhandledexception"></a><span data-ttu-id="b2bca-101">\<workflowUnhandledException></span><span class="sxs-lookup"><span data-stu-id="b2bca-101">\<workflowUnhandledException></span></span>
<span data-ttu-id="b2bca-102">Comportement de service qui vous permet de spécifier l'action à exécuter lorsqu'une exception non prise en charge est levée dans un service de workflow.</span><span class="sxs-lookup"><span data-stu-id="b2bca-102">A service behavior that enables you to specify the action to take when an unhandled exception occurs within a workflow service.</span></span>  
  
<span data-ttu-id="b2bca-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="b2bca-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="b2bca-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="b2bca-104">\<behaviors></span></span>  
<span data-ttu-id="b2bca-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="b2bca-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="b2bca-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="b2bca-106">\<behavior></span></span>  
<span data-ttu-id="b2bca-107">\<workflowUnhandledException></span><span class="sxs-lookup"><span data-stu-id="b2bca-107">\<workflowUnhandledException></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b2bca-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2bca-108">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <workflowUnhandledException action="Abandon/AbandonAndSuspend/Cancel/Terminate" />
    </behavior>
  </serviceBehaviors>
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b2bca-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="b2bca-109">Attributes and Elements</span></span>  
 <span data-ttu-id="b2bca-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="b2bca-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b2bca-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="b2bca-111">Attributes</span></span>  
  
|<span data-ttu-id="b2bca-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="b2bca-112">Attribute</span></span>|<span data-ttu-id="b2bca-113">Description</span><span class="sxs-lookup"><span data-stu-id="b2bca-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="b2bca-114">action</span><span class="sxs-lookup"><span data-stu-id="b2bca-114">action</span></span>|<span data-ttu-id="b2bca-115">Chaîne qui spécifie l'action à entreprendre lorsqu'une exception non gérée se produit.</span><span class="sxs-lookup"><span data-stu-id="b2bca-115">A string that specifies the action to take when an unhandled exception occurs.</span></span> <span data-ttu-id="b2bca-116">Cet attribut est de type <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionAction></span><span class="sxs-lookup"><span data-stu-id="b2bca-116">This attribute is of type <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionAction></span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b2bca-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b2bca-117">Child Elements</span></span>  
 <span data-ttu-id="b2bca-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b2bca-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="b2bca-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b2bca-119">Parent Elements</span></span>  
  
|<span data-ttu-id="b2bca-120">Élément</span><span class="sxs-lookup"><span data-stu-id="b2bca-120">Element</span></span>|<span data-ttu-id="b2bca-121">Description</span><span class="sxs-lookup"><span data-stu-id="b2bca-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b2bca-122">\<comportement > de \<serviceBehaviors ></span><span class="sxs-lookup"><span data-stu-id="b2bca-122">\<behavior> of \<serviceBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/behavior-of-servicebehaviors-of-workflow.md)|<span data-ttu-id="b2bca-123">Spécifie un élément de comportement.</span><span class="sxs-lookup"><span data-stu-id="b2bca-123">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b2bca-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2bca-124">See also</span></span>
- <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionBehavior>
- <xref:System.ServiceModel.Activities.Configuration.WorkflowUnhandledExceptionElement>
