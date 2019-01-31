---
title: <behaviors> de flux de travail
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: 3c6017b6-0c4f-4192-bd67-9515f5d1ec82
ms.openlocfilehash: e61a2078c5989a3b100e77e6b2f753b0ee5dd934
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271784"
---
# <a name="behaviors-of-workflow"></a><span data-ttu-id="80e72-102">\<comportements > de flux de travail</span><span class="sxs-lookup"><span data-stu-id="80e72-102">\<behaviors> of workflow</span></span>
<span data-ttu-id="80e72-103">Cet élément contient le **serviceBehaviors** collection.</span><span class="sxs-lookup"><span data-stu-id="80e72-103">This element contains the **serviceBehaviors** collection.</span></span>  <span data-ttu-id="80e72-104">Chaque élément dans la collection définit des éléments de comportement consommés par des services de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="80e72-104">Each element in the collection defines behavior elements consumed by workflow services.</span></span> <span data-ttu-id="80e72-105">Chaque élément de comportement est identifié par son unique **nom** attribut.</span><span class="sxs-lookup"><span data-stu-id="80e72-105">Each behavior element is identified by its unique **name** attribute.</span></span>  
  
 <span data-ttu-id="80e72-106">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="80e72-106">\<system.ServiceModel></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="80e72-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80e72-107">Syntax</span></span>  
  
```xml  
<behaviors>  
  <serviceBehaviors>  
  </serviceBehaviors>  
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="80e72-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="80e72-108">Attributes and Elements</span></span>  
 <span data-ttu-id="80e72-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="80e72-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="80e72-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="80e72-110">Attributes</span></span>  
 <span data-ttu-id="80e72-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="80e72-111">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="80e72-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="80e72-112">Child Elements</span></span>  
  
|<span data-ttu-id="80e72-113">Élément</span><span class="sxs-lookup"><span data-stu-id="80e72-113">Element</span></span>|<span data-ttu-id="80e72-114">Description</span><span class="sxs-lookup"><span data-stu-id="80e72-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="80e72-115">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="80e72-115">\<serviceBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/servicebehaviors-of-workflow.md)|<span data-ttu-id="80e72-116">Cette section de configuration représente tous les comportements définis pour un service de flux de travail spécifique.</span><span class="sxs-lookup"><span data-stu-id="80e72-116">This configuration section represents all the behaviors defined for a specific workflow service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="80e72-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="80e72-117">Parent Elements</span></span>  
  
|<span data-ttu-id="80e72-118">Élément</span><span class="sxs-lookup"><span data-stu-id="80e72-118">Element</span></span>|<span data-ttu-id="80e72-119">Description</span><span class="sxs-lookup"><span data-stu-id="80e72-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="80e72-120">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="80e72-120">\<system.serviceModel></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md)|<span data-ttu-id="80e72-121">Élément racine de tous les éléments de configuration de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="80e72-121">The root element of all workflow configuration elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="80e72-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80e72-122">See also</span></span>
- <xref:System.ServiceModel.Configuration.BehaviorsSection>
- <xref:System.ServiceModel.Configuration.ServiceBehaviorElementCollection>
- <xref:System.ServiceModel.Configuration.ServiceBehaviorElement>
- [<span data-ttu-id="80e72-123">Configuration et extension de l’exécution à l’aide de comportements</span><span class="sxs-lookup"><span data-stu-id="80e72-123">Configuring and Extending the Runtime with Behaviors</span></span>](../../../../../docs/framework/wcf/extending/configuring-and-extending-the-runtime-with-behaviors.md)
