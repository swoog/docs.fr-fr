---
title: '&lt;dispatcherSynchronization&gt;'
ms.date: 03/30/2017
ms.assetid: cc030f9c-4e38-4b14-94dc-9a0e41ec8e2d
ms.openlocfilehash: 537dee408f1af29a06042de439a2c1e7d7874222
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54555386"
---
# <a name="ltdispatchersynchronizationgt"></a><span data-ttu-id="be441-102">&lt;dispatcherSynchronization&gt;</span><span class="sxs-lookup"><span data-stu-id="be441-102">&lt;dispatcherSynchronization&gt;</span></span>
  
<span data-ttu-id="be441-103">Spécifie un comportement de point de terminaison qui permet à un service d'envoyer des réponses de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="be441-103">Specifies an endpoint behavior that enables a service to send replies asynchronously.</span></span>  
  
<span data-ttu-id="be441-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="be441-104">\<system.serviceModel></span></span>  
<span data-ttu-id="be441-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="be441-105">\<behaviors></span></span>  
<span data-ttu-id="be441-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="be441-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="be441-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="be441-107">\<behavior></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="be441-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be441-108">Syntax</span></span>  
  
```xml  
<dispatcherSynchronizationBehavior asynchronousSendEnabled="Boolean"
                                   maxPendingReceives="Integer" />
```  
  
## <a name="type"></a><span data-ttu-id="be441-109">Type</span><span class="sxs-lookup"><span data-stu-id="be441-109">Type</span></span>  
  
`Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="be441-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="be441-110">Attributes and elements</span></span>  
  
<span data-ttu-id="be441-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="be441-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="be441-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="be441-112">Attributes</span></span>

| <span data-ttu-id="be441-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="be441-113">Attribute</span></span>               | <span data-ttu-id="be441-114">Description</span><span class="sxs-lookup"><span data-stu-id="be441-114">Description</span></span>       |
| ----------------------- | ----------------- |
| <span data-ttu-id="be441-115">asynchronousSendEnabled</span><span class="sxs-lookup"><span data-stu-id="be441-115">asynchronousSendEnabled</span></span> | <span data-ttu-id="be441-116">Valeur booléenne qui indique si un comportement d'envoi asynchrone est activé.</span><span class="sxs-lookup"><span data-stu-id="be441-116">A Boolean that specifies whether asynchronous send behavior is enabled.</span></span> |
| `maxPendingReceives`    | <span data-ttu-id="be441-117">Entier qui spécifie le nombre de réceptions simultanées qui peuvent être émises sur le canal.</span><span class="sxs-lookup"><span data-stu-id="be441-117">An integer that specifies the number of concurrent receives that can be issued on the channel.</span></span><br /><br /> <span data-ttu-id="be441-118">Cette valeur doit être configurée uniquement après avoir correctement configuré le comportement de limitation de service.</span><span class="sxs-lookup"><span data-stu-id="be441-118">This value should be configured only after you have properly configured service throttling behavior.</span></span> |

### <a name="child-elements"></a><span data-ttu-id="be441-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="be441-119">Child elements</span></span>

<span data-ttu-id="be441-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="be441-120">None.</span></span>

### <a name="parent-elements"></a><span data-ttu-id="be441-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="be441-121">Parent elements</span></span>

| <span data-ttu-id="be441-122">Élément</span><span class="sxs-lookup"><span data-stu-id="be441-122">Element</span></span> | <span data-ttu-id="be441-123">Description</span><span class="sxs-lookup"><span data-stu-id="be441-123">Description</span></span> |  
| ------- | ----------- |  
| [<span data-ttu-id="be441-124">\<behavior></span><span class="sxs-lookup"><span data-stu-id="be441-124">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="be441-125">Spécifie un comportement de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="be441-125">Specifies an endpoint behavior.</span></span> |

## <a name="see-also"></a><span data-ttu-id="be441-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be441-126">See also</span></span>

- <xref:System.ServiceModel.Configuration.DispatcherSynchronizationElement>
- <xref:System.ServiceModel.Description.DispatcherSynchronizationBehavior>
