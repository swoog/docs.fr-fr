---
title: <workflowInstanceManagement>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 63ac89ba-c844-4ae2-96ae-cd752a90a109
ms.openlocfilehash: 98bc1b24da6e65a11a39d133057c1bb55b003a58
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59191612"
---
# <a name="workflowinstancemanagement"></a><span data-ttu-id="2a19b-101">\<workflowInstanceManagement></span><span class="sxs-lookup"><span data-stu-id="2a19b-101">\<workflowInstanceManagement></span></span>
<span data-ttu-id="2a19b-102">Comportement de service qui vous permet de spécifier des paramètres qui contrôlent le mode d'exécution des instances de flux de travail, notamment la persistance, le comportement d'exception non prise en charge et le comportement inactif.</span><span class="sxs-lookup"><span data-stu-id="2a19b-102">A service behavior that enables you to specify settings that control how workflow instances are run, including persistence, unhandled Exception behavior and idle behavior.</span></span>  
  
<span data-ttu-id="2a19b-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="2a19b-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="2a19b-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="2a19b-104">\<behaviors></span></span>  
<span data-ttu-id="2a19b-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="2a19b-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="2a19b-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="2a19b-106">\<behavior></span></span>  
<span data-ttu-id="2a19b-107">\<workflowInstanceManagement></span><span class="sxs-lookup"><span data-stu-id="2a19b-107">\<workflowInstanceManagement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2a19b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a19b-108">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <workflowInstanceManagement authorizedWindowsGroup="" />
    </behavior>
  </serviceBehaviors>
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2a19b-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="2a19b-109">Attributes and Elements</span></span>  
 <span data-ttu-id="2a19b-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="2a19b-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2a19b-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="2a19b-111">Attributes</span></span>  
  
|<span data-ttu-id="2a19b-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="2a19b-112">Attribute</span></span>|<span data-ttu-id="2a19b-113">Description</span><span class="sxs-lookup"><span data-stu-id="2a19b-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="2a19b-114">authorizedWindowsGroup</span><span class="sxs-lookup"><span data-stu-id="2a19b-114">authorizedWindowsGroup</span></span>||  
  
### <a name="child-elements"></a><span data-ttu-id="2a19b-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2a19b-115">Child Elements</span></span>  
 <span data-ttu-id="2a19b-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="2a19b-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="2a19b-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2a19b-117">Parent Elements</span></span>  
  
|<span data-ttu-id="2a19b-118">Élément</span><span class="sxs-lookup"><span data-stu-id="2a19b-118">Element</span></span>|<span data-ttu-id="2a19b-119">Description</span><span class="sxs-lookup"><span data-stu-id="2a19b-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2a19b-120">\<comportement > de \<serviceBehaviors ></span><span class="sxs-lookup"><span data-stu-id="2a19b-120">\<behavior> of \<serviceBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/behavior-of-servicebehaviors-of-workflow.md)|<span data-ttu-id="2a19b-121">Spécifie un élément de comportement.</span><span class="sxs-lookup"><span data-stu-id="2a19b-121">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="2a19b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a19b-122">See also</span></span>

- <xref:System.ServiceModel.Activities.Description.WorkflowInstanceManagementBehavior>
- <xref:System.ServiceModel.Activities.Configuration.WorkflowInstanceManagementElement>
