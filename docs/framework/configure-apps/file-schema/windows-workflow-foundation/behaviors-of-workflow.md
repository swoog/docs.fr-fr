---
title: '&lt;behaviors&gt; de workflow'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 3c6017b6-0c4f-4192-bd67-9515f5d1ec82
ms.openlocfilehash: b4ad7fb54cc8a03f5dd698055da5a29e719775c4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54731671"
---
# <a name="ltbehaviorsgt-of-workflow"></a><span data-ttu-id="bd9bb-102">&lt;behaviors&gt; de workflow</span><span class="sxs-lookup"><span data-stu-id="bd9bb-102">&lt;behaviors&gt; of workflow</span></span>
<span data-ttu-id="bd9bb-103">Cet élément contient le **serviceBehaviors** collection.</span><span class="sxs-lookup"><span data-stu-id="bd9bb-103">This element contains the **serviceBehaviors** collection.</span></span>  <span data-ttu-id="bd9bb-104">Chaque élément dans la collection définit des éléments de comportement consommés par des services de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="bd9bb-104">Each element in the collection defines behavior elements consumed by workflow services.</span></span> <span data-ttu-id="bd9bb-105">Chaque élément de comportement est identifié par son unique **nom** attribut.</span><span class="sxs-lookup"><span data-stu-id="bd9bb-105">Each behavior element is identified by its unique **name** attribute.</span></span>  
  
 <span data-ttu-id="bd9bb-106">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="bd9bb-106">\<system.ServiceModel></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bd9bb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd9bb-107">Syntax</span></span>  
  
```xml  
<behaviors>  
  <serviceBehaviors>  
  </serviceBehaviors>  
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bd9bb-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="bd9bb-108">Attributes and Elements</span></span>  
 <span data-ttu-id="bd9bb-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="bd9bb-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bd9bb-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="bd9bb-110">Attributes</span></span>  
 <span data-ttu-id="bd9bb-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="bd9bb-111">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="bd9bb-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bd9bb-112">Child Elements</span></span>  
  
|<span data-ttu-id="bd9bb-113">Élément</span><span class="sxs-lookup"><span data-stu-id="bd9bb-113">Element</span></span>|<span data-ttu-id="bd9bb-114">Description</span><span class="sxs-lookup"><span data-stu-id="bd9bb-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="bd9bb-115">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="bd9bb-115">\<serviceBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/servicebehaviors-of-workflow.md)|<span data-ttu-id="bd9bb-116">Cette section de configuration représente tous les comportements définis pour un service de flux de travail spécifique.</span><span class="sxs-lookup"><span data-stu-id="bd9bb-116">This configuration section represents all the behaviors defined for a specific workflow service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="bd9bb-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="bd9bb-117">Parent Elements</span></span>  
  
|<span data-ttu-id="bd9bb-118">Élément</span><span class="sxs-lookup"><span data-stu-id="bd9bb-118">Element</span></span>|<span data-ttu-id="bd9bb-119">Description</span><span class="sxs-lookup"><span data-stu-id="bd9bb-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="bd9bb-120">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="bd9bb-120">\<system.serviceModel></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md)|<span data-ttu-id="bd9bb-121">Élément racine de tous les éléments de configuration de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="bd9bb-121">The root element of all workflow configuration elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="bd9bb-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd9bb-122">See also</span></span>
- <xref:System.ServiceModel.Configuration.BehaviorsSection>
- <xref:System.ServiceModel.Configuration.ServiceBehaviorElementCollection>
- <xref:System.ServiceModel.Configuration.ServiceBehaviorElement>
- [<span data-ttu-id="bd9bb-123">Configuration et extension de l’exécution à l’aide de comportements</span><span class="sxs-lookup"><span data-stu-id="bd9bb-123">Configuring and Extending the Runtime with Behaviors</span></span>](../../../../../docs/framework/wcf/extending/configuring-and-extending-the-runtime-with-behaviors.md)
