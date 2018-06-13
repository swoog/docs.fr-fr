---
title: '&lt;synchronousReceive&gt;, élément'
ms.date: 03/30/2017
ms.assetid: cc070387-3d11-4b02-a952-bc08ad2df05a
ms.openlocfilehash: af1ca2ee1fe3c03c33f05e0c30c7b843b3720a36
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32753259"
---
# <a name="ltsynchronousreceivegt-element"></a><span data-ttu-id="eb047-102">&lt;synchronousReceive&gt;, élément</span><span class="sxs-lookup"><span data-stu-id="eb047-102">&lt;synchronousReceive&gt; element</span></span>
<span data-ttu-id="eb047-103">Cet élément de configuration est utilisé en vue de spécifier le comportement de réception des messages au moment de l'exécution dans une application cliente ou de service.</span><span class="sxs-lookup"><span data-stu-id="eb047-103">This configuration element is used to specify run-time behavior for receiving messages in either a service or client application.</span></span> <span data-ttu-id="eb047-104">Il n'a aucun attribut ou élément enfant.</span><span class="sxs-lookup"><span data-stu-id="eb047-104">It does not have any attributes or child elements.</span></span>  
  
 <span data-ttu-id="eb047-105">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="eb047-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="eb047-106">\<comportements ></span><span class="sxs-lookup"><span data-stu-id="eb047-106">\<behaviors></span></span>  
<span data-ttu-id="eb047-107">\<endpointBehaviors ></span><span class="sxs-lookup"><span data-stu-id="eb047-107">\<endpointBehaviors></span></span>  
<span data-ttu-id="eb047-108">\<comportement ></span><span class="sxs-lookup"><span data-stu-id="eb047-108">\<behavior></span></span>  
<span data-ttu-id="eb047-109">\<synchronousReceive ></span><span class="sxs-lookup"><span data-stu-id="eb047-109">\<synchronousReceive></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eb047-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb047-110">Syntax</span></span>  
  
```xml  
<synchronousReceive />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="eb047-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="eb047-111">Attributes and Elements</span></span>  
 <span data-ttu-id="eb047-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="eb047-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="eb047-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="eb047-113">Attributes</span></span>  
 <span data-ttu-id="eb047-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="eb047-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="eb047-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="eb047-115">Child Elements</span></span>  
 <span data-ttu-id="eb047-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="eb047-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="eb047-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="eb047-117">Parent Elements</span></span>  
  
|<span data-ttu-id="eb047-118">Élément</span><span class="sxs-lookup"><span data-stu-id="eb047-118">Element</span></span>|<span data-ttu-id="eb047-119">Description</span><span class="sxs-lookup"><span data-stu-id="eb047-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="eb047-120">\<behavior></span><span class="sxs-lookup"><span data-stu-id="eb047-120">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="eb047-121">Spécifie un comportement de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="eb047-121">Specifies an endpoint behavior.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="eb047-122">Notes</span><span class="sxs-lookup"><span data-stu-id="eb047-122">Remarks</span></span>  
 <span data-ttu-id="eb047-123">Utilisez ce comportement pour indiquer à l’écouteur de canal d’utiliser une réception synchrone au lieu de celle par défaut (asynchrone).</span><span class="sxs-lookup"><span data-stu-id="eb047-123">Use this behavior to instruct the channel listener to use a synchronous receive rather than the default, asynchronous.</span></span> <span data-ttu-id="eb047-124">Windows Communication Foundation (WCF) émet un nouveau thread pour pomper Chaque canal accepté.</span><span class="sxs-lookup"><span data-stu-id="eb047-124">Windows Communication Foundation (WCF) issues a new thread to pump for each accepted channel.</span></span> <span data-ttu-id="eb047-125">Si le nombre de canaux est important, il est possible de rencontrer une insuffisance de threads.</span><span class="sxs-lookup"><span data-stu-id="eb047-125">If there are a lot of channels, there is the possibility of running out of threads.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eb047-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb047-126">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.SynchronousReceiveElement>  
 <xref:System.ServiceModel.Description.SynchronousReceiveBehavior>
