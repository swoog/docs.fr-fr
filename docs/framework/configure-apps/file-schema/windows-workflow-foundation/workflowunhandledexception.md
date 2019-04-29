---
title: <workflowUnhandledException>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 57adeab5-f06a-44b2-916b-0e177cf0f4a6
ms.openlocfilehash: cfe3350ac42d1e0e837b79f25753f62dc2051dd2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61613389"
---
# <a name="workflowunhandledexception"></a><span data-ttu-id="61ce8-101">\<workflowUnhandledException></span><span class="sxs-lookup"><span data-stu-id="61ce8-101">\<workflowUnhandledException></span></span>
<span data-ttu-id="61ce8-102">Comportement de service qui vous permet de spécifier l'action à exécuter lorsqu'une exception non prise en charge est levée dans un service de workflow.</span><span class="sxs-lookup"><span data-stu-id="61ce8-102">A service behavior that enables you to specify the action to take when an unhandled exception occurs within a workflow service.</span></span>  
  
<span data-ttu-id="61ce8-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="61ce8-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="61ce8-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="61ce8-104">\<behaviors></span></span>  
<span data-ttu-id="61ce8-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="61ce8-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="61ce8-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="61ce8-106">\<behavior></span></span>  
<span data-ttu-id="61ce8-107">\<workflowUnhandledException></span><span class="sxs-lookup"><span data-stu-id="61ce8-107">\<workflowUnhandledException></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="61ce8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61ce8-108">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <workflowUnhandledException action="Abandon/AbandonAndSuspend/Cancel/Terminate" />
    </behavior>
  </serviceBehaviors>
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="61ce8-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="61ce8-109">Attributes and Elements</span></span>  
 <span data-ttu-id="61ce8-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="61ce8-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="61ce8-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="61ce8-111">Attributes</span></span>  
  
|<span data-ttu-id="61ce8-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="61ce8-112">Attribute</span></span>|<span data-ttu-id="61ce8-113">Description</span><span class="sxs-lookup"><span data-stu-id="61ce8-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="61ce8-114">action</span><span class="sxs-lookup"><span data-stu-id="61ce8-114">action</span></span>|<span data-ttu-id="61ce8-115">Chaîne qui spécifie l'action à entreprendre lorsqu'une exception non gérée se produit.</span><span class="sxs-lookup"><span data-stu-id="61ce8-115">A string that specifies the action to take when an unhandled exception occurs.</span></span> <span data-ttu-id="61ce8-116">Cet attribut est de type <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionAction></span><span class="sxs-lookup"><span data-stu-id="61ce8-116">This attribute is of type <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionAction></span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="61ce8-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="61ce8-117">Child Elements</span></span>  
 <span data-ttu-id="61ce8-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="61ce8-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="61ce8-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="61ce8-119">Parent Elements</span></span>  
  
|<span data-ttu-id="61ce8-120">Élément</span><span class="sxs-lookup"><span data-stu-id="61ce8-120">Element</span></span>|<span data-ttu-id="61ce8-121">Description</span><span class="sxs-lookup"><span data-stu-id="61ce8-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="61ce8-122">\<comportement > de \<serviceBehaviors ></span><span class="sxs-lookup"><span data-stu-id="61ce8-122">\<behavior> of \<serviceBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/behavior-of-servicebehaviors-of-workflow.md)|<span data-ttu-id="61ce8-123">Spécifie un élément de comportement.</span><span class="sxs-lookup"><span data-stu-id="61ce8-123">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="61ce8-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61ce8-124">See also</span></span>

- <xref:System.ServiceModel.Activities.Description.WorkflowUnhandledExceptionBehavior>
- <xref:System.ServiceModel.Activities.Configuration.WorkflowUnhandledExceptionElement>
