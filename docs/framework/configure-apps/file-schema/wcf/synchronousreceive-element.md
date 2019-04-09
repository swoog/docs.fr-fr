---
title: <synchronousReceive> d'élément
ms.date: 03/30/2017
ms.assetid: cc070387-3d11-4b02-a952-bc08ad2df05a
ms.openlocfilehash: 20390f747c8beaccba1cfea7a9ea0ed366037ecb
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59166541"
---
# <a name="synchronousreceive-element"></a><span data-ttu-id="38b31-102">\<synchronousReceive > élément</span><span class="sxs-lookup"><span data-stu-id="38b31-102">\<synchronousReceive> element</span></span>
<span data-ttu-id="38b31-103">Cet élément de configuration est utilisé en vue de spécifier le comportement de réception des messages au moment de l'exécution dans une application cliente ou de service.</span><span class="sxs-lookup"><span data-stu-id="38b31-103">This configuration element is used to specify run-time behavior for receiving messages in either a service or client application.</span></span> <span data-ttu-id="38b31-104">Il n'a aucun attribut ou élément enfant.</span><span class="sxs-lookup"><span data-stu-id="38b31-104">It does not have any attributes or child elements.</span></span>  
  
 <span data-ttu-id="38b31-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="38b31-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="38b31-106">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="38b31-106">\<behaviors></span></span>  
<span data-ttu-id="38b31-107">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="38b31-107">\<endpointBehaviors></span></span>  
<span data-ttu-id="38b31-108">\<behavior></span><span class="sxs-lookup"><span data-stu-id="38b31-108">\<behavior></span></span>  
<span data-ttu-id="38b31-109">\<synchronousReceive></span><span class="sxs-lookup"><span data-stu-id="38b31-109">\<synchronousReceive></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="38b31-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38b31-110">Syntax</span></span>  
  
```xml  
<synchronousReceive />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="38b31-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="38b31-111">Attributes and Elements</span></span>  
 <span data-ttu-id="38b31-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="38b31-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="38b31-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="38b31-113">Attributes</span></span>  
 <span data-ttu-id="38b31-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="38b31-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="38b31-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="38b31-115">Child Elements</span></span>  
 <span data-ttu-id="38b31-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="38b31-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="38b31-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="38b31-117">Parent Elements</span></span>  
  
|<span data-ttu-id="38b31-118">Élément</span><span class="sxs-lookup"><span data-stu-id="38b31-118">Element</span></span>|<span data-ttu-id="38b31-119">Description</span><span class="sxs-lookup"><span data-stu-id="38b31-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="38b31-120">\<behavior></span><span class="sxs-lookup"><span data-stu-id="38b31-120">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="38b31-121">Spécifie un comportement de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="38b31-121">Specifies an endpoint behavior.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="38b31-122">Notes</span><span class="sxs-lookup"><span data-stu-id="38b31-122">Remarks</span></span>  
 <span data-ttu-id="38b31-123">Utilisez ce comportement pour indiquer à l'écouteur de canal d'utiliser une réception synchrone au lieu de celle par défaut (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="38b31-123">Use this behavior to instruct the channel listener to use a synchronous receive rather than the default, asynchronous.</span></span> <span data-ttu-id="38b31-124">Windows Communication Foundation (WCF) émet un nouveau thread pour pomper Chaque canal accepté.</span><span class="sxs-lookup"><span data-stu-id="38b31-124">Windows Communication Foundation (WCF) issues a new thread to pump for each accepted channel.</span></span> <span data-ttu-id="38b31-125">Si le nombre de canaux est important, il est possible de rencontrer une insuffisance de threads.</span><span class="sxs-lookup"><span data-stu-id="38b31-125">If there are a lot of channels, there is the possibility of running out of threads.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="38b31-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38b31-126">See also</span></span>

- <xref:System.ServiceModel.Configuration.SynchronousReceiveElement>
- <xref:System.ServiceModel.Description.SynchronousReceiveBehavior>
