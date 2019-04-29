---
title: <bufferReceive>
ms.date: 03/30/2017
ms.topic: reference
ms.assetid: b23c3a54-10d4-4f13-ab6d-98b26b76f22a
ms.openlocfilehash: 360d26fda964fa33640e833ad22dab7e06e153f6
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61790258"
---
# <a name="bufferreceive"></a><span data-ttu-id="bd8d2-101">\<bufferReceive></span><span class="sxs-lookup"><span data-stu-id="bd8d2-101">\<bufferReceive></span></span>
<span data-ttu-id="bd8d2-102">Comportement de service qui permet à un service d'utiliser le traitement de la réception mise en mémoire tampon, ce qui permet à un service de flux de travail de traiter les messages dans le désordre.</span><span class="sxs-lookup"><span data-stu-id="bd8d2-102">A service behavior that enables a service to use buffered receive processing, which enables a workflow service to process out-of-order messages.</span></span>  
  
<span data-ttu-id="bd8d2-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="bd8d2-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="bd8d2-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="bd8d2-104">\<behaviors></span></span>  
<span data-ttu-id="bd8d2-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="bd8d2-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="bd8d2-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="bd8d2-106">\<behavior></span></span>  
<span data-ttu-id="bd8d2-107">\<bufferReceive></span><span class="sxs-lookup"><span data-stu-id="bd8d2-107">\<bufferReceive></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bd8d2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd8d2-108">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <bufferReceive maxPendingMessagesPerChannel="Integer" />
    </behavior>
  </serviceBehaviors>
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="bd8d2-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="bd8d2-109">Attributes and Elements</span></span>  
 <span data-ttu-id="bd8d2-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="bd8d2-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="bd8d2-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="bd8d2-111">Attributes</span></span>  
  
|<span data-ttu-id="bd8d2-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="bd8d2-112">Attribute</span></span>|<span data-ttu-id="bd8d2-113">Description</span><span class="sxs-lookup"><span data-stu-id="bd8d2-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="bd8d2-114">maxPendingMessagesPerChannel</span><span class="sxs-lookup"><span data-stu-id="bd8d2-114">maxPendingMessagesPerChannel</span></span>|<span data-ttu-id="bd8d2-115">Entier qui spécifie le nombre maximal de messages en attente autorisé pour chaque canal.</span><span class="sxs-lookup"><span data-stu-id="bd8d2-115">An integer that specifies the maximum number of pending messages allowed for each channel.</span></span> <span data-ttu-id="bd8d2-116">La valeur par défaut est 512.</span><span class="sxs-lookup"><span data-stu-id="bd8d2-116">The default value is 512.</span></span> <span data-ttu-id="bd8d2-117">Cette propriété limite le nombre de messages non ordonnés qui peuvent être reçus par un service de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="bd8d2-117">This property limits the number of out-of-order messages that can be received by a workflow service.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="bd8d2-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bd8d2-118">Child Elements</span></span>  
 <span data-ttu-id="bd8d2-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="bd8d2-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="bd8d2-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="bd8d2-120">Parent Elements</span></span>  
  
|<span data-ttu-id="bd8d2-121">Élément</span><span class="sxs-lookup"><span data-stu-id="bd8d2-121">Element</span></span>|<span data-ttu-id="bd8d2-122">Description</span><span class="sxs-lookup"><span data-stu-id="bd8d2-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="bd8d2-123">\<comportement > de \<serviceBehaviors ></span><span class="sxs-lookup"><span data-stu-id="bd8d2-123">\<behavior> of \<serviceBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/behavior-of-servicebehaviors-of-workflow.md)|<span data-ttu-id="bd8d2-124">Spécifie un élément de comportement.</span><span class="sxs-lookup"><span data-stu-id="bd8d2-124">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="bd8d2-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd8d2-125">See also</span></span>

- <xref:System.ServiceModel.Activities.Description.BufferedReceiveServiceBehavior>
- <xref:System.ServiceModel.Activities.Configuration.BufferedReceiveElement>
