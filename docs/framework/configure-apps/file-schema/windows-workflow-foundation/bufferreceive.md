---
title: '&lt;bufferReceive&gt;'
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: b23c3a54-10d4-4f13-ab6d-98b26b76f22a
ms.openlocfilehash: 507d58f852544c0eadcefaf997b2345d5e123cfa
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54607512"
---
# <a name="ltbufferreceivegt"></a><span data-ttu-id="0ad15-102">&lt;bufferReceive&gt;</span><span class="sxs-lookup"><span data-stu-id="0ad15-102">&lt;bufferReceive&gt;</span></span>
<span data-ttu-id="0ad15-103">Comportement de service qui permet à un service d'utiliser le traitement de la réception mise en mémoire tampon, ce qui permet à un service de flux de travail de traiter les messages dans le désordre.</span><span class="sxs-lookup"><span data-stu-id="0ad15-103">A service behavior that enables a service to use buffered receive processing, which enables a workflow service to process out-of-order messages.</span></span>  
  
<span data-ttu-id="0ad15-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="0ad15-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="0ad15-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="0ad15-105">\<behaviors></span></span>  
<span data-ttu-id="0ad15-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="0ad15-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="0ad15-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="0ad15-107">\<behavior></span></span>  
<span data-ttu-id="0ad15-108">\<bufferReceive></span><span class="sxs-lookup"><span data-stu-id="0ad15-108">\<bufferReceive></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0ad15-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ad15-109">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <bufferReceive maxPendingMessagesPerChannel="Integer" />
    </behavior>
  </serviceBehaviors>
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0ad15-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="0ad15-110">Attributes and Elements</span></span>  
 <span data-ttu-id="0ad15-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="0ad15-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0ad15-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="0ad15-112">Attributes</span></span>  
  
|<span data-ttu-id="0ad15-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="0ad15-113">Attribute</span></span>|<span data-ttu-id="0ad15-114">Description</span><span class="sxs-lookup"><span data-stu-id="0ad15-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="0ad15-115">maxPendingMessagesPerChannel</span><span class="sxs-lookup"><span data-stu-id="0ad15-115">maxPendingMessagesPerChannel</span></span>|<span data-ttu-id="0ad15-116">Entier qui spécifie le nombre maximal de messages en attente autorisé pour chaque canal.</span><span class="sxs-lookup"><span data-stu-id="0ad15-116">An integer that specifies the maximum number of pending messages allowed for each channel.</span></span> <span data-ttu-id="0ad15-117">La valeur par défaut est 512.</span><span class="sxs-lookup"><span data-stu-id="0ad15-117">The default value is 512.</span></span> <span data-ttu-id="0ad15-118">Cette propriété limite le nombre de messages non ordonnés qui peuvent être reçus par un service de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="0ad15-118">This property limits the number of out-of-order messages that can be received by a workflow service.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0ad15-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0ad15-119">Child Elements</span></span>  
 <span data-ttu-id="0ad15-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0ad15-120">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="0ad15-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0ad15-121">Parent Elements</span></span>  
  
|<span data-ttu-id="0ad15-122">Élément</span><span class="sxs-lookup"><span data-stu-id="0ad15-122">Element</span></span>|<span data-ttu-id="0ad15-123">Description</span><span class="sxs-lookup"><span data-stu-id="0ad15-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0ad15-124">\<comportement > de \<serviceBehaviors ></span><span class="sxs-lookup"><span data-stu-id="0ad15-124">\<behavior> of \<serviceBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/behavior-of-servicebehaviors-of-workflow.md)|<span data-ttu-id="0ad15-125">Spécifie un élément de comportement.</span><span class="sxs-lookup"><span data-stu-id="0ad15-125">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0ad15-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ad15-126">See also</span></span>
<!-- <xref:System.ServiceModel.Activities.Description.BufferReceiveServiceBehavior>  -->
- <xref:System.ServiceModel.Activities.Configuration.BufferedReceiveElement>
